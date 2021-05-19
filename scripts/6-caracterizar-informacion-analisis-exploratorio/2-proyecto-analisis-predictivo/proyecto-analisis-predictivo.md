```python
import pandas as pd
import numpy as np
import seaborn as sns
import os

import matplotlib.pyplot as plt
%matplotlib inline
```


```python
path = '/home/oscar-dev/Platzimaster/Week11/CursoFundamentosDeEstadisticaYAnalisisDeDatosConPython/scripts/6-caracterizar-informacion-analisis-exploratorio/proyecto-titanic'
```


```python
os.chdir(path)
```


```python
os.listdir()
```




    ['1-parte',
     'titanic-master-table.csv',
     'test.csv',
     'csv_procesado.csv',
     'train.csv']




```python
df = pd.read_csv('titanic-master-table.csv')
```


```python
df.columns
```




    Index(['Unnamed: 0', 'PassengerId', 'Survived', 'Name', 'Age', 'SibSp',
           'Parch', 'Ticket', 'Fare', 'is-Pclass-1', 'is-Pclass-2', 'is-Sex-male',
           'is-Embarked-S', 'is-Embarked-C', 'family_size'],
          dtype='object')




```python
y = df['Survived']
X = df[['Age', 'SibSp', 'Parch', 'Fare', 'is-Pclass-1', 'is-Pclass-2', 'is-Sex-male', 'is-Embarked-S', 'is-Embarked-C', 'family_size']]
```


```python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.15, random_state=1)
```


```python
from sklearn.linear_model import LogisticRegression
from sklearn.tree import DecisionTreeClassifier
```


```python
clf = [
    (LogisticRegression(), 'reg_log'),
    (DecisionTreeClassifier(), 'arbol-class')
]
```


```python
# Librería para modelos de analítica. Permite guardar los resultados del entrenamiento de cada uno, para cuando seleccionemos el mejor, podamos cargarlo nuevamente
import joblib
from sklearn.metrics import accuracy_score

for model, name in clf:
    #Entrenar
    model.fit(X_train, y_train)
    
    #Medir
    y_pred = model.predict(X_test)
    accuracy = accuracy_score(y_test, y_pred)
    print(name)
    print('Resultado en la prueba del modelo: ', round(accuracy*100, 2), ' %')
    
    #Guardar el modelo
    job_file = 'modelo-'+name+'.pkl'
    joblib.dump(model, job_file)
```

    reg_log
    Resultado en la prueba del modelo:  79.35  %
    arbol-class
    Resultado en la prueba del modelo:  76.09  %


    /home/oscar-dev/anaconda3/lib/python3.7/site-packages/sklearn/linear_model/_logistic.py:940: ConvergenceWarning: lbfgs failed to converge (status=1):
    STOP: TOTAL NO. of ITERATIONS REACHED LIMIT.
    
    Increase the number of iterations (max_iter) or scale the data as shown in:
        https://scikit-learn.org/stable/modules/preprocessing.html
    Please also refer to the documentation for alternative solver options:
        https://scikit-learn.org/stable/modules/linear_model.html#logistic-regression
      extra_warning_msg=_LOGISTIC_SOLVER_CONVERGENCE_MSG)


# Elección: Regresión Logística

Debido a que el resultado del modelo de regresión logística es mayor que el árbol de decisión, se elige la regresión logística para hacer el cálculo del modelo de supervivencia en el Titanic.
