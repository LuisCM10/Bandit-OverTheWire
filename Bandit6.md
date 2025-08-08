# Bandit6 → Bandit7

## Descripción del Reto

En este reto, el objetivo es conectarse al servidor mediante SSH y obtener la contraseña para el siguiente nivel.

- **Usuario:** `bandit6`
- **Host:** `bandit.labs.overthewire.org`
- **Puerto:** `2220`

## Pasos Realizados

1. **Conexión por SSH**

    ```bash
    ssh bandit6@bandit.labs.overthewire.org -p 2220
    ```

2. **Lectura del archivo de contraseña**

    El archivo con la contraseña está en el directorio home y es un archivo oculto con permisos restringidos. Puede que necesites permisos especiales para leerlo.

    ```bash
    ls -la
    cat .<nombre_del_archivo>
    ```
    Si no tienes permisos, revisa los permisos del archivo con `ls -l`.

3. **Guardar la contraseña**

    Copia la contraseña mostrada para usarla en el siguiente nivel.

## Explicación Completa de la Solución

1. **Acceso por SSH:**
   - Conéctate usando el usuario y la contraseña del nivel anterior.

2. **Buscar archivos ocultos:**
   - Usa `ls -la` para ver todos los archivos, incluidos los ocultos.
   - Identifica el archivo oculto que no sea `.` ni `..`.

3. **Verifica permisos:**
   - Si no puedes leer el archivo, revisa los permisos con `ls -l`.

4. **Lectura de la contraseña:**
   - Usa `cat .<nombre_del_archivo>` para mostrar la contraseña.

## Comandos Utilizados

```bash
ssh bandit6@bandit.labs.overthewire.org -p 2220
ls -la
cat .<nombre_del_archivo>
```

## Notas y Consejos

- Si no puedes leer el archivo, consulta con `ls -l` para ver los permisos.
- Los archivos ocultos suelen tener información sensible.

## Recursos

- [Comandos básicos de Linux](https://ryanstutorials.net/linuxtutorial/)
