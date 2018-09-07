# APIStream
Ejemplos API Stream


## 15.1 Predicate<T>
El método abstracto es:
```
boolean test(T t);
```

Comprueba si se cumple o no una condición. Se utiliza mucho junto a expresiones lambda a la hora de filtrar:

```
list.stream().filter((p) -> p.getEdad() >= 35L)

Predicate<Persona> edad = (p) -> p.getEdad() >= 35L;
```

Se pueden componer predicados más complejos con sus métodos and , or y negate .