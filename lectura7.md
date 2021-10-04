# Interactive recommender systems: a survey of the state of the art and future research challenges and opportunities

Esta publicación presenta un marco conceptual para analizar las interfaces visuales interactivas que han sido desarrolladas para apoyar sistemas recomendadores. Estas interfaces buscan dotar a los sistemas recomendadores con virtudes que mejoran la experiencia del usuario, como transparencia, confianza y control, además de mitigar problemas como *Cold Start*.

En su segunda sección, el árticulo comienza resumiendo los desafíos que atañen a los sistemas recomendadores: mitigación del *Cold Start* para el filtrado colaborativo, mejorar la explicabilidad de los fundamentos de cada recomendación y desarrollo de las vías para obtener información contextual del usuario. En la tercera sección, señala que una interfaz visual interactiva está apuntada al usuario final y permite que él visualice la información sobre su representación personal (por ejemplo, lista de recomendaciones que ha hecho), sus datos contextuales (ubicación, género, etc.), representación en el *medio* (por ejemplo, una región en el espacio latente) y/o sus recomendaciones. Además, permite que este usuario entregue *feedback* al sistema recomendador, lo que actualiza su visualización en tiempo real.

En la cuarta sección, se presenta un análisis de 24 sistemas recomendadores que ya han incorporado alguna interfaz interactiva. Estos son divididos en grupos, dependiendo de cuál es la cualidad que pretenden mejorar como su objetivo principal: transparencia, justificación, controlabilidad, diversidad, *Cold Start* y contexto.

Hay un par de ideas que me parecieron interesantes y que considero provechoso destacar. En primer lugar, TasteWeights es un sistema interactivo de recomendación híbrida, es decir, combina tanto *Content-Based* como filtrado colaborativo. No obstante, su interfaz permite a los usuarios controlar qué tanto peso tienen los dos paradigmas de recomendación. Siguiendo la nomenclatura de Janach et. al. (2010), correspondería a una hibridización paralela *mixed*. En segundo lugar, Pharos intenta aliviar el *Cold Start* ofreciéndole al usuario unirse a una "comunidad" de usuarios con gustos similares. Esta técnica sigue el paradigma del "*clustering*", en la medida que puede agrupar a usuarios que sean cercanos en gustos. Así, no es necesario calcular la similitud del usuario nuevo hacia otros usuarios, sino se pude comenzar usando el promedio de su *cluster* como aproximación inicial.


En la quinta sección, primero se estructura la información y finalmente (5.4) se resumen las evaluaciones sobre el impacto que las interfaces visuales interactivas tiene sobre los sistemas recomendadores estudiados. Varios criterios son utilizados, por ejemplo efectividad (si la interfaz ayuda a que los usuarios acepten mejor las recomendaciones), desempeño (si disminuye el tiempo que le toma al usuario para encontrar un ítem relevante), confianza, etc.. A mi parecer, los resultados más relevantes son lo siguientes:

- Cuando la interfaz otorga control al usuario, es posible mejorar el *accuracy* de las recomendaciones.
- Cuando el usuario busca un ítem en particular, la búsqueda manual es más efectiva que la interfaz interactiva.
- Cuando los usuarios sobre-ajustan la interfaz a sus preferencias, el sistema recomendador pierde diversidad.
- Cuando la interfaz ayuda a los usuarios a ahorrar tiempo y encontrar ítems más relevantes, esto puede aumentar su compromiso con el sistema.
- Darle completo control sobre su perfil al usuario no necesariamente mejora su confianza, debido a temores relacionados con la privacidad.
- No todas las formas de visualización son igual de útiles: diagramas de árboles tienden a ser más útiles que los diagramas circulares, porque los límites entre capas están más claros.

Las conclusiones de la lista anterior me parecen excesivamente útiles para una persona que está diseñando un sistema recomendador interactivo. Aprendiendo de la experiencia, la podría usar como *checklist* para asegurar que su interfaz realmente esté mejorando la experiencia del usuario. Esto, sumado a los criterios entregados en la segunda sección, podrían servir para entender realmente cuál es el aporte que la interfaz puede hacer a las recomendaciones: no se trata sólo de presentar los resultados de forma estética, sino de estrechar la relación multidimensional entre el usuario y el sistema recomendador.

Finalmente, la sexta sección resume los resultados anteriores y, en base a lo que no había sido explorado hasta la fecha, proponen líneas de investigación para el futuro. Creo que esto es muy valioso para alguien que está comenzando a investigar en el rubro de los sistemas recomendadores interactivos, por lo que esta publiación es ideal para comenzar.

Referencias bibliográficas
- Jannach, D., Zanker, M., Felfernig, A., & Friedrich, G. (2010). Recommender systems: an introduction. Cambridge University Press. Chicago
