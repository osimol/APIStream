# APIStream
Ejemplos API Stream


## 1. Predicate<T>
El m�todo abstracto es:
```
boolean test(T t);
```

Comprueba si se cumple o no una condici�n. Se utiliza mucho junto a expresiones lambda a la hora de filtrar:

```
list.stream().filter((p) -> p.getEdad() >= 35L)

Predicate<Persona> edad = (p) -> p.getEdad() >= 35L;
```

Se pueden componer predicados m�s complejos con sus m�todos and , or y negate.

## 2. Consumer<T>
El m�todo abstracto es:
s
void accept(T t);
```

Sirve para consumir objetos. Uno de los ejemplos m�s claros es imprimir.
```
//...    .forEach(System.out::println)
```

Adicionalmente, tiene el m�todo andThen, que permite componer consumidores, para encadenar una secuencia de operaciones.

## 3. Function<T, R>
El m�todo abstracto es:

R apply(T t);
Sirve para aplicar una transformaci�n a un objeto. El ejemplo m�s claro es el mapeo de objetos en otros.
```
//...
    .map((p) -> p.getNombre())
```
Adicionalmente, tiene otros m�todos:

andThen , que permite componer funciones.
compose , que compone dos funciones, a la inversa de la anterior.
identity , una funci�n que siempre devuelve el argumento que recibe

## 4. Supplier<T>
El m�todo abstracto es:
```
T get();
```
Sirve para devolver un valor.

Tiene algunos interfaces especializados para tipos b�sicos:

* IntSupplier
* LongSupplier
* DoubleSupplier
* BooleanSupplier