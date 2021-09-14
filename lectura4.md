# Lectura 4: Content-Based Recommendation Systems

El paper de esta semana trata sobre recomendación basada en contenido. Se discuten distintas formas de representar los items, formas de ubicar usuarios en un espacio afín, algortimos para recomendar items en cada representación (con sus ventajas y desventajas) y finalmente concluye con conjeturas sobre el futuro de la investigación en este rubro.

La primera sección me parece muy interesante, ya que siempre me había preguntado cómo lo hacían los algoritmos para llevar textos de lenguaje natural a un espacio vectorial. Incluso, me parece que hacer una explicación simple de la métrica *term-frequency times inverse document frequency* es amigable con los lectores que no están familiarizados con términos de *parsing*.

Sin embargo, la sección siguiente, *10.2 User Profiles*, es notoriamente más confusa. Por los primeros párrafos, se entiende que se hablará de métodos para ubicar a los usuarios en un espacio vectorial, tal como los ítems. Sin embargo, pasa inmediatamente a explicar métodos para recomendar items a los usuarios. No me queda claro en que punto se hace la división entre estas dos etapas.
