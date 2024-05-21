# Principio Abierto/Cerrado

Las entidades de software (clases, módulos, funciones, etc.) deben estar **abiertas** para su extensión pero **cerradas** para su modificación. 

Las nuevas funcionalidades o comportamientos entran sin modificar el código existente, mediante el uso de herencia, composición o interfaces.

## Cuándo se rompe este principio

- Cuando usamos atributos que no sean privados.
- Cuando usamos variables globales.
- Cuando se procede a consultar el tipo de objeto polimórfico.

Pero claro, dado que el cierre no puede ser completo, debe ser una estrategia. Estos es, los diseñadores deben elegir la clase de cambios contra los cuales cerrar el diseño. Esto toma cierta cantidad de **presciencia** derivada de la experiencia. 

Los diseñadores experimentados conocen a los usuarios y la industria suficientemente bien para juzgar la probabilidad de diferentes clases de cambios.

