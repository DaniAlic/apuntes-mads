
## Desarrollo lean



<img src="diapositivas/desarrollo-lean.001.png" width="800px">

<img src="diapositivas/desarrollo-lean.002.png" width="800px">

<img src="diapositivas/desarrollo-lean.003.png" width="800px">

- El software es un **producto** muy distinto a los productos
  tradicionales: una aplicación no es una bicicleta, ni un televisor,
  ni un edificio. Tanto su desarrollo como su funcionamiento es
  singular.

- El proceso de desarrollo de software es un **proceso creativo** que
  tiene más elementos de **diseño** que de fabricación.
      - Los procesos de fabricación tradicionales son rígidos. En
        general los planos y características del objeto a producir
        están claramente determinados a priori y hay pocas decisiones
        que tomar.
      - En un proceso de diseño hay muchos **grados de libertad**, se
        deben escoger entre muchas posibles soluciones. El proceso
        intenta obtener la mejor opción, cumpliendo un conjunto de
        **restricciones** necesarias. Por ejemplo: el diseño de nuevo
        móvil, de un automóvil o de un mueble.

- Veremos que la filosofía _lean_ acerca ambos planteamientos: permite
  introducir **flexibilidad** en los procesos de fabricación tradicionales
  y un cierto **orden y método** en un proceso de diseño.

<img src="diapositivas/desarrollo-lean.004.png" width="800px">

