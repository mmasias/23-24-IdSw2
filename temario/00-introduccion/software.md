# Software

## ¿Por qué?

### Hardware

La humanidad gracias a sus herramientas y, en particular, al conocimiento (ciencias, ingenierías, etc.), ha construido grandes sistemas artificiales: acueductos, telares con tarjetas perforadas, red eléctrica, red telefónica, etc.​ para automatizar tareas, o sea, simplificar y reutilizar

- 8000 aec., Los sumerios construyen telares para cubrirse
- 1642 ec., Blaise Pascal construye la Pascalina, primera calculadora mecánica girando ruedas
- 1801 ec., Jacquard construye el primer telar mecánico y automático con tarjetas perforadas para definir los dibujos
- 1842 ec., Charles Babbage y Ada Lovalace trabajan sobre la Máquina Analítica, con las tarjetas perforadas de los telares …​ pero no llegó a funcionar aunque Ada ya escribió las primeras líneas de código de la historia.
- 1884 ec., Hollerith desarrolló la Máquina Tabular de tarjetas perforadas para ordenar el registro de propiedad en la Conquista del Oeste
- 1936 ec., Konrad Zuse, ingeniero alemán, diseñó y fabricó la Z1, la que para muchos es la primera computadora programable de la historia

## ¿Qué?

|||
|-|-|
Software es la información que suministra el desarrollador al ordenadir para que manipule de forma automática la información que suministrará el usuario — Brad Cox|![](/images/modelosUML/modelosUML/sistemaDeInformacion.svg)

### Naturaleza de Lenguajes y Formatos

||||
|-|-|-|
Programas en lenguajes de programación (Java, C/C++, …​),|Scripts para la generación de páginas dinámicas en aplicaciones Web (JSP, PHP,…​),|Datos de configuración en diversos formatos (texto libre, XML, JSON, …​)
Scripts para la creación de las tablas de las bases de datos y su población (SQL),|Presentaciones en lenguajes de formato para aplicaciones Web (HTML, CSS, …​)|Multimedia en formatos de imagen, sonido o video para elementos gráficos en la Interfaz de Usuario (*.png, *.waw, *.mpeg, …​)

## ¿Para qué?

||Capacidad cualitativa|Capacidad cuantitativa|
|-|-|-|
|**Ser humano**|Muy buena: reconocimiento de patrones, asociaciones, recursividad, …​|Muy mala: pequeña, errores por cansancio, desmotivación, …​ y muy lentos
|**Máquina**|Muy mala: ningún computador superó la prueba de Turing (de momento)|Muy buena: sin errores y a toda velocidad

---

|![](/images/modelosUML/modelosUML/software.svg)|
|-|

### Sistema de Información

Un sistema de información es un conjunto de elementos orientados al tratamiento y administración de datos e información, organizados y listos para su uso posterior, generados para cubrir una necesidad o un objetivo

- **Gestión** (CRUD), es el tratamiento de la información:
  - **altas** (Create) de información en el sistema
  - **bajas** (Delete) de información en el sistema
  - **modificaciones** (Update) de información en el sistema
  - **consultas** (Read) de información en el sistema

## ¿Cómo?

**El trabajo con software es el más complejo que jamás haya emprendido la humanidad** — F. Brooks

|Métrica|Proyecto de Software|Don Quijote de la Mancha|
|-|-|-|
|Extensión|Proyecto mediano: 100.000 lineas y ~3 palabras/línea|300.000 palabras
|Entidades|*identificadores* …​ centenares|*Dulcinea, Sancho Panza*, …​ decenas
|Autor|6-8 personas|Miguel de Cervantes Saavedra
|Duración|entre 6 meses y años|18 años
|Coste|Miles de €|"gratis" (en la cárcel)
|Ámbito|Definido por otra(s) persona(s)|suyo

### Sistemas 

|Sistema de software|¿Es complejo?|
|-|-|
|Conjunto de clases/módulos relacionándose por herencia, composición, … o interdependientes formando una aplicación. Cada aplicación está delimitada por su entorno tecnologíco-comercial, descrito por su arquitectura del software y requisitos y expresado en su ejecución|Software de una aplicación media (~100.000 líneas de código) tiene una complejidad que excede con creces la capacidad intelectual humana|

### Características de los sistemas complejos

