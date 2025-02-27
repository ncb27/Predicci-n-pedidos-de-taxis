# Predicción pedidos de taxis
El objetivo del proyecto era desarrollar un modelo de Machine Learning para predecir la cantidad de pedidos de taxis en la próxima hora, ayudando a la empresa Sweet Lift Taxi a optimizar la disponibilidad de conductores en horas pico.
### Metodología
#### Preprocesamiento de datos:

Se cargaron los datos desde taxi.csv, conteniendo información sobre pedidos de taxis en intervalos de 10 minutos.
Se convirtió la columna de fecha a formato datetime y se remuestrearon los datos a intervalos de 1 hora, sumando los pedidos.
#### Entrenamiento y evaluación de modelos:

#### Se probaron tres modelos: Regresión Lineal, Random Forest y XGBoost.
El mejor modelo fue Random Forest, logrando un RECM de 23.03 en el conjunto de prueba, seguido de XGBoost (26.60) y Regresión Lineal (28.78).
#### Optimización de hiperparámetros:

Se utilizó GridSearchCV para afinar Random Forest, obteniendo los mejores parámetros:
max_depth=20, min_samples_leaf=1, min_samples_split=5, n_estimators=200.
Con estos ajustes, el modelo alcanzó un RECM de 25.82 en entrenamiento.
#### Validación cruzada:

Se realizó validación cruzada con 5 particiones, obteniendo un promedio de RECM de 40.71, lo que sugiere cierta variabilidad y problemas de generalización.
### Conclusiones
Random Forest fue el modelo más efectivo, aunque su desempeño varió en diferentes conjuntos de validación.
La predicción de pedidos puede mejorar la gestión de la oferta y la demanda de taxis en horas pico.
Se podrían explorar nuevas características y técnicas para mejorar la capacidad de generalización del modelo.
