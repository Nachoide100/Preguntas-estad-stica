# 📊 Laboratorio de Estadística: Conceptos y Casos Prácticos

Este repositorio es una base de conocimientos dedicada a los fundamentos estadísticos necesarios para el análisis de datos riguroso. Aquí documento desde conceptos básicos hasta la resolución de dilemas complejos en experimentación y pruebas de hipótesis.

---

### 🗺️ Navegación Rápida

[![](https://img.shields.io/badge/Nivel-Fácil-brightgreen?style=for-the-badge)](#-nivel-fácil-fundamentos)
[![](https://img.shields.io/badge/Nivel-Intermedio-yellow?style=for-the-badge)](#-nivel-intermedio-aplicación)
[![](https://img.shields.io/badge/Nivel-Difícil-red?style=for-the-badge)](#-nivel-difícil-avanzado)

---

## 🟢 Nivel: Fácil (Fundamentos)

### ❓ ¿Qué es el Teorema del Límite Central y por qué es útil?
<details>
  <summary><b>Ver Respuesta 🔑</b></summary>

  El **Teorema del Límite Central (TLC)** sostiene que si extraemos muestras de una población un gran número de veces, la distribución de las medias de dichas muestras tendrá una forma cercana a la **normal**, independientemente de si la distribución original lo es.

  **Utilidad principal:**
  * **Inferencia estadística:** Permite tratar a los promedios de las muestras como si tuvieran una distribución normal, lo que es vital para realizar estimaciones y pruebas de hipótesis sin conocer la distribución real de la población.
  
  
</details>

### ❓ ¿Cómo explicarías los Intervalos de Confianza a una audiencia no técnica?
<details>
  <summary><b>Ver Respuesta 🔑</b></summary>

  Imagina que quieres saber el peso promedio de todos los osos de un parque nacional. Como es imposible pesarlos a todos, pesas a unos pocos (muestra) y calculas el promedio. Ese número es solo una estimación.
  
  Un **Intervalo de Confianza** (ej. 95%) indica que nuestro método es fiable: si repitiéramos el experimento muchas veces, el 95% de los rangos calculados contendrían el peso real de todos los osos. Cuanto más estrecho es el rango, más precisa es nuestra estimación y menor la incertidumbre.
</details>

### ❓ Compara la Covarianza y la Correlación.
<details>
  <summary><b>Ver Respuesta 🔑</b></summary>

  | Característica | Covarianza | Correlación |
  | :--- | :--- | :--- |
  | **¿Qué mide?** | La dirección de la relación. | La dirección y la **fuerza**. |
  | **Escala** | Sin límites (cualquier número). | Estrictamente entre **-1 y +1**. |
  | **Unidades** | Depende de las variables (kg x m). | Sin unidades (número puro). |
  | **Utilidad** | Cálculos matemáticos internos. | Estimación visual de la relación. |

  
</details>

---

## 🟡 Nivel: Intermedio (Aplicación)

### ❓ ¿Qué es un Z-test y cuándo usarlo frente a un t-test?
<details>
  <summary><b>Ver Respuesta 🔑</b></summary>

  Ambos sirven para saber si un estadístico es significativamente distinto de lo esperado.
  * **Z-test:** Se usa con muestras grandes (>30) o cuando conocemos la varianza de la población.
  * **t-test:** Se usa con muestras pequeñas o cuando estimamos la varianza de la población a partir de la muestra. La distribución *t* tiene "colas más gruesas" para admitir mayor probabilidad de valores extremos por azar.
</details>

### ❓ ¿Cuáles son los peligros comunes en un Test A/B?
<details>
  <summary><b>Ver Respuesta 🔑</b></summary>

  1. **Errores Tipo I y II:** Falsos positivos y falsos negativos.
  2. **Pruebas múltiples:** Hacer muchas pruebas simultáneas aumenta la probabilidad de hallar un falso positivo por puro azar.
  3. **Calidad de datos:** Meter más datos no siempre ayuda; si son irrelevantes, generan ruido y resultados contraproducentes.
</details>

### ❓ Describe los Errores Tipo I y Tipo II.
<details>
  <summary><b>Ver Respuesta 🔑</b></summary>

  * **Tipo I (Falso Positivo):** Rechazar la hipótesis nula cuando es verdadera (ej. decir que alguien tiene cáncer cuando está sano).
  * **Tipo II (Falso Negativo):** No rechazar la nula cuando es falsa (ej. decir que alguien está sano cuando está enfermo).
  
  Existe una **relación inversa**: al intentar reducir uno, solemos aumentar el otro. La gravedad depende del contexto (seguridad vs. medicina).

  
</details>

---

## 🔴 Nivel: Difícil (Avanzado)

### ❓ Caso Práctico: 10 caras seguidas en una moneda. ¿Es justa?
<details>
  <summary><b>Ver Respuesta 🔑</b></summary>

  * **Hipótesis Nula ($H_0$):** La moneda es justa (50% probabilidad). Cualquier resultado es puro azar.
  * **P-value:** Probabilidad de obtener 10 caras seguidas por suerte si la moneda fuera justa.
  * **Cálculo:** $0.5^{10} \approx 0.001$.
  * **Conclusión:** Como $0.001 < 0.05$ (alfa común), tenemos evidencia fuerte para **rechazar la $H_0$**. Es extremadamente improbable que la moneda sea normal.
</details>

### ❓ Explica el trasfondo estadístico del "Poder" (Statistical Power).
<details>
  <summary><b>Ver Respuesta 🔑</b></summary>

  El poder es la capacidad de una prueba para detectar un efecto real (probabilidad de rechazar $H_0$ cuando es falsa). Está ligado al Error Tipo II.
  
  **Factores que lo afectan:**
  1. **Tamaño de muestra:** A más datos, más poder.
  2. **Tamaño del efecto:** Es más fácil detectar cambios grandes que pequeños.
  3. **Nivel de significación:** El umbral establecido (alfa).
  
  Generalmente se busca un poder del **80%**. Se usa para calcular cuántos datos necesitamos *antes* de empezar un experimento.
</details>

### ❓ Consideraciones al comprobar cientos de hipótesis (Múltiples t-tests).
<details>
  <summary><b>Ver Respuesta 🔑</b></summary>

  Al hacer cientos de pruebas, el riesgo de error tipo I se acumula (Data Snooping). Si "torturas" los datos lo suficiente, algo saldrá por azar.
  
  **Medidas correctivas:**
  * **Corrección de Bonferroni:** Dividir el nivel de error (alfa) por el número de pruebas.
  * **Holdout Set:** Reservar datos nuevos para validar los hallazgos tras la exploración inicial.
</details>

---
<p align="right">(<a href="#-laboratorio-de-estadística-conceptos-y-casos-prácticos">Volver arriba ⬆️</a>)</p>
