# Bandit14 → Bandit15

## Descripción del Reto

En este reto, el objetivo es conectarse al servidor mediante SSH y obtener la contraseña para el siguiente nivel.

- **Usuario:** `bandit14`
- **Host:** `bandit.labs.overthewire.org`
- **Puerto:** `2220`

## Pasos Realizados

1. **Conexión por SSH**

    ```bash
    ssh bandit14@bandit.labs.overthewire.org -p 2220
    ```

2. **Lectura del archivo de contraseña**

    El archivo con la contraseña está encriptado y requiere el uso de un comando especial para desencriptarlo.

    ```bash
    nc localhost 30000
    # o
    openssl s_client -connect localhost:30001
    ```

3. **Guardar la contraseña**

    Copia la contraseña mostrada para usarla en el siguiente nivel.