- Ya hemos enlazado alguna otra vez las
  [diapositivas](http://dl.dropbox.com/u/1018963/Henrik%20Kniberg%20Agile%20Lean%20Slides.pdf)
  de [Henrik Kniberg](https://www.crisp.se/konsulter/henrik-kniberg).

<img src="diapositivas/desarrollo-lean.005.png" width="800px">


<img src="diapositivas/desarrollo-lean.006.png" width="800px">

- El objetivo de Ohno **no era conseguir producción en masa**. Su
  ideal era fabricar y entregar un producto **inmediatamente después**
  de que el cliente hubiera realizado un pedido. Pensaba que era mejor
  esperar un pedido que construir un inventario en anticipación del
  pedido.

- El concepto de "desperdicio" (_waste_) es un concepto muy general:
  es todo aquello que **no crea valor al cliente**: piezas que no se
  usan, elementos innecesarios, transporte, movimiento, espera,
  procesamiento extra, defectos.

- Toyota transfirió el concepto de desperdicio en fabricación al
**desarrollo del producto**. Cuando se comienza un proceso de
desarrollo, el objetivo es completarlo tan rápidamente como sea
posible, porque todo el trabajo que va en desarrollo no está añadiendo
valor **hasta que el coche sale de la línea de producción**. En cierto
sentido, los proyectos de desarrollo en marcha son idénticos al
inventario. Los diseños y los prototipos no son útiles a los clientes,
reciben valor sólo cuando se entrega el nuevo producto.

- Hay estudios que estiman que la aplicación de sistemas similares al
  TPS en empresas automovilísticas de Japón tiene como resultado una
  reducción a la mitad del esfuerzo de ingeniería y **reduce en 1/3 el
  tiempo de desarrollo** comparado con los enfoques tradicionales.

- Una de las características es el desarrollo rápido y concurrente y
  la habilidad de realizar cambios tarde en el ciclo de desarrollo. No
  hay que hacer decisiones irreversibles en primer lugar, hay que
  **retrasar las decisiones** tanto como sea posible, manteniendo
  abiertas distintas opciones, y cuando se realicen, hacerlas con la
  mejor información posible.

- Más información sobre el Toyota Production System (TPS) en la
  [Wikipedia](https://en.wikipedia.org/wiki/Toyota_Production_System).

<img src="diapositivas/desarrollo-lean.007.png" width="800px">

- [Citas](https://blog.deming.org/w-edwards-deming-quotes/large-list-of-quotes-by-w-edwards-deming/)
  de Edwards Deming.

<img src="diapositivas/desarrollo-lean.008.png" width="800px">

- Avanzamos un ejemplo de aplicación de una de estas técnicas al
  desarrollo de software. El **value stream map** (**mapa de flujo de
  valor**) consiste en analizar todas las fases por las que pasa una
  funcionalidad, característica, historia de usuario, tarea,
  etc. desde que se decide desarrollar hasta que se sube a
  producción. Dibujar una caja por cada uno de los pasos y estudiar el
  tiempo de trabajo y tiempo de espera en cada una de las fases. Es
  recomendable hacerlo con características reales, una vez terminadas.

<img src="value-stream-mapping.png" width="800px">

- En el ejemplo anterior las fases serían: (1) crear el documento de requerimiento, (2)
  dividir en tareas y estimar, (3) documento de planificación, (4)
  revisión del plan y obtener visto bueno, (5) desarrollar software,
  (6) pruebas del software, (7) validación del alcance, (8) despliegue.

- Cada empresa, dependiendo de la metodología de desarrollo que use,
  tiene un mapa de flujo de valor distinto. Es una herramienta
  importante para diseñar los tableros kanban.

- ¿Qué unidades son las que hay que analizar? ¿Historias de usuario?
  ¿Funcionalidades?. La recomendación es que sean elementos que no
  tengan mucha variabilidad de tamaño. Un concepto que se suele usar
  es el de **minimal marketable feature** (MMF): el "trozo" más
  pequeño de funcionalidad del producto que los clientes (o el
  _product owner_) puede priorizar. Suelen tomar forma de una historia
  de usuario, un requerimiento o una petición de funcionalidad. En el
  caso de Scrum, son los ítems del backlog.

<img src="diapositivas/desarrollo-lean.009.png" width="800px">

<img src="diapositivas/desarrollo-lean.010.png" width="800px">

- WIP: **Work In Process**, es un término lean que indica el número de
  ítems que están siendo procesados en una determinada celda o fase
  del proceso. En Kanban veremos que para cada una de las fases del
  proceso se define un límite en el WIP, que obliga a no aceptar más
  ítems una vez que se ha llegado al WIP. Cuando algún ítem termine el
  proceso y pase a la fase siguiente, se vuelve a coger un ítem
  nuevo. Pero nunca estaremos procesando más ítems que los definidos
  por el WIP.

- El flujo de trabajo pull, junto con el WIP, garantiza que no se
  produce sobre inventario y permite **detectar** fácilmente **cuellos
  de botella** en el proceso, procesos que consumen demasiado tiempo y
  que obligan a esperas e impiden una cadencia fluida (flujo,
  **flow**). Una fase que tarda demasiado en procesar los ítems hace
  que las fases previas se queden paradas, esperando, porque no pueden
  sobrepasar su WIP. En un sistema push esas fases seguirían
  procesando ítems, que se acumularían.

- El flujo pull y el mapa de flujo de valor permiten **analizar y
  reflexionar** sobre el proceso de producción.

<img src="diapositivas/desarrollo-lean.011.png" width="800px">

-
  [Sistema de producción pull](https://www.youtube.com/watch?v=ZIv2e61SH1A) (YouTube)

<img src="diapositivas/desarrollo-lean.012.png" width="800px">

- [Toyota just-in-time production system](http://www.toyota-global.com/company/vision_philosophy/toyota_production_system/just-in-time.html)

<img src="diapositivas/desarrollo-lean.013.png" width="800px">

- Henrik Kniberg:
  [Lean from the trenches](https://pragprog.com/book/hklean/lean-from-the-trenches)
  ([PDF](https://www.google.es/url?sa=t&rct=j&q=&esrc=s&source=web&cd=1&ved=0ahUKEwie0Pe2gbXPAhUCOxQKHfE_DwkQFggeMAA&url=https%3A%2F%2Fwww.crisp.se%2Ffile-uploads%2FLean-from-the-trenches.pdf&usg=AFQjCNFLq9y4a6bq1CCWa03EfonPhMbV5w))

<img src="diapositivas/desarrollo-lean.014.png" width="800px">

<img src="diapositivas/desarrollo-lean.015.png" width="800px">

<img src="diapositivas/desarrollo-lean.016.png" width="800px">

<img src="diapositivas/desarrollo-lean.017.png" width="800px">

<img src="diapositivas/desarrollo-lean.018.png" width="800px">

- Para hacer un diagrama de flujo acumulado (_cummulative flow
  diagram_) de una fase del desarrollo (columna del tablero Kanban o
  fase del mapa de flujo de valor) vamos contando semana a semana
  cuantos ítems se terminan en esa fase de desarrollo, y anotamos el
  incremento en el diagrama. 

<img src="incrementos-semanales.png" width="400px">

- De esta forma podemos, por ejemplo, hacer el diagrama de flujo
  acumulado de las historias de usuario terminadas. Este diagrama nos
  sirve para estimar una velocidad de desarrollo, lo que nos permite a
  su vez estimar número de historias terminadas en una determinada
  fecha. Suponemos ítems de tamaño similar. Si hay variabilidad en el
  tamaño de los ítems podemos estimar el tamaño de los ítems en
  **puntos de historia** (**_story points_**) y hacer un diagrama en
  el que el eje vertical sean los _story points_ en lugar del número
  de ítems.

<img src="cummulative.png" width="400px">

- Se puede hacer un diagrama conjunto de flujo acumulado de las
  distintas fases del desarrollo, para tener una visión de conjunto de
  todo el proceso de desarrollo. Para ello dibujamos varias líneas,
  cada una de un color, correspondientes a las distintas fases (ver
  ejemplo en la diapositiva o en el artículo de Pawel Brodzinski).

- Otro concepto importante es el **cycle time** o **lead time**, el
  tiempo medio en que una funcionalidad tarda en terminarse. Podemos
  representar las distintas funcionalidades terminadas en una gráfica,
  en el orden en el que se van terminando, y hacer un diagrama del
  tiempo transcurrido por cada una de ellas. De esta forma podemos ir
  obteniendo un conocimiento que nos servirá para estimar mejor las
  siguientes historias.

- Los diagramas anteriores están sacados de: 
    - José Manuel Beas: [Burn-up chart](http://jmbeas.es/guias/burn-up-chart/)
    - Pawel Brodzinski: [Cumulative Flow Diagram](http://brodzinski.com/2013/07/cumulative-flow-diagram.light)
    - Henrik Kniberg: [Lean from the trenches](https://pragprog.com/book/hklean/lean-from-the-trenches)


<img src="diapositivas/desarrollo-lean.019.png" width="800px">

- Cuando estamos comenzando a desarrollar las primeras funcionalidades
  del sistema, deberíamos **evitar tomar decisiones** sobre elementos
  críticos del diseño que no tengamos claros y que sean difíciles de
  cambiar en el futuro. En su lugar, debemos probar más de una
  alternativa y dejar abierta la posibilidad de cambio para el
  futuro. Estas alternativas deben incluir **todas las capas del
  desarrollo**: de la interfaz de usuario al _backend_. Serán ejemplos
  mínimos del sistema que se irán ampliando en cada iteración. Es lo
  que se denomina una **_trazer bullet_** (bala trazadora): una
  pequeña funcionalidad o ejemplo que afecta a todas las capas del
  desarrollo y que permite comprobar el funcionamiento de todos los
  elementos del sistema.

- En lugar de un plan fijo con fechas marcadas para entregar cada
  funcionalidad, el compromiso de un equipo ágil es **entregar valor**
  en forma de incremento cada 3 semanas (una buena analogía es una
  publicación periódica, como una revista semanal o mensual, cada
  semana o cada mes debe haber un nuevo ejemplar en los quioscos).

- Una idea importante es la denominada **option thinking**: podemos
  mantener distintas opciones abiertas y tomar la decisión de qué
  entregar lo más tarde posible. Esta idea es muy importante tanto en
  el diseño y el desarrollo del software, como en la selección de
  funcionalidades del _backlog_. Por ejemplo, en el caso del diseño,
  podríamos hacer un diseño que nos permita refactorizar fácilmente
  entre más de una implementación alternativa. En el caso de selección
  de funcionalidades por el _product owner_ hay que considerar el
  _backlog_ del sprint como opciones, no como compromisos. El PO puede
  modificar, añadir o eliminar ítems del sprint actual, asegurándose
  siempre que al final del sprint se entregará un incremento que
  aporte valor adicional.

- En el post de Kent Beck
  [Taming Complexity with Reversibility](https://m.facebook.com/notes/kent-beck/taming-complexity-with-reversibility/1000330413333156),
  se reflexiona sobre la ventaja de poder **deshacer decisiones** tomadas
  e incorporadas al producto, en el contexto de Facebook. En la
  mayoría de las ocasiones no estamos en situaciones irreversibles y
  podemos tomar decisiones que después tengamos que cambiar. Usemos la
  flexibilidad del software para desarrollar y desplegar pensando que
  podemos tener que deshacer lo que ya hemos hecho:
      - Sistema de control de versiones que permita recuperar
versiones pasadas puestas en producción.
      - Sistema de revisión de código que permita deshacer la
        integración de funcionalidades.
      - Sistema flexible de puesta en producción que permita deshacer
        el último cambio si las métricas caen después de haber sido
        probado por millones de personas.

<img src="diapositivas/desarrollo-lean.020.png" width="800px">

<img src="diapositivas/desarrollo-lean.021.png" width="800px">

<img src="diapositivas/desarrollo-lean.022.png" width="800px">

<img src="diapositivas/desarrollo-lean.023.png" width="800px">

- Interview with Mary Poppendieck: [An introduction to Lean Software Development](http://www.citerus.se/interview-with-mary-poppendieck-an-introduction-to-lean-software-development/)
