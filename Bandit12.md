# Bandit12 → Bandit13

- **Usuario:** `bandit12`
- **Host:** `bandit.labs.overthewire.org`
- **Puerto:** `2220`

## Pasos Realizados

1. **Conexión por SSH**

    ```bash
    ssh bandit12@bandit.labs.overthewire.org -p 2220
    ```

2. **Lectura y decodificación del archivo de contraseña**

    El archivo `data.txt` contiene la contraseña cifrada con ROT13. Para decodificarlo, utilice el siguiente comando:

    ```bash
    cat data.txt | tr 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ' 'nopqrstuvwxyzabcdefghijklmNOPQRSTUVWXYZABCDEFGHIJKLM'
    ```

3. **Guardar la contraseña**

    Copia la contraseña mostrada para usarla en el siguiente nivel.

## Explicación de los comandos usados
- `cat` - Muestra el contenido del archivo `data.txt`.
- `tr` - Aplica la transformación ROT13 al texto.
- `|` - Pasa la salida del comando `cat` como entrada al comando `tr`.
## Referencias
- [ROT13 Cipher](https://en.wikipedia.org/wiki/ROT13)
- [tr Command](https://linux.die.net/man/1/tr)
