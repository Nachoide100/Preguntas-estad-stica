# 📊 Estadística

Repositorio de conceptos fundamentales y avanzados de estadística para el análisis de datos. He intentado responde lo mejor posible a las preguntas, según entiendo yo los conceptos y sus aplicaciones. Como siempre, si alguien no está de acuerdo en alguna respuesta, comunicadlo!

### 🗺️ Navegación Rápida

[![](https://img.shields.io/badge/Nivel-Fácil-brightgreen?style=for-the-badge)](#-nivel-fácil)
[![](https://img.shields.io/badge/Nivel-Intermedio-yellow?style=for-the-badge)](#-nivel-intermedio)
[![](https://img.shields.io/badge/Nivel-Difícil-red?style=for-the-badge)](#-nivel-difícil)

---

## 🟢 Nivel: Fácil

### 📖 Explica el Teorema del Límite Central. ¿Por qué es útil?
<details>
  <summary><b>Ver respuesta 🔑</b></summary>

  El teorema del límite central sostiene que si extraemos muestras de la población un gran número de veces, la distribución de las medias de dichas muestras tendrá una forma cercana a la normal, independientemente de si la distribución original lo es.
  
  

  Entre sus principales utilidades destacan:
  * **Facilita la inferencia estadística** → permite tratar a los promedios de las muestras como si tuvieran una distribución normal, incluso si no conocemos la distribución real de la población, lo que es vital para realizar estimaciones y pruebas de hipótesis.
</details>

### 📖 ¿Cómo explicarías los intervalos de confianza a una audiencia no técnica?
<details>
  <summary><b>Ver respuesta 🔑</b></summary>

  Imaginamos que queremos saber el peso promedio de todos los osos de un parque nacional, pero es imposible pesarlos a todos. Para resolverlo, pesamos a unos pocos (muestra) y calculamos el promedio. Sin embargo, sabemos que ese número no es exacto para toda la población, puesto que es solo una estimación. Aquí es donde entran los intervalos de confianza.
  
  El nivel de confianza (95% por ejemplo) indica que nuestro método es confiable: si repitiéramos el experimento muchas veces y calculáramos un nuevo intervalo cada vez, el 95% de esos intervalos contendrían el valor real.
  
  El nivel de confianza se determina por un margen de error establecido con anterioridad al experimento. Cuanto más estrecho se hace el umbral, más precisa se hace la estimación, puesto que implica una menor incertidumbre (puedo asegurar gracias a la calidad de mis datos que el valor real estará dentro de un rango más pequeño).
</details>

### 📖 Explica la covarianza y la correlación y compáralas.
<details>
  <summary><b>Ver respuesta 🔑</b></summary>

  La covarianza es una medida que nos indica si dos variables se mueven en la misma dirección (si una aumenta la otra también y viceversa). Una covarianza positiva será la relación entre el peso y la altura (por lo general, si alguien es más alto, también tiende a pesar más).
  
  La covarianza tiene el problema de que depende totalmente de las unidades de medida. Si medimos la altura en metros o en centímetros, el número de la covarianza cambiará drásticamente, lo que hace que sea muy difícil saber si una relación es “fuerte” o “débil”.
  
  Ahí es donde entra la correlación. La correlación es básicamente una covarianza estandarizada, que podemos utilizar para comparar cualquier variable con una escala fija entre 1 y -1. Además, nos indica qué tan estrecha es la relación entre las variables, cuanto más cerca se encuentre el valor de 1 y -1.

  

  | Característica | Covarianza | Correlación |
  | :--- | :--- | :--- |
  | **¿Qué mide?** | La dirección de la relación (si suben o bajan juntas). | La dirección y la fuerza de la relación. |
  | **Escala** | No tiene límites (puede ser cualquier número). | Limitada estrictamente entre -1 y +1. |
  | **Unidades** | Depende de las unidades de las variables (kilos x metros). | No tiene unidades; es un número puro. |
  | **Utilidad** | Útil para cálculos matemáticos internos en modelos complejos. | La mejor técnica para estimar visualmente qué tan relacionadas están dos cosas. |
</details>

### 📖 ¿Cuáles son algunos de los peligros / dificultades comunes en el test A/B?
<details>
  <summary><b>Ver respuesta 🔑</b></summary>

  Los principales peligros y dificultades del test estadístico son los siguientes:
  * **Errores del Tipo I y Tipo II:** cometer un falso positivo que ocurre cuando se rechaza la hipótesis nula (se cree que hay un efecto) a pesar de que la conjetura es falsa. Cometer un falso negativo, que sucede cuando la conjetura es válida, pero no se logra rechazar la hipótesis nula.
  * **Problema de las pruebas múltiples:** al realizar muchas pruebas de hipótesis simultáneas, la probabilidad de obtener al menos un falso positivo aumenta drásticamente.
  * **Calidad y relevancia de los datos:** agregar grandes cantidades de datos no siempre mejora la precisión, ya que si los datos de entrada son irrelevantes, pueden ser contraproducentes para alcanzar el resultado deseado. Es esencial realizar una selección de características para identificar las variables que realmente contribuyen a la hipótesis.
</details>

### 📖 Describe qué son los errores Tipo I y Tipo II y la relación entre ellos.
<details>
  <summary><b>Ver respuesta 🔑</b></summary>

  El error Tipo I ocurre cuando rechazamos la hipótesis nula a pesar de que es verdadera. Un ejemplo cotidiano sería por ejemplo someter a alguien a una prueba de cáncer y que el resultado sea positivo, cuando el paciente no tiene la enfermedad.
  
  El error Tipo II sucede al contrario, cuando la hipótesis nula es falsa pero no conseguimos rechazarla. Sería concluir que un paciente está sano cuando en realidad sí tiene la enfermedad.
  
  

  Entre ellos existe una relación inversa, lo que significa que si intentamos reducir la probabilidad de cometer uno, generalmente aumentamos la probabilidad del otro: si ajustamos la prueba para que sea muy sensible (no perdernos ningún caso real), es más probable que cometamos errores de tipo I, mientras que si hacemos la prueba muy estricta, será más probable que cometamos errores de tipo II.
  
  De todas formas, la gravedad de cada error depende del contexto en el que apliquemos la prueba. En una prueba de seguridad en aeropuertos, preferimos un error de tipo I (revisar una maleta de más) que un error de tipo II (dejar pasar algo peligroso). Sin embargo, en el caso de una cirugía de riesgo, preferimos evitar el error tipo I (operar a alguien que no lo necesita).
</details>

### 📖 ¿Qué es un Z-test y cuándo lo usaríamos frente a un t-test?
<details>
  <summary><b>Ver respuesta 🔑</b></summary>

  Un Z-test es una prueba estadística que se utiliza para saber si un estadístico de un grupo de datos es significativamente distinto de lo que se esperaba o de otro grupo, basándose en la distribución normal.
  
  **¿Cuándo merece la pena usarlo?** Se utiliza cuando el tamaño de la muestra es grande (> 30 para poder aplicar el Teorema del Límite Central) o cuando conocemos la varianza o desviación estándar de toda la población. En cambio, usar el t-test será útil cuando el grupo de datos es pequeño o cuando tenemos que estimar la varianza de la población a partir de una muestra.
  
  Como consecuencia de esto, la distribución utilizada en el t-test tiene las “colas más gruesas” (student’s t-distribution) puesto que al no conocer la varianza de la población admitimos una mayor probabilidad de observar valores extremos por puro azar.
  ![Distribuciones](https://github.com/Nachoide100/Preguntas-estad-stica/blob/e1939096bbe27b6ead10f155c22b4d06a21108ee/visualizations/Captura%20de%20pantalla%202026-02-03%20192122.png)

  La distribución roja sería la t - student. Conforme la n aumentase, esta ser iría pareciendo a la distribución normal. 
</details>

### 📖 Imagina que tiras una moneda 10 veces y solo observas caras, ¿cuál sería tu hipótesis nula y el p-value para comprobar si la moneda está trucada o no?
<details>
  <summary><b>Ver respuesta 🔑</b></summary>

  La hipótesis nula es la suposición básica de que cualquier resultado que veamos se debe simplemente al azar, por lo que en nuestro caso sería que la moneda es justa y que no está trucada. Bajo esta suposición, esperaríamos que la probabilidad de obtener cara en cada lanzamiento fuera del 50%.
  
  Por otro lado, el p-value señala cómo de probable es que el resultado que observamos (10 caras seguidas) haya ocurrido por pura suerte, suponiendo que la moneda no esté trucada (hipótesis nula).
  
  Ahora, si calculamos la probabilidad de que salgan 10 caras seguidas por azar:
  $$\frac{1}{0.5^{10}}$$
  Obtenemos un valor p aproximado de **0,001**.
  
  Si comparamos ese valor con el límite alfa que normalmente se fija en 0,05, vemos que está por debajo, lo que indica una evidencia fuerte contra la hipótesis nula y un resultado “estadísticamente significativo”.
  
  En conclusión, dado que obtener 10 caras seguidas es algo extremadamente improbable si la moneda no está trucada, tenemos razones sólidas para rechazar la idea de que la moneda es normal.
</details>

### 📖 Explica el trasfondo estadístico del poder.
<details>
  <summary><b>Ver respuesta 🔑</b></summary>

  El poder estadístico se puede entender como la capacidad de una prueba para detectar un efecto o cambio real cuando este realmente existe, es decir, la probabilidad de rechazar la hipótesis nula cuando dicha hipótesis es falsa. Está muy relacionado con el error de tipo II, puesto que el poder estadístico pretende evitar no captar un fenómeno que sí está ocurriendo.
  
  El poder estadístico se basa en:
  * **El tamaño de la muestra:** cuantos más datos recolectemos, más poder tendrá nuestra prueba de detectar lo que está pasando.
  * **Tamaño del efecto (effect size):** la magnitud de la diferencia que queremos detectar. Es más fácil detectar un cambio gigante (aumento de 20% en ventas) que uno diminuto.
  * **Nivel de significación:** el umbral que establecemos para dar un resultado estadísticamente significativo.
  * **Suposición previa:** generalmente se apunta a tener un poder del 80%, lo que supone aceptar un 20% de probabilidad de no detectar un efecto real.
  
  La utilidad más común del poder estadístico es el cálculo del tamaño de la muestra antes de empezar un experimento. Si diseñamos un experimento sin considerar el poder, corremos el riesgo de invertir tiempo y dinero en una prueba que termine siendo inconcluyente, no porque no haya un efecto, sino porque no teníamos suficientes datos para detectarlo.
</details>

### 📖 Digamos que estás comprobando cientos de hipótesis, cada una con un t-test. ¿Qué consideraciones deberíamos tomar si hacemos esto?
<details>
  <summary><b>Ver respuesta 🔑</b></summary>

  Si realizamos cientos de t-test deberemos tener en cuenta los siguientes fenómenos:
  * **Error de Tipo I:** si hacemos un solo test solemos aceptar un margen de error del 5%, pero al hacer cientos de pruebas el riesgo de obtener un resultado por azar se acumula, lo que aumenta en gran cantidad la probabilidad de cometer un falso positivo.
  * **Data snooping:** existe un dicho que dice que “Si torturas los datos lo suficiente, tarde o temprano confesarán”. Esto quiere decir que si buscamos patrones en una base de datos haciendo cientos de preguntas distintas sin un plan previo, acabaremos encontrando algo que nos parezca interesante, pero que en realidad es solo ruido estadístico.
  
  Entre las principales medidas que podemos tomar para evitar estos problemas son la **corrección de Bonferroni** (dividir el nivel de error por el número de pruebas a realizar) y el **Holdout Set** (guardar datos de reserva para una comprobación en datos nuevos una vez pensamos que hemos encontrado algo).
</details>

---

## 🟡 Nivel: Intermedio

---

## 🔴 Nivel: Difícil

<p align="right">(<a href="#-wiki-de-estadística-aplicada">Volver arriba ⬆️</a>)</p>


