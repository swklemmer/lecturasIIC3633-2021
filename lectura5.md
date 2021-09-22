# Combining Predictions for Accurate Recommender Systems

La publicación analiza el uso de *ensemble learning* en algoritmos recomendadores. Estos métodos "combinan" varios algortimos de Filtrado Colaborativo en uno solo. La base de datos de prueba es la famosa *Netflix Prize Dataset*. Finalmente, los autores demuestran que combinar varios algortimos de CF resulta en un algoritmo más preciso que cada algortimo de CF por sí solo.

Para combinar algoritmos, el método más fácil consiste en promediar los ratings predichos por cada uno. Una forma un poco más compleja, el *Linear Blending*, consiste en hacer una suma ponderada de aquellos, donde los pesos para el rating de cada algoritmo son entrenados. Sin embargo, el mejor desempeño se alcanza usando técnicas de combinación más sofisticadas como *A*, *B* o *C*.

Luego de la introducción, los autores explican brevemente cada uno de los algoritmos de CF usados en el *Dataset*: *User-KNN*, *Item-KNN*, factorización matricial SVD, *Assymetric Factor Model* (AFM), SVD extendido, *Resctricted Boltzmann Machines* (RBM) y *Global Effects* (GE). Me parece un excelente resumen, ya que además de explicar el funcionamiento del algoritmo, explica sus requerimientos computacionales y desempeño en comparación al resto sin extenderse demasiado.

En particular, los algoritmos no vistos en clase son explicados brevemente a continuación:
- AFM: Es un tipo de factorización matricial donde el vector latente de cada usuario se obtiene directamente desde los items con los que ha interactuado.
- SVD extendido: SVD, pero que además de usar las features obtenidas desde las interacciones, usa features relacionadas al tiempo en que cada rating ocurrió.
- RBM: red neuronal de una capa de entrada y una capa oculta. Cada usuario recibe una probabilidad de consumir un cierto item.
- GE: parecido a SVD, pero los factores latentes son "diseñados a mano".

El concepto de residuales me parece sumamente interesante. Creo que corresponde explicar un poco mejor de dónde proviene. Si bien, se hace una referencia a la cita [20], no está demás explicitar de qué década son las ideas de entrenamiento residual.

Se explica que cada algoritmo fue entrenado con un Set de Entrenamiento de incluía al subconjunto *pTrain* y *pTest*. Luego, la función de *Blending*, la cual se encarga de combinar las predicciones de cada algoritmo, se entrena usando exclusivamente *pTrain* y luego se evalúa usando *pTest*. Aquí surge la duda si hay alguna interacción entre los dos procesos de entrenamiento. También surge la duda si se está "haciendo trampa" al usar las muestras de *pTest* tanto en el entrenamiento de los algoritmos individuales como en la evaluación del *Blending*. Por ende, creo que en esta parte falta justificación.

Los métodos de *Blending* estudiados son,
- *Linear Regression*: Asigna pesos constantes a la predicción de cada algoritmo.
- *Binned Linear Regression*: Para entrenar la regresión, separa los datos previamente en *bins*, siguiendo algún criterio.
- Redes Neuronales: genera automáticamente un modelo no lineal para mapear las predicciones de cada algoritmo a una sola predicción conjunta.
- *Bagged Gradient Boosted Decision Tree* (BGBDT): un conjunto de *Decission Trees* se entrenan en paralelo sobre distintos subconjuntos de datos aleatorios. En cascada, se entrenan más árboles sobre los residuos de los anteriores.
- *Kernel Ridge Regression Blending* (KRR): ajusta los pesos de cada algoritmo para minimizar una función de pérdida gausiana.
- KNN Blending: dado un vector de predicciones, para encontrar la predicción resultante, encuentra a los k vectores de predicciones más cercanos del set de entrenamiento y genera el promedio sus predicciones reales.

Para reportar el RMSE de cada Blend, el número de decimales no es constante, por lo que es un poco más confusa la comparación. Recomiendo siempre dejarlo constante.


Idea: ¿Usan nDCG? si no, accuracy no es suficiente para saber si la mejora ayudará a dar mejores recomendaciones, en la medida que estas nuevas predicciones se traduzcan a *rankings* distintos.
