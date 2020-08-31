# Intervalos de Confianza


```python
import pandas as pd
import numpy as np

import matplotlib.pyplot as plt
import seaborn as sns

%matplotlib inline
```


```python
Muestra = [4046, 2578, 3796, 3412, 3315, 3228, 3666, 3877, 3154, 4062, 4365, 3776, 3761, 2587, 2911, 3184, 3810, 4459, 3385, 3899, 3602, 2701, 2821, 2790, 2557, 2540, 4119, 2712, 2743, 2713, 4466, 3937, 3871, 4427, 3177, 2556, 2903, 3522, 4155, 4010, 4453, 3080, 3008, 3865, 3356, 2799, 3308, 2759, 4347, 2576, 4075, 3333, 2936, 3746, 3334, 3940, 4113, 4220, 3580, 3922]
```


```python
from scipy.stats import norm

alpha = 0.05
```


```python
lim_inf = norm.ppf(alpha)
lim_sup = norm.ppf(1-(alpha))
lim_inf, lim_sup
```




    (-1.6448536269514729, 1.6448536269514722)




```python
promedio = np.mean(Muestra)
desviacion = np.std(Muestra)
len(Muestra)
```




    60




```python
lim_inf = lim_inf * desviacion + promedio
lim_sup = lim_sup * desviacion + promedio
lim_inf, lim_sup
```




    (2494.1372815063205, 4450.629385160346)



Este resultado quiere decir que el 95% de los datos se encontrará entre el rango 2494.13 y 4450.62 de la muestra.

# Asumiendo una distribución T


```python
from scipy.stats import t

alpha = 0.05
```


```python
lim_inf = t.ppf(alpha, df = 1000)
lim_sup = t.ppf(1-(alpha), df = 1000)
lim_inf, lim_sup
```




    (-1.6463788172854645, 1.6463788172854639)




```python
lim_inf = lim_inf * desviacion + promedio
lim_sup = lim_sup * desviacion + promedio
lim_inf, lim_sup
```




    (2493.2302029687135, 4451.536463697952)


