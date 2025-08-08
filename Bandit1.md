# Bandit Level 1 → Level 2

## Objetivo

Conseguir la contraseña para el usuario `bandit2`.

## Información de acceso

- **Usuario:** bandit1
- **Contraseña:** [contraseña obtenida en el nivel anterior]
- **Host:** bandit.labs.overthewire.org
- **Puerto:** 2220

## Instrucciones

1. Conéctate al servidor usando SSH:
    ```sh
    ssh bandit1@bandit.labs.overthewire.org -p 2220
    ```

2. El archivo con la contraseña para el siguiente nivel se encuentra en el archivo llamado `-` en el directorio home. Este nombre es especial porque el guion suele usarse para referirse a la entrada estándar en muchos comandos de Linux.

3. Para leer el contenido del archivo `-`, no basta con escribir `cat -` porque esto esperaría entrada estándar. Debes especificar la ruta o usar comillas:
    ```sh
    cat ./-
    ```
    Esto mostrará la contraseña en pantalla.

4. Copia la contraseña mostrada para usarla en el siguiente nivel.

## Explicación Completa de la Solución

1. **Acceso por SSH:**
   - Conéctate usando el usuario y la contraseña obtenida en el nivel anterior.

2. **Identificar el archivo especial:**
   - El archivo `-` es un nombre válido en Linux, pero puede causar confusión porque muchos comandos lo interpretan como entrada estándar.
   - Por eso, se recomienda usar `./-` o comillas para referirse a él.

3. **Lectura de la contraseña:**
   - El comando `cat ./-` mostrará la contraseña.

## Comandos Utilizados

```sh
ssh bandit1@bandit.labs.overthewire.org -p 2220
ls -l
cat ./-
```

## Notas y Consejos

- Si usas solo `cat -`, el comando esperará entrada estándar y no mostrará el contenido del archivo.
- Puedes usar la tecla `Tab` para autocompletar nombres de archivos.

## Recursos

- [Página oficial de Bandit](https://overthewire.org/wargames/bandit/)
- [Guía de comandos básicos de Linux](https://ryanstutorials.net/linuxtutorial/)
