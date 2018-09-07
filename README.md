# APIStream
Ejemplos API Stream


## 1. Predicate<T>
El método abstracto es:
```
boolean test(T t);
```

Comprueba si se cumple o no una condición. Se utiliza mucho junto a expresiones lambda a la hora de filtrar:

```
list.stream().filter((p) -> p.getEdad() >= 35L)

Predicate<Persona> edad = (p) -> p.getEdad() >= 35L;
```

Se pueden componer predicados más complejos con sus métodos and , or y negate.

## 2. Consumer<T>
El método abstracto es:
```
void accept(T t);
```

Sirve para consumir objetos. Uno de los ejemplos más claros es imprimir.
```
//...    .forEach(System.out::println)
```

Adicionalmente, tiene el método andThen, que permite componer consumidores, para encadenar una secuencia de operaciones.

## 3. Consumer<T>