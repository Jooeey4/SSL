# TP Nro 01 - "Fases de la Traducción y Errores"

- **Autores de la Resolución**
    - **Usuario github:** Jooeey4
    - **Legajo:** 156.097-9
    - **Apellido:** Mato
    - **Nombre:** Joan
- **Transcripción del enunciado** 
    - . Investigar las funcionalidades y opciones que su compilador presenta para limitar el inicio y fin de las fases de traducción
    - Para la siguiente secuencia de pasos:
        - Transicribir en readme.md cada comando ejecutado
        - Describir en readme.md el resultado u error obtenidos para cada paso
- **Hipótesis:** Identificar las fases de traducción y errores

---

## Solución

### Ejercicio 2

**Comando** | gcc -E -std=c11 hello2.c -o hello2.i
**Observación:** Vemos como en el archivo hello2.i se reemplaza el include de stdio por su contenido. Vemos como se reemplazan los comentario por espacio.

### Ejercicio 4 

Los tres puntos significan que la función recibe una cantidad n de parámetros

### Ejercicio 5 

**Comando** | gcc -E -std=c11 hello3.c -o hello3.i
**Observación:** Las diferencias entre los archivos hello3.c y gello3.i son las siguientes lineas que agrega el preprocesador

> \# 1 "hello3.c"
> \# 1 "<built-in>"
> \# 1 "<command-line>"
> \# 31 "<command-line>"
> \# 1 "/usr/include/stdc-predef.h" 1 3 4
> \# 32 "<command-line>" 2
> \# 1 "hello3.c"

Luego, en diferencia al archivo hello2.i, vemos que al no incluir 'stdio.h' no agrega tanto contenido dentro.

