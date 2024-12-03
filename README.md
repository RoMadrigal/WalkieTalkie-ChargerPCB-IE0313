# WalkieTalkie-ChargerPCB-IE0313

Repositorio para la tarea del curso IE0313 sobre el diseño de una PCB de una fuente de alimentación para un Walkie-Talkie. Contiene el circuito esquemático, el diseño de la PCB en KiCad y documentación sobre los componentes a utilizar, el procedimiento de diseño y otros detalles. 

Este repositorio y sus contenidos fueron diseñados durante el curso IE0313 durante el periodo II-2024 por los siguientes integrantes del equipo:

<div align="center">

|        **Integrantes**      | **Carné** |
|:---------------------------:|:---------:|
|    Anthony Calvo García     |   C11433  |
|   Rodrigo Madrigal Montes   |   C24458  |

</div>

## Circuito base

El circuito del que partimos para diseñar la PCB es el que se diseñó en la **Tarea 3**:

<div align="center">

| ![Circuto de la fuente de alimentación*](images/CircuitoFuenteAlimentacion.png) |
|:--:|
| *Circuto de la fuente de alimentación* |

</div>

Para este ciruito se tiene el siguiente listado de componentes:

<div align="center">

|     Componente     | Especificación |
|:------------------:|:--------------:|
|    Transformador   |      20:1      |
| Diodo rectificador |     1N4007     |
|      Capacitor     |     1.1 mF     |
|     Resistencia    |      6 Ω       |
|     Diodo Zener    |     1N5338B    |
|      Fusible 1     |     400 mA     |
|      Fusible 2     |     200 mA     |

</div>

## Diseño del esquemático 

Primero para el diseño del esquemático de la PCB se seleccionó la opción *Schematic Editor* en *KiCad*, posteriormente se siguió la metodología de pasos descrita en la página de [Arcos-Lab Wiki](https://wiki.arcoslab.org/en/tutorials/kicad/example), a lo cual primero se definieron el el título, fecha y revisión del proyecto. 

Posteriormente se procedió a agregar los símbolos de cada componente a utilizar en el esquemático, acomodarlos y realizar las conexiones, a lo cual se obtuvo lo siguiente:

<div align="center">

| ![Diseño del esquemático*](images/img1.png) |
|:--:|
| *Diseño del esquemático* |

</div>

Aquí hay algunas elecciones que es importante mencionar son:

### Transformador

Se realizó una investigación sobre diseños de circuitos en el mismo programa que eran similares a este y se encontró que en base a las recomendaciones y experiencias de estos usuarios determinamos que era mejor dejar el transformador fuera de la PCB ya que consumen mucho más espacio y es más seguro conectarlo como un componente externo, por lo cual para este diseño consideramos que la salida del transformador se conecta en la terminal `J1`. 

### Elección de huellas y componentes

Por otro lado en cuanto a las huellas de los componentes por ejemplo para los diodos, tanto para los `1n4007` y el `1n5338B` se utilizo la huella que ya venía asignada por defecto en el programa; y aplicamos lo mismo para la resistencia y las terminales. Ahora bien en cuanto al capacitor se realizó la busqueda de varios capacitores disponibles en el mercado para poder determinar las dimensiones a utilizar del mismo. 

Nos terminamos decantando por los modelos de capacitor del fabricante **Vishay** de una capacitancia de 1200 μF que es lo más cercano al valor teórico que definimos en el circuito. Y se utilizaron las medidas presentes en el [Datasheet 135D, 135J, 135L](https://www.vishay.com/docs/40024/135d-135j-135l.pdf) y se asignaron a la huella en el esquemático. Y además se agregó el *Datasheet* del mismo en la tabla de componentes en el programa para poder acceder rápidamente al mismo sin necesidad de salir del programa y buscarlo. 

Después se procedió a colocar las etiquetas a los nodos `Vs` y `gnd` para los nodos de alimentación y tierra, y se colocaron los símbolos de `PWR_FLAG` para indicar a *KiCad* que es por medio de estos nodos que se alimentará el circuito. 

Y una vez realizados todos los pasos anteriores se procedió a seleccionar la opción *Perform electrical rules check* para verificar que no haya conexiones inválidas o algún error en alguna configuración del circuito a lo cual obtuvimos una salida sin errores. 

## Diseño de la PCB

Primero se realizó la configuración previa en el editor de PCB, donde definimos que la placa tendría dos capas y se definieron el el título, fecha y revisión del proyecto en esta página. Posteriormente se utilizó la opción *Update PCB with schematic changes* para poder importar los modelos del esquemático a la página del editor de PCB.

