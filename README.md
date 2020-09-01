# Curso Fundamentos De Estadística Y Análisis De Datos Con Python

![Logo](https://static.platzi.com/media/achievements/badge-estadistica-analisis-datos-python-112b289c-f196-44d0-ac60-3175bff2b3ec.png)

<hr>

# Archivos

[Inferencia Estadística: Teoría y Problemas](/files/estadistica-inferencial.pdf)

<hr>

# Proyecto de Curso

## Predicción en el Titanic

Realiza una predicción de la probabilidad de salvarse en el Titanic con las herramientas aprendidas en este curso!

<hr>

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
    * [Distribuciones continuas de mayor aplicación](#distribuciones-continuas-de-mayor-aplicación)
    * [Estandarización, covarianza y correlación](#estandarización-covarianza-y-correlación)
* [Construir conceptos estadísticos analíticos](#construir-conceptos-estadísticos-analíticos)
    * [Estimadores a través de datos](#estimadores-a-través-de-datos)
    * [Estimadores de máxima verosimilitud](#estimadores-de-máxima-verosimilitud)
    * [Distribuciones muestrales](#distribuciones-muestrales)
    * [Teorema del límite central](#teorema-del-límite-central)
* [Realizar inferencias estadisticas a partir de una muestra](#realizar-inferencias-estadisticas-a-partir-de-una-muestra)
    * [Pruebas de hipótesis](#pruebas-de-hipótesis)
    * [Errores estadísticos Tipo 1 y Tipo 2](#errores-estadísticos-tipo-1-y-tipo-2)
    * [Intervalos de confianza](#intervalos-de-confianza)
* [Usar modelos estadísticos para exploración y predicción](usar-modelos-estadísticos-para-exploración-y-predicción)
    * [Regresión Lineal](#regresión-lineal)
    * [Regresión logística](#regresión-logística)
    * [Árboles de regresión y de clasificación](#árboles-de-regresión-y-de-clasificación)
* [Introducir conceptos de analítica avanzada](#introducir-conceptos-de-analítica-avanzada)
    * [Proyecto análisis exploratorio: Descriptivos, outliers, creación y selección de variables](#proyecto-análisis-exploratorio-descriptivos-outliers-creación-y-selección-de-variables)

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

[Carpeta de introducción](/scripts/1-intro)

[Archivo Readme](/scripts/1-intro/Fundamentos.md)

## Conceptos clave sobre estadística

### Tipos de datos
* numéricos: continuos, porcentajes y enteros.
* categóricos: Ordinales(fechas, estrato socio económico) y clases sin sentido ordinal(países o colores).

### Variables determinísticas vs variables aleatorias
* Deterministica: asume un valor puntual.
* Aleatorias: puede tomar valores que cambian en rangos determinados, se asume que conocemos esos valores.

### Probabilidad en aleatórias univariadas

![Probabilidad de laplace](/images/laplace_probability.png)

[Conceptos básicos](/scripts/1-intro/conceptos_basicos.md)

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

[Medidas de tendencia central con python](/scripts/1-intro/medidas_tendencia_central.md)

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

[Práctica: Diágramas de frecuencia](/scripts/1-intro/diagramas_frecuencia.md)

## Visualización de datos usando Python

Los analistas de datos tenemos como nuestro mayor reto, poder comunicar los análisis que hacemos con un gran volumen de información, para esto, contamos con la ayuda de las herramientas visuales, que pueden ser el éxito o el fracaso de nuestro análisis.

**Matplotlib** no organiza los histogramas en orden cómo fueron almacenados, sino que los almacena de mayor a menor.

[Visualización de datos en python](/scripts/1-intro/visualizacion_datos.md)

[Más información sobre el gráfico de torta](https://www.data-to-viz.com/caveat/pie.html)

[Más información de visualización de datos](https://www.data-to-viz.com/)

## Boxplot y scatterplot

Los boxplots y los scatterplots son la mejor opción para visualizar los cuartiles. 

Nos permiten ver las variables en 2 dimensiones, mapeandolas, no solo en función de su distribución sino de los conteos de otras variables.

Scatterplot y boxplot son los 2 gráficos más utilizados en el análisis estadístico, porque nos permite observar la relación que tienen 2 variables.

Si no encontramos un patrón, podremos decir que las variables no están relacionadas.

Si encontramos relaciones entre las variables, podemos explorar relaciones más profundas entre estas.

[Visualización de datos en python](/scripts/1-intro/boxplot-scatterplot/boxplot_scatterplot.md)

# Aplicar conceptos de probabilidad a eventos aleatorios

[Carpeta de trabajo](/scripts/2-aplicando-conceptos/)

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

[Probabilidad condicional: Teorema de Bayes](/scripts/2-aplicando-conceptos/probabilidad-condicional.md)

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

![Valor esperado](/images/valor-esperado.png)

### Varianza

![Valor esperado](/images/varianza.png)

[Funciones de distribución discreta y continua](/scripts/2-aplicando-conceptos/distribucion-discreta-continua/funciones_distribucion_discreta_continua.md)

binom.pmf: Probability Mass Function - [Función de probabilidad](https://es.wikipedia.org/wiki/Funci%C3%B3n_de_probabilidad). Es una función que asocia a cada punto de su espacio muestral X la probabilidad de que esta lo asuma. 

![Fórmula](/images/pmf-formula.png)

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

[Funciones de distribución discreta y continua](/scripts/2-aplicando-conceptos/distribucion-discreta-continua-2/distribucion-discreta-continua-2.md)

## Distribuciones discretas de mayor aplicación

1. Bernoulli: Experimento Binario asociado a éxito o fracaso.
2. Distribución Binomial: Número de éxitos x en N ensayos.
3. Distribución Geométrica: Número de ensayos x hasta 1 éxito.
4. Distribución Binomial Negativa: Número de ensayos x hasta el k-ésimo éxito.
5. Distribución de Poisson: Número de llegadas en N a una longitud de tiempo t.

[Distribuciones discretas de mayor aplicación](/scripts/2-aplicando-conceptos/distribuciones_discretas_aplicacion/distribuciones-discretas-mas-utilizadas.md)

## Distribuciones continuas de mayor aplicación

* Distribución **Exponencial**: Es el caso inverso de la distribución de Poisson, se cuenta el tiempo que nos toma llegar a un evento. Utilizada generalmente para análisis de fiabilidad, p.e: probabilidad de que un componente falle transcurrido una cierta cantidad de tiempo. 
* Distribución **Normal**: Dadas sus características, se utiliza para inferencia estadística, es decir, estimar/evaluar parámetros de toda una población, basados en una muestra. Aquí es donde se utilizan los famosos intervalos de confianza.
* Distribución **Uniforme**. Asume que cada uno de los eventos posee la misma probabilidad. Se utiliza generalmente en el ámbito de simulación, por ejemplo “creación” de escenarios aleatorios, números aleatorios, etc.

[Distribuciones Continuas más Utilizadas](/scripts/2-aplicando-conceptos/distribuciones-continuas-mas-utilizadas/distribuciones-continuas-mas-utilizadas.md)

## Estandarización, covarianza y correlación

### Estandarización o tipificación de variables

1. **Centrar** la variable: Restar su media a cada uno de los valores originales.
2. **Reducir** la variable: Dividir todos sus valores por la desviación.

![Estandarización](/images/estandarizacion.png)

El resultado de la aplicación de la estandarización es una Variable Aleatoria (V.A.) **Z**.
* Adimensional: Datos independientes de la escala escogida.
* E(Z) = 0 y V(Z) = 1

### Covarianza y Correlación

Ambas miden el valor de la **relación lineal** entre 2 variables aleatorias X y Y.

#### Covarianza

* Mide dirección (signo) de la relación entre X y Y.
* Magnitud **no estandarizada**.
* Rango Cov(X) = [-inf, inf]

![Covarianza](/images/covarianza.png)

#### Correlación
* Mide **dirección** (signo) de la relación entre X y Y.
* Mide la **fuerza** (magnitud **estandarizada**).
* Rango Cor(X) = [-1, 1]
* Relación lineal perfecta = *-1 o 1*.

[Estandarización, covarianza y correlación](/scripts/2-aplicando-conceptos/estandarizacion-covarianza-correlacion/estandarizacion-covarianza-correlacion.md)

![Correlación](/images/correlacion.png)

# Construir conceptos estadísticos analíticos

[Carpeta de trabajo](/scripts/3-construccion-conceptos-estadisticos-analiticos/)

## Estimadores a través de datos

![Uso de Estimadores](/images/estimadores.png)

**Definición**

Criterios para la selección de un estimador:
1. Que sea **centrado** (insesgado), es decir, que ![Estimado](/images/ETeta.png).
2. De **mínima varianza** en el sentido que si ![Teta 1](/images/E1.png) y ![Teta 2](/images/E2.png) son estimadores centrados de ![Teta](/images/teta.png), se considera mejor aquel de menor varianza.
3. Es deseable que sea **lineal** respecto a las variables de la muestra.

[Estimadores](/scripts/3-construccion-conceptos-estadisticos-analiticos/1-estimadores/estimadores.md).

## Estimadores de máxima verosimilitud

[Más información](https://tereom.github.io/est-computacional-2018/maxima-verosimilitud.html )

1. El método de máxima verosimilitud consiste en obtener el valor de lambda donde la **L(lambda) sea máximo**.
1. L(lambda) es la **función de máxima verosimilitud**, y está definida como el producto entre todos los valores de la muestra aleatoria evaluados en su función de densidad.
1. En este caso la distribución a estudiar es una **exponencial**, esto es importante, porque TODA distribución exponencial tiene función de **densidad = parametro * e^(parametro*x)**, entonces ya tenemos una función con que trabajar.
1. Se desarrolla la función para después aplicar Logaritmo natural.
1. **¿Por qué logaritmo natural?** Por dos razones, una tiene que ver con lo práctico de utilizar logaritmos en términos operatorios, pero la mas importante es que, dadas las propiedades de los logaritmos, **la función L(lambda) es máxima en el mismo punto que Ln(L(lambda))**.
1. Se desarrolla la nueva función que se simplifica gracias a las propiedades de los logaritmos.
1. **¿Por qué se deriva y se iguala a cero?** recuerden que la primera derivada hace referencia a la pendiente de la función, y si la pendiente es cero significa que e**stamos en presencia de un mínimo o un máximo**.
1. Acá falto algo, porque para poder asegurar que ese valor de lambda es máximo, se debe derivar por segunda vez, si la segunda derivada es < 0 entonces estamos frente a un máximo, no se puede asegurar nada sin hacer este análisis.
1. Sorpresa! el estimador de max verosimilitud de una función es el promedio muestral.

![Mejores estimadores](/images/mejores-estimadores.png)

## Distribuciones muestrales

* **Estimador**: **V.A.** en función de la muestra de la forma `f(x1, x2, ... , xn)`.
* **Estadístico**: **V.A.** en función de la muestra y los parámetros poblacionales de la forma: `f(x1, x2, ... , xn, θ1, θ2, ..., θn)` sigue una distribución particular.

Donde los parámetros desconocidos son reemplazados por valores bajo una hipótesis nula o 0, `(θ1 = θ10, θ2 = θ20, ... , θn = θn0)`.

![Distribuciones muestrales](/images/distribuciones-muestrales.png)

1. Distribución de la V.A. original como parámetro poblacional mu desconocido.
2. Distribución del promedio muestral como mejor estimador de mu.
3. Definición de la hipótesis sobre los valores de los parámetros poblacionales.
4. Estandarización del promedio muestral tomando como cierta la hipótesis definida.

![Distribuciones muestrales](/images/distribuciones-muestrales2.png)

(N-1): [Grados de libertad](https://www.webyempresas.com/grados-de-libertad-en-estadistica/).

[Distribuciones muestrales](/scripts/3-construccion-conceptos-estadisticos-analiticos/2-distribuciones-muestrales/distribuciones-muestrales.md)

## Teorema del límite central

Este concepto nos permite aproximar la función de distribución de una variable aleatoria de la cual no conocemos previamente su distribución.

Indica que si sumamos n cantidad de variables aleatorias independientes con un n > 30, podemos aproximar la función utilizando la curva de la distribución normal, incluso si las variables aleatorias originales no se distribuyen como una normal.

[Teorema del límite central](/scripts/3-construccion-conceptos-estadisticos-analiticos/3-teorema-del-limite-central/teorema-del-limite-central.md)

# Realizar inferencias estadisticas a partir de una muestra

[Carpeta de trabajo](/scripts/4-inferencia-estadistica-partir-muestra/)

## Pruebas de hipótesis

Una *prueba de hipótesis* es una regla que especifica si se puede aceptar o rechazar una afirmación acerca de un **parámetro poblacional** (lambda, sigma, mu, etc), dependiendo de la evidencia proporcionada por una muestra de datos (x1, x2, x3, ..., xn).

### Pasos para hacer una prueba de hipótesis

1. Parámetro a probar (theta, lamda, mu, varianza, covarianza, etc.).
2. 
    * Hipotesis Nula (siempre de igualdad =)
    * Hipotesis Alterna (mayor que >, menor que <, o diferente que !=)
3. Identificar el estimador (promedio muestral o varianza muestral).
4. Identificar el estadístico y su distribución (normal, t-student, chi-cuadrada, F-fisher, etc).
5. Valor del estadístico | H0
6. Tolerancia al error alfa, valor crítico y criterio de rechazo de H0.
7. Conclusión de rechazo o no rechazo de H0 con un margen de error de alfa.

### Caso de Ejemplo

* La empresa Mustage S.A. está desarrollando una plataforma para otorgar créditos de bajo monto.
* El tiempo para completar exitosamente una consulta de información de clientes ante las fuentes de buro **no debe ser superior a 30 segundos en promedio**.
* Muestra de **n = 50** clientes consultados.
* La empresa está dispuesta a asumir un error del 5% en a prueba.

**¿El proveedor de información satisface estadísticamente este requerimiento?**

[Prueba de hipótesis](/scripts/4-inferencia-estadistica-partir-muestra/1-pruebas-hipotesis/pruebas-hipotesis.md)

El caso de valor crítico es Rojo, todo lo que esté por encima del valor crítico es poco probable bajo los valores del estimador, los valores poblacionales de mi variable aleatoria y bajo la muestra que he tomado, por lo tanto, con este criterio de rechazo, se puede decir que se tiene suficiente prueba estadística para concluir que mu no tiene un valor igual a 30, y en favor de la hipotesis alterna, mu probablemente sea mayor que 30.

![Valor crítico y criterio de Rechazo de H0](/images/valor-critico-de-rechazo.png)

Las pruebas de hipotesis nos han permitido evidenciar qué tan probable es que nuestro valor poblacional mu tenga un valor 30 o superior dada una muestra, en este caso, tenemos una muestra de mayor o igual, que sería el caso 3 o de cola derecha.

También se podrían tener hipotesis de diferencia, caso en el cual sería prueba de 2 colas, y debemos dividir la probabilidad del error para que se distribuya en ambas zonas de la distribución y tendremos también un criterio de rechazo en ambos sentidos, siempre que el valor del estadístico sea menor al Valor Crítico A (región inferior), o al Valor Crítico B (región superior) deberíamos rechazar la hipotesis nula.

También existe un caso que el criterio de rechazo es el menor, que es el que la hipotesis alterna es de caso menor, asume que nuestro parámetro poblacional será menor a un valor dado, que es el caso 1 o Prueba de cola izquierda, y debemos hacer el calculo del error y del valor crítico en un valor de probabilidad que acumule el error en la cola izquierda.

### Conclusión del Ejemplo

Estaría a favor de que el tiempo que le toma a una persona logearse y poder acceder a un crédito es mayor a los requisitos que los requerimientos que necesitan sobre el proveedor.

![Prueba Mustage](/scripts/4-inferencia-estadistica-partir-muestra/1-pruebas-hipotesis/output_11_1.png)

## Errores estadísticos Tipo 1 y Tipo 2

![Errores estadísticos](/images/errores-estadisticos.png)

* Siempre vamos a trabajar con las hipotesis nula y alterna por lo tanto, siempre tenemos la opción de aceptar la hipotesis y en contraste saber si la hipotesis era o no verdadera. En este caso, tenemos la hipotesis nula y la opción de que la hipotesis nula sea verdadera o no, y aceptar la hipotesis alterna y que esta sea verdadera o no.

![Descripción del Error](/images/descripcion-error.png)

[Errores estadísticos Tipo 1 y Tipo 2](/scripts/4-inferencia-estadistica-partir-muestra/2-erores-estadisticos-tipo1-tipo2/erores-estadisticos-tipo1-tipo2.md)

Siendo Alfa la probabilidad de equivocarnos al no rechazar H0 siendo esta verdadera, es deseable que esta sea el error que tienda a 0, también tenemos en contraposición la potencia de la prueba que es `1 - beta` o el error tipo 2, sin embargo, beta no es facilmente calculable por lo cual se suele optimizar el error asociado a alfa, a no rechazar la hipotesis nula cuando esta es verdadera.

## Intervalos de confianza

Nos permiten encontrar el límite inferior y superior tales que acumulen cierta probabilidad o confianza de que el parámetro poblacional estará contenido y podrá tomar ese valor en ese escenario bajo los cuales será medida esta variable. De esta manera, por ejemplo, si tuvieramos una muestra de 20 casos (100%) asociados al promedio de una variable aleatoria X en 19 de los casos (95%) podríamos asegurar que ese valor se encuentra en un intervalo de confianza del 95%.

### Pasos y elementos de un intervalo de confianza

1. Parametro a probar (theta, lambda, mu, varianza, covarianza, etc).
2. Identificar el estimador (promedio muestral o varianza muestral).
3. Identificar el estadístico y su distribución (normal, t-student, chi-cuadrada, f-fisher, etc).
4. Tolerancia al error alfa, estimación puntual y rango de error.
5. Conclusión del intervalo.
6. **Opcional**: Pruebas de hipótesis usando Intervalos de Confianza.

[Intervalos de Confianza](/scripts/4-inferencia-estadistica-partir-muestra/3-intervalos-confianza/intervalos-confianza.md)

# Usar modelos estadísticos para exploración y predicción

[Carpeta de Trabajo](/scripts/5-modelos-estadisticos-exploracion-prediccion/)

## Regresión Lineal

Es un modelo, algoritmo o función matemática que aproxima de forma **óptima** la relación entre una variable Y y una variable X o un set de variables (X1, X2, X3, ..., Xn), utilizando la función de la recta (es decir, una línea).

**Función de la Recta**: Y = aX +b, *a* = pendiente y *b* = corte en el eje de las coordenadas.

**Función de Regresión**: Y = aX + b + error, X y Y V.A.

*a* y *b* son los **parámetros poblacionales** de la función que relaciona a Y y X.

El objetivo de un análisis de regresión es encontrar los mejores estimadores de *a* y *b* con el **mínimo error**.

## Pasos

1. Identificar a partir de un conjunto de variables X1, X2, ..., Xk cuáles son las que mejor explican linealmente a una V.A. de interés Y.
2. A partir del modelo de regresión lineal, predecir el comportamiento de una V.A. Y con base en el comportamiento de un conjunto de variables X1, X2, ..., Xk.

![Regresión lineal](/images/regresion-lineal.png)

Comentario de: [Riccilob](https://platzi.com/@riccilob)

La ‘aleatoriedad’ en realidad se refiere a los residuos (y- y_pred), también llamados errores o residuales. Y se requiere porque es un supuesto del modelo. A eso hace referencia la gráfica que facilita visualizar cómo se distribuyen los errores (o las diferencias, o los residuos, como la quieran llamar). Si no se observa un patrón se suele asumir que son aleatorias (otro supuestos en el análisis de residuales es que tengan una distribción normal y una varianza constante).

Residuales independientes:

![Residuales independientes](/images/independant-residuals.jpg)

Residuales No independientes (claramente se ve un patrón), lo que significa que la destribución de los residuos no es aleatoria (y hay que corregir el modelo o quizá porbar con un modelo no lineal):

![Residuales NO independientes](/images/non-independant-residuals.jpg)

[Fuente](https://www.jmp.com/en_us/statistics-knowledge-portal/what-is-regression/simple-linear-regression-assumptions.html)

El modelo de regresión busca minimizar estos valores, pero siempre se asume que hay un término de ‘Error’ asociado al modelo y que es porpio de la naturaleza del fenómeno que estamos analizando.

### Funciones utilizadas

* OLS Ordinary Least Squares: Será la manera en la que optimicemos los parámetros de la función de Regresión Lineal.
    * reg_lin = sm.OLS(y, sm.add_constant(X)).fit(), recibe 2 parámetros, la variable dependiente Y (en este caso los salarios) y la constante X, que en este caso, como estamos evaluando 2 posibilidades (gpa(promedio acumulado en la carrera) y experiencia, usaremos la X mayúsculas, por tener una matriz. Obtendremos lo siguiente.
```
                            OLS Regression Results                            
==============================================================================
Dep. Variable:                salario   R-squared:                       0.798
Model:                            OLS   Adj. R-squared:                  0.794
Method:                 Least Squares   F-statistic:                     211.0
Date:                Mon, 31 Aug 2020   Prob (F-statistic):           7.37e-38
Time:                        21:29:53   Log-Likelihood:                -1135.4
No. Observations:                 110   AIC:                             2277.
Df Residuals:                     107   BIC:                             2285.
Df Model:                           2                                         
Covariance Type:            nonrobust                                         
==============================================================================
                 coef    std err          t      P>|t|      [0.025      0.975]
------------------------------------------------------------------------------
const       4968.0099   4325.267      1.149      0.253   -3606.328    1.35e+04
gpa         2.024e+04   1364.423     14.831      0.000    1.75e+04    2.29e+04
experien    1973.1918    148.539     13.284      0.000    1678.730    2267.653
==============================================================================
Omnibus:                        0.779   Durbin-Watson:                   1.909
Prob(Omnibus):                  0.678   Jarque-Bera (JB):                0.857
Skew:                          -0.191   Prob(JB):                        0.651
Kurtosis:                       2.795   Cond. No.                         72.2
==============================================================================

Warnings:
[1] Standard Errors assume that the covariance matrix of the errors is correctly specified.
```
Dep. Variable:                salario -> Variable dependiente
Model:                            OLS -> Modelo utilizado (Ordinary List Squares)
R-squared: Es una medida de desempeño en este caso nos indica que nuestra regresión en nuestras variables X están explicando la variabilidad de Y en un 79%.
F-statistic: Se usa en generación de pruebas de hipotesis para medir la significancia de esta regresión que será apróximada a partir de este estadístico.
Prob (F-statistic): La probabilidad de que no rechacemos de que la significancia de esta regresión sea nula.

Nuestro interés principal son los coeficientes que corresponden a alpha y beta, donde alpha o a será la pendiente, en este caso por tener 2 variables explicativas (gpa y experien) estarán asociadas a las variables X definidas previamente. La constante en la tabla es dónde se cortan en el eje Y.

std err nos hace referencia al error asociado a los coeficientes, con estos 2, podemos construir una función t, sobre t probar la significancia de estos parámetros, en este caso, al probar la significancia de los parámetros tenemos una función o una hipótesis nula de que el parámetros es igual a cero, nos está indicando la probabilidad de que esta t o mejor, de que el error tipo I o probabilidad de rechazo, es muy cercana a 0.
```
  P>|t|
----------
  0.253
  0.000
  0.000
```
Por lo cual rechazaríamos esta hipotesis nula, y tendríamos que estadísticamente hablando el coeficiente asociado a gpa es diferente de cero, por lo que la variable es significativa y permite explicar a Y. 
```
   [0.025      0.975]
-----------------------
 -3606.328    1.35e+04
  1.75e+04    2.29e+04
  1678.730    2267.653
```
Estos son los intervalos de confianza para cada una de las variables que hemos definido. 

Por último se muestran una serie de pruebas que deben hacerse para chequear la estabilidad del modelo que hemos generado en particular los modelos de regresión deben chequear 3 cosas:
* Que el error se distribuya normal, para ello entonces, se genera una figura de los errores.
```
# Figura de los errores
fig, ax = plt.subplots()
y_pred = reg_lin.predict(sm.add_constant(X))
ax.scatter(y, y-y_pred)
plt.axhline(y=0, color='black', alpha = 0.8, linestyle='--') 
```
![Random](/images/random.png)

Como el diagrama de puntos no identifica ningún patrón, sino que son aleatorios, podemos decir que la muestra es aleatoria. Lo mismo puede probarse con la prueba de Jarque-Bera (JB).

Otro chequeo importante que se debe hacer es que no haya multi-colinealidad entre los regresores o las variables X y esta se puede probar a través de la prueba Cond. No., y la prueba omnibus nos permite saber si las varianzas del modelo son iguales o están igualmente distribuidas, que es otro fuerte del modelo de regresión, lo que se conoce como elasticidad de la varianza.

![Resultado](/images/results.png)

### Conclusión

El modelo de regresión lineal nos va a permitir identificar los pesos que tienen las variables a la hora de explicar a Y y también hacer predicciones en el futuro sobre la variable Y.

[Regresión Lineal](/scripts/5-modelos-estadisticos-exploracion-prediccion/1-regresion-lineal/regresion-lineal.md)

## Regresión logística

Los modeos de regresión lineal tienen como variable de respuesta (Y) una variable **cuantitativa**.

¿Qué pasa si la variable de respuesta fuera **cualitativa**?

Por ejemplo, una variable cualitativa o de naturaleza Bernoulli, que indique si una persona compra o no un producto.

X = 0: **NO COMPRADOR**,          X = 1: **COMPRADOR**

Ahora la regresión lineal no se puede aplicar porque al estimar los valores 0 o 1 incurriríamos en valores menores a 0 y mayores que 1.

Transformaremos la variable de salida con el operador logístico, el cual acotará el resultado a **0** o **1**, a través de la siguiente fórmula:

![Fórmula: Regresión Logística](/images/formula-regresion-logistica.png)



[Regresión Logistíca](/scripts/5-modelos-estadisticos-exploracion-prediccion/2-regresion-logistica/regresion-logistica.md)

## Árboles de regresión y de clasificación

[Documentación oficial Scikit-Learn: Árbol de Decisiones](https://scikit-learn.org/stable/modules/tree.html)

No solo están inspirados en la naturaleza sino en la forma en la que los humanos tomamos decisión. Un árbol de decisión al igual que la regresión, va a necesitar una serie de inputs o variables aleatorias X que pasaremos a través de las decisiones del árbol y nos permitirá aproximar el valor de Y.

![Árbol de decisión](/images/arbol-decision.png)

Los árboles de decisión son ampliamente utilizados debido a su **alta capacidad explicativa** a la hora de estimar Y con un conjunto de variables X.
* Las preguntas en cada nodo pueden ser variables categóricas o numéricas.
* Los árboles de decisión pueden ser de regresión cuando aproximan una variable numérica o de clasificación cuando aproximan una categoría.

![Ejemplo: Árbol de Decisión](/images/minitree.png)

Los árboles necesitan o están compuestos por unos nodos, ramas, y las hojas. En los nodos encontramos las variables aleatorias X, en las ramas las decisiones o reglas que se aplican a X y en las hojas el valor de Y, bajo las decisión que hemos tomado para X.

### Base fundamental para entrenar modelos
Dividir la muestra para poder probar el desempeño del modelo en 2 partes.

Se divide en X y en Y. Esto es una parte de la base que el modelo nunca verá y que nos permitirá probar con más certeza el desempeño del modelo.

`X_train, X_test, y_train, y_test = train_test_split(X, y, test_size = 0.2, random_state = 1)`
0.2 es el porcentaje que queremos que quede en la base de la base en test. El random_state sirve para que el sampling aleatorio que se hace para generar estas diferentes muestras siempre sea reproducible.

clf = classifier (Clasificador)
```
clf = DecisionTreeClassifier(criterion = 'entropy', max_depth = 3)
clf = clf.fit(X_train, y_train)
y_pred = clf.predict(X_test)
```
[Documentación: DecisionTreeClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html)

StringIO nos va a permitir establecer las reglas del árbol de decisión que generamos en strings.
`dot_data = StringIO()`

Después usamos la función export_graphviz, sobre él vamos a pasar el árbol de decisión entrenado y un outfile, que utilizará el dot_data generado anteriormente. Filled y rounded son parámetros de visualización.

`export_graphviz(clf, outfile = dot_data, filled = True, rounded = True, special_characters = True, feature_names = X.columns, class_names = y.value_counts().index)`

[Documentación: export_graphviz](https://scikit-learn.org/stable/modules/generated/sklearn.tree.export_graphviz.html)

[Árbol de Decisión](/scripts/5-modelos-estadisticos-exploracion-prediccion/3-arbol-decision/arbol-decision.md)

# Introducir conceptos de analítica avanzada

## Proyecto análisis exploratorio: Descriptivos, outliers, creación y selección de variables



[Proyecto](/scripts/6-caracterizar-informacion-analisis-exploratorio/1-proyecto-analisis-exploratorio/proyecto-analisis-exploratorio.md)