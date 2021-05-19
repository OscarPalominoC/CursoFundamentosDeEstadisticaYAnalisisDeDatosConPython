```python
# Numpy es clave en el desarrollo de funciones numéricas.
import numpy as np
import pandas as pd
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
y = df['bicis-compartidas'].values
```


```python
y
```




    array([182, 138, 134, ..., 337, 224, 139])




```python
# Limpiamos el arreglo de los ceros, valores que no permiten hacer calculo en numpy. 
# Le estamos diciendo, con  numpy "donde cuente y==0 cambielo por un 1 si no, conserve y"
y = np.where(y == 0, 1, y)
```


```python
np.min(y)
```




    1




```python
np.max(y)
```




    7860




```python
# promedio: sum(yi)/n
np.mean(y)
```




    1143.1016997817849




```python
np.sum(y)/len(y)
```




    1143.1016997817849




```python
# MEDIA ARMÓNICA
scipy.stats.mstats.hmean(y)
```




    241.65180305136826




```python
# Mediana
np.median(y)
```




    844.0




```python
# Moda
moda = np.nan

valores, frecuencias = np.unique(y, return_counts = True)
pos = np.argmax(frecuencias)
moda = valores[pos]
```


```python
moda
```




    46




```python
# Medida de dispersión

#Desviación estándar: Qué tanto se distancian los valores
np.std(y)
```




    1085.0768508213835



# Revisiones


```python
y_alterado = y.copy()
y_alterado [y_alterado == max(y_alterado)] = 10000000
```


```python
print(np.mean(y))
print(np.mean(y_alterado))
```

    1143.1016997817849
    1716.9009417709888



```python
print(np.median(y))
print(np.median(y_alterado))
```

    844.0
    844.0

