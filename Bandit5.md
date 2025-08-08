# Bandit5 → Bandit6

## Descripción del Reto

En este reto, el objetivo es conectarse al servidor mediante SSH y obtener la contraseña para el siguiente nivel.

- **Usuario:** `bandit5`
- **Host:** `bandit.labs.overthewire.org`
- **Puerto:** `2220`

## Pasos Realizados

1. **Conexión por SSH**

    ```bash
    ssh bandit5@bandit.labs.overthewire.org -p 2220
    ```

2. **Lectura del archivo de contraseña**

    El archivo con la contraseña está en el directorio `inhere` y es el único archivo legible por humanos (archivo de texto plano).

    ```bash
    cd inhere
    ls -l
    file *
    cat <archivo_legible>
    ```
    Usa el comando `file *` para identificar cuál archivo es de tipo "ASCII text".

3. **Guardar la contraseña**

    Copia la contraseña mostrada para usarla en el siguiente nivel.

## Explicación Completa de la Solución

1. **Acceso por SSH:**
   - Conéctate usando el usuario y la contraseña del nivel anterior.

2. **Buscar el directorio y archivos:**
   - Entra al directorio `inhere`.
   - Usa `ls -l` para ver los archivos y sus permisos.
   - Usa `file *` para identificar el archivo de texto.

3. **Lectura de la contraseña:**
   - Usa `cat <archivo_legible>` para mostrar la contraseña.

## Comandos Utilizados

```bash
ssh bandit5@bandit.labs.overthewire.org -p 2220
ls
cd inhere
ls -l
file *
cat <archivo_legible>
```

## Notas y Consejos

- Si hay muchos archivos, solo uno será de tipo texto.
- Puedes usar `file` para identificar rápidamente el correcto.

## Recursos

- [Comandos básicos de Linux](https://ryanstutorials.net/linuxtutorial/)
