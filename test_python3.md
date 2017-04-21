1. ¿Podemos usar la instrucción `input` en Python2 y en Python3?

* [ ] No, sólo se puede usar en Python3
* [x] Si, aunque en python3 siempre devuelve un valor de tipo str
* [ ] Si, en ambas versiones funciona del mismo modo
* [ ] No, sólo se puede usar en Python2

2. En el interprete de Python3 la variable _:

* [x] Tiene el valor de la última expresión que se haya evaluado
* [ ] Me permite acceder a un método de una clase
* [ ] Me permite indicar un número négativo
* [ ] Tiene el valor de la última variable declarada

3. Cuando vamos a realizar la identación de una línea en un programa python.

* [ ] Sólo puedo utilizar 4 espacios
* [ ] Sólo puedo usar tabuladores
* [ ] Se puede usar tabuladores o espacios, pero no se pueden mezclar
* [x] Se puede usar tabuladores o espacios

4. De las siguientes funciones o métodos, indica la que no es una función predefinida:

* [ ] ascii
* [ ] max
* [x] upper
* [ ] input

5. ¿Qúe sálida obtenemos al ejecutar `type(b'hola')`?

* [x] byte
* [ ] str
* [ ] unicode
* [ ] list

6. Indica el que no es un tipo númerico:

* [ ] Tipo entero (int)
* [ ] Tipo real (float)
* [ ] Tipo numérico (complex)
* [x] Tipo real doble precisión (double)

7. Si tenemos esta instrucción python ´var = 3; var = "hola"´¿Qúe sálida obtenemos al ejecutar `type(var)`?

* [ ] La instrucción es incorrecta no se puede utilziar el `;`
* [ ] En python3 no podemos cambiar el valro de una variable asignada
* [x] Python3 es un lenguaje dinámico, por lo tanto la salida sería `str`
* [ ] Python3 es un lenguaje dinámico, por lo tanto la salida sería `int`

