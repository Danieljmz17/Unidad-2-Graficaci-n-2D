Unidad 2: Graficación 2D
2.1 Transformación bidimensional

Las transformaciones bidimensionales son operaciones matemáticas que permiten modificar la posición, orientación, tamaño o forma de los objetos en un plano cartesiano (2D). Estas transformaciones son fundamentales en la computación gráfica, ya que permiten manipular figuras sin necesidad de redefinir completamente sus coordenadas originales. Se aplican comúnmente en videojuegos, interfaces gráficas, animaciones y diseño asistido por computadora.

Las transformaciones 2D trabajan sobre puntos representados como pares ordenados (x, y), y suelen implementarse mediante operaciones matriciales para facilitar su composición y eficiencia computacional.

2.1.1 Traslación

La traslación consiste en desplazar un objeto en el plano sin alterar su forma ni su orientación. Este movimiento se realiza sumando un vector de desplazamiento (tx, ty) a cada punto del objeto.

Matemáticamente, si un punto original es (x, y), después de la traslación se convierte en (x + tx, y + ty). Esta transformación es ampliamente utilizada en animaciones, por ejemplo, para mover un personaje en pantalla.

2.1.2 Escalamiento

El escalamiento permite cambiar el tamaño de un objeto, ya sea ampliándolo o reduciéndolo. Esto se logra multiplicando las coordenadas del objeto por factores de escala (sx, sy) en los ejes x e y.

Si sx y sy son mayores que 1, el objeto crece; si están entre 0 y 1, el objeto se reduce. Es importante considerar el punto de referencia (origen o centro del objeto), ya que afecta el resultado visual del escalamiento.

2.1.3 Rotación

La rotación consiste en girar un objeto alrededor de un punto fijo, generalmente el origen o su centro. El ángulo de rotación determina cuánto gira el objeto, y puede ser en sentido horario o antihorario.

Este tipo de transformación es esencial en simulaciones, videojuegos y modelado gráfico. La rotación modifica tanto la posición como la orientación del objeto.

2.1.4 Sesgado

El sesgado (o “shearing”) es una transformación que distorsiona la forma de un objeto desplazando sus puntos en una dirección proporcional a su posición en otro eje. Como resultado, el objeto parece inclinado.

Este tipo de transformación es útil para efectos visuales o simulaciones de perspectiva en gráficos 2D.

2.2 Representación matricial de las transformaciones bidimensionales

Las transformaciones 2D se representan comúnmente mediante matrices, lo que permite combinarlas de forma eficiente mediante multiplicación matricial. Para facilitar esto, se utilizan coordenadas homogéneas, añadiendo una tercera componente (w = 1) a los puntos.

Por ejemplo, un punto (x, y) se representa como (x, y, 1). Cada transformación (traslación, rotación, escalamiento, etc.) se expresa como una matriz 3x3. Esto permite aplicar múltiples transformaciones en una sola operación mediante la multiplicación de matrices.

El uso de matrices es fundamental en motores gráficos, ya que mejora el rendimiento y la organización del código.


2.3 Trazo de líneas curvas

El trazo de curvas en gráficos 2D permite representar formas más complejas y suaves que las líneas rectas. Estas curvas son ampliamente utilizadas en diseño gráfico, animación y modelado.

Las curvas se definen mediante puntos de control y funciones matemáticas que determinan su forma.

2.3.1 Bézier

Las curvas de Bézier son uno de los métodos más utilizados para generar curvas suaves. Se definen mediante un conjunto de puntos de control, donde la curva no necesariamente pasa por todos ellos, pero sí se aproxima a su forma.

Son muy utilizadas en programas de diseño como Adobe Illustrator y en gráficos vectoriales. Su principal ventaja es la facilidad para manipular la forma de la curva ajustando los puntos de control.

2.3.2 B-spline

Las curvas B-spline (Basis spline) son una generalización de las curvas de Bézier. Permiten mayor flexibilidad y control local sobre la forma de la curva.

A diferencia de las curvas de Bézier, modificar un punto de control en una B-spline solo afecta una parte de la curva, lo que las hace ideales para modelado complejo y animaciones.

<img width="1331" height="993" alt="image" src="https://github.com/user-attachments/assets/362574e8-24ac-47c3-ab0b-682bbb914da4" />


2.4 Fractales

Los fractales son estructuras geométricas complejas que se caracterizan por su autosimilitud, es decir, presentan patrones que se repiten a diferentes escalas. Se generan mediante algoritmos iterativos y funciones matemáticas.

Son utilizados en gráficos por computadora para generar paisajes naturales, texturas y efectos visuales. Ejemplos conocidos incluyen el conjunto de Mandelbrot y los copos de nieve de Koch.

Los fractales combinan matemáticas, arte y programación, siendo un tema importante en la visualización computacional.

2.5 Uso y creación de fuentes de texto

En la graficación 2D, el manejo de texto es fundamental para interfaces gráficas y visualización de información. Las fuentes de texto (tipografías) pueden ser de mapa de bits o vectoriales.

Las fuentes vectoriales son las más utilizadas actualmente, ya que permiten escalar el texto sin pérdida de calidad. Estas fuentes están basadas en curvas (generalmente Bézier), lo que facilita su renderizado en diferentes tamaños y resoluciones.

La creación de fuentes implica diseñar cada carácter utilizando herramientas especializadas, considerando aspectos como legibilidad, estilo y proporciones.

Referencias:
Foley, J. D., van Dam, A., Feiner, S. K., & Hughes, J. F. (1996). Computer Graphics: Principles and Practice (2nd ed.). Addison-Wesley.
Hearn, D., & Baker, M. P. (2010). Computer Graphics with OpenGL (4th ed.). Pearson.
Angel, E., & Shreiner, D. (2015). Interactive Computer Graphics: A Top-Down Approach with WebGL (7th ed.). Addison-Wesley.
Rogers, D. F. (2001). An Introduction to NURBS: With Historical Perspective. Morgan Kaufmann.
Salomon, D. (2006). Curves and Surfaces for Computer Graphics. Springer.
