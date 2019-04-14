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
> 
> \# 1 \"\<built-in>"
> 
> \# 1 \"\<command-line>"
> 
> \# 31 \"\<command-line>"
> 
> \# 1 "/usr/include/stdc-predef.h" 1 3 4
> 
> \# 32 \"\<command-line>" 2
> 
> \# 1 "hello3.c"
> 

Luego, en diferencia al archivo hello2.i, vemos que al no incluir 'stdio.h' no agrega tanto contenido dentro.

### Ejercicio 6

**Comando:** gcc -S hello3.c

### Ejercicio 8

**Comando:** gcc -S hello4.c
**Observación:** En el archivo 'hello4.s' vemos el código en assembler

### Ejercicio 9

**Comando:** as -o hello4.o hello4.s 
**Observación:** Genera el archivo 'hello4.o' que es binario con el código máquina.

### Ejercicio 10

**Comando:** ld -o hello4 hello4.o
**Observación:** Falla al crear el ejecutable porque no esta definida la referencia a la función 'printf'.

### Ejercicio 12

**Comando:** gcc hello5.c -o hello5.exe
**Observación:** Muestra por pantalla lo siguiente:

> joan@joan-desktop:~/Documents/utn/sintaxis/SSL/01-FasesErrores$ ./hello5.exe 
>
> La respuesta es 1450851288

Lo que vemos es que al no pasarle por parametro la variable con un valor, lo rellena con un valor random.

### Ejercicio 13

**Comando:** gcc hello6.c -o hello6.exe
**Observación:** Muestra por pantalla lo siguiente:

> joan@joan-desktop:~/Documents/utn/sintaxis/SSL/01-FasesErrores$ ./hello6.exe 
>
> La respuesta es 42

### Ejercicio 14

**Comando:** gcc hello7.c -o hello7.exe
**Observación:** Muestra por pantalla lo siguiente:

> joan@joan-desktop:~/Documents/utn/sintaxis/SSL/01-FasesErrores$ ./hello6.exe 
>
> La respuesta es 42

Muestra por pantalla un 'warning' diciendo que hay una declaración implicita de la función 'printf'. Igualmente, funciona ya que por default, se vincula contra la libreria estandar, la cual incliye a 'stdio.h'.