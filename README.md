# TFM: Análisis longitudinal y focalización de hogares vulnerables - HSNP (Kenia)

Trabajo Fin de Máster del Master Data Science, Big Data & Business Analytics (UCM).

Aplicación de técnicas de Ciencia de Datos para analizar un programa de protección social y mejorar la identificación de hogares vulnerables, usando como caso de estudio el Hunger Safety Net Programme (HSNP), un programa de transferencias monetarias en el norte de Kenia.

Memoria completa en PDF: memoria-tfm.pdf

Análisis completo en HTML: analisis-tfm.html

## Objetivo

El trabajo combina dos enfoques que responden a preguntas distintas:

1. Análisis longitudinal: estudiar la evolución de los hogares participantes frente al grupo de comparación mediante Difference-in-Differences (DiD).
2. Modelo predictivo: identificar qué hogares tienen más probabilidades de seguir siendo vulnerables, para orientar mejor los recursos.

## Parte 1. Análisis longitudinal (DiD)

Datos: datos longitudinales del Banco Mundial de hogares de Kenia (línea de base 2009, seguimiento 1 en 2010-2011, seguimiento 2 en 2012).

Método: Difference-in-Differences (DiD) para comparar la evolución de hogares participantes y grupo de comparación.

Resultados analizados: inseguridad alimentaria, gasto equivalente real y proporción del gasto destinada a alimentación.

Resultado: no se observaron diferencias estadísticamente significativas entre grupos en los resultados analizados. Este análisis es descriptivo y exploratorio, y no permite extraer conclusiones causales fuertes sobre el efecto del programa.

## Parte 2. Modelo de focalización

Dataset: 4.636 hogares y 24 variables explicativas.

Variable objetivo: inseguridad alimentaria en el primer seguimiento.

Modelos comparados: regresión logística, árbol de decisión, Random Forest y Gradient Boosting.

Metodología: validación cruzada, métricas de evaluación y optimización de hiperparámetros.

Modelo final: Random Forest optimizado.

Métricas en test: ROC-AUC de 0,791 y recall de 0,743.

Interpretabilidad: importancia de variables, coeficientes de la regresión logística y SHAP.

Simulación de focalización: al seleccionar el 20 % de hogares con mayor riesgo predicho, el 87 % de ese grupo presentaba inseguridad alimentaria, frente al 55,7 % de la muestra general. Esto supone una mejora relativa de aproximadamente el 56,1 % en la concentración de hogares vulnerables.

## Tecnologías utilizadas

Python (pandas, NumPy, scikit-learn, SHAP, matplotlib, seaborn)

Estadística: Difference-in-Differences

Machine Learning: regresión logística, árboles de decisión, Random Forest, Gradient Boosting

Productivización: Flask (API de predicción)

Control de versiones: Git y GitHub

## Contenido del repositorio

memoria-tfm.pdf: memoria completa del trabajo.

analisis-tfm.html: notebook del análisis exportado a HTML, con código y resultados.

analisis-tfm.ipynb: notebook original del análisis.

README.md: este documento.

Nota: el análisis se desarrolló en Google Colab. Las rutas del notebook hacen referencia a Google Drive.

## Limitaciones

El modelo no sustituye una evaluación causal ni decide automáticamente quién debe recibir ayudas. Es una herramienta potencial de apoyo para orientar mejor los recursos de un programa social.

## Autor

Mónica García Higuera

Master Data Science, Big Data & Business Analytics (UCM)
