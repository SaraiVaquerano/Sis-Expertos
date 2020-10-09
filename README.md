# Sis-Expertos
En este caso se genera una estructura de datos de 10 millones de puntos con la función de numpy random, con distribución normal con media de 500 y escala de 30 para lo cual se utiliza la función de numpy normal (loc, scale, size). Luego se procede a en la variable **suma_puntos** meter todos los datos menores a 500,000 de la variable **puntos** en otro array para finalmente sumarlos. 

**importar librerias**
import time
import numpy as np

**inicializacion de variables y generacion de datos al azar**
inicio = time.time ()
puntos = np.random.normal(500,30,10000000) 

**suma de datos menores a 500,000**
suma_puntos=puntos[puntos<=500000]
suma_puntos=np.sum(suma_puntos)

**imprimir resultados**
print(suma_puntos)
print('Duracion: {} segundos'.format(time.time() - inicio))
