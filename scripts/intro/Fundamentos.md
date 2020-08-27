```python
print('Hola Mundo')
```

    Hola Mundo


# Cargar datos


```python
import datos_profesora
```


```python
datos_profesora.MASCOTAS
```




    'Dos extraños gatos'




```python
# Datos de fuentes locales

# Sistema operativo
import os
os.name
```




    'posix'




```python
os.getcwd()
```




    '/home/oscar-dev/Platzimaster/Week11/CursoFundamentosDeEstadisticaYAnalisisDeDatosConPython/scripts/intro'




```python
os.listdir('.')
```




    ['__pycache__',
     'Fundamentos.ipynb',
     'datos_profesora.py',
     '.ipynb_checkpoints',
     'bicicletas-compartidas.csv']




```python
path = '/home/oscar-dev/Platzimaster/Week11/'
```


```python
#Con cd change directory le estamos diciendo que nos actualice la ruta de trabajo alojada en la variable Path.
os.chdir(path)
```


```python
os.getcwd()
```




    '/home/oscar-dev/Platzimaster/Week11'




```python
path = '/home/oscar-dev/Platzimaster/Week11/CursoFundamentosDeEstadisticaYAnalisisDeDatosConPython/scripts/intro'
```


```python
os.chdir(path)
```


```python
os.getcwd()
```




    '/home/oscar-dev/Platzimaster/Week11/CursoFundamentosDeEstadisticaYAnalisisDeDatosConPython/scripts/intro'




```python
# Importamos pandas que es una librería par ael manejo de bases de datos.
import pandas as pd
# Con esto leo bases de datos, o archivos csv. Y lo guardo en una variable df (DataFrame)
df = pd.read_csv('bicicletas-compartidas.csv')
```


```python
# Este método devuelve los primeros 5 valores del data set
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>fecha</th>
      <th>bicis-compartidas</th>
      <th>temp-obs</th>
      <th>sens-temp</th>
      <th>hum</th>
      <th>viento</th>
      <th>codigo-clima</th>
      <th>festivo</th>
      <th>findesemana</th>
      <th>cuartil-ano</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2015-01-04 00:00:00</td>
      <td>182</td>
      <td>3.0</td>
      <td>2.0</td>
      <td>93.0</td>
      <td>6.0</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2015-01-04 01:00:00</td>
      <td>138</td>
      <td>3.0</td>
      <td>2.5</td>
      <td>93.0</td>
      <td>5.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2015-01-04 02:00:00</td>
      <td>134</td>
      <td>2.5</td>
      <td>2.5</td>
      <td>96.5</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2015-01-04 03:00:00</td>
      <td>72</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>100.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2015-01-04 04:00:00</td>
      <td>47</td>
      <td>2.0</td>
      <td>0.0</td>
      <td>93.0</td>
      <td>6.5</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>3.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Me devuelve el listado de las columnas ( Este método no tiene paréntesis.¿Porqué?)
df.columns
```




    Index(['fecha', 'bicis-compartidas', 'temp-obs', 'sens-temp', 'hum', 'viento',
           'codigo-clima', 'festivo', 'findesemana', 'cuartil-ano'],
          dtype='object')




```python
# Me devuelve el número de (filas, columnas) de nuestro dataframe
df.shape
```




    (17414, 10)



## Indica que hay 17414 registros en 10 columnas


```python
# Este ejemplo tiene como propósito evidenciar que es posible importar información desde otras fuentes.
# Se usa para procesamiento de imagenes
import tensorflow as tf
```


```python
# Podemos cargar unas bases de datos (fashion_mnist)propias de las librerías.
fashion_mnist = tf.keras.datasets.fashion_mnist

# Cargamos a dos variables las imágenes y categorías.
(imagenes, categorias) = fashion_mnist.load_data()[0]

# Se cargan como matrices de pixeles
imagenes.shape
```

    Downloading data from https://storage.googleapis.com/tensorflow/tf-keras-datasets/train-labels-idx1-ubyte.gz
    32768/29515 [=================================] - 0s 2us/step
    Downloading data from https://storage.googleapis.com/tensorflow/tf-keras-datasets/train-images-idx3-ubyte.gz
    26427392/26421880 [==============================] - 10s 0us/step
    Downloading data from https://storage.googleapis.com/tensorflow/tf-keras-datasets/t10k-labels-idx1-ubyte.gz
    8192/5148 [===============================================] - 0s 1us/step
    Downloading data from https://storage.googleapis.com/tensorflow/tf-keras-datasets/t10k-images-idx3-ubyte.gz
    4423680/4422102 [==============================] - 2s 0us/step





    (60000, 28, 28)




```python
# Estoy viendo el tamaño de mi arreglo y llamo a categorías o tags para poder generar patrones.
imagenes[0].shape, categorias[0]

```




    ((28, 28), 9)




