# Laboratorio de Estadística · Gráficas de distribuciones de frecuencias

**Herramienta web para construir las gráficas de una distribución de frecuencias, con datos agrupados o no agrupados, y descargarlas como imagen JPG.**

🔗 **Usar la herramienta:** https://temocbzc.github.io/Graficas_de_distribuciones_de_frecuencias/

🔗 **Módulos anteriores:**
[Tabla de datos no agrupados](https://temocbzc.github.io/Tabla_de_Distribucion_de_frecuencias_sin_datos_agrupados/) ·
[Tabla de datos agrupados](https://temocbzc.github.io/Tabla_de_Distribucion_de_frecuencias_con_datos_agrupados/)

---

## Sobre el Laboratorio de Estadística

Este módulo es parte del **Laboratorio de Estadística**, un proyecto de herramientas digitales abiertas para los cursos de **Estadística y Probabilidad I y II** de nivel bachillerato, pensado especialmente para el **Colegio de Ciencias y Humanidades (CCH) de la UNAM**.

El laboratorio sigue la propuesta del Programa de Estudios 2024 del CCH, que pide incorporar la computadora y las herramientas tecnológicas para organizar datos, calcular medidas y construir gráficas. La intención es que el tiempo de clase se dedique a **analizar e interpretar** la información y no a hacer cálculos repetitivos a mano.

---

## Este módulo: representación gráfica

**Ubicación en el programa:** Estadística y Probabilidad I · Unidad 1, *Análisis de información estadística para una variable* · Representación gráfica.

### Qué hace

1. Recibe los datos de una muestra, en un **archivo CSV** o escritos directamente en la página.
2. Construye la tabla de distribución de frecuencias, con **datos no agrupados** o **agrupados** en intervalos de clase.
3. Dibuja la gráfica elegida y permite decidir **qué frecuencia se muestra en cada eje vertical**.
4. Genera una imagen **JPG** en alta resolución, lista para un reporte o una tarea.

Está diseñada para usarse desde el **celular**.

### Gráficas disponibles

| Gráfica | Datos no agrupados | Datos agrupados |
|---|---|---|
| **Puntos** | Un punto por dato, apilados sobre cada valor $x_i$ | Puntos apilados sobre la marca de clase de cada intervalo |
| **Circular** | Un sector por cada valor, proporcional a $fr_i$ | Un sector por intervalo |
| **Barras / Histograma** | Barras separadas sobre cada $x_i$ | Barras unidas de $LI_i$ a $LS_i$ (histograma) |
| **Polígono de frecuencias** | Une los puntos $(x_i,\ f_i)$ | Une las marcas de clase; se cierra en el eje con una clase vacía antes y después |
| **Barras + polígono** | Barras y polígono en la misma gráfica | Histograma y polígono en la misma gráfica |
| **Ojiva** | Une los puntos $(x_i,\ F_i)$ | Parte de $(LI_1,\ 0)$ y une los puntos $(LS_i,\ F_i)$ |

Si la variable es **cualitativa** (por ejemplo, medio de transporte), solo se activan las gráficas de puntos, circular y de barras: el polígono y la ojiva necesitan que los valores tengan un orden numérico.

### Ejes verticales a elegir

En las gráficas de barras, histograma, polígono y ojiva, el alumno elige qué muestra **cada eje**:

| Eje | Opciones |
|---|---|
| Izquierdo | Frecuencia absoluta · Frecuencia relativa % · Sin eje |
| Derecho | Frecuencia absoluta · Frecuencia relativa % · Sin eje |

Como $fr_i = \dfrac{f_i}{n}\times 100$, la frecuencia absoluta y la relativa son proporcionales: **la misma gráfica se puede leer en los dos ejes**. En la ojiva los ejes muestran las frecuencias acumuladas $F_i$ y $Fr_i\ \%$.

### Datos agrupados: mismo método que la tabla

Se usa el procedimiento del [módulo de datos agrupados](https://temocbzc.github.io/Tabla_de_Distribucion_de_frecuencias_con_datos_agrupados/):

- $R = x_{\text{máx}} - x_{\text{mín}}$
- $k = 1 + 3.322 \log(n)$, aproximado al entero siguiente (regla de Sturges)
- $A = R / k$, aproximado hacia arriba con los decimales de los datos
- $LI_1 = x_{\text{mín}}$; intervalos $[LI_i,\ LS_i)$ y el último cerrado $[LI_k,\ LS_k]$

El alumno también puede **elegir su propio $k$ y su propio $A$** y ver cómo cambia el histograma.

### Formato del archivo CSV

- La **celda A1** lleva el **nombre de la variable**.
- Debajo, en la misma columna, van **todos los datos**, uno por celda.
- En Excel o Google Sheets: *Archivo → Guardar como / Descargar → CSV*.

En el repositorio hay tres archivos de ejemplo: [`ejemplo_numero_de_hermanos.csv`](ejemplo_numero_de_hermanos.csv) (discreta), [`ejemplo_estaturas.csv`](ejemplo_estaturas.csv) (continua) y [`ejemplo_medio_de_transporte.csv`](ejemplo_medio_de_transporte.csv) (cualitativa).

### Privacidad

Los datos se procesan **solo en el navegador** del usuario. No se envían ni se guardan en ningún servidor.

---

## Actividades sugeridas para el aula

1. **¿Qué gráfica conviene?** Con los tres archivos de ejemplo, decidir qué gráficas tienen sentido para cada variable y por qué el polígono no aplica a una variable cualitativa.
2. **Dos ejes, una gráfica.** Construir el histograma con la frecuencia absoluta a la izquierda y la relativa a la derecha. ¿Por qué coinciden las alturas? ¿Qué pasa con el eje relativo si se duplica la muestra con los mismos porcentajes?
3. **Leer la ojiva.** ¿Qué porcentaje de los datos es menor que cierto límite superior? ¿Dónde se lee la mediana de forma aproximada?
4. **El efecto de k.** Construir el histograma con $k = 4$, con el valor de Sturges y con $k = 12$. ¿Qué forma de la distribución se ve en cada caso?
5. **Circular contra barras.** Comparar las dos gráficas con los mismos datos: ¿en cuál es más fácil comparar categorías parecidas?

---

## Mapa del laboratorio

| Módulo | Estado |
|---|:---:|
| [Distribución de frecuencias, datos no agrupados](https://temocbzc.github.io/Tabla_de_Distribucion_de_frecuencias_sin_datos_agrupados/) | ✅ Disponible |
| [Distribución de frecuencias, datos agrupados](https://temocbzc.github.io/Tabla_de_Distribucion_de_frecuencias_con_datos_agrupados/) | ✅ Disponible |
| [Actividad: calidad del aire en la CDMX](https://temocbzc.github.io/Tabla_de_Distribucion_de_frecuencias_con_datos_agrupados/calidad-aire/) | ✅ Disponible |
| Gráficas: puntos, circular, barras, histograma, polígono de frecuencias, ojiva | ✅ Disponible |
| Medidas de tendencia central, dispersión y posición | 🔜 Planeado |
| Datos bivariados: tablas de contingencia, correlación y regresión | 🔜 Planeado |
| Azar y probabilidad: simulación y probabilidad condicional | 🔜 Planeado |
| Distribuciones binomial y normal, Teorema del Límite Central, inferencia | 🔜 Planeado |

---

## Contenido del repositorio

| Archivo | Descripción |
|---|---|
| `index.html` | Herramienta web (un solo archivo, sin dependencias que instalar) |
| `ejemplo_numero_de_hermanos.csv` | Variable cuantitativa discreta |
| `ejemplo_estaturas.csv` | Variable cuantitativa continua (50 estaturas) |
| `ejemplo_medio_de_transporte.csv` | Variable cualitativa |

---

## Autor

**Dr. Ignacio Cuauhtémoc Benítez Zúñiga** · Profesor de Estadística y Probabilidad, Colegio de Ciencias y Humanidades, UNAM.

Proyecto desarrollado dentro del trabajo sobre el uso de la inteligencia artificial generativa en la enseñanza de la estadística en el bachillerato.

## Referencia

Colegio de Ciencias y Humanidades, UNAM (2024). *Programas de Estudio. Área de Matemáticas. Estadística y Probabilidad I–II.* https://cch.unam.mx/sites/default/files/programas2024/ESTADISTICA_PROBABILIDAD_I_II.pdf
