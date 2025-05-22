Informe Detallado del Análisis de Ecuaciones Estructurales (SEM) sobre Bienestar Laboral
Fecha: 21 de Mayo, 2025
Investigación: Impacto de las Condiciones de Trabajo sobre el Burnout, mediado por Motivación y Vulnerabilidad Psicológica.
Conjunto de Datos: labour_wellbeing_processed_v1.csv (N=992, después de la preparación inicial y sin valores faltantes en las variables del modelo).

1. Introducción y Evolución del Modelo
El presente estudio tuvo como objetivo principal investigar las complejas relaciones entre diversas condiciones de trabajo, las orientaciones motivacionales (controlada y autónoma), la vulnerabilidad psicológica y el burnout en una muestra de trabajadores. El modelo conceptual inicial, visualizado en el diagrama proporcionado por el equipo de investigación, planteaba un efecto de las "Condiciones de Trabajo" (X) sobre el "Burnout" (BO), con la "Motivación" (X1: Controlada, X2: Autónoma) y la "Vulnerabilidad" (V) actuando como variables mediadoras en una secuencia causal.

Un primer intento de modelado trató "Condiciones de Trabajo" (X) como una variable latente única, medida por nueve indicadores observables. Sin embargo, este modelo inicial presentó serios problemas de ajuste a los datos (CFI ≈ 0.54, TLI ≈ 0.43, RMSEA ≈ 0.137) y dificultades en la estimación de los parámetros de la variable latente X (errores estándar muy grandes y varianza de X cercana a cero). Estos resultados indicaron que los nueve indicadores no convergían adecuadamente para formar un único constructo latente coherente de "Condiciones de Trabajo" en esta muestra.

Ante estos hallazgos, se tomó la decisión metodológica de transitar hacia un Modelo de Senderos (Path Analysis). En este enfoque, los nueve indicadores de condiciones de trabajo se tratan como variables observadas exógenas separadas, permitiendo evaluar su impacto individual sobre las variables mediadoras y el resultado final. Este cambio estratégico resultó en un modelo con un ajuste significativamente mejor y parámetros interpretables, como se detalla a continuación.

2. Preparación de Datos y Diagnósticos del Modelo de Senderos
2.1. Carga y Preparación de Datos

Los datos se cargaron desde la URL proporcionada. Se realizaron los siguientes pasos de preparación:

Renombrado de columnas: Effort [%] a Effort_perc e Income EURO a Income_EURO para compatibilidad.

Creación de variables compuestas para motivación:

WM_Controlled_Motivation: Promedio de WM_Extrinsic_Social, WM_Extrinsic_Material, WM_Introjected_Motivation.

WM_Autonomous_Motivation: Promedio de WM_Identified_Motivation, WM_Intrinsic_Motivation.

Se confirmó la ausencia de valores perdidos (NaNs) en todas las variables incluidas en el modelo final.

2.2. Análisis de Colinealidad (Factor de Inflación de la Varianza - VIF)

Se evaluó la multicolinealidad entre los nueve indicadores de condiciones de trabajo (que actúan como predictores simultáneos en varias ecuaciones del modelo).

Resultados del VIF:
| Característica         | VIF     |
| :--------------------- | :------ |
| Perceived_Autonomy     | 1.505   |
| Quality_Leadership     | 1.405   |
| Avg_Work_Hours_HE      | 1.360   |
| Sense_Community        | 1.302   |
| Academic_Resources     | 1.299   |
| Income_EURO            | 1.203   |
| Policy_Influence       | 1.106   |
| Performance_Pressure   | 1.104   |
| Effort_perc            | 1.078   |

Interpretación: Todos los valores VIF son muy inferiores a 5 (y considerablemente inferiores al umbral más laxo de 10). Esto indica que la colinealidad entre estos predictores es baja y no representa un problema para la estabilidad de las estimaciones de los coeficientes en el modelo.

