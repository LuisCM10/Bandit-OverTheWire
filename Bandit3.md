# Bandit3 → Bandit4

## Descripción del Reto

En este reto, el objetivo es conectarse al servidor mediante SSH y obtener la contraseña para el siguiente nivel.

- **Usuario:** `bandit3`
- **Host:** `bandit.labs.overthewire.org`
- **Puerto:** `2220`

## Pasos Realizados

1. **Conexión por SSH**

    ```bash
    ssh bandit3@bandit.labs.overthewire.org -p 2220
    ```

2. **Lectura del archivo de contraseña**

    El archivo con la contraseña para el siguiente nivel está en un archivo llamado `inhere` en el directorio home. Este archivo es visible con un `ls` normal.

    ```bash
    ls
    cat inhere
    ```
    El comando `cat inhere` mostrará la contraseña.

3. **Guardar la contraseña**

    Copia la contraseña mostrada para usarla en el siguiente nivel.

## Explicación Completa de la Solución

1. **Acceso por SSH:**
   - Conéctate usando el usuario y la contraseña del nivel anterior.

2. **Buscar el archivo `inhere`:**
   - Usa `ls` para listar los archivos del directorio home.
   - El archivo `inhere` debe estar presente.

3. **Lectura de la contraseña:**
   - Usa `cat inhere` para mostrar la contraseña.

## Comandos Utilizados

```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
ls
cat inhere
```

## Notas y Consejos

- Si el archivo no aparece, asegúrate de estar en el directorio correcto (`cd ~`).

## Recursos

- [Comandos básicos de Linux](https://ryanstutorials.net/linuxtutorial/)
