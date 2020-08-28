```python
import pandas as pd
import numpy as np
import scipy
import scipy.stats
```


```python
df = pd.read_csv('bicicletas-compartidas.csv')
```


```python

df.columns
```




    Index(['fecha', 'bicis-compartidas', 'temp-obs', 'sens-temp', 'hum', 'viento',
           'codigo-clima', 'festivo', 'findesemana', 'cuartil-ano'],
          dtype='object')




```python
# Frecuencias categoricas
y_cat = df['cuartil-ano']
```


```python
y_cat
```




    0        3.0
    1        3.0
    2        3.0
    3        3.0
    4        3.0
            ... 
    17409    3.0
    17410    3.0
    17411    3.0
    17412    3.0
    17413    3.0
    Name: cuartil-ano, Length: 17414, dtype: float64




```python
y_cat = y_cat.apply(lambda x: 'Cat-' + str(int(x)))
y_cat
```




    0        Cat-3
    1        Cat-3
    2        Cat-3
    3        Cat-3
    4        Cat-3
             ...  
    17409    Cat-3
    17410    Cat-3
    17411    Cat-3
    17412    Cat-3
    17413    Cat-3
    Name: cuartil-ano, Length: 17414, dtype: object




```python
valores, conteo_freq = np.unique(y_cat, return_counts = True)
```


```python
valores, conteo_freq
```




    (array(['Cat-0', 'Cat-1', 'Cat-2', 'Cat-3'], dtype=object),
     array([4394, 4387, 4303, 4330]))




```python
tabla_frecuencias = dict(zip(valores, conteo_freq))
tabla_frecuencias
```




    {'Cat-0': 4394, 'Cat-1': 4387, 'Cat-2': 4303, 'Cat-3': 4330}




```python
# Variable numérica
y_num = df['viento'].copy()
```


```python
np.min(y_num), np.max(y_num)
```




    (0.0, 56.5)




```python
np.percentile(y_num, q=100)
```




    56.5




```python
np.percentile(y_num, q=50)
```




    15.0




```python
np.percentile(y_num, q=0)
```




    0.0




```python
np.percentile(y_num, q=75)
```




    20.5




```python
np.median(y_num)
```




    15.0




```python
valores = [0, 25, 50, 75, 100]
np.percentile(y_num, q = valores)
```




    array([ 0. , 10. , 15. , 20.5, 56.5])




```python
# Quintiles: 100/5 = 20, por eso van de 20 en 20
valores = [0, 20, 40, 60, 80, 100]
np.percentile(y_num, q = valores)
```




    array([ 0. ,  9. , 13. , 17. , 22. , 56.5])




```python
# deciles: 100/10 = 10, por eso van de 10 en 10
valores = [0, 10, 20, 30, 40, 50, 60, 70, 80, 90, 100] # valores = list(range(0, 101, 10))
np.percentile(y_num, q = valores)
```




    array([ 0. ,  6.5,  9. , 11. , 13. , 15. , 17. , 19.5, 22. , 27. , 56.5])



# Valores atípicos


```python
y = df['bicis-compartidas']
y.describe()
```




    count    17414.000000
    mean      1143.101642
    std       1085.108068
    min          0.000000
    25%        257.000000
    50%        844.000000
    75%       1671.750000
    max       7860.000000
    Name: bicis-compartidas, dtype: float64




```python
# Outlier: Puede pertenecer a una distribución diferente a un segmento que debe ser tratado de una forma distinta

# Primero se debe determinar el cuartil 1 y el cuartil 3.
Q1 = np.percentile(y_num, q = 25)
Q3 = np.percentile(y_num, q = 75)

# Rango intercualtilico
RI = Q3 - Q1

# Límites del rango
lim_inf = Q1-1.5*RI
lim_sup = Q3+1.5*RI

[lim_inf, lim_sup]
```




    [-5.75, 36.25]




```python
import matplotlib.pyplot as plt
%matplotlib inline
```


```python
plt.hist(y)
```




    (array([8.274e+03, 4.416e+03, 2.355e+03, 1.241e+03, 5.610e+02, 4.710e+02,
            8.800e+01, 2.000e+00, 3.000e+00, 3.000e+00]),
     array([   0.,  786., 1572., 2358., 3144., 3930., 4716., 5502., 6288.,
            7074., 7860.]),
     <a list of 10 Patch objects>)




![png](/output_23_1.png)

