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
```
void accept(T t);
```

Sirve para consumir objetos. Uno de los ejemplos m�s claros es imprimir.
```
//...    .forEach(System.out::println)
```

Adicionalmente, tiene el m�todo andThen, que permite componer consumidores, para encadenar una secuencia de operaciones.

## 3. Consumer<T>