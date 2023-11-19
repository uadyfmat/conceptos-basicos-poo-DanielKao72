## 1. Diferencia entre Clase y Objeto
Una clase es una representación del mundo real abstraída de tal manera que tiene características (atributos) y comportamientos (métodos), es decir, sería una descripción del *qué* de una entidad. Por otro lado, el objeto es un ejemplo de la entidad, la cual define cómo se caracteriza y comporta, por lo que cada objeto es único. 

De esta manera, la diferencia radica en que la clase define el qué es la entidad, mientras que el objeto define el cómo es dicha entidad.
## 2. Diferencia entre Clase e Interfaz
Como se mencionó anteriormente, la clase define el qué es la entidad. En el caso de la interfaz, ésta establece un comportamiento sin contexto alguno.

De esta manera, su diferencia radica en que una clase define el comportamiento de una entidad en concreto, mientras que una interfaz solo tiene comportamiento sin estar asociado a una entidad.

## 3. ¿Qué es el polimorfismo? Ejemplifica
El polimorfismo consiste en la capacidad que tiene un objeto de comportarse de diferentes maneras dependiendo del contexto.

Por ejemplo, sea una interfaz "Busqueda" que tenga el método no implementado de "hacerBusqueda", y hayan tres clases de tipos de busqueda distintas: "BusquedasLink", "BusquedasPivotes" y "BusquedasCadena" que implementen la interfaz. Una clase "Scrapping" implementa un método "imprimirBusqueda" que acepta cualquier objeto que implemente la interfaz "Busqueda", por lo que las tres clases pueden pasar por ese método gracias al polimorfismo, el cual les permite ser de tipo "Busqueda".
## 4. ¿Qué representan las asociaciones en un diagrama de clase? Ejemplifica
Las asociaciones en un diagrama de clase representan las relaciones que existen entre las clases de un programa, y las cuales tienen características en particular, y permite modular todo un proyecto. 

Por ejemplo, sea la clase "Link" y la clase "Egresado", entre éstas existe una relación de composición, la cual consiste en que a cada Egresado le corresponde un solo Link de un perfil de LinkedIn.
## 5. Diferencia entre Composición y Agregación. Ejemplifica
Ambas son asociaciones o relaciones que pueden existir entre las clases de un programa. Son similares, pero no iguales, pues consisten en que una clase se compone de otra o que a partir de clases *base* se creen entidades más complejas. Sin embargo, la diferencia radica en la dependencia entre las clases relacionadas. Por parte de la Composición, si la clase más compleja es eliminada, entonces las clases *base* pierden sentido en la abstracción del programa, pero en la Agregación, no hay problema, pues las entidades pueden existir por separado.

Se puede tomar el ejemplo anterior, donde la clase "Egresado" tiene como atributo un objeto de la clase "Link", pues a cada egresado le corresponde un enlace a perfil de LinkedIn. Este es un ejemplo de Composición, pues "Link" deja de tener sentido si se eliminara "Egresado", puesto que ésta primera clase solamente existe para componer a un "Egresado".

## 6. ¿Qué es el encapsulamiento? ¿Qué ventajas tiene? Ejemplifica
El encapsulamiento coniste en la privacidad, ocultamiento o acceso de los datos de una clase, define si la información es pública, privada o protegida. Sus ventajas son:
* Limita el acceso a la información de una clase por parte de clases ajenas.
* Permite un código más legible y fácil de mantener en el futuro.

Por ejemplo, el patrón de diseño Singleton utiliza el encapsulamiento para que una clase tenga una sola instancia durante todo el programa. Se la clase "Connections", que realiza la conexión a una base de datos, tiene el constructor privado, lo que obliga a implementar un método para crear una instancia de "Connections", y su vez, permite que no haya más de una conexión durante la ejecución del código.

## 7. ¿De qué manera se representa la modularidad en POO? Ejemplifica
En POO, para dividir las tareas que realiza un proyecto de software se crean y utilizan paquetes (conformados por las clases necesarias para el proceso); cuyos nombres, cantidad y forma en la que estén organizados depende de la abstracción hecha del proyecto.

Un ejemplo de modularidad, en POO, es el patrón de diseño MVC, el cual divide el proyecto en tres partes/paquetes fundamentales:

* Un Modelo donde se encuentran las abstracciones de la información que se maneja durante el programa.
* Una Vista que se despliega para que el usuario pueda interactuar.
* Un Controlador que es un intermediario entre la Vista y el Modelo, y gestiona la lógica del programa y la interacción del usaurio.
    

## 8. Considera el polimorfismo. ¿Cuál es la diferencia entre Herencia e Interfaz? (Ventajas y Desventajas)
Sabemos que el polimorfismo se refiere a la capacidad de un objeto de comportarse de distintas maneras, lo cual logra a través de Interfaces o Herencia. La Interfaz define comportamiento sin algún contexto y la Herencia establece una relación de derivación, pues define que una clase hereda características de otra.

Su diferencia, conceptualmente hablando, radica en el polimorfismo, pues un objeto que implemente Interfaces puede cambiar su comportamientos a través de un "¿qué puede hacer?", mientras que la Herencia lo hace a través de un "¿qué puede ser?"

### Herencia
* Ventajas:
    1. Permite una buena abstracción del programa, pues es fácil ver una jerarquía.
    2. Permite reutilizar código.
* Desventajas:
    1. La jerarquía puede volverse confusa.

### Interfaces
* Ventajas:
    1. Permite que varias clases pueden implementar la misma interfaz.
    2. Se puede implementar más de una interfaz.
    3. Reutilización de código.
* Desventajas:
    1. No se cuenta con el comportamiento (métodos) establecidos.
    2. Es posible que se duplique por error el comportamiento (duplicado de métodos).