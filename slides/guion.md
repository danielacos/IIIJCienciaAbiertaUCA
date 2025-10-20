# Guion charla III Jornadas de Ciencia Abierta UCA

Buenos días a todos. En primer lugar, quiero agradecer a los organizadores de las III Jornadas de Ciencia Abierta UCA por la oportunidad de estar aquí hoy y compartir con ustedes algunas ideas sobre la importancia de la ciencia abierta en el mundo académico y científico y, en particular, en las matemáticas.

En esta charla, que he titulado "Modelar, simular y compartir: ciencia abierta en la investigación matemática", voy a introducir las herramientas que usamos en nuestro grupo de investigación para simular procesos físicos a partir de modelos matemáticos.

## Introducción

Primero, voy a hablar un poco sobre mí. Actualmente soy Profesor Ayudante Doctor en el Departamento de Matemáticas. Defendí mi tesis doctoral en 2024 sobre el análisis y la simulación numérica de modelos de crecimiento tumoral, en cotutela académica entre la Universidad de Cádiz y la Universidad de Tennessee en Chattanooga, Estados Unidos. Mi investigación se centra en el desarrollo y análisis de modelos matemáticos para describir fenómenos biológicos complejos, como la migración celular, el crecimiento de tumores y la interacción entre fluidos.

Este proceso tiene dos partes fundamentales: la modelización matemática y la simulación numérica.

La modelización matemática implica la formulación de ecuaciones que describen el comportamiento del sistema que estamos estudiando. Para esto, utilizamos herramientas de análisis matemático y teoría de ecuaciones diferenciales parciales. Por ejemplo, aquí he presentado un modelo matemático que describe el crecimiento de un tumor en función del tiempo y el espacio. Este modelo incluye ecuaciones que representan la proliferación celular, la difusión de nutrientes y la interacción entre tumor y nutrientes.

Una vez planteados estos modelos que describen la evolución de un fenómeno de interés, este sistema de ecuaciones hay que resolverlo. En este sentido, los modelos resultantes son habitualmente demasiado complejos como para aspirar a encontrar una solución exacta de los mismos. Es por ello que normalmente recurrimos a la simulación numérica, que consiste en implementar algoritmos computacionales para aproximar la solución de estas ecuaciones y obtener resultados que puedan ser interpretados y analizados. Hay diversas técnicas para llevar a cabo esta simulación numérica, como el método de elementos finitos, el método de diferencias finitas, el método de volúmenes finitos o el método de Galerkin discontinuo. Nosotros usamos principamente los métodos de elementos finitos y de Galerkin discontinuo, que son técnicas muy potentes y flexibles para resolver ecuaciones en derivadas parciales en geometrías complejas.

## Software

Estos algoritmos se implementan en software especializado, existiendo diversas opciones en el mercado, tanto de código cerrado como de código abierto.

Entre las herramientas de código cerrado, destacan Matlab, COMSOL Multiphysics, Ansys y Simscale. Estas plataformas ofrecen interfaces gráficas intuitivas y una amplia gama de funcionalidades para la simulación numérica. Además tienen una documentación extensa y buen soporte. Sin embargo, su uso puede estar limitado por licencias costosas, restricciones en la personalización del código y falta de transparencia en los algoritmos utilizados.

Entre las alternativas de software libre destacan FreeFEM++, FEniCS, Firedrake, MFEM, Dune, entre otras. Estas herramientas permiten a los investigadores acceder al código fuente, modificarlo según sus necesidades y compartir sus propias implementaciones con la comunidad científica. Además, fomentan la colaboración y la transparencia en la investigación, ya que los resultados obtenidos pueden ser reproducidos y verificados por otros investigadores. Sin embargo, estas herramientas pueden tener una curva de aprendizaje más pronunciada y una documentación menos extensa en comparación con las opciones de código cerrado. Además, el soporte técnico puede depender de la comunidad de usuarios y desarrolladores.

En nuestro grupo de investigación, utilizamos principalmente FEniCS para la simulación numérica de modelos matemáticos. FEniCS es una plataforma de código abierto que permite a los investigadores implementar y resolver ecuaciones en derivadas parciales utilizando el método de elementos finitos. Se trata de un proyecto iniciado en 2003 y que sufrió una gran actualización en 2021 con FEniCSx que permite muchas más funcionalidades. Esta biblioteca está programada principalmente en C++ y ofrece una interfaz de programación en Python, lo que facilita la implementación de algoritmos y la integración con otras bibliotecas científicas. Además, FEniCS cuenta con una comunidad activa de usuarios y desarrolladores que contribuyen al desarrollo continuo del software, tiene muy buena documentación y ofrecen soporte a través de foros.

Aquí está la web de FEniCS, desde donde podemos **acceder al código fuente** en GitHub, la **documentación**, los **tutoriales** y el **foro de preguntas**.

## Ejemplos

Con esta biblioteca hemos sido capaces de simular diversos fenómenos físicos.

Por ejemplo, la migración de neuroblastos, un tipo de célula progenitora del sistema nervioso central, que se desplazan desde la zona subventricular hasta el bulbo olfatorio en el cerebro. A la izquierda, podemos ver una imagen de un microscopio que muestra la distribución de estas células en el cerebro y a la derecha, una simulación numérica que reproduce este proceso de migración celular utilizando un modelo matemático basado en ecuaciones en derivadas parciales. Este trabajo ha sido publicado este año en la revista Mathematical Bioscience en abierto.

Ahora podemos observar una simulación de un proceso de crecimiento de un tumor. a la izquierda, vemos un tumor inicial esférico que crece con el tiempo buscando las zonas de mayor densidad de nutrientes, que se representan a la derecha, mediante un proceso de quimiotaxis. El tumor, crece de forma no simétrica consumiendo estos nutrientes. Este trabajo fue publicado en 2023 en la revista Computers & Mathematics with Applications y se puede encontrar en abierto en arXiv.

Finalmente, podemos ver la simulación de una gota de un fluido que está inmerso en un fluido de menor densidad y que cae al fondo del recipiente debido a la gravedad. La simulación muestra cómo la gota se deforma hasta que va alcanzando la situación de equilibrio. Este trabajo ha sido publicado en 2025 en la revista Applied Numerical Mathematics and Computation en abierto.

Además, los códigos utilizados para llevar a cabo estas simulaciones están disponibles en repositorios públicos de GitHub, lo que permite a otros investigadores acceder a ellos, reproducir y validar los resultados y construir sobre nuestro trabajo.

## Conclusiones

[Leer conclusiones en las diapositivas]