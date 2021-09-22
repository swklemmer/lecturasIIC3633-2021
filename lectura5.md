# Combining Predictions for Accurate Recommender Systems

La publicación analiza el uso de *ensemble learning* en algoritmos recomendadores. Estos métodos "combinan" varios algortimos de Filtrado Colaborativo en uno solo. La base de datos de prueba es la famosa *Netflix Prize Dataset*. Finalmente, los autores demuestran que combinar varios algortimos de CF resulta en un algoritmo más preciso que cada algortimo de CF por sí solo.

Para combinar algoritmos, el método más fácil consiste en promediar los ratings predichos por cada uno. Una forma más sofisticada, el *Linear Blending*, consiste en hacer una suma ponderada de aquellos, donde los pesos para el rating de cada algoritmo son entrenados. Sin embargo, el mejor desempeño se alcanza usando técnicas de combinación como *A*, *B* o *C*.

Luego de la introducción, los autores explican brevemente cada uno de los algoritmos de CF usados en el *Dataset*: *User-KNN*, *Item-KNN*, factorización matricial SVD, *Assymetric Factor Model* (AFM), SVD extendido, *Resctricted Boltzmann Machines* (RBM) y *Global Effects* (GE). Me parece un excelente resumen, ya que además de explicar el funcionamiento del algoritmo, explica sus requerimientos computacionales y desempeño en comparación al resto sin extenderse demasiado.

En particular, los algoritmos no vistos en clase son explicados brevemente a continuación:
- AFM:
- SVD extendido
- RBM:
- GE:



Idea: ¿Usan nDCG? si no, accuracy no es suficiente para saber si la mejora ayudará a dar mejores recomendaciones, en la medida que estas nuevas predicciones se traduzcan a *rankings* distintos.
