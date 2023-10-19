# Parcial-SPD
![imagen de presentación](https://github.com/Belkism/Parcial-SPD/assets/138260690/3dc65a4c-1b0b-405a-9553-27a1dc9a1321)

INTEGRANTES

- Mauricio Gabriel Harriet Thery
- Belkis Yolanda Guanipa López
- Cheimienst Hernández Gómez


Primera parte: Controlar un contador con botones en un programa que utiliza 2 displays de 7 segmentos en multiplexación.
![primera parte](https://github.com/Belkism/Parcial-SPD/assets/138260690/0c165d63-309b-4d5e-9bfa-c638d340c64b)

1) Descripción
  

Este proyecto involucra la implementación de un contador utilizando dos visualizadores de siete segmentos. El control del contador se realiza mediante tres botones: uno para incrementar el contador, 
otro para disminuirlo y un tercero para restablecerlo. La estructura fundamental del código comprende los siguientes elementos:

1)Definición de nombres significativos para diversos valores, lo cual no solo mejora la legibilidad del código, sino también optimiza el uso de la memoria.

2)Declaración de las variables necesarias para el desarrollo adecuado del programa.

3)Una función llamada setup()que configura los pines de entrada para los botones.

4)Una función llamada loop()que contiene la lógica principal del programa y se ejecuta continuamente mientras Arduino está encendido.

5)Una función de llamada presionarPulsador()que detecta si los botones se han presionado o no.

6)Una función llamada apagarDisplay()que se encarga de apagar todos los segmentos de los visualizadores.

7)Una función de llamada mostrarNumero()que se encarga de activar los segmentos correspondientes en el visualizador.

8)Una función de llamada prendeDigito()que permite activar los dígitos de unidades o decenas en los visualizadores.

9)Por último, una función llamada mostrarContador()que se encarga de presentar los valores de unidades y decenas en los visualizadores.

Además, en términos de la electrónica utilizada, se emplea la multiplexación y evita problemas de ruido de señal, como el fenómeno conocido como "debounce" o "efecto rebote" .

2) Enlace del proyecto:

[SPD - Primer parcial - Parte 1](https://www.tinkercad.com/things/lCP1Yd2mde5-parte-1-controlar-un-contador-por-medio-de-pulsadores-en-un/editel)

Segunda Parte: Cambio de estado por medio de un interruptor deslizante + sensor de flexión.

![segunda parte](https://github.com/Belkism/Parcial-SPD/assets/138260690/f1209fe4-5870-4e35-b15e-0bfa21d5502b)

1) Descripción
   
Para la parte 1, agregamos ahora un interruptor, donde su funcionamiento es alternar el estado entre, mostrar los números del contador de la misma manera que la parte 1, y mostrar de manera automática los números primos (números que solo son divisibles por 1 y por si mismos) que se encuentren entre el rango de 0 a 99. Para esto, declaramos una función llamadadetectarPrimo()

Además, se agregó un sensor de flexión , este dispositivo detecta la flexión o curvatura de un objeto, como un cable o una pieza flexible y entrega el ángulo de inclinación. Para esto se declara una función de nombre mostrarAngulo().

2) Enlace del proyecto
[SPD - Primer parcial - Parte 2](https://www.tinkercad.com/things/dzCsGi5BjrA-parte-2-cambio-de-estado-utilizando-un-interruptor-deslizante/editel)
   


