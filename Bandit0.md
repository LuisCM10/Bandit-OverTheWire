# Bandit0 → Bandit1

## Descripción del Reto

En este reto, el objetivo es conectarse al servidor mediante SSH y obtener la contraseña para el siguiente nivel.

- **Usuario:** `bandit0`
- **Host:** `bandit.labs.overthewire.org`
- **Puerto:** `2220`

## Pasos Realizados

1. **Conexión por SSH**

    ```bash
    ssh bandit0@bandit.labs.overthewire.org -p 2220
    ```

2. **Lectura del archivo de contraseña**

    Una vez dentro, debes buscar el archivo `readme` en el directorio home. Este archivo contiene la contraseña para el siguiente nivel.

    ```bash
    cat readme
    ```

    El comando `cat` muestra el contenido del archivo en pantalla. Si el archivo no aparece, puedes usar `ls` para listar los archivos del directorio actual.

3. **Guardar la contraseña**

    Copia la contraseña mostrada y guárdala en un lugar seguro. La necesitarás para acceder al siguiente nivel (`bandit1`).

## Explicación Completa de la Solución

1. **Acceso por SSH:**
   - Se utiliza el comando `ssh` para conectarse al servidor remoto con el usuario y puerto especificados.
   - Si es la primera vez que te conectas, acepta la clave del host.

2. **Buscar el archivo de contraseña:**
   - Al iniciar sesión, estarás en el directorio home del usuario. El archivo `readme` está ahí.
   - Usa `ls` para confirmar que el archivo existe.
   - Usa `cat readme` para ver la contraseña.

3. **Uso de la contraseña:**
   - Copia la contraseña y úsala para el usuario `bandit1` en el siguiente nivel.

## Comandos Utilizados

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
ls
cat readme
```

## Notas y Consejos

- El archivo `readme` es visible para el usuario y no requiere permisos especiales.
- Si tienes problemas de conexión, revisa tu red y el puerto.
- Puedes pegar la contraseña en la terminal usando clic derecho o `Shift+Insert`.

## Recursos

- [OverTheWire: Bandit](https://overthewire.org/wargames/bandit/)
- [Guía SSH](https://www.ssh.com/academy/ssh/command)
