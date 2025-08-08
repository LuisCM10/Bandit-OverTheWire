# Bandit2 → Bandit3

## Descripción del Reto

En este reto, el objetivo es conectarse al servidor mediante SSH y obtener la contraseña para el siguiente nivel.

- **Usuario:** `bandit2`
- **Host:** `bandit.labs.overthewire.org`
- **Puerto:** `2220`

## Pasos Realizados

1. **Conexión por SSH**

    ```bash
    ssh bandit2@bandit.labs.overthewire.org -p 2220
    ```

2. **Lectura del archivo de contraseña**

    El archivo con la contraseña para el siguiente nivel está oculto en el directorio home y su nombre comienza con un punto (`.`), lo que significa que no se muestra con un `ls` normal.

    ```bash
    ls -la
    cat .nombre_del_archivo
    ```
    Usa `ls -la` para listar todos los archivos, incluidos los ocultos. Busca el archivo que no sea `.` ni `..` y que comience con un punto.

    Por ejemplo, si ves `.abc`, usa `cat .abc` para mostrar la contraseña.

3. **Guardar la contraseña**

    Copia la contraseña mostrada para usarla en el siguiente nivel.

## Explicación Completa de la Solución

1. **Acceso por SSH:**
   - Conéctate usando el usuario y la contraseña del nivel anterior.

2. **Buscar archivos ocultos:**
   - Los archivos que comienzan con punto (`.`) son ocultos en Linux.
   - Usa `ls -la` para verlos.
   - Identifica el archivo oculto que contiene la contraseña.

3. **Lectura de la contraseña:**
   - Usa `cat .<nombre_del_archivo>` para mostrar la contraseña.

## Comandos Utilizados

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
ls -la
cat .<nombre_del_archivo>
```

## Notas y Consejos

- Los archivos ocultos suelen usarse para configuraciones o información sensible.
- Si hay más de un archivo oculto, revisa el contenido de cada uno.

## Recursos

- [Comandos básicos de Linux](https://ryanstutorials.net/linuxtutorial/)
