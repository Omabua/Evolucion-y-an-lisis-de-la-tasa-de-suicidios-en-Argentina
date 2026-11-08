# 📊 Análisis de la Evolución de la Tasa de Suicidios: Argentina vs. El Mundo (2000 - 2021)

Este proyecto de análisis de datos explora la evolución temporal de la tasa de mortalidad por suicidio en Argentina, la compara con el contexto regional e internacional, y profundiza en sus determinantes demográficos (grupos etarios) y macroeconómicos.

El estudio utiliza datos oficiales de la **Organización Mundial de la Salud (OMS)** y del **Banco Mundial (BM)** para el período comprendido entre los años 2000 y 2021.

## 📋 Preguntas de Investigación
1. **¿Cómo evolucionó estadísticamente la tasa de suicidios en Argentina entre 2000 y 2021?**
2. **¿Cómo se compara la situación de Argentina frente a sus países vecinos?**
3. **¿Qué particularidades presenta la distribución por grupos de edad en Argentina en comparación con la tendencia global?**
4. **Anexo Macroeconómico:** ¿Existe una correlación estadística medible entre la tasa de suicidio y variables como el desempleo, el PIB per cápita o la inflación en Argentina?

---

## 🛠️ Tecnologías y Librerías Utilizadas
* **Lenguaje:** Python 3
* **Manipulación de Datos:** `pandas`, `numpy`
* **Visualización de Datos:** `matplotlib`, `seaborn` (estáticos) y `plotly` (gráficos dinámicos e interactivos)
* **Ingesta de Datos (APIs):** `pandas_datareader` (para conectar con la API del Banco Mundial)
* **Procesamiento de Texto:** `difflib` (Fuzzy Matching para estandarización de nombres de países)

---

## 📌 Principales Hallazgos y Conclusiones

### 1. Robustez en la Comparación Internacional (Anomalía Demográfica)
Al ponderar las tasas globales por la población real de cada país para construir un **Promedio Mundial Ponderado**, se ratificó una **anomalía demográfica crítica en Argentina**:
* **Tendencia Global:** A nivel mundial, la tasa de suicidios se incrementa exponencialmente con la edad, teniendo su pico en la población de más de 70 años.
* **Caso Argentino:** En Argentina, la problemática se concentra críticamente en los **jóvenes de 20 a 29 años** y adolescentes de **10 a 19 años**, superando las medias y medianas de referencia global para esos rangos.

### 2. Co-movimiento Macroeconómico (Determinantes Sociales)
El análisis de correlación de Pearson ($r$) evidenció que las fluctuaciones de la tasa de suicidio en Argentina están fuertemente ligadas a los ciclos de estabilidad socioeconómica:
* **Desempleo:** Se halló una **fuerte correlación positiva ($r = 0.63$)** con la tasa de desocupación. El pico histórico de suicidios coincide exactamente con el colapso de la crisis de 2001-2002.
* **PIB Per Cápita:** Se demostró una **correlación negativa ($r = -0.27$)**, lo que indica que la contracción del nivel de actividad actúa como un factor de vulnerabilidad social.

---

## 📂 Estructura del Repositorio
* `notebooks/
  * `Buamden - Proyecto b.ipynb`: Notebook de Jupyter/Colab con el pipeline completo (ETL, Limpieza, EDA, Visualización y Análisis).
* `data/` *(Generados en el Notebook)*:
  * `suicidios_limpio_oms.csv`: Dataset de salud mental depurado de variables constantes.
  * `argentina_macroeconomia_suicidios.csv`: Dataset integrado listo para análisis macroeconómicos.
  * `comparativa_anual_ponderada.csv` & `comparativa_edades_2021.csv`: Archivos preparados para fácil importación en **Power BI** o **Tableau**.
* `dashboard/
  * `Proyecto final Power BI` : Tablero interactivo con conclusiones.
---

## 🚀 Cómo Ejecutar el Proyecto
1. Clona este repositorio:
   ```bash
   git clone https://github.com/tu-usuario/nombre-del-repositorio.git
Instala las dependencias necesarias:
pip install pandas numpy matplotlib seaborn plotly pandas_datareader
Abre y ejecuta el archivo .ipynb en tu entorno local de Jupyter o súbelo a Google Colab.
📈 Fuentes de Datos
Organización Mundial de la Salud (OMS): [redacted link]
Banco Mundial: Indicadores de Población (SP.POP.TOTL), PIB per Cápita (NY.GDP.PCAP.CD) y Desempleo (SL.UEM.TOTL.ZS).
