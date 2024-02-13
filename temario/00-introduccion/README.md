# Disciplina de diseño

## ¿Por qué?

Los proyectos de software sufren de inefectividad (ineficacia y/o ineficiencia) debido a:

- Al sufrir de malas variables en su economía:
  - Ámbito incumplido y/o
  - Tiempo incumplido y/o
  - Coste incumplido
- Debido a la mala calidad del software, malas *-ilities*:
  - Fiabilidad
  - Usabilidad
  - Interoperatividad
  - Seguridad, 
  - etc...
- Porque tiene mala mantenibilidad:
  - **Viscoso**, porque no se puede entender con facilidad y/o
  - **Rígido**, porque no se puede cambiar con facilidad y/o
  - **Frágil**, porque no se puede probar con facilidad y/o
  - **Inmovil**, porque no se puede reutilizar con facilidad.
- Porque tiene complejidad arbitraria.


|🤔||
|-|-|
"Si tienes una función o procedimiento con diez parámetros, probablemente hayas olvidado uno"|Alan Perlis, MIT, catedrático, director ACM, Premio Turing, ...
“Si tienes muchos casos especiales, algo estás haciendo mal”|Craig Zerouni, miembro de BAFTA, ACM/SIGGRAPH, IEEE, ...
"Está bien investigar y resolver misteriosos asesinatos, pero no deberías necesitar hacerlo con el código. Simplemente deberías poder leerlo"|Steve McConnell, Rapid Development, Software Estimation y Code Complete, una de las tres personas más influyentes, ...
"Es raro que mantener el código de otro desarrollador sea como entrar en un edificio de gran diseño que admiras mientras paseas por él y planeas cómo añadirle un ala o algún elemento decorativo. Lo más frecuente es que sea como tirarse de cabeza a un gran montón de basura maloliente"|Bill Venners
"La mayoría del software actual es muy parecido a una pirámide egipcia, con millones de ladrillos puestos unos encima de otros sin una estructura integral, simplemente realizada a base de fuerza bruta y miles de esclavos" |Alan Kay, Xerox, Atari, ..., Smalltalk
"Se dice que las grandes disciplinas científicas son ejemplos de gigantes subidos a los hombros de otros gigantes. También se dice que la industria del software es un ejemplo de enanos subidos a los dedos de los pies de otros enanos"|Alan Cooper, Microsoft, VisualBasic, Ruby, ...
"La gestión manual de bloques de memoria en C es como hacer malabarismos con pastillas de jabón en la ducha de la prisión: todo diversión hasta que cometes un fallo"|Un usuario anónimo de un foro en Usenet
“Copiar código de internet y pegarlo en un sistema para producción es como usar un chicle encontrado en la calle”|Mike Johnson
"La complejidad es destructiva. Chupa la sangre de los desarrolladores, hace que los productos sean difíciles de planificar, construir y probar, introduce problemas de seguridad y provoca la frustración de usuarios finales y administradores"|Ray Ozzie, Lotus, arquitecto Microsoft, ...
"Programar sin una arquitectura o diseño en mente es como explorar una gruta sólo con una linterna: no sabes dónde estás, dónde has estado ni hacia dónde vas"|Danny Thorpe, Borland, Delphi, Visual Studio, ...
"No puedes crear un gran software sin un gran equipo, y la mayoría de los equipos de desarrollo se comportan como familias disfuncionales"|Jim McCarthy, inteligencia artificial, MIT, Premio Turing, ...
“Nada es más permanente que una solución temporal”|Primera ley de Thomas


|🤔||
|-|-|
"Tenemos que cambiar la tradicional actitud ante la construcción de software. En vez de pensar que nuestra principal tarea es indicar a un ordenador qué hacer, concentrémonos en explicar a las personas lo que queremos que el ordenador haga"|Donald E. Knuth, TEX, análisis de algoritmos, Premio Turing 1974
“El reto principal de los científicos informáticos es no confundirse con la complejidad de su propia creación”|E. W. Dijkstra, programación estructurada, concurrencia, Premio Turing 72
"Controlar la complejidad es la esencia de la programación"|Brian Kernigan, sistema operativo UNIX, ...
"Primero resuelve el problema. Entonces, escribe el código"|John Johnson
"Los buenos programadores usan sus cerebros, pero unas buenas directrices nos ahorran de tener que hacerlo en cada caso"|Francis Glassborow
“Se trata más de ser suficientemente bueno que de ser bueno o malo”|James Bach, Lessons Learned in Software Testing
“La calidad es gratis, pero sólo para aquellos que están dispuestos a pagar mucho por ella”|Tom deMarco, AT&T Bell Laboratories, análisis estrucutrado, ...
“Hay únicamente dos problemas realmente duros en informática: el primero es la invalidación de cachés, y el segundo darles nombres apropiados a las cosas”|Phil Karlton, Netscape
“El objetivo es entregar código limpio que funcione… ahora”|Kent Beck, eXtreme Programming, patrones de diseño, TDD, Smalltalk
"Antes de que un software sea reutilizable debería ser utilizable"|Ralph Johnson, GoF de Design Patterns
"Codifica siempre como si la persona que finalmente mantendrá tu código fuera un psicópata violento que sabe dónde vives"|Rick Osborne o Martin Golding o John Woods o Damian Conway, Perl


