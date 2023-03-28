

***ELECTRÓNICA IV – CURSO 2023***

***Trabajo Práctico de Laboratorio Nº1***

***Convertidores DC/DC y transistores MOS***

**Objetivo:** Familiarizarse con el funcionamiento de los transistores MOS de potencia (disparo, formas de

onda, tiempos) y de una topología de convertidor DC/DC básica de modo analítico y empírico. Analizar los

modos de funcionamiento de un convertidor DC/DC (continuo y discontinuo) y los elementos que afectan la

eficiencia y su cálculo.

Lea y analice atentamente el trabajo en su totalidad antes de comenzar. Los diagramas esquemáticos y los

valores de componentes son sólo orientativos, debe diseñar y calcular sus propios circuitos y componentes.

\1) Topología: funcionamiento teórico y simulado

a. Diseñe un convertidor DC/DC de acuerdo con los valores de la tabla y el diagrama esquemático **de**

**referencia** adjuntos. Calcule (considerando el diodo ideal):

\-

\-

\-

Valores de los componentes.

Valores máximos, mínimos, medios y rms de tensiones y corrientes.

Rango de operación del circuito en cada modo, corriente de salida en modo “boundary”

y corriente máxima de salida (calcule los resistores necesarios).

Obtenga las formas de onda teóricas del circuito, trabajando en los tres modos de

funcionamiento (para continuo utilice la máxima potencia de carga).

\-

b. Considere en su circuito la caída de tensión real del diodo elegido, calcule el nuevo valor de D

necesario para trabajar en modo continuo y explique qué modifica este valor en las formas de onda.

c. Construya un modelo en LTSPICE utilizando todos los valores reales de componentes y compare los

resultados de simulación con las curvas teóricas. Explique las diferencias.

Grupo

Tipo

Fsw

Vd

Vo

∆푉

푂⁄푉

VGG

Inductor

푂

1

2

3

Boost

Boost

Boost

50KHz

40KHz

60KHz

12

6

12

20

15

24

5%

7%

2%

18

18

18

RLB9012-221KL \*\*

RLB9012-221KL \*\*

RLB9012-221KL \*\*

\*\* www.digikey.com

Tabla 1. Valores de diseño por grupo

R4= 0,5 Ω

Figura 1. Circuito esquemático de referencia

\2) Disparo de un transistor MOSFET:

a. Calcule los tiempos de conmutación del MOS (encendido y apagado) en el caso real de su

circuito trabajando a máxima carga.

b. Analice y compare las curvas de conmutación teóricas y simuladas. Explique las diferencias,

descartando los efectos del circuito de disparo.

Electrónica IV

TP Lab. Nº 1 – Curso 2023

Pág. 1





c. Calcule la potencia disipada en el transistor y el diodo. Analice la necesidad de utilizar

disipador y en caso de que sea necesario calcule la resistencia térmica necesaria.

\3) Construcción del prototipo:

a. Diseñe la disposición física de componentes (Layout) de su circuito, muestre la distribución

teórica de lazos de corriente en cada momento de la conmutación (ON, OFF y

conmutaciones) y verifique con las simulaciones.

b. Arme físicamente el circuito en una placa universal cableada o en PCB, trate de utilizar la

placa más pequeña posible que le permita realizar bien las mediciones (objetivo aprox.

5x5cm).

c. Mida con el osciloscopio todas las formas de onda del circuito, analícelas y compare con las

teóricas y simuladas. Explique las diferencias, justificando sus hipótesis mediante las

simulaciones.

**Informe:**

Este trabajo debe entregarse el **viernes 14 de abril** de 2023, al finalizar el horario de clase; mediante un

informe de 6 carillas como máximo (no se contará todo el material excedente), que se enviará a través del

campus virtual. En caso de tener inconvenientes con la entrega enviar por mail a <mweill@itba.edu.ar>[ ](mailto:mweill@itba.edu.ar)y

<ltori@itba.edu.ar>

**Restricciones:**

●

●

Utilice transistores y diodos de potencia disponibles en el pañol. Asegúrese que los BJT de disparo

soportan la corriente de Gate (o sea… ¡calcule la corriente de Gate!). Asegúrese de calcular

correctamente las resistencias de base y colector para disparar los transistores adecuadamente.

**NUNCA dispare un MOS de potencia directamente con el generador de señales, SIEMPRE utilice un**

**circuito de disparo intermedio.**

**Recomendaciones:**

●

●

Utilice cables o pistas lo más cortos posible. Asegúrese que los lazos de corriente no quedan

entrelazados (acoplamiento magnético).

Utilice transistores y diodos que no estén demasiado excedidos en sus características (dentro de lo

disponible en el pañol). Por ejemplo: utilice un diodo MUR160 en lugar de MUR460 si la corriente no

