```python
import numpy as np
import datetime
from datetime import date
```


```python
# Ejemplo clásico de lanzamiento de una moneda

universo = ['cara', 'sello']

```


```python
# Número de resultados favorables / número de resultados totales
p_cara = 1/2
```


```python
from scipy.stats import bernoulli
```


```python
# rvs => Random Variable Sample
bernoulli.rvs(p=p_cara)
```




    1




```python
universo[bernoulli.rvs(p=p_cara)]
```




    'sello'




```python
# Demostración de la probabilidad
bernoulli.rvs(p=p_cara, size=10)
```




    array([1, 1, 1, 0, 1, 0, 0, 1, 0, 1])




```python
sum(bernoulli.rvs(p=p_cara, size=10))
```




    6




```python
from scipy.stats import binom
```


```python
# Esto nos permite identificar la distribución de probabilidad. Algunos valores tienen más probabilidad de darse.
binom.rvs(p = p_cara, n = 10, size = 100)
```




    array([ 4,  3, 10,  3,  1,  3,  2,  3,  6,  1,  7,  5,  7,  4,  4,  6,  8,
            5,  4,  7,  4,  6,  5,  2,  2,  5,  5,  5,  7,  5,  4,  5,  2,  6,
            6,  3,  5,  5,  5,  4,  4,  6,  6,  3,  5,  6,  3,  5,  5,  7,  7,
            6,  5,  3,  9,  4,  8,  6,  2,  5,  2,  6,  4,  4,  5,  7,  4,  4,
            7,  6,  5,  5,  3,  5,  4,  5,  3,  4,  3,  6,  3,  6,  6,  6,  7,
            4,  7,  4,  6,  5,  5,  6,  7,  5,  2,  2,  5,  5,  4,  6])




```python
# Importamos pandas para calcular esta serie como un data frame.
# Value counts nos devuelve la frecuencia que más se repite. Al dividir sobre /100 nos devuelve una probabilidad de los casos totales evaluados.
import pandas as pd
pd.Series(binom.rvs(p = p_cara, n = 10, size = 100)).value_counts()/100
```




    4     0.29
    5     0.24
    6     0.17
    3     0.12
    7     0.06
    8     0.04
    2     0.04
    9     0.03
    10    0.01
    dtype: float64


