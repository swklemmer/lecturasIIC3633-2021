# Lectura 4: Content-Based Recommendation Systems

El paper de esta semana trata sobre recomendación basada en contenido. Se discuten distintas formas de representar los items, formas de ubicar usuarios en un espacio afín, algortimos para recomendar items en cada representación (con sus ventajas y desventajas) y finalmente concluye con conjeturas sobre el futuro de la investigación en este rubro.

La primera sección me parece muy interesante, ya que siempre me había preguntado cómo lo hacían los algoritmos para llevar textos de lenguaje natural a un espacio vectorial. Incluso, me parece que hacer una explicación simple de la métrica *term-frequency times inverse document frequency* es amigable con los lectores que no están familiarizados con términos de *natural language processing*.

Sin embargo, la sección siguiente, *10.2 User Profiles*, es notoriamente más confusa. Por los primeros párrafos, se entiende que se hablará de métodos para ubicar a los usuarios en un espacio vectorial, tal como los ítems. Sin embargo, pasa inmediatamente a explicar métodos para recomendar items a los usuarios. No me queda claro en que punto se hace la división entre estas dos etapas.

Más adelante, cuando se describen las métodos para generar el "modelo de un usuario" a partir de los datos, se introducen los árboles de decisión. Al contrario de lo que ocurrió con el *stemming*, este concepto es tratado de manera muy superficial. Para la suerte mía, yo conocía este concepto gracias al curso "Reconocimiento de Patrones", pero para una persona que no lo conozca, no debe quedar muy claro. Recomiendo usar una ayuda visual para explicarlo: se puede mostrar como este algoritmo va dividiendo un espacio de dos dimensiones en particiones, dado unos datos de entrenamiento.

En cuanto al *Roccio's Algorithm*, no queda muy claro cómo se verían una *query* y un *prototype* en un ejemplo real. En efecto, bajar la teoría a la práctica con un ejemplo concreto siempre ayuda a fortalecer el aprendizaje.

Me parece correcto que en la sección sobre el enfoque Bayesiano, el último párrafo explique que asumir independencia estadística entre palabras no necesariamente daña la optimalidad de la adaptación de un algoritmo a un conjunto de entrenamiento. Esto llama la atención, ya que el sentido común sugiere que la probabilidad de que una palabra aparezca en un texto es afectada por las palabras que están en su misma frase.

En la sección final, me parece muy interesante el uso de recomendación basada en contenido junto con filtrado colaborativo. Sin embargo, en la sección inicial dice que va a presentar los desafíos futuros del rubro del *Content-Based Recommendation Systems*, lo cual no hace en gran medida. Siento que faltó una última sección que tratara este tema en mayor profundidad.
