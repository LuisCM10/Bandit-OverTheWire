# Bandit4 → Bandit5

## Descripción del Reto

En este reto, el objetivo es conectarse al servidor mediante SSH y obtener la contraseña para el siguiente nivel.

- **Usuario:** `bandit4`
- **Host:** `bandit.labs.overthewire.org`
- **Puerto:** `2220`

## Pasos Realizados

1. **Conexión por SSH**

    ```bash
    ssh bandit4@bandit.labs.overthewire.org -p 2220
    ```

2. **Lectura del archivo de contraseña**

    El archivo con la contraseña para el siguiente nivel está en el directorio `inhere`. Debes buscar dentro de ese directorio.

    ```bash
    cd inhere
    ls
    cat <nombre_del_archivo>
    ```
    Puede haber varios archivos, revisa el contenido de cada uno si es necesario.

3. **Guardar la contraseña**

    Copia la contraseña mostrada para usarla en el siguiente nivel.

## Explicación Completa de la Solución

1. **Acceso por SSH:**
   - Conéctate usando el usuario y la contraseña del nivel anterior.

2. **Buscar el directorio `inhere`:**
   - Usa `ls` para ver los directorios y archivos.
   - Entra al directorio con `cd inhere`.

3. **Buscar el archivo correcto:**
   - Usa `ls` para listar los archivos dentro de `inhere`.
   - Usa `cat <nombre_del_archivo>` para ver el contenido de cada archivo hasta encontrar la contraseña.

## Comandos Utilizados

```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
ls
cd inhere
ls
cat <nombre_del_archivo>
```

## Notas y Consejos

- Si hay muchos archivos, puedes usar `file *` para identificar archivos de texto.

## Recursos

- [Comandos básicos de Linux](https://ryanstutorials.net/linuxtutorial/)
