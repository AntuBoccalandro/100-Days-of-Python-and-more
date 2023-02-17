![](../../images/Cover%20Main%20Page.png)

***Índice de contenidos:***
* Imprimir valores por terminal
  * La función print()
  * Imprimir texto de una sola línea
  * Uso de comillas
  * Imprimir texto de varias líneas
  * Imprimir variables
  * Realizar operaciones dentro de la función print()
  * Objectos imprimibles por la función print()
  * Imprimir texto junto a variables
    * Por medio de comas
    * Por medio de concadenación
    * Por medio de f-strings
    * Por medio de formateo
  * Parámetros opcionales de la función print()
    * end
    * sep

# 🖨️ **Imprimir valores por terminal**

Cuando hablamos de imprimir valores por terminal nos referimos a mostar valores, ya sea numéricos o texto a través de la terminal del sistema operativo. Para esta tarea todos los lenguajes tienen una función, en Python se utiliza la función `print()` para esta tarea.

## 🔢 La función print()

La función `print()` imprime valores por la terminal del sistema. Para llamarla simplemente escribimos su sintáxis, como parámetros esta función puede recibir varios pero se puede ejecutar sin ningún parámetro. Si no recibe ningún parámetro se imprimirá un caracter de salto de línea o más conocido como ENTER.

```python
print()
```

## 👊 Imprimir texto de una sola línea

La mayoría de las veces utilizaremos esta función para imprimir texto. Para imprimir texto se debe encerrar al mismo entre comillas simples o dobles. 

```python
print('Hola')
# Hola

print("Hola")
# Hola
```

## 😉 Uso de comillas

El uso de las comillas dependerá de la situación: si se quiere remarcar un texto entre comillas simples dentro del texto se utilizarán comillas dobles que encierren a todo el texto, y visceversa.

```python
print("Esta es una "frase" con estilo")
# Error

print('Esta es una "frase" con estilo')
# Esta es una "frase" con estilo

print("Esta es una 'frase' con estilo")
# Esta es una 'frase' con estilo
```

## 🗑️ Imprimir texto de varias líneas

Si se quiere imprimir texto de varias líneas si bien hay caracteres que nos permiten realizar saltos de línea se puede optar por utilizar tripe comillas simples o dobles que encierren a todo el texto, las reglas de como utilizar las comillas simples o dobles son las mismas. 

```python
print('''
    Primera línea
    Segunda línea
    Tercera línea
''')

#    Primera línea
#    Segunda línea
#    Tercera línea

print("""
    Primera línea
    Segunda línea
    Tercera línea
""")
#       Primera línea
#       Segunda línea
#       Tercera línea

```

El inconveniente es que al imprimir varias líneas como se mostró es que se agrega una tabulación a la izquierda y en ocaciones queremos eliminar esa tabulación, para ello existe una librería que se puede utilizar en esta situación, llamada `textwrap`, se puede instalar con el comando `pip install textwrap`.

```python
import textwrap

var = '''
    Python
    Javascript
    Java
    PHP
    Django
    '''

print(textwrap.dedent(var))
# Python
# Javascript
# Java
# PHP
# Django
```

## 👍 Imprimir valores de variables

Además de texto se puede mostrar valores en la terminal que provengan de variables, el tipo de dato de esta no afecta para nada. Se pueden mostrar números, strings, listas, etc. Si se quiere imprimir el valor de una varaible solo basta con colocar el nombre de la varaible dentro de la función print(). Si se quiere imprimi varias variables no hace falta utilizar la función print() varias veces si no que se pueden separar por comas los nombres de las variables. 

    ```python
    var = 'Hola'
    print(var)
    # Hola

    num = 10
    print(num)
    # 10

    print(var, num)
    # Hola 10
    ```
## 🔠 Realizar operaciones dentro de la función print()

Dentro de la función print() se puede realizar todo tipo de operaciones, como sumas, restas, comparaciónes, etc...es decir que se mostrará el resultado de dicha operación en la terminal. 

