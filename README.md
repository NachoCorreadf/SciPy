# SciPy

## Media
#### La media es el promedio de un conjunto de datos. En SciPy, la función para calcular la media es "scipy.mean()", pero lo más común es usar "numpy.mean()" para este propósito. Sin embargo, te mostraré el uso de scipy.

## Mediana
#### La mediana es el valor central de un conjunto de datos cuando están ordenados. Si el número de elementos es par, es el promedio de los dos valores centrales. SciPy tiene la función "scipy.stats.median()".

## Moda
#### La moda es el valor que más veces se repite en el conjunto de datos. SciPy tiene la función "scipy.stats.mode()" para calcularla.

## Ejemplo de codigo
 ~~~~
import numpy as np
from scipy import stats

# Datos de ejemplo
datos = [1, 2, 2, 3, 4, 5, 5, 5, 6, 7, 8, 9]

# 1. Media (usando numpy)
media = np.mean(datos)
print(f"Media: {media}")

# 2. Mediana (usando scipy)
mediana = np.median(datos)
print(f"Mediana: {mediana}")

# 3. Moda (usando scipy.stats.mode)
moda_resultado = stats.mode(datos)
moda = moda_resultado.mode[0]  # Obtener el valor de la moda
print(f"Moda: {moda} (Frecuencia: {moda_resultado.count[0]})")
 ~~~~

## Explicacion
* Media: Utilizamos "np.mean(datos)" para obtener la media.
* Mediana: Usamos "np.median(datos)" para obtener la mediana.
* Moda: Con "stats.mode(datos)", obtenemos el valor más frecuente en el conjunto de datos y la cantidad de veces que se repite.

  ## Salida esperada
~~~~
Media: 4.416666666666667
Mediana: 5.0
Moda: 5 (Frecuencia: 3)
~~~~
