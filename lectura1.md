# Lectura 1: Collaborative Filtering Recommender Systems

Este paper explica los conceptos claves del "Collaborative Filtering", sus usos principales, sus consideraciones de diseño y la forma en que se evalúan. Finalmente, presenta los problemas éticos relacionados a la privacidad de los usuarios y las preguntas que esto abre.

La sección introductoria 9.1 no me parece apta para comenzar el paper. En primer lugar, presenta páginas y aplicaciones arcaicas que generan más preguntas que respuestas para un usuario que lee esto en 2021. Entiendo que intente mostrar el contexto histórico que dió inicio a CF, pero creo que llegar rápidamente a la explicación de los algortimos es más claro y más general que comenzar directamente con ejemplos de la vida real.

Por otra parte, la sección 9.2.3 sobre propiedades de los set de datos me parece mucho más "insightfull". Permite relacionar directamente las capacidades de CF son posbiles aplicaciones y le brinda al lector un criterio para preferir CF frente a otras alternativas. Este criterio se vuelve más claro aún cuando CF es comparado con "Content Based Filtering" en la sección 9.2.4.

Otro aspceto que genera confusión es la introducción de un criterio para categorizar algoritmos de CF en "memory-based" y "model-based". Este se presenta brevemente y luego nunca vuelve a ser utilizado. Por ende, me parece que estaría mejor ubicado en el pie de página o en un anexo. No obstante, en los capítulos siguientes, donde se presentan las variantes e implementaciones novedosas de los CF probabilísticos y no-probabilisticos (lo cual es el criterio que sí se utiliza), se dan descripciones breves y precisas de cada uno. En particular, se le asigna el espacio y profunidad necesario para entender la estrategia detrás de cada uno, junto a sus ventajas y desventajas, sin extenderse demasiado.

De igual forma, en las consideraciones de diseño, los autores no se detienen demasiado tiempo, sino dedican lo justo y suficiente para explicar las diferencias entre ratings explícitos o implícitos, distintas escalas de rating o métodos para enfrentar el "Cold Start".

Por último, cuesta entender el contexto en el que este artículo es publicado. Esto se debe a que alterna entre información seria y ejemplos burdos, lo cual genera un sensación ambivalente sobre la dirección de la publicación: no se entiende si está apuntada a ingenieros o al público general.
