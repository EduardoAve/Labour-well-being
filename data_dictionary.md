# Diccionario de Datos

Este diccionario describe las variables contenidas en el conjunto de datos utilizado en este proyecto.

## Estructura de la Tabla

| Nombre de la Variable             | Descripción                                                | Tipo de Dato | Rango |
|-----------------------------------|------------------------------------------------------------|--------------|--------|
| Country                           | País de residencia del encuestado                          | Categórico   | - |
| Version                           | Versión de la encuesta                                     | Categórico   | - |
| Gender                            | Género del encuestado                                      | Categórico   | 1 = Masculino, 2 = Femenino, 3 = Otro |
| Age                               | Edad del encuestado                                        | Numérico     | 18 - 99 |
| Marital_Status                    | Estado civil del encuestado                                | Categórico   | 1-5 (Opciones de estado civil) |
| Care_Responsibilities             | Indica si el encuestado tiene responsabilidades de cuidado | Categórico   | 0 = No, 1 = Sí |
| HEI_Type                          | Tipo de institución de educación superior                  | Categórico   | 1 = Pública, 2 = Privada, 3 = Estatal |
| Faculty_Subject_Area              | Área de la facultad                                        | Categórico   | Diferentes áreas académicas |
| Employment_Contract_Duration      | Duración del contrato de empleo                           | Categórico   | 1-5 (Opciones de duración) |
| HEI_Employment_Hours              | Horas de empleo en la institución                         | Numérico     | 0 - 80 |
| HEI_Actual_Weekly_Hours           | Horas reales trabajadas semanalmente                      | Numérico     | 0 - 80 |
| Effort_Level                      | Nivel de esfuerzo percibido                               | Categórico   | 1-5 |
| Effort_Percentage                 | Porcentaje de esfuerzo en el trabajo                      | Numérico     | Variable |
| Income_EURO                       | Ingreso en euros                                          | Numérico     | Variable |
| Euro_Adjusted                     | Ingreso ajustado en euros                                 | Numérico     | Variable |
| Salary_per_Hour                   | Salario por hora                                          | Numérico     | Variable |
| Salary_Effort_per_Hour            | Salario ajustado por nivel de esfuerzo                    | Numérico     | Variable |
| Leadership_Position               | Indica si tiene un puesto de liderazgo                    | Categórico   | 0 = No, 1 = Sí |
| Policy_Influence                  | Influencia en políticas                                   | Categórico   | 1-5 |
| Other_Paid_Job                    | Indica si tiene otro trabajo remunerado                   | Categórico   | 0 = No, 1 = Sí |
| Other_Job_Weekly_Hours_1          | Horas trabajadas en otro empleo                          | Numérico     | 0 - 80 |
| Academic_or_Non_Academic          | Indica si es académico (2) o no académico (1)             | Categórico   | 1 = No académico, 2 = Académico |
| Teaching_Hours (solo académicos)  | Horas dedicadas a la enseñanza                            | Numérico     | 0 - 40 |
| Research_Hours (solo académicos)  | Horas dedicadas a la investigación                        | Numérico     | 0 - 40 |
| Funded_Research_Activities (solo académicos) | Actividades de investigación financiada     | Numérico     | 0 - 40 |
| Administrative_Activities (solo académicos)  | Horas dedicadas a tareas administrativas | Numérico     | 0 - 40 |
| Job_Category (solo no académicos) | Categoría del empleo                                      | Categórico   | Variable |
| Highest_Education_Level (solo no académicos) | Nivel educativo más alto alcanzado         | Categórico   | Variable |
| Career_Length_CZ (solo no académicos) | Longitud de la carrera en la República Checa | Numérico     | Variable |
| Performance_Pressure               | Nivel de presión por desempeño                           | Numérico     | 1 - 5 |
| Perceived_Autonomy                 | Nivel de autonomía percibida                             | Numérico     | 1 - 5 |
| Quality_of_Leadership              | Percepción sobre la calidad del liderazgo               | Numérico     | 1 - 5 |
| Sense_of_Community                 | Sentimiento de comunidad en el trabajo                  | Numérico     | 1 - 5 |
| Job_Satisfaction                   | Nivel de satisfacción laboral                           | Numérico     | 1 - 5 |
| Burnout                            | Nivel de agotamiento profesional                        | Numérico     | 1 - 5 |
| Current_Position                   | Posición actual del encuestado                          | Categórico   | Variable |

**Nota:** Las variables marcadas como "solo académicos" o "solo no académicos" aplican exclusivamente a esos grupos. Para el otro grupo, los valores han sido asignados como nulos.