```python
a = 10
b = 9

print(a+b)
# 19

print(a>b)
# True
```

## 🧑‍💻 Objetos imprimibles por la función print()

La función print() soporta todo tipo de objeto:

* Datos de tipo secuencia: list, tuple
* Datos de tipo numéricos: int, float, complex
* Datos booleanos: True/False
* Datos de tipo diccionario
* Datos de tipo set
* Objetos
* Funciones
* Operaciones aritméticas/relación/lógicas
* Métodos

## 👌 Imprimir texto junto a variables

Hemos visto como imprimir texto y varaibles, pero en ocaciones se quieren imprimir estos dos elementos de manera conjunta para, por ejemplo, mostrar el valor de una variable a la vez que se indica en texto a que variable pertenece ese valor. Para esto hay muchos métodos y son los siguientes. 

**Por medio de comas**: se separa el texto y las variables por comas.
```python
lenguaje = 'Python'
año = 1991

print(lenguaje, 'se creó en ', año)
# Python se creó en 1991
```

**Por medio de concadenación**: se utiliza el operador `+` para sumar el texto y los datos de tipo string de las variables.
```python
lenguaje = 'Python'
año = '1991'

print(lenguaje+'se creó en'+año)
# Python se creó en 1991
```

Como vemos se imprimimen los valores de las variables entre medio del texto pero hay un inconveniente. Al sumar los datos todos tienen que ser de tipo string y el año es un número por lo que requiere de una conversión de número entero a string, se puede encerrar al número entero entre comillas y transformarlo en un string o utilizar la función incporporada `str()` para realizar esa conversión.

```python
lenguaje = 'Python'
año = 1991

print(lenguaje+'se creó en'+str(año))
# Python se creó en 1991
```
 
**Por medio de f-strings**: se utilizan los f-strings para poder combinar las variables dentro del texto por medio de llaves. Esta es una de mis maneras preferidas ya que es muy cómoda y facilmente entendible. 
```python
lenguaje = 'Python'
año = 1991

print(f'{lenguaje} se creó en {año}')
# Python se creó en 1991
```

**Por medio de formateo**: se crean juegos de llaves en los cuales luego le pasaremos una lista de elementos que queremos representar en cada llave. Es importante que los elementos estén en orden con respecto a sus llaves.
```python
lenguaje = 'Python'
año = 1991

print('{} se creó en {}'.format(lenguaje, año))
# Python se creó en 1991
```

## 🌐 Parámetros opcionales de la función print()

La función print() puede recibir varios parámetros opcionales que permiten darle un formato diferente a los valores que se imprimirán.

**print(< content >, < end='' >)**: el parámetro `end=''` permite especificar el caracter con el cual se quiere que termine la impresión, por defecto es un caracter de salto de línea `\n`, pero se puede colocar qualquier otro. 
```python
print('Python', end='-')
# Python-

print('Python ', end='lenguaje')
# Python lenguaje
```

NOTA: si se define el parámetro end='' con un string vacío lograremos que la próxima impresión que hagamos se vea al lado de la anterior.

```python
print('Python', end='')
# Python

print('Hello')
# PythonHello
```

**print(< content >, < sep='' >)**: el parámetro `sep=''` permite definir un caracter que separá los elementos que se vallan a imprimir.  
```python
print('Python', 'Javascript', 'PHP', sep='-')
# Python-Javascript-PHP

print('Python', 'Javascript', 'PHP', sep=' ')
# Python Javascipt PHP
```

<center style="font-size: 30px"> <b>>>> Controles <<< </b></center>

<center style="font-size: 30px"> <b><a href="https://github.com/AntuBoccalandro/100-Days-of-Python-and-more/tree/master/Semana_01/Día_001/03_Comentarios.md">⬅️</a> <a href="https://github.com/AntuBoccalandro/100-Days-of-Python-and-more">🏠</a> <a href="https://github.com/AntuBoccalandro/100-Days-of-Python-and-more/tree/master/Semana_01/Día_001/05_Variables.md">➡️</a></b></center>