3. Especificación y Ajuste del Modelo de Senderos Final
3.1. Especificación del Modelo

El modelo de senderos final se especificó de la siguiente manera (sintaxis semopy):

# Modelo Estructural con Indicadores de X como predictores observados separados
WM_Controlled_Motivation ~ Avg_Work_Hours_HE + Income_EURO + Effort_perc + Policy_Influence + Academic_Resources + Performance_Pressure + Perceived_Autonomy + Quality_Leadership + Sense_Community
WM_Autonomous_Motivation ~ Avg_Work_Hours_HE + Income_EURO + Effort_perc + Policy_Influence + Academic_Resources + Performance_Pressure + Perceived_Autonomy + Quality_Leadership + Sense_Community
Vulnerability ~ WM_Controlled_Motivation + WM_Autonomous_Motivation
Burnout_Score ~ Avg_Work_Hours_HE + Income_EURO + Effort_perc + Policy_Influence + Academic_Resources + Performance_Pressure + Perceived_Autonomy + Quality_Leadership + Sense_Community + Vulnerability

Aclaración: El signo + en las ecuaciones anteriores indica que se estima un efecto separado para cada variable predictora sobre la variable dependiente, controlando estadísticamente los efectos de los otros predictores en la misma ecuación.

3.2. Bondad de Ajuste del Modelo

El modelo se ajustó utilizando el estimador de Máxima Verosimilitud (MLW), ya que no había datos faltantes. Los índices de bondad de ajuste fueron:

Índice

Valor

Interpretación (Umbrales Comunes)

χ 
2
  (gl)

229.376 (57)

-

p-value (χ 
2
 )

0.000

Sensible a N grande; no concluyente por sí solo

CFI

0.953

Excelente (>0.95)

TLI

0.928

Bueno (>0.90)

RMSEA

0.0396

Excelente (<0.05-0.06)

GFI

0.939

Bueno (>0.90)

AGFI

0.907

Aceptable/Bueno (>0.90)

Conclusión del Ajuste: A pesar del χ 
2
  significativo (esperado con N=992), los índices CFI, TLI y RMSEA indican de manera robusta y consistente que el modelo de senderos presenta un excelente ajuste a los datos observados.

4. Análisis de Efectos Directos
Se examinaron los coeficientes estandarizados (β) para interpretar la fuerza y dirección relativa de los efectos directos. A continuación, se resumen los hallazgos significativos (p < 0.05).

A. Influencia de las Condiciones de Trabajo sobre WM_Controlled_Motivation:

Efectos Positivos (aumentan la motivación controlada): Performance_Pressure (β=0.189, el más fuerte), Academic_Resources (β=0.070).

Efectos Negativos (disminuyen la motivación controlada): Policy_Influence (β=−0.084, el más fuerte negativo), Perceived_Autonomy (β=−0.060), Income_EURO (β=−0.058).

No significativos (p > 0.05, según la última tabla de coeficientes estandarizados proporcionada): Avg_Work_Hours_HE (p=0.401), Effort_perc (p=0.211), Quality_Leadership (p=0.091), Sense_Community (p=0.071).

B. Influencia de las Condiciones de Trabajo sobre WM_Autonomous_Motivation:

Efectos Positivos (aumentan la motivación autónoma): Perceived_Autonomy (β=0.364, el más fuerte por diferencia), Performance_Pressure (β=0.104), Avg_Work_Hours_HE (β=0.094), Effort_perc (β=0.068), Policy_Influence (β=0.075), Sense_Community (β=0.070).

Efectos Negativos (disminuyen la motivación autónoma): Academic_Resources (β=−0.024, p=0.031).

No significativos (p > 0.05): Income_EURO (p=0.208), Quality_Leadership (p=0.703).

C. Influencia de la Motivación sobre Vulnerability:

WM_Controlled_Motivation → Vulnerability: β=0.158 (Positivo y significativo; la motivación controlada aumenta la vulnerabilidad).