8. ¿Qué salida obtenemos con esta instrucción `print ("%.2f" % 1.1234)?

* [x] 1.12
* [ ] 1.234
* [ ] 1
* [ ] 0.1234

9. Queremos ejecutar la siguiente instrucción: `a = int("123.3")`. ¿Qué valor tendría la variable `a`?

* [ ] 123
* [x] La variable no se crea, esa instrucción provoca una excepción
* [ ] 123.3
* [ ] La variable se crea pero no tiene ningún valor, esa instrucción provoca una excepción

10. Indica para que sirve la función `all()`:

* [x] Recibe un iterador y devuelve True si todos los elementos son verdaderos o el iterador está vacío.
* [ ] Recibe una lista y te devuelve todos los elementos
* [ ] Recibe una secuencia y me permite recorrerla
* [ ] Recibe un iterador y me dedvuelve True si todos los elementos son de tipo booleano.

11. Para añadir una condición alternativa a una declaración condicional if se utiliza

* [ ] elsif
* [ ] else if
* [ ] elseif
* [x] elif 

12. ¿Cuál es la forma correcta de escribir un bucle while?

* [x] while a < 5:
* [ ] while a in range(0..4)
* [ ] while (a < 5)
* [ ] while a foreach[0..4] 

13. Indica de los siguientes tipos, el que no es una secuencia:

* [ ] list
* [x] dict
* [ ] set
* [ ] range

14. ¿Qué valor devuelve la siguiente expresión `[1,2,3][-1]`?

* [ ] [1,2]
* [ ] Produce un error
* [x] 3
* [ ] [0,1,2]

15. ¿Qué valor devuelve la siguiente expresión `[1,2,3,4,2,3].index(2)`?

* [ ] 2
* [x] 1
* [ ] (1,4)
* [ ] Produce un error

16. `[x for x in range(10) if x % 2 == 0]`

* [ ] Devuelve una tupla con los números pares del 1 al 10
* [x] Devuelve una lista con los números pares del 1 al 10
* [ ] Devuelve una lista con números pares aleatorios
* [ ] Devuelve una lista con 10 números pares

17. Esta asignación en python: `var = 1,2,3`

* [ ] No se puede realizar
* [ ] La variable vale 1
* [ ] La varaible es una lista con 3 elementos
* [x] La variable es una tupla

18. ¿Qué valor devuelve esta instrucción: `2 in range(1,11,2)`?

* [ ] True
* [ ] 2
* [x] False
* [ ] No se puede utilizar un operador de pertencia con ese tipo de datos

19. En python3 las cadenas de caracteres están codificadas con...

* [x] unicode
* [ ] utf-8
* [ ] latin1
* [ ] ascii

20. Si tengo esta instrucción en python: `cad="hola"; cad[3]='e'` ¿Qué cadena obtenemos?

* [ ] hole
* [ ] holeee
* [ ] No podemos modifcar la cedana por qué el índice 3 no existe
* [x] No podemos modificar la cadena, por que es un tipo inmutable

21. Indica de los siguientes tipos, el que es mutable:

* [ ] int
* [x] dict
* [ ] str
* [ ] bytes

22. Para que el resultado devuelto sea "bbbbb" escribiremos

* [ ] "aaaaa".substr("a", "b")
* [ ] "aaaaa".replaceAll("b", "a")
* [ ] "aaaaa".replace("b", "a")
* [x] "aaaaa".replace("a", "b") 

23. Tenemos una variable de tipo `bytes` y ejecutamos la siguiente instrucción: `byte1.decode("utf-8")`:

* [ ] La convierte a utf-8
* [ ] La convierte a unicode
* [x] La convierte a unicode si byte1 está codificada con utf-8
* [ ] Nios devuelve una variable de tipo bytesarray

24. ¿Qué valor devuelve esta instrucción: `{1,2,3}[1]`?

* [x] Los conjuntos no permiten la indexación.
* [ ] 2
* [ ] Nos devuelve un conjunto y una lista
* [ ] {2}

25. ¿qué valor devuelve esta instrucción: `var = range(1,10);next(var)`?

* [ ] 1
* [x] Un tipo `range` no es un iterador
* [ ] Para iterar un rango lo tengo que convertir primero en una lista
* [ ] 11

26. ¿Cuál de los siguientes es un objeto de tipo diccionario?

* [x] diccionario = {'Numero': 1, 'Nombre': 'Miguel'}
* [ ] diccionario = {'Numero' => 1, 'Nombre' => 'Miguel'}
* [ ] diccionario = {'Numero' -> 1, 'Nombre' -> 'Miguel'}
* [ ] diccionario = ('Numero': 1, 'Nombre': 'Miguel') 

27. Si tenemos un objeto de tipo diccionario (`dict1`). ¿Qué devuelve el método `items()`?

* [ ] Los valores del diccionarios
* [ ] Las claves del diccionario
* [ ] El número de elementos del diccionario
* [x] Los elementos del diccionario (clave y valor)

28. Si abro un fichero de la siguiente forma: `f=open("ejemplo.txt")`:

* [*] No puedo escribir en el fichero
* [ ] Al escribir se añade el contenido al final del fichero
* [ ] Al escribir se elimina el contenido anterior del fichero
* [ ] No puedo leer el fichero porque el puntero se situa al final del fichero

29. Después de una declaración try para capturar una excepción usaremos

* [ ] raise
* [x] except
* [ ] catch
* [ ] throw 

30. Si importo un paquete de esta forma: `from math import sqrt`. ¿Cómo debo utilizar la función?

* [ ] math.sqrt
* [*] sqrt
* [ ] math->sqrt
* [ ] math["sqrt"]

31. Llamamos a un programa de la siguiente manera: `python sumar.py 5 6 7`. ¿Qué valor devolvería esta instrucción `len(sys.argv)`?

* [ ] 1
* [ ] 3
* [*] 4
* [ ] El resultado de la suma

32. Para que funcione la instrucción `datetime.now()`, tengo que importar el paquete de la siguiente forma:

* [ ] import datetime
* [*] from datetime import datetime
* [ ] from datetime import now
* [ ] import now

33. El comando `pip`:

* [ ] Me crea un entorno virtual
* [ ] Es un interprete python alternativo
* [ ] Es un IDE para programar en python
* [x] Es un instalador de paquetes python

34. La forma correcta de escribir una función es

* [ ] function nombrefuncion()
* [ ] define nombrefuncion()
* [x] def nombrefuncion():
* [ ] nombrefuncion: function()
