# Bandit8 → Bandit9

## Descripción del Reto

En este reto, el objetivo es conectarse al servidor mediante SSH y obtener la contraseña para el siguiente nivel.

- **Usuario:** `bandit8`
- **Host:** `bandit.labs.overthewire.org`
- **Puerto:** `2220`

## Pasos Realizados

1. **Conexión por SSH**

    ```bash
    ssh bandit8@bandit.labs.overthewire.org -p 2220
    ```

2. **Lectura del archivo de contraseña**

    El archivo con la contraseña está comprimido en varios formatos. Debes descomprimirlo paso a paso.

    ```bash
    ls
    file <archivo>
    <comando decompresión>
    # Repite según el tipo de archivo
    cat <archivo_final>
    ```

3. **Guardar la contraseña**

    Copia la contraseña mostrada para usarla en el siguiente nivel.