|Estructura jerárquica|Elementos primitivos relativos|Separación de asuntos|Patrones comunes|Formas intermedias estables|
|-|-|-|-|-|
|Un sistema complejo está compuesto de subsistemas interrelacionados que a su vez tienen sus propios subsistemas y así hasta que se alcanza algún elemento del más bajo nivel.|La elección de qué componentes en un sistema son primitivos es relativamente arbitraria y suele estar a discreción del observador del sistema|Las intra-conexiones de componentes son más fuertes que las inter-conexiones de componentes. |Los sistemas jerárquicos se componen generalmente de sólo unos pocos tipos diferentes de subsistemas en varias combinaciones y órdenes. |Un sistema complejo que funciona invariablemente se encuentra que ha evolucionado a partir de un sistema sencillo que funcionó. 
|Los niveles de su jerarquía representan los diferentes niveles de abstracción cada uno construido sobre otro y cada uno comprensible por sí mismo.|.|Este hecho tiene el efecto de separar los componentes con dinámica de alta frecuencia (involucrando la interacción entre componentes) de los de dinámica de baja frecuencia. |Nos encontramos con una gran similitud en la forma de mecanismos compartidos unificando esta vasta jerarquía.|Un sistema complejo diseñado desde cero no funciona y no puede ser remendado para hacer que funcione. 
|En cada nivel de abstracción, encontramos una colección de elementos que colaboran para proveer servicios a niveles superiores|.|Hay una clara separación de asuntos entre las partes de diferentes niveles de abstracción|.|Hay que comenzar de nuevo, a partir de un sistema sencillo de trabajo

***“La observación general es que el principal enemigo de la fiabilidad, y tal vez de la calidad del software en general, es la complejidad”*** - Bertrand Meyer

### Software & Sistemas complejos I

#### Abstracción

- “Proceso mental de extracción de las características esenciales de algo, ignorando los detalles superfluos” [Booch]
- Proporciona límites conceptuales claramente definidos.
- Es subjetiva.
- Separa el comportamiento esencial de un objeto de su implantación.
- Es paralela al vocabulario del dominio.

#### Encapsulación

- “Proceso por el que se ocultan los detalles del soporte de las características esenciales de una abstracción” [Booch]
- Proporciona barreras explícitas entre abstracciones ⇒ Conduce a una clara separación de asuntos.
- ∴ Podremos cambiar los soportes de las características de una abstracción sin afectar a quienes la utilicen.

#### Abstracción & Encapsulación

Todo aquello que no sea necesario dar a conocer, no se debe dar a conocer.

`Clase = interfaz + implementación`

Entonces:

- La abstracción debe preceder a las decisiones de implantación.
- Ninguna parte de un sistema complejo debe depender de detalles internos de otra parte.
- **Interfaz**: vista exterior. Único lugar donde establecemos las suposiciones que puede hacer un cliente.
- **Implementación**: Mecanismo para conseguir el comportamiento deseado.

#### Modularidad

- “Proceso de descomposición de un sistema en un conjunto de piezas poco acopladas y cohesivas”  [Booch]

|Acoplamiento|Cohesión|
|-|-|
|El acoplamiento “[...] es la medida de fuerza de la asociación establecida por una conexión entre un módulo -elemento- y otro. El acoplamiento fuerte complica un sistema porque los módulos son más difíciles de comprender, cambiar o corregir por sí mismos si están muy interrelacionados con otros módulos” [Booch, 96]. |“La cohesión mide el grado de conectividad entre los elementos de un solo módulo.” [Booch, 96] |
|Por tanto, hay que minimizar las dependencias entre módulos|Por tanto, un módulo cohesivo debe tener significado propio por sí mismo agrupando abstracciones lógicamente relacionadas|

|Descomponer para||
|-|-|
|poder refinar independientemente.
|crear límites bien definidos.
|entender algunas partes a la vez en lugar de todas a la vez.
||***divide et impera***

Debería ser posible cambiar la implementación de unos módulos sin el conocimiento de la aplicación ni de otros módulos y sin afectar el comportamiento de los otros módulos.

El bajo acoplamiento de un módulo se basa en la **abstracción** que limita su interfaz a lo esencial y en la **encapsulación** que oculta todos los detalles necesarios para su implantación pero innecesarios para otros módulos que se relacionen con éste.

#### Jerarquía

“Clasificación u ordenamiento de las abstracciones” [Booch]

Organización de elementos en niveles de responsabilidad, clasificación o composición.


### Software & Sistemas complejos II

|Estructura jerárquica|Elementos primitivos relativos|Separación de asuntos|Patrones comunes|Formas intermedias estables|
|-|-|-|-|-|
|Gracias a sus jerarquías de herencia, composición, paquetes con clases con atributos y métodos, métodos con sentencias, sentencias con expresiones, …​|Gracias a sus tipos primitivos dependiendo del lenguaje (enteros, cadena de caracteres?, fechas?, …) y los definidos por el usuario|Gracias a la encapsulación y modularidad|Gracias a algunos métodos de clases que corresponden al paso de mensajes a objetos|Gracias a las metodologías iterativas o por culpa de nuevas tecnologías o nuevas necesidades|


