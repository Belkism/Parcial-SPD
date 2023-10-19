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

3) Sugerencia como componente adicional:

![Motor CC](https://github.com/Belkism/Parcial-SPD/assets/138260690/65185ad6-a575-4e2c-9d8d-505475fdc439)

![Motor CC](https://github.com/Belkism/Parcial-SPD/assets/138260690/90384f39-0780-4629-af59-a4c76ba6e354)

Se le puede agregar al proyecto un "motor de aficionado", llamado así porque es un motor de cc (corriente continua) que se le acopló una carcasa para generar movimiento, ya sea para brazos, ruedas, hélices, etc. sobre este, podemos incluir al proyecto un "controlador de motor" o también llamado "Puente H" . En el siguiente enlace se enseña cómo podría usarse dicho motor y controlador en una placa arduino para controlar el sentido de giro del motor.


![ejemplo](https://github.com/Belkism/Parcial-SPD/assets/138260690/7c83c7d7-3b27-4b6c-ba4f-85aa3e04a380)

Enlace del ejemplo:
[Ejemplo Motor CC](https://www.tinkercad.com/things/4rXMr6WlaqW-super-gaaris-albar/editel?tenant=circuits)

Tercera Parte: Implementación de un fotodiodo en el proyecto

![Tercera parte](https://github.com/Belkism/Parcial-SPD/assets/138260690/ba2f4cfd-bff8-427f-9072-79e2ed682c98)


A la parte 2 le agregamos un fotodiodo . Un fotodiodo es un dispositivo semiconductor que genera una corriente eléctrica cuando se exponen a la luz. Esto se logra mediante la absorción de fotografías de luz que liberan electrones en el material semiconductor. Estos electrones generan una corriente eléctrica detectable. Para poder funcionar correctamente, un fotodiodo se compone de una polarización inversa, que permite el adecuado flujo de electrones o la corriente en sentido inverso. Los fotodiodos son muy sensibles y tienen una respuesta rápida a cambios en la intensidad de la luz. Pueden estar diseñados para detectar luz en un rango específico del espectro electromagnético, como infrarrojo, ultravioleta o visible. Los fotodiodos se utilizan en aplicaciones que requieren alta sensibilidad y precisión, como en fotodetectores, comunicaciones ópticas, lectores de códigos de barras y sistemas de control automático.



2) Explicación de su funcionamiento
Desde su salida negativa (Cátodo) la alimentamos con 5V y desde su salida positiva (Ánodo) la conectamos, a una entrada analógica de la placa de Arduino, ya una resistencia de 50kOhm que esta conectada a Tierra (Podemos colocarle otro valor a la resistencia , pero en este caso sugerimos colocarle ese valor para trabajar con ella, en el caso de querer colocar otra resistencia, tendriamos que regular todo otra vez). Ahora, por medio de una variable, en este caso lectura_luz, tomamos un rango de todos los valores que nos va dando el sensor a medida que incrementa o disminuye la intensidad luminosa, en este caso, nos entrega un rango de (49 - 1023), por lo que para saber que porcentaje de intensidad lumínica es, llamamos a otra variable, en este caso es luzutilizando la función map() para poner esos valores entre un rango del 0% al 100%. De esta manera, sabemos que a menor porcentaje de intensidad luminosa, el fotodiodo entrega menor voltaje y mayor porcentaje de luz liminica, el fotodiodo entrega un mayor voltaje.


Algunos ejemplos de uso del fotodiodo son:


Comunicaciones.
Lectores de códigos de barras.
Sensores de proximidad.
Sistemas de seguridad y alarmas.
Fotodetectores en experimentos científicos.
Radiometria y fotometria.
Detectores de infrarrojos (IR).
Detección de radiación UV.

![fotodiodo](https://github.com/Belkism/Parcial-SPD/assets/138260690/06a9db71-0aaf-4e20-b75c-606414c6fcb5)




