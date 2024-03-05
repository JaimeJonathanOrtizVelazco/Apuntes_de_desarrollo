# Gang of Four

## Creational Patterns / Patrones de creación

Son patrones de diseño para la creación de objetos.

### Singleton

Restringe la inicializaron de clases para asegurar que solamente una instancia sea creada por cada clase.

### Factory

Toma la responsabilidad de una clases de crear instancias para moverla a una fabrica de instancias.

Básicamente dependiendo de los valores que le pasemos a la fabrica, va a ser la dependencia que nos va a regresar

### Abstract Factory

Nos permite crear una fabrica de clases fabrica

### Builder

Crea un objecto paso a paso y tiene un método para finalizar y regresar la instancia del objeto regresado.

Aquí es tener una inner class estática que sea el builder en la clase de interés y setters para las variables de la clase principal.

## Prototype

Crea una nueva instancia de un objeto desde otra instancia y hace las modificaciones acuerdo a los requerimientos
