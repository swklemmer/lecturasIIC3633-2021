# Evaluating Recommendation Systems

Este paper entrega un repertorio de métodos para evaluar y comparar algoritmos recomendadores. Además, entrega directrices sobre cómo llevar a cabo estas evaluaciones con tal de extraer conclusiones correctas a partir de los resultados obtenidos. Los métodos de evaluación son divididos en tres clases: métodos *offline*, estudio de usuarios y métodos *online*. Vale la pena mencionar que esta publicación no es oficial, sino un borrador. En efecto, es cómun encontrar fórmulas no resueltas, *typos* u otros errores de formato.

Es apropiado que, en la sección 2.3, finalmente se relacionen las tres familias de evaluación. En específico, el paper indica que es recomendable comenzar la evaluación de un sistema de manera *offline*, después posiblemente llevar a cabo estudios de usuarios y finalizar con evaluación *online*. Este orden se debe a que la evaluación *online* es más sencilla y barata, por lo que puede ayudar a descartar inmediataamente sistemas inviables. Luego, los estudios de usuario son más caros y demorosos, pero pueden proveer información muy útil para el lanzamiento del sistema. Finalmente, la evaluación *online* puede ser un excelente método para comparar varios algoritmos, pero si alguno de los algortimos probados tiene muy mal desempeño, puede afectar negativamente la opinión de algunos usuarios. Esto ayuda a ver que los métodos presentados no son excluyentes, sino se complementan para analizar holísticamente un sistema recomendador.

En la sección 2.4.2, "Paired results", se indica cómo se puede determinar objetivamente si un sistema A es mejor que uno B cuando ambos han sido sometidos a los mismos experimentos. Para esto, se presentan varios test estadísticos que nos entregan una métrica de confianza, como el *p-value*, en base a varios experimentos de los cuales se extrae el desempeño de ambos sistemas. Sin embargo, nunca se especifica qué forma podrían tomar estas medidas de desempeño: ¿se usa el *accuracy*? ¿se mide el consumo del usuario?

En la siguiente sección se presenta el test de Mann-Withney. Este sirve para evaluar sistemas que no fueron sometidos a los mismos experimentos. Aquí, las ecuaciones son presentadas en líneas de texto, por lo que cuesta imaginar cómo se verá finalmente el test estadístico. Creo que siempre es ventajoso mantener el formato de las ecuaciones de una misma forma, cómo el presentado en la sección anterior.

En la sección 3.2.2, "Measuring Usage Prediction", los siguientes conceptos son introducidos para cuantificar qué tan bueno es un sistema recomendador a la hora de generar listas de recomendaciones (sin predecir específicamente el rating de cada item):

- *Precision*: De todas las recomendadas, cuales efectivamente son preferidas por el usuario. Idealmente 1.
- *Recall o TP-Rate*: De todas las preferidas por el usuario, cuales fueron recomendadas. Idealmente 1.
- *FP-Rate*: De las que el usuario no prefirio, cuales fueron erróneamente recomendadas. Idealmente 0.

Complementariamente, las curvas *Precision-Recall*, *ROC*, *CROC* y *GROC* son introducidas. Sin embargo, nunca se muestran figuras con ejemplos de estas curvas. Este me parece un error gravísimo, ya que desaprovecha el potencial de incluir un material gráfico pertinente. Asimismo, creo que es buena idea resumir los resultados de la sección siguiente, "3.2.3 Ranking Measures", en una tabla al final de la sección. En esta podrían aparecer todas las cifras para evaluar rankings presentadas (NDPM, Spearman, Kendall, R-score, NDCG y ARHR) junto con sus fórmulas y aplicaciones.

En las secciones finales, se describen una serie de conceptos que pueden complementar la evaluación de un sistema recomendador.
- *Novelty*: capacidad del algoritmo de recomendar items que el usuario no ha consumido.
- *Serendipity*: capacidad de recomendar exitosamente un item que el usuario considere inesperado.
- *Diversity*: capacidad de recomendar items que sean lejanos en un espacio de características.
- *Utility*: Beneficio que el sistema recomendador trae a su anfitrión o usuarios.
- *Risk*: Varianza esperada del *utility*.
- *Robustness*: Protección del algoritmo contra información falsa.
- *Privacy*: Protección del algoritmo de la información personal de sus usuarios.
- *Adaptivity*: Velocidad con que un algoritmo responde a cambios en la base de datos de usuarios, ratings o items.
- *Scalability*: Relación entre crecimiento de bases de datos e incremento de recursos (velocidad, memoria) necesarios.

Por un lado, la idea de ocultar ciertos ratings a partir de algún instante temporal para evaluar *novelty* me pareció mu inteligente. Creo que dedica el tiempo necesario a explicar el concepto, dar un ejemplo y plantear formas de medirlo. De igual forma, ocultar ciertos datos para medir *serendipity* me pareció ingenioso y claro. No obstante, al igual que en la sección pasada, falta una tabla de resumen o recurso visual que pueda ayudar a resumir toda la información.