WM_Autonomous_Motivation → Vulnerability: β=−0.287 (Negativo y significativo; la motivación autónoma reduce la vulnerabilidad, siendo el efecto más fuerte sobre la vulnerabilidad).

D. Influencia sobre Burnout_Score:

Efectos Positivos Directos (aumentan el burnout): Vulnerability (β=0.231, el más fuerte), Performance_Pressure (β=0.176), Avg_Work_Hours_HE (β=0.129), Effort_perc (β=0.080), Policy_Influence (β=0.059).

Efectos Negativos Directos (reducen el burnout): Perceived_Autonomy (β=−0.176, el protector más fuerte), Academic_Resources (β=−0.086), Quality_Leadership (β=−0.071), Sense_Community (β=−0.056).

No significativo (p > 0.05): Income_EURO (p=0.097).

5. Análisis de Mediación: Comparación Detallada Sobel vs. Bootstrapping
Se evaluó la significancia de los efectos indirectos de las 9 condiciones de trabajo sobre el Burnout_Score, a través de las cadenas de motivación (WM_Controlled_Motivation o WM_Autonomous_Motivation) y Vulnerability.

5.1. Método de Prueba de Sobel

La prueba de Sobel asume normalidad en la distribución del efecto indirecto.

5.2. Método de Bootstrapping (2000 Muestras)

El bootstrapping no asume normalidad y genera un intervalo de confianza (IC) del 95% para el efecto indirecto. Si el IC no incluye cero, el efecto es significativo. Este método se considera más robusto.

5.3. Comparación de Resultados y Hallazgos de Mediación

Vía de Mediación (X → M1 → M2 → Y)

IE (Sobel)

p (Sobel)

Sig. (Sobel)

IE Medio (Boot)

IC 95% (Boot)

Sig. (Boot)

Concordancia

Avg_Work_Hours_HE → WM_C → V → BO

0.000055

0.4049

No

0.000058

[-0.000077, 0.000206]

No

Sí

Avg_Work_Hours_HE → WM_A → V → BO

-0.000432

0.0003

Sí

-0.000417

[-0.000668, -0.000201]

Sí

Sí

Income_EURO → WM_C → V → BO

-0.000001

0.0264

Sí

-0.000001

[-0.000002, -0.000000]

Sí*

Sí

Income_EURO → WM_A → V → BO

-0.000001

0.2131

No

-0.000001

[-0.000003, 0.000000]

No**

Sí

Effort_perc → WM_C → V → BO

-0.000019

0.2204

No

-0.000023

[-0.000073, 0.000003]

No

Sí

Effort_perc → WM_A → V → BO

-0.000081

0.0026

Sí

-0.000098

[-0.000201, -0.000038]

Sí

Sí

Policy_Influence → WM_C → V → BO

-0.002255

0.0017

Sí

-0.002267

[-0.003913, -0.000961]

Sí

Sí

Policy_Influence → WM_A → V → BO

-0.003605

0.0013

Sí

-0.003629

[-0.005913, -0.001604]

Sí

Sí

Academic_Resources → WM_C → V → BO

0.002860

0.0108

Sí

0.002826

[0.000778, 0.005149]

Sí

Sí

Academic_Resources → WM_A → V → BO

0.001757

0.3115

No

0.001724

[-0.001837, 0.005225]

No

Sí

Performance_Pressure → WM_C → V → BO

0.005518

0.0000

Sí

0.005537

[0.003474, 0.008053]

Sí

Sí

Performance_Pressure → WM_A → V → BO

-0.005477

0.0000

Sí

-0.005442

[-0.008322, -0.002857]

Sí

Sí

Perceived_Autonomy → WM_C → V → BO

-0.002033

0.0377

Sí

-0.002050

[-0.004238, -0.000152]

Sí

Sí

Perceived_Autonomy → WM_A → V → BO

-0.022361

0.0000

Sí

-0.022441

[-0.028754, -0.016791]

