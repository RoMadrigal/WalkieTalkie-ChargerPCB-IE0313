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

Se realizó una investigación sobre diseños de circuitos en el mismo programa que eran similares a este y se encontró que en base a las recomendaciones y experiencias de estos usuarios determinamos que era mejor dejar el transformador fuera de la PCB y 