supera 1A.

●

●

●

Utilice Leds y resistores como carga (máximo 20mA por cada Led).

Piense bien antes de tomar una imagen del osciloscopio. ¿Qué quiere mostrar?

Marque sobre las imágenes con color indicando lo más relevante o agregando información, con el fin de

que sean útiles para explicar el comportamiento del circuito.

En la topología boost se sugiere analizar, entre otras cosas, lo siguiente:

●

●

●

●

●

Medición de tensión y corriente de entrada.

Medición de la corriente en el inductor.

Duty Cycle del convertidor en CCM y DCM.

Al finalizar Ton, medir la tensión en el colector. (¿Qué sucede si estamos en DCM?).

Medir la tensión de salida contrastándola con el disparo del transistor (analizar las tensiones

máxima/mínima verificando la carga del capacitor durante el Toff). Tener en cuenta la ESR del

capacitor.

●

Utilizar una señal como referencia cuando se obtengan mediciones del osciloscopio, de manera de

poder comparar los distintos gráficos, por ejemplo la tensión de Gate.

***¡Recuerde que la parte más importante del trabajo son sus observaciones y conclusiones!***

Qué es lo más importante para los TPs de la materia?:

\-

No intentar construir el mejor convertidor Boost, sino dedicar el tiempo a analizar lo que construyeron.

Por ejemplo: es mucho más valioso poder determinar porque el ripple de tensión real es mayor que el

calculado, demostrándolo con algún experimento (cambiando la tecnología del capacitor u otra medida

similar), que mostrar una imagen de osciloscopio de un convertidor sin ripple.

\-

¿Transferencia? No desarrollarla, está en el libro y se toma en el parcial. Mostrar el D calculado en

función de la entrada y salida, y analizar las diferencias. Mostrar las corrientes y tensiones en todos los

componentes en todos los estados del circuito y analizarlas. Analizar el circuito, realizar hipótesis y

comprobarlas, por ejemplo: ¿qué pasa si se deja el circuito sin carga?

Electrónica IV

TP Lab. Nº 1 – Curso 2023

Pág. 2





\-

\-

\-

\-

\-

¿Qué criterio se utilizó para calcular el capacitor en función del ripple de tensión de salida? ¿Se verifican

los cálculos en la práctica? ¿Cómo puedo explicar las diferencias?

¿Simulación? Sí, ¡hay que hacerla! Empezar con componentes para familiarizarse con las formas de onda

“macroscópicas”, para luego ir incorporando detalles.

Muestren sus circuitos, esquemas, fotos y formas de onda con las leyendas necesarias para que sea fácil

entender qué están mostrando.

Verifiquen su circuito paso a paso: ¿están disparando bien al transistor? ¿Los tiempos de conmutación

son acordes a lo calculado?

Imágenes del osciloscopio: siempre indicar qué, dónde y CÓMO se mide la señal de la imagen. Incluir

alguna donde se aprecie el ripple de salida y/o tensión en la inductancia o alguna variable importante

en un componente importante según la topología. Agreguen una imagen para verificar que el circuito

funciona bien en modo DCM o CCM (el deseado). Incluir formas de onda combinadas, como VGate, VDrain

y VL (según topología), o VOut en AC y VGate (con escala para ver el ripple y entender sus distintas partes).

Modifiquen la carga entre los extremos de operación para verificar que el circuito funciona

correctamente en todos los puntos intermedios.

Comparación entre teoría, simulación y práctica. Si hay diferencias entre el duty calculado y el real

justificar por qué (utilizar la simulación de componentes ideales y modificarla para que la misma iguale

a la práctica).

\-

\-

\-

Conclusiones y aportes extras (por ejemplo: medir eficiencia Pout/Pin). En las conclusiones no poner

teoría, sólo observaciones prácticas, ¿qué pasó?, ¿qué fue difícil de medir?, ¿qué se debería cambiar

para mejorar el circuito? JUSTIFIQUEN todas sus aseveraciones, por ejemplo: el ripple de tensión en el

capacitor es mayor que el pedido por la tecnología del capacitor, lo cual fue verificado agregando

capacitores de otra tecnología (o midiendo el capacitor por separado), etc.

**RECORDAR**: Una imagen de osciloscopio/simulación sin información extra no suma nada en el informe. Les

recomendamos marcar e indicar lo más importante tomando de ejemplo la siguiente imagen.

¿Por qué este

salto?

¿Por qué esta forma

de onda durante la

descarga?

Dar datos y

mostrarlos sobre

las mediciones

Electrónica IV

TP Lab. Nº 1 – Curso 2023

Pág. 3