Sí

Sí

Quality_Leadership → WM_C → V → BO

0.001193

0.1032

No (Marginal)

0.001159

[-0.000167, 0.002700]

No

Sí

Quality_Leadership → WM_A → V → BO

-0.000453

0.7034

No

-0.000454

[-0.002954, 0.002077]

No

Sí

Sense_Community → WM_C → V → BO

0.001473

0.0833

No (Marginal)

0.001537

[-0.000003, 0.003365]

No**

Sí

Sense_Community → WM_A → V → BO

-0.004123

0.0046

Sí

-0.004167

[-0.007487, -0.001186]

Sí

Sí

*Nota: * El IC para Income_EURO → WM_C → V → BO es [-0.000002, -0.000000]. Aunque el límite superior es extremadamente cercano a cero, técnicamente no lo incluye, por lo que se considera significativo.
*Nota: ** El IC para Income_EURO → WM_A → V → BO y Sense_Community → WM_C → V → BO incluye cero (o un límite es cero), por lo que no son significativos por bootstrapping.

Discusión de la Comparación Sobel vs. Bootstrapping:
Existe una alta concordancia entre los dos métodos. Todas las vías que fueron significativas (p<0.05) con la prueba de Sobel también lo fueron con el bootstrapping (IC 95% no incluye cero), y las que no fueron significativas con Sobel tampoco lo fueron con bootstrapping (con la excepción de los casos límite donde el IC de bootstrap apenas toca el cero). Esto refuerza la confianza en los hallazgos de mediación. El bootstrapping, al ser más robusto, confirma los resultados de la prueba de Sobel en este caso.

Principales Hallazgos de Mediación (basados en Bootstrapping):

La Autonomía Percibida (Perceived_Autonomy) ejerce el efecto indirecto protector más fuerte contra el burnout, principalmente al fomentar la WM_Autonomous_Motivation, que a su vez reduce la Vulnerability.

La Presión de Desempeño (Performance_Pressure) tiene efectos indirectos significativos y opuestos: aumenta el burnout a través de la vía de WM_Controlled_Motivation y lo disminuye a través de la vía de WM_Autonomous_Motivation.

Otras condiciones como Avg_Work_Hours_HE, Effort_perc, Policy_Influence, Income_EURO (vía WM_C), Academic_Resources (vía WM_C) y Sense_Community (vía WM_A) también muestran efectos indirectos significativos sobre el burnout a través de los mecanismos de motivación y vulnerabilidad.

6. Conclusión General del Proceso de Modelado y Principales Hallazgos
El proceso de modelado, que evolucionó desde un modelo de variable latente a un modelo de senderos más ajustado, ha sido exitoso. El modelo de senderos final presenta un excelente ajuste a los datos y está libre de problemas serios de multicolinealidad.

Los efectos directos revelan que condiciones de trabajo específicas como la Perceived_Autonomy (protectora) y la Performance_Pressure (de riesgo) son predictores directos importantes del burnout. Además, la Vulnerability es un fuerte predictor directo del burnout, mientras que la WM_Autonomous_Motivation reduce la vulnerabilidad y la WM_Controlled_Motivation la aumenta.

El análisis de mediación, validado robustamente mediante bootstrapping, confirma que la motivación (controlada y autónoma) y la vulnerabilidad psicológica son mecanismos clave a través de los cuales múltiples condiciones de trabajo ejercen su influencia sobre el burnout. Destaca el rol protector de la autonomía percibida, que opera indirectamente fomentando la motivación autónoma. El complejo papel de la presión de desempeño, con efectos indirectos opuestos, sugiere dinámicas interesantes que merecen mayor exploración teórica.

En conjunto, estos hallazgos proporcionan una comprensión detallada y matizada de las interrelaciones entre el entorno laboral, los estados motivacionales, la vulnerabilidad individual y el burnout, ofreciendo una base sólida para futuras investigaciones e intervenciones prácticas.
