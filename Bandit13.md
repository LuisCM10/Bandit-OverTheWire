# Bandit13 → Bandit14

- **Usuario:** `bandit13`
- **Host:** `bandit.labs.overthewire.org`
- **Puerto:** `2220`

## Pasos Realizados

1. **Conexión por SSH**

    ```bash
    ssh bandit13@bandit.labs.overthewire.org -p 2220
    ```

2. **Descompresión recursiva de archivos**

    El archivo que contiene la contraseña está comprimido varias veces en diferentes formatos (gzip, bzip2, tar, etc.). Debes descomprimirlo recursivamente hasta obtener el archivo de texto con la contraseña. Puedes usar un script como el siguiente para automatizar el proceso:

    ```bash
    #!/bin/bash
    file="data.txt"
    while true; do
      case "$(file --mime-type -b "$file")" in
        application/x-gzip)
          mv "$file" "${file}.gz"
          gunzip "${file}.gz"
          ;;
        application/x-bzip2)
          mv "$file" "${file}.bz2"
          bunzip2 "${file}.bz2"
          ;;
        application/x-tar)
          mv "$file" "${file}.tar"
          tar -xf "${file}.tar"
          file=$(tar -tf "${file}.tar" | head -n 1)
          ;;
        text/plain)
          cat "$file"
          break
          ;;
        *)
          echo "Formato desconocido: $(file --mime-type -b "$file")"
          break
          ;;
      esac
    done
    ```

3. **Guardar la contraseña**
Copia la contraseña mostrada para usarla en el siguiente nivel.

## Explicación de los comandos usados

- `file`: Detecta el tipo de archivo para saber cómo descomprimirlo.
- `mv`: Renombra el archivo para añadir la extensión correspondiente antes de descomprimir.
- `gunzip`, `bunzip2`: Descomprimen archivos `.gz` y `.bz2` respectivamente.
- `tar -xf`: Extrae archivos de un archivo tar.
- `tar -tf`: Lista el contenido de un archivo tar.
- `cat`: Muestra el contenido del archivo de texto final.

## Script
El siguiente script automatiza la descompresión recursiva de los archivos hasta obtener la contraseña:

```bash
#!/bin/bash
file="data.txt"
while true; do
    case "$(file --mime-type -b "$file")" in
        application/x-gzip)
            mv "$file" "${file}.gz"
            gunzip "${file}.gz"
            ;;
        application/x-bzip2)
            mv "$file" "${file}.bz2"
            bunzip2 "${file}.bz2"
            ;;
        application/x-tar)
            mv "$file" "${file}.tar"
            tar -xf "${file}.tar"
            file=$(tar -tf "${file}.tar" | head -n 1)
            ;;
        text/plain)
            cat "$file"
            break
            ;;
        *)
            echo "Formato desconocido: $(file --mime-type -b "$file")"
            break
            ;;
    esac
done
```

## Referencias
- [OverTheWire Bandit Walkthrough](https://overthewire.org/wargames/bandit/bandit14.html)
- [Comando file](https://man7.org/linux/man-pages/man1/file.1.html)
- [Comando tar](https://man7.org/linux/man-pages/man1/tar.1.html)
- [Comando gunzip](https://man7.org/linux/man-pages/man1/gzip.1.html)
- [Comando bunzip2](https://man7.org/linux/man-pages/man1/bzip2.1.html)
