# Estructura de los sistemas operativos

## Qué es un Sistema Operativo

:::{tip} Personas: Mary Allen Wilkes (1937 - )
:class: dropdown
En los años 1959 a 1963, Participó en el  proyecto {abbr}`LINC (Laboratory Instrument Computer)`, un dispositivo enfocado en el procesamiento de datos en tiempo real en biomedicina. En ese proyecto, asumió la responsabilidad de escribir todo el software de sistema. Su principal aporte fue LAP6 (LINC Assembly Program 6), un entorno operativo y de programación interactiva [@wilkes1970conversational] ([copia local](./docs/[1970]Conversational-Access.pdf)). Fue el primer sistema operativo que estaba entre el hardware y los programas. (["Pioneers in Tech"](https://leahycenterblog.champlain.edu/2022/03/29/pioneers-in-tech-mary-allen-wilkes/)). Además, al integrar al sistema LINC un editor de texto que utilizaba una pantalla y teclado, cimentó las bases de interacción con los sistemas de cómputo actuales ([ver nota](https://www.mobolize.com/2023/03/07/womens-history-month-mary-allen-wilkes-was-a-linc-programmer-and-first-to-use-a-pc-at-home/))

```{figure} images/02-allen.png
:label:02-allen
:width: 50%
:align: center

Mary Allen en el año 2017 con el ordenador personal de 1960 que ella desarrolló. Fotografía: Imago/EDP/Werner Kruepe
```

:::

Un Sistema Operativo ({abbr}`SO (Sistema Operativo)`) se define formalmente como la capa de software fundamental que actúa como intermediario crítico entre el hardware subyacente y las aplicaciones de usuario, gestionando de manera eficiente, equitativa y segura los recursos computacionales [@Silberschatz2018]. Desde la perspectiva de la arquitectura de sistemas, el hardware provee las capacidades físicas primarias —tales como unidades de procesamiento, jerarquías de memoria, subsistemas de almacenamiento y dispositivos de entrada/salida—, mientras que los programas y aplicaciones definen los requerimientos funcionales y de rendimiento. El {abbr}`SO (Sistema Operativo)` arbitra estas demandas mediante algoritmos de planificación (*scheduling*), control de concurrencia y políticas de asignación, determinando cómo se utilizan dichos recursos para resolver problemas computacionales complejos en entornos dinámicos.


```{figure} images/02-arq-ssoo-01.png
:label: 02-arq-ssoo-01
:width: 50%
:align: center

Esquema de tres niveles para un sistema de cómputo genérico. El Sistema Operativo actúa como un intermediario entre las aplicaciones y el hardware disponible.
```

Para lograr lo anterior, un {abbr}`SO (Sistema Operativo)` debe proveer un conjunto de abstracciones del hardware a las aplicaciones que se ejecutan en el sistema. Estas abstracciones transforman los componentes físicos en entidades lógicas (por ejemplo, procesos e hilos en lugar de registros de CPU y ciclos de reloj; espacios de direcciones virtuales en lugar de celdas de memoria física; sistemas de archivos en lugar de bloques en discos magnéticos o de estado sólido). Como consecuencia directa de este diseño, distintos Sistemas Operativos definen diferentes modelos de abstracción sobre una misma arquitectura de hardware, priorizando aspectos específicos como el rendimiento en tiempo real, el aislamiento de seguridad, la eficiencia energética o la portabilidad [@muralidhar2022energy].

Actualmente, las arquitecturas de cómputo se caracterizan por ser heterogéneas (procesadores multi-core, GPUs y TPUs) y estar implantados en entornos distribuidoss. Debido a esto, el rol de las abstracciones del SO es fundamental para el uso masivo de estos sistemas. Investigaciones recientes en el área de sistemas operativos [@gill2024modern] [@deng2024cloud] destacan que la evolución de las interfaces de abstracción es importante para cerrar la brecha entre la complejidad del hardware emergente y las altas exigencias de rendimiento de las aplicaciones basadas inteligencia artificial a gran escala, por ejemplo.


## Abstracciones del HW

### Proceso

Un proceso es un programa en ejecución junto con todos los recursos que necesita para operar (espacio de memoria, registros de la CPU, identificadores y archivos abiertos). A diferencia de un programa —que es una estructura pasiva almacenada en un sistema de almacenamiento persistente como código ejecutable—, el proceso es una entidad activa que consume ciclos de procesador y memoria RAM gestionada por el sistema operativo.

Los componentes del procesos son almacenados en una estructura denominada {abbr}`PCB (Process Control BLock)` (ver {numref}`Figura %s <PCB-01>`) contiene los siguientes elementos (entre otros):

* Espacio de direcciones en memoria que contienen el Texto o Código (instrucciones en lenguaje máquina) que ejecutadas en la {abbr}`PU (Process Unit)`.

* Espacio de direcciones en memoria para almacenar variables globales, variables locales (stack)

* Espacio de direcciones en memoria para almacenar datos que el código solicita en forma dinámica (heap)

* Identificador de proceso (PID), que es un número entero sin signo que identifica al proceso

* Registros que está utilizando en la {abbr}`PU (Process Unit)`. El principal es el {abbr}`PC (Programm Counter)`

* Estado actual (Ready, Running, Blocked, Waiting)

* Archivos utilizados

* Información de gestión de recursos: Punteros de memoria asignada, descriptores de archivos abiertos y dispositivos de E/S en uso.


```{figure} images/02-PCB-01.png
:label: PCB-01
:width: 50%
:align: center

Representación del PCB de un proceso
```

### Unidad de procesamiento




## Sistema Multiprogramados

## Sistemas de Tiempo Compartido

## Operación de un Sistema Operativo