|😣||
|-|-|
"Un gran operario de tornos vale varias veces más que un operario medio, pero un gran escritor de código vale 10.000 veces el precio de un desarrollador medio"|Bill Gates, Microsoft
"Un hacker puede ser capaz de producir, en unos pocos meses, algo que un pequeño grupo de desarrolladores (digamos de 7 u 8 personas) podría tener trabajado duramente juntos más de un año. IBM solía decir que ciertos programadores podían ser 100 veces más productivos que otros trabajadores, o más"|Peter Seebach
"Los mejores programadores no son sólo marginalmente mejores que los buenos. Se trata de un orden de magnitud mayor, medida por cualquier estándar: creatividad conceptual, velocidad, ingenio o habilidad para solucionar problemas"|Randall E. Stross
“Eliminar a un mal desarrollador del equipo de un proyecto es a menudo más productivo que añadir un desarrollador bueno”|Tom DeMarco, AT&T Bell Laboratories, análisis estrucutrado


|😣||
|-|-|
"Es inevitable que la gente programe mal y la formación no mejorará sustancialmente las cosas. Tenemos que aprender a vivir con ello"|Alan Perlis, MIT, catedrático, director ACM, Premio Turing
"La formación en informática no puede convertir a nadie en experto programador, de la misma forma que estudiar pinceles y pigmentos no puede hacer a alguien un experto pintor"|Eric Raymond, La catedral y el bazar, Movimiento Open Source, anarcocapitalista

|🤔||
|-|-|
"Los programas deben ser escritos para que los lean las personas y sólo incidentalmente, para que lo ejecuten las máquinas"|Abelson and Sussman
"La mayoría de ustedes están familiarizados con las virtudes del programador. Son tres, por supuesto: pereza, impaciencia y orgullo desmedido"|Larry Wall, Perl
“La simplicidad es un prerequisito para la fiabilidad”|E. W. Dijkstra, programación estructurada, concurrencia, Premio Turing 72
"La simplicidad llevada al extremo se convierte en elegancia"|Jon Franklin
“La belleza es más importante en informática que en ninguna otra tecnología debido a la gran complejidad del software. La belleza es la defensa definitiva contra la complejidad”|David Gelernter, computación paralela, universidad de Yale
“Simplicidad: el arte esencial de maximizar la cantidad de trabajo no realizado”|Manifiesto Ágil
“Uno de mis días más productivos fue aquél en el que eliminé 1000 líneas de código”|Ken Thompson, lenguaje B, previo a C, AT&T Bell Laboratories
“Código eliminado es código depurado”|-- Jeff Sickel

## ¿Qué?

**[DISEÑO](https://dle.rae.es/dise%C3%B1o)**

|Análisis|Diseño|
|-|-|
Estudiar los requisitos a través de su refinamiento y estructura para realizar una compresión más precisa de los requisitos, una descripción de los requisitos que es fácil de mantener y ayuda a estructurar el sistema|Estudiar enfocados en los requisitos no funcionales y en el dominio de la solución para preparar para la implementación y pruebas del sistema
Dar una especificación más precisa de los requisitos obtenidos en la captura de requisitos|Adquirir una comprensión profunda sobre los aspectos de los requisitos no funcionales y limitaciones relacionadas con:
Describir usando el lenguaje de los desarrolladores y poder introducir más formalismo y ser utilizado para razonar sobre el funcionamiento interno del sistema|los lenguajes de programación,
Estructurar los requisitos de manera que facilite su comprensión, cambiándolos y, en general, mantenerlos|la reutilización de componentes,
Acercase al diseño, aunque sea un modelo en sí mismo, y es por tanto un elemento esencial cuando el sistema está conformado en diseño e implementación|sistemas operativos,
||tecnologías de distribución y concurrencia,
||tecnologías de bases de datos,
||tecnologías de interfaz de usuario,
||tecnologías de gestión de transacciones,





## ¿Para qué?



## ¿Cómo?

