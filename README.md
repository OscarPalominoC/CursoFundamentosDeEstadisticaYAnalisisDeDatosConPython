# Curso Fundamentos De Estadística Y Análisis De Datos Con Python

![Logo](https://static.platzi.com/media/achievements/badge-estadistica-analisis-datos-python-112b289c-f196-44d0-ac60-3175bff2b3ec.png)

<hr>

# Proyecto de Curso

## Predicción en el Titanic

Realiza una predicción de la probabilidad de salvarse en el Titanic con las herramientas aprendidas en este curso!


# Índice

* [Introducir conceptos básicos del curso](#introducir-conceptos-básicos-del-curso)
    * [Introducción](#introducción)
    * [Conceptos clave sobre estadística](#conceptos-clave-sobre-estadística)
    * [Medidas de tendencia central](#medidas-de-tendencia-central)
    * [Diagramas de frecuencias para variables continuas y discretas](#diagramas-de-frecuencias-para-variables-continuas-y-discretas)
    * [Visualización de datos usando Python](#visualización-de-datos-usando-python)
    * [Boxplot y scatterplot](#boxplot-y-scatterplot)
* [Aplicar conceptos de probabilidad a eventos aleatorios](#aplicar-conceptos-de-probabilidad-a-eventos-aleatorios)
    * [Probabilidad condicional - Teorema de Bayes](#probabilidad-condicional---teorema-de-bayes)
    * [Funciones de distribución discreta y continua](#funciones-de-distribución-discreta-y-continua)
    * [Funciones de distribución discreta y continua con Python](#funciones-de-distribución-discreta-y-continua-con-python)
    * [Distribuciones discretas de mayor aplicación](#distribuciones-discretas-de-mayor-aplicación)

<hr>

# Introducir conceptos básicos del curso

## Introducción

### Python y Estadística

* Estadística en Papel
* Estadística en open source: big data y capacidad de cómputo, memoria ram, procesador, ambientes virtuales (paralelización - spark/apache).

### Python y la estadística: ¿Porqué usar pythony no R para estadística?.

R es un lenguaje dedicado a la estadística, python es un lenguaje de propósito general con módulos estadísticos.

R está especializado para estadística y tiene más features que python. Pero cuando se trata de construir complejos piplines para el análisis que mezcla estadística con análisis de imágenes, minería de texto la riqueza de python es invaluable.

La estadística actual requiere una gran cantidad de procesamiento y almacenamiento de información.

Aquí entran los ambientes virtuales.

Los ambientes virtuales como Collabs, Jupyter, facilitan el trabajo en estas variables de volumen y procesamiento, así como el uso de librerías.

[Carpeta de introducción](/scripts/intro)

[Archivo Readme](/scripts/intro/Fundamentos.md)

## Conceptos clave sobre estadística

### Tipos de datos
* numéricos: continuos, porcentajes y enteros.
* categóricos: Ordinales(fechas, estrato socio económico) y clases sin sentido ordinal(países o colores).

### Variables determinísticas vs variables aleatorias
* Deterministica: asume un valor puntual.
* Aleatorias: puede tomar valores que cambian en rangos determinados, se asume que conocemos esos valores.

### Probabilidad en aleatórias univariadas

![Probabilidad de laplace](/images/laplace_probability.png)

[Conceptos básicos](/scripts/intro/conceptos_basicos.md)

## Medidas de tendencia central

Herramientas visuales y numéricas para caracterizar las variables numéricas con que trabajamos.

RAW : Medidas de tendencia central

Es importante que no todas las medidas de tendencia son aplicables a los dos tipos de variables, numéricas y categóricas, y que también algunas de ellas son más susceptibles a los valores extremos (outliers)

### Medidas de tendencia

* Media o promedio geométrico y aritmético
* Mediana
* Moda
* Error típico o desviación estándar

### Criterios de aplicación

* Según el tipo de variables y susceptibilidad a valores extremos.

### Conceptos

**MEDIA ARMÓNICA**: La media armónica es la recíproca de la media aritmética. **Los elementos del conjunto deben ser necesariamente no nulos**. Esta media es poco sensible a los valores grandes y los infravalora respecto a la media aritmética, pero muy sensible a los valores próximos a cero, ya que los recíprocos 1/Xi son muy altos, por lo que les da más peso que en las medias aritmética y geométrica. Si algún valor fuese cero, la media armónica quedaría indeterminada.

Ésta no tiene un uso muy extenso en el mundo científico. Suele utilizarse principalmente para calcular la media de velocidades, tiempos o en electrónica. 

![Fórmula media armónica](/images/media-armonica.png)

[Medidas de tendencia central con python](/scripts/intro/medidas_tendencia_central.md)

## Diagramas de frecuencias para variables continuas y discretas

### Histogramas

Representación categórica y numérica de la distribución de los datos.

**Variables categóricas**: Tablas de frecuencia.

**Variables numéricas**: Percentiles, deciles, quintiles y cuartiles, outliers o valores extremos.

**Percentil**

Un percentil es una medida estadística utilizada para comparar datos. Consiste en un número de 0 a 100 que indica el porcentaje de datos que son igual o menor que un determinado valor.

Los percentiles son muy conocidos por su uso en los percentiles de crecimiento. Por ejemplo, si el peso de un bebé está en el percentil 65, quiere decir que el 65% de los bebés de la misma edad pesan igual o menos.

![Percentil](/images/percentil.png)

**Cuartiles**

Los cuartiles son los valores utilizados para dividir un conjunto de números en cuatro grupos iguales. Pon los números en orden y divídelos por la mitad con una mediana. A la izquierda de la mediana, los números se separan de nuevo, y a la derecha de la mediana, haz una tercera separación. En este punto, los datos se dividen en cuatro grupos y los tres marcadores son los cuartiles reales. Observa que hay cuatro grupos, pero esto se hace con tres cuartiles, que están numerados de izquierda a derecha como Cuartil-1, Cuartil-2 y Cuartil-3

![Cuartiles](/images/cuartil.webp)

[Percentiles, media y mediana](https://medium.com/@ankur_anand/an-in-depth-introduction-to-99-percentile-for-programmers-22e83a00caf)

[Outliers](https://towardsdatascience.com/why-1-5-in-iqr-method-of-outlier-detection-5d07fdc82097)

[Práctica: Diágramas de frecuencia](/scripts/intro/diagramas_frecuencia.md)

## Visualización de datos usando Python

Los analistas de datos tenemos como nuestro mayor reto, poder comunicar los análisis que hacemos con un gran volumen de información, para esto, contamos con la ayuda de las herramientas visuales, que pueden ser el éxito o el fracaso de nuestro análisis.

**Matplotlib** no organiza los histogramas en orden cómo fueron almacenados, sino que los almacena de mayor a menor.

[Visualización de datos en python](/scripts/intro/visualizacion_datos.md)

[Más información sobre el gráfico de torta](https://www.data-to-viz.com/caveat/pie.html)

[Más información de visualización de datos](https://www.data-to-viz.com/)

## Boxplot y scatterplot

Los boxplots y los scatterplots son la mejor opción para visualizar los cuartiles. 

Nos permiten ver las variables en 2 dimensiones, mapeandolas, no solo en función de su distribución sino de los conteos de otras variables.

Scatterplot y boxplot son los 2 gráficos más utilizados en el análisis estadístico, porque nos permite observar la relación que tienen 2 variables.

Si no encontramos un patrón, podremos decir que las variables no están relacionadas.

Si encontramos relaciones entre las variables, podemos explorar relaciones más profundas entre estas.

[Visualización de datos en python](/scripts/intro/boxplot-scatterplot/boxplot_scatterplot.md)

# Aplicar conceptos de probabilidad a eventos aleatorios

[Carpeta de trabajo](/scripts/aplicando-conceptos/)

## Probabilidad condicional - Teorema de Bayes

En términos más generales y menos matemáticos, el teorema de Bayes es de enorme relevancia puesto que vincula la probabilidad de A dado B con la probabilidad de B dado A. Es decir, por ejemplo, que sabiendo la probabilidad de tener un dolor de cabeza dado que se tiene gripe, se podría saber (si se tiene algún dato más), la probabilidad de tener gripe si se tiene un dolor de cabeza. Muestra este sencillo ejemplo la alta relevancia del teorema en cuestión para la ciencia en todas sus ramas, puesto que tiene vinculación íntima con la comprensión de la probabilidad de aspectos causales dados los efectos observados.

[Concepto](https://es.wikipedia.org/wiki/Teorema_de_Bayes)

### Fórmula del Teorema de Bayes

Probabilidad de A y B
```
P(A and B) = P(A)* P(B|A)
P(B|A): Probabilidad de B dado A
```
Probabilidad de B
```
P(B) = P(A)* P(B|A) + P(¬A) * P(B|¬A)
P(¬A): Probabilidad que no suceda A
```

**Terema de Bayes**
```
P(A | B) = (P(A) * P(B | A)) / P(B)
```

![Fórmula](/images/bayes-theorem.png)

### Conceptos

* **Probabilidad univariada**: Incluye todas las técnicas que hacen referencia a la descripción e inferencia de una sola variable. También se conoce como *Estadística Descriptiva*.
* **Probabilidad conjunta bivariada**: Se investiga la influencia de la variable Independiente, por vez, con respecto a la variable Dependiente. 
* **Probabilidad condicional**: Es la probabilidad de que ocurra un evento A, sabiendo que también sucede otro evento B. La probabilidad condicional se escribe P(A|B) o P(A/B), y se lee «la probabilidad de A dado B».

[Probabilidad condicional: Teorema de Bayes](/scripts/aplicando-conceptos/probabilidad-condicional.md)

## Funciones de distribución discreta y continua

### Distribución de probabilidad discreta

![Probabilidad discreta](/images/probabilidad-discreta.png)

* El rango debe cumplir y contener a todos los valores de X.
* La probabilidad de cada uno de los valores de X, no debe superar el valor de 1.
* La probaacumulada es la suma de las probabilidades de tener un número igual o menor a Xi.
* Regla de completitud, debemos contemplar todos los valores posibles que puede tomar una sola variable aleatoria X, luego la sumatoria de todas las probabilidades de nuestro rango, siempre deben sumar 1.
* Debemos tener siempre en cuenta todas las medidas de tendencia central, para poder hallar el valor esperado o promedio.
* Y la desviación estándar que en este caso llamaremos varianza que es el cuadrado de la diferencia de la media y el valor Xi evaluado.

### Distribución de densidad continua

![Probabilidad discreta](/images/densidad-continua.png)

Debemos evaluar los mismos conceptos de la [distribución de probabilidad discreta](#distribución-de-probabilidad-discreta).

### Valor esperado

Al igual que la varianza también cumple una serie de características y una forma específica a la hora de calcularse.

[Valor esperado](/images/valor-esperado.png)

### Varianza

[Valor esperado](/images/varianza.png)

[Funciones de distribución discreta y continua](/scripts/aplicando-conceptos/distribucion-discreta-continua/funciones_distribucion_discreta_continua.md)

binom.pmf: Probability Mass Function - [Función de probabilidad](https://es.wikipedia.org/wiki/Funci%C3%B3n_de_probabilidad). Es una función que asocia a cada punto de su espacio muestral X la probabilidad de que esta lo asuma. 

[Fórmula](/images/pmf-formula.png)

para k en {0, 1, ..., n}.

Binom toma n y p como parámetros de forma.

La función de masa de probabilidad anterior se define en la forma "estandarizada". Para cambiar la distribución, use el parámetro loc. Específicamente, binom.pmf (k, n, p, loc) es idénticamente equivalente a binom.pmf (k - loc, n, p).

[Documentación: Funciones binomiales](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.binom.html)

## Funciones de distribución discreta y continua con Python

### Conceptos

* **ASIMETRÍA** Es una medida de forma de una distribución que permite identificar y describir la manera como los datos tiende a reunirse de acuerdo con la frecuencia con que se hallen dentro de la distribución. Permite identificar las características de la distribución de datos sin necesidad de generar el gráfico
* **CURTOSIS O APUNTAMIENTO** La curtosis mide el grado de agudeza o achatamiento de una distribución con relación a la distribución normal, es decir, mide cuán puntiaguda es una distribución.

**TIPOS DE CURTOSIS**

La curtosis determina el grado de concentración que presentan los valores en la región central de la distribución. Así puede ser:
* Leptocúrtica.- Existe una gran concentración.
* Mesocúrtica.- Existe una concentración normal. 
* Platicúrtica.- Existe una baja concentración.

binom.cdf: Cumulative distribution function - [Función de distribución acumulada](https://es.wikipedia.org/wiki/Funci%C3%B3n_de_distribuci%C3%B3n). función de probabilidad acumulada asociada a una variable aleatoria real: X (mayúscula) sujeta a cierta ley de distribución de probabilidad, es una función matemática de la variable real: x (minúscula); que describe la probabilidad de que X tenga un valor menor o igual que x.

Intuitivamente, asumiendo la función f como la ley de distribución de probabilidad, la FDA sería la función con la recta real como dominio, con imagen del área hasta aquí de la función f, siendo aquí el valor x para la variable aleatoria real X.

La FDA asocia a cada valor x, la probabilidad del evento: «la variable X toma valores menores o iguales a x».

El concepto de FDA puede generalizarse para modelar variables aleatorias multivariantes definidas en ![Reales potencia de n](/images/rn.svg)

[Funciones de distribución discreta y continua](/scripts/aplicando-conceptos/distribucion-discreta-continua-2/distribucion-discreta-continua-2.md)

## Distribuciones discretas de mayor aplicación

1. Bernoulli: Experimento Binario asociado a éxito o fracaso.
2. Distribución Binomial: Número de éxitos x en N ensayos.
3. Distribución Geométrica: Número de ensayos x hasta 1 éxito.
4. Distribución Binomial Negativa: Número de ensayos x hasta el k-ésimo éxito.
5. Distribución de Poisson: Número de llegadas en N a una longitud de tiempo t.

[Distribuciones discretas de mayor aplicación](/scripts/aplicando-conceptos/distribuciones_discretas_aplicacion/distribuciones-discretas-mas-utilizadas.md)