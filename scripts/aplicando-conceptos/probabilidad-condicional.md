```python
# Análisis estadístico
import numpy as np
import pandas as pd
import scipy.stats

#Visualización
import matplotlib.pyplot as plt
import seaborn as sns

%matplotlib inline
```


```python
df = pd.read_csv('juego-azar.csv', sep= ';')
df.columns
```




    Index(['bola', 'color', 'numero'], dtype='object')




```python
# Probabilidades univariadas
df.numero.value_counts()
```




    1    4
    3    3
    2    3
    Name: numero, dtype: int64




```python
df.numero.value_counts()/len(df)
```




    1    0.4
    3    0.3
    2    0.3
    Name: numero, dtype: float64




```python
# Probabilidad univariada de los colores
df.color.value_counts()/len(df)
```




    negro     0.6
    blanco    0.4
    Name: color, dtype: float64




```python
# Probabilidades conjuntas bivariadas de tener una esfera de algún color y número específico
df.groupby(['color', 'numero']).size()
# Muestra el color de la bola, su número y la cantidad de ellas
```




    color   numero
    blanco  1         1
            2         1
            3         2
    negro   1         3
            2         2
            3         1
    dtype: int64




```python
# Probabilidades de escoger un color y que les salga un número
df.groupby(['color', 'numero']).size()/len(df)
```




    color   numero
    blanco  1         0.1
            2         0.1
            3         0.2
    negro   1         0.3
            2         0.2
            3         0.1
    dtype: float64




```python
df.groupby(['numero', 'color']).size()
```




    numero  color 
    1       blanco    1
            negro     3
    2       blanco    1
            negro     2
    3       blanco    2
            negro     1
    dtype: int64




```python
# P(A|B) = P(B|2) => Blanco y # 2 = 1 y #2 = 3 => color blanco / cantidad #2 = 1/3
1/3 
```




    0.3333333333333333




```python
# P(A)

# P(A|B)

# P(B)

# p_blanca = 4/10

# p(p_blanca|1)+p(p_blanca|2)+p(p_blanca|3)
# 1 + 1 + 2

#p(blanco) = p(p_blanca|1)*p(1) + p(p_blanca|2)*p(2) + p(p_blanca|3)*p(3)
(1/4)*(4/10) + (1/3)*(3/10) + (2/3)*(3/10)
```




    0.4


