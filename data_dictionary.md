# Diccionario de Datos del Conjunto de Datos de Encuesta

Este documento describe las variables contenidas en el conjunto de datos de la encuesta. La información se basa en un análisis descriptivo inicial.

**Número total de observaciones:** 2748

## Descripción de Variables

| Nombre de la Variable             | Descripción                                                                 | Tipo de Dato | Valores/Rango          | Notas                                     |
|-----------------------------------|-----------------------------------------------------------------------------|--------------|------------------------|-------------------------------------------|
| `Country`                         | País de residencia del encuestado (codificado numéricamente)                | Categórico   | 1, 2                   |                                           |
| `Version`                         | Versión de la encuesta utilizada (codificada numéricamente)                 | Categórico   | 1 - 4                  |                                           |
| `Gender`                          | Género autopercibido del encuestado                                         | Categórico   | 1=Masculino, 2=Femenino, 3=Otro |                                           |
| `Age`                             | Edad del encuestado en años                                                 | Numérico     | 18 - 84                |                                           |
| `Marital_Status`                  | Estado civil del encuestado (codificado numéricamente)                      | Categórico   | 1 - 6                  | Contiene valores nulos (28)               |
| `Care_Responsibilities`           | Responsabilidades de cuidado del encuestado (codificado numéricamente)      | Categórico   | 1 - 4                  | Contiene valores nulos (19)               |
| `HEI_Type`                        | Tipo de institución de educación superior (codificado numéricamente)        | Categórico   | 1 - 8                  |                                           |
| `Faculty_Subject_Area`            | Área temática principal de la facultad (codificada numéricamente)           | Categórico   | 1 - 13                 | Contiene valores nulos (28)               |
| `Employment_Contract_Duration`    | Duración del contrato de empleo (codificada numéricamente)                  | Categórico   | 1 - 7                  | Contiene valores nulos (3)                |
| `HEI_Employment_Hours`            | Horas de empleo semanales según contrato en la institución de educación superior | Numérico     | 0.5 - 80               |                                           |
| `HEI_Actual_Weekly_Hours`         | Horas reales trabajadas semanalmente en la institución                      | Numérico     | 0 - 80* | *Rango basado en diccionario original     |
| `Effort_Level`                    | Nivel de esfuerzo percibido en el trabajo (escala Likert)                   | Categórico   | 1 - 5* | *Rango basado en diccionario original     |
| `Effort_Percentage`               | Porcentaje estimado de esfuerzo dedicado al trabajo                         | Numérico     | Variable* | *Rango basado en diccionario original     |
| `Income_EURO`                     | Ingreso mensual o anual en Euros (sin ajustar)                              | Numérico     | Variable* | *Rango basado en diccionario original     |
| `Euro_Adjusted`                   | Ingreso ajustado en Euros (posiblemente por PPP o inflación)                | Numérico     | Variable* | *Rango basado en diccionario original     |
| `Salary_per_Hour`                 | Salario calculado por hora trabajada                                        | Numérico     | Variable* | *Rango basado en diccionario original     |
| `Salary_Effort_per_Hour`          | Salario por hora ajustado por el nivel de esfuerzo percibido                | Numérico     | Variable* | *Rango basado en diccionario original     |
| `Leadership_Position`             | Indica si el encuestado ocupa un puesto de liderazgo                        | Categórico   | 0=No, 1=Sí* | *Rango basado en diccionario original     |
| `Policy_Influence`                | Nivel percibido de influencia en las políticas institucionales (escala Likert) | Categórico   | 1 - 5* | *Rango basado en diccionario original     |
| `Other_Paid_Job`                  | Indica si el encuestado tiene otro trabajo remunerado                       | Categórico   | 0=No, 1=Sí* | *Rango basado en diccionario original     |
| `Other_Job_Weekly_Hours_1`        | Horas semanales trabajadas en el otro empleo remunerado                     | Numérico     | 0 - 80* | *Rango basado en diccionario original     |
| `Academic_or_Non_Academic`        | Clasificación del puesto del encuestado                                     | Categórico   | 1=No académico, 2=Académico* | *Rango basado en diccionario original     |
| `Teaching_Hours`                  | Horas semanales dedicadas a la enseñanza                                    | Numérico     | 0 - 75                 | Solo aplica a personal académico (n=2150) |
| `Research_Hours`                  | Horas semanales dedicadas a la investigación                                | Numérico     | 0 - 75                 | Solo aplica a personal académico (n=2150) |
| `Funded_Research_Activities`      | Horas semanales dedicadas a actividades de investigación financiadas        | Numérico     | 0 - 50                 | Solo aplica a personal académico (n=2150) |
| `Administrative_Activities`       | Horas semanales dedicadas a tareas administrativas                          | Numérico     | 0 - 80                 | Solo aplica a personal académico (n=2150) |
| `Job_Category`                    | Categoría específica del empleo                                             | Categórico   | Variable* | Solo aplica a personal no académico* |
| `Highest_Education_Level`         | Nivel educativo más alto alcanzado                                          | Categórico   | Variable* | Solo aplica a personal no académico* |
| `Career_Length_CZ`                | Duración de la carrera profesional en la República Checa (en años)          | Numérico     | Variable* | Solo aplica a personal no académico* |
| `Performance_Pressure`            | Nivel de presión por desempeño percibido (escala Likert)                    | Numérico     | 1 - 5                  | Contiene valores nulos (8)                |
| `Perceived_Autonomy`              | Nivel de autonomía percibida en el trabajo (escala Likert)                  | Numérico     | 1 - 5                  | Contiene valores nulos (48)               |
| `Quality_of_Leadership`           | Percepción sobre la calidad del liderazgo en la institución (escala Likert) | Numérico     | 1 - 5                  | Contiene valores nulos (16)               |
| `Sense_of_Community`              | Sentimiento de comunidad en el lugar de trabajo (escala Likert)             | Numérico     | 1 - 5                  | Contiene valores nulos (1)                |
| `Job_Satisfaction`                | Nivel general de satisfacción laboral (escala Likert)                       | Numérico     | 1 - 5                  | Contiene valores nulos (3)                |
| `Burnout`                         | Nivel de agotamiento profesional (escala Likert)                            | Numérico     | 1 - 7                  | Contiene valores nulos (6)                |
| `Current_Position`                | Posición o rol actual del encuestado (codificado numéricamente)             | Categórico   | 0 - 13                 |                                           |

**Notas Generales:**

* Las variables marcadas con `*` en la columna "Valores/Rango" o "Notas" no estaban presentes en el resumen estadístico (`describe()`) proporcionado. Sus rangos y descripciones se basan en el diccionario original y podrían necesitar verificación adicional.
* Las variables indicadas como "Solo aplica a personal académico" o "Solo aplica a personal no académico" tendrán valores nulos (NaN) para los encuestados del grupo opuesto.
* La columna "Valores/Rango" para variables categóricas muestra los códigos numéricos encontrados en los datos. Se recomienda consultar la documentación original de la encuesta para obtener las etiquetas exactas de cada código si es necesario.
* La presencia de valores nulos se indica cuando el conteo (`count`) de la variable en el análisis descriptivo es menor que el número total de observaciones (2748). El número entre paréntesis es la cantidad de valores nulos.
