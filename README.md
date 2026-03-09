# 📊 Telecom X - Análisis de Evasión de Clientes (Churn)

## 📝 Descripción del Proyecto
Este proyecto forma parte del **Challenge 2 de Data Science LATAM** (Alura / Oracle Next Education). El objetivo principal es analizar la base de datos de la empresa de telecomunicaciones "Telecom X" para identificar y comprender los factores que influyen en la evasión de clientes (*Churn*). 

A través de un proceso integral de ETL (Extracción, Transformación y Carga) y un Análisis Exploratorio de Datos (EDA), los datos crudos fueron limpiados y estructurados para extraer *insights* de negocio. Este análisis sienta las bases para el futuro desarrollo de modelos predictivos y estrategias de retención.

## 🎯 Objetivos
* Importar y manipular datos anidados desde una API en formato JSON.
* Aplicar técnicas de limpieza de datos: manejo de valores ausentes, corrección de tipos de datos y estandarización de variables categóricas.
* Realizar un Análisis Exploratorio de Datos (EDA) utilizando visualizaciones estadísticas.
* Generar recomendaciones estratégicas basadas en el comportamiento de los usuarios (permanencia, tipo de contrato, y cargos mensuales).

## 🛠️ Tecnologías y Herramientas Utilizadas
* **Lenguaje:** Python 3
* **Manipulación de Datos:** Pandas, NumPy
* **Visualización de Datos:** Matplotlib, Seaborn
* **Entorno:** Jupyter Notebook / Google Colab

## 📂 Estructura del Análisis

1. **Extracción y Aplanamiento:** Lectura del archivo `TelecomX_Data.json` y uso de `pd.json_normalize()` para aplanar las estructuras de diccionarios anidados.
2. **Limpieza de Datos:**
   * Eliminación de registros sin información en la variable objetivo (`Churn`).
   * Corrección de formato en la variable de cargos totales (`account.Charges.Total`), limpiando espacios en blanco y transformándola a formato numérico (`float64`).
   * Conversión de variables de tiempo de permanencia (`tenure`) a formato entero.
3. **Análisis Exploratorio (EDA):**
   * Gráficos de barras (`sns.barplot`) para visualizar la distribución general de la evasión.
   * Uso de subgráficos (`subplots`) para analizar la relación del Churn con el tipo de contrato, método de pago y servicios contratados.
   * Gráficos de cajas (`boxplot`) para entender el impacto del tiempo de retención y los cargos mensuales sobre la cancelación del servicio.

## 💡 Principales Insights
* **La fuga es temprana:** La gran mayoría de los clientes que abandonan la empresa lo hacen durante los primeros meses de servicio. Los clientes antiguos demuestran un alto nivel de lealtad.
* **El tipo de contrato importa:** El modelo de pago "mes a mes" (Month-to-month) concentra casi la totalidad de las cancelaciones, evidenciando que la falta de compromiso a largo plazo facilita la evasión.
* **Sensibilidad al precio:** Los clientes que cancelan sus cuentas tienden a tener cargos mensuales más altos, lo que sugiere una insatisfacción con el valor percibido del servicio.

## 🚀 Cómo ejecutar el proyecto
1. Clona este repositorio en tu máquina local:
   ```bash
   git clone [https://github.com/TU_USUARIO/challenge2-data-science-LATAM.git](https://github.com/TU_USUARIO/challenge2-data-science-LATAM.git)