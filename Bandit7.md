# Bandit7 → Bandit8

## Descripción del Reto

En este reto, el objetivo es conectarse al servidor mediante SSH y obtener la contraseña para el siguiente nivel.

- **Usuario:** `bandit7`
- **Host:** `bandit.labs.overthewire.org`
- **Puerto:** `2220`

## Pasos Realizados

1. **Conexión por SSH**

    ```bash
    ssh bandit7@bandit.labs.overthewire.org -p 2220
    ```

2. **Lectura del archivo de contraseña**

    El archivo con la contraseña está en el directorio home y es un archivo de texto comprimido.

    ```bash
    ls
    file <archivo>
    gzip -d <archivo>
    cat <archivo_descomprimido>
    ```

3. **Guardar la contraseña**

    Copia la contraseña mostrada para usarla en el siguiente nivel.