```python
## Arreglo de 28 * 28, que son los diferentes valores numéricos que son el color asociado a cada píxel
imagenes[0]
```




    array([[  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
              0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
              0,   0],
           [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
              0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
              0,   0],
           [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
              0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
              0,   0],
           [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   1,
              0,   0,  13,  73,   0,   0,   1,   4,   0,   0,   0,   0,   1,
              1,   0],
           [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   3,
              0,  36, 136, 127,  62,  54,   0,   0,   0,   1,   3,   4,   0,
              0,   3],
           [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   6,
              0, 102, 204, 176, 134, 144, 123,  23,   0,   0,   0,   0,  12,
             10,   0],
           [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
              0, 155, 236, 207, 178, 107, 156, 161, 109,  64,  23,  77, 130,
             72,  15],
           [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   1,   0,
             69, 207, 223, 218, 216, 216, 163, 127, 121, 122, 146, 141,  88,
            172,  66],
           [  0,   0,   0,   0,   0,   0,   0,   0,   0,   1,   1,   1,   0,
            200, 232, 232, 233, 229, 223, 223, 215, 213, 164, 127, 123, 196,
            229,   0],
           [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
            183, 225, 216, 223, 228, 235, 227, 224, 222, 224, 221, 223, 245,
            173,   0],
           [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
            193, 228, 218, 213, 198, 180, 212, 210, 211, 213, 223, 220, 243,
            202,   0],
           [  0,   0,   0,   0,   0,   0,   0,   0,   0,   1,   3,   0,  12,
            219, 220, 212, 218, 192, 169, 227, 208, 218, 224, 212, 226, 197,
            209,  52],
           [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   6,   0,  99,
            244, 222, 220, 218, 203, 198, 221, 215, 213, 222, 220, 245, 119,
            167,  56],
           [  0,   0,   0,   0,   0,   0,   0,   0,   0,   4,   0,   0,  55,
            236, 228, 230, 228, 240, 232, 213, 218, 223, 234, 217, 217, 209,
             92,   0],
           [  0,   0,   1,   4,   6,   7,   2,   0,   0,   0,   0,   0, 237,
            226, 217, 223, 222, 219, 222, 221, 216, 223, 229, 215, 218, 255,
             77,   0],
           [  0,   3,   0,   0,   0,   0,   0,   0,   0,  62, 145, 204, 228,
            207, 213, 221, 218, 208, 211, 218, 224, 223, 219, 215, 224, 244,
            159,   0],
           [  0,   0,   0,   0,  18,  44,  82, 107, 189, 228, 220, 222, 217,
            226, 200, 205, 211, 230, 224, 234, 176, 188, 250, 248, 233, 238,
            215,   0],
           [  0,  57, 187, 208, 224, 221, 224, 208, 204, 214, 208, 209, 200,
            159, 245, 193, 206, 223, 255, 255, 221, 234, 221, 211, 220, 232,
            246,   0],
           [  3, 202, 228, 224, 221, 211, 211, 214, 205, 205, 205, 220, 240,
             80, 150, 255, 229, 221, 188, 154, 191, 210, 204, 209, 222, 228,
            225,   0],
           [ 98, 233, 198, 210, 222, 229, 229, 234, 249, 220, 194, 215, 217,
            241,  65,  73, 106, 117, 168, 219, 221, 215, 217, 223, 223, 224,
            229,  29],
           [ 75, 204, 212, 204, 193, 205, 211, 225, 216, 185, 197, 206, 198,
            213, 240, 195, 227, 245, 239, 223, 218, 212, 209, 222, 220, 221,
            230,  67],
           [ 48, 203, 183, 194, 213, 197, 185, 190, 194, 192, 202, 214, 219,
            221, 220, 236, 225, 216, 199, 206, 186, 181, 177, 172, 181, 205,
            206, 115],
           [  0, 122, 219, 193, 179, 171, 183, 196, 204, 210, 213, 207, 211,
            210, 200, 196, 194, 191, 195, 191, 198, 192, 176, 156, 167, 177,
            210,  92],
           [  0,   0,  74, 189, 212, 191, 175, 172, 175, 181, 185, 188, 189,
            188, 193, 198, 204, 209, 210, 210, 211, 188, 188, 194, 192, 216,
            170,   0],
           [  2,   0,   0,   0,  66, 200, 222, 237, 239, 242, 246, 243, 244,
            221, 220, 193, 191, 179, 182, 182, 181, 176, 166, 168,  99,  58,
              0,   0],
           [  0,   0,   0,   0,   0,   0,   0,  40,  61,  44,  72,  41,  35,
              0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
              0,   0],
           [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
              0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
              0,   0],
           [  0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
              0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,   0,
              0,   0]], dtype=uint8)


