# **Análisis de Datos sobre Educadores en República Checa y Austria**  

## 📌 **Descripción del Proyecto**  
Este repositorio contiene un análisis detallado de un conjunto de datos basado en encuestas realizadas a educadores en República Checa y Austria. El objetivo es procesar, limpiar y analizar la información recopilada para extraer conclusiones relevantes sobre las condiciones laborales y bienestar de los encuestados.  

## 📂 **Estructura del Repositorio**  

### **1️⃣ Data Preparation (`Data_preparation.ipynb`)**  
Este notebook documenta el proceso de limpieza y preparación de datos. Se incluyen los siguientes pasos:  

✔ **Carga de datos** → Lectura del conjunto de datos original.  
✔ **Renombrado de columnas** → Asignación de nombres más claros y representativos.  
✔ **Tratamiento de valores nulos** → Imputación mediante media, moda y eliminación en casos necesarios.  
✔ **Creación de variables calculadas** → Promedios de indicadores clave como autonomía percibida, presión por desempeño y satisfacción laboral.  
✔ **Diferenciación entre académicos y no académicos** → Ajustes específicos para cada grupo.  
✔ **Exportación del dataset limpio** → Guardado en formatos `.csv` y `.xlsx` para facilitar el análisis posterior.  

### **2️⃣ Diccionario de Datos (`data_dictionary.md`)**  
Este archivo describe detalladamente cada variable del conjunto de datos. Incluye:  

✔ **Nombre de la variable** → Tal como aparece en el dataset.  
✔ **Descripción** → Explicación del significado de la variable.  
✔ **Tipo de dato** → Si es numérico, categórico u ordinal.  
✔ **Rango de valores** → Valores posibles o escala utilizada en la encuesta.  
✔ **Consideraciones especiales** → Variables aplicables solo a académicos o no académicos.  

Este diccionario facilita la comprensión del dataset y su correcta utilización en análisis posteriores.  

### **3️⃣ Data Analysis (`data_analysis.ipynb`)**  
Este notebook documenta el proceso de análisis exploratorio y estadístico sobre el dataset de la encuesta de bienestar laboral académico en instituciones de educación superior de Austria y República Checa. Se realizan los siguientes procedimientos:  

✔ **Análisis Univariado**  
   - Exploración de la distribución de cada variable numérica mediante estadísticas descriptivas (utilizando el método `describe()`) para verificar que presentan comportamientos esperados según su naturaleza.  
   - Visualización de distribuciones con histogramas, boxplots y curvas de densidad para evaluar la dispersión y concentración de los datos.  
   - Revisión de variables categóricas utilizando etiquetas descriptivas, lo que facilita identificar el balance y comportamiento de cada grupo (por ejemplo, "Masculino" y "Femenino", "Austria" y "República Checa", etc.).  

✔ **Análisis Multivariado**  
   - Generación de matrices de dispersión (pairplots) que permiten observar las relaciones entre todas las variables de forma compacta.  
   - Construcción de matrices de correlación (Pearson, Kendall y Spearman) mediante mapas de calor, aplicando máscaras y ajustes visuales para resaltar patrones sin saturar la visualización.  
   - Evaluación de la correlación entre variables, identificando que muchas no se reflejan de forma clara en los valores de R², lo cual es importante para el desarrollo posterior de modelos estadísticos.  

✔ **Evaluación y Selección de Variables**  
   - Identificación de variables, como los ingresos en distintas divisas, que pueden generar problemas de multicolinealidad y sobreajuste debido a la alta varianza de los coeficientes. Se recomienda su omisión o transformación en el modelado.  
   - Recomendación de trabajar inicialmente con variables categóricas decodificadas (manteniendo sus etiquetas descriptivas) para facilitar la visualización y análisis. Posteriormente, se pueden codificar para la etapa de modelación.  
   - Realización de estadísticas agrupadas por categorías para evaluar efectos de interacción y sesgos en función del contexto socioeconómico, costumbres, género, políticas y otros factores relevantes.  

---

📌 **Próximo Paso:** Si se desarrollan modelos predictivos o inferenciales, se pueden documentar en una sección adicional del repositorio. 🚀  


