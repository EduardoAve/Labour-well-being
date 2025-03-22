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

---


