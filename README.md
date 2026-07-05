# HVAC Predictive Maintenance & Energy Efficiency

## Descripción del proyecto

Este proyecto analiza lecturas operativas de equipos HVAC para identificar patrones asociados con fallas próximas y consumo energético. El objetivo es construir una solución de análisis que ayude a priorizar mantenimiento preventivo antes de que los equipos fallen.

> Nota: el dataset incluido es simulado con lógica realista de operación HVAC. Se utiliza para demostrar habilidades de análisis de datos, limpieza, visualización, modelado y comunicación de resultados.

## Problema de negocio

En mantenimiento HVAC, muchas fallas se detectan cuando el equipo ya dejó de operar correctamente. Esto puede generar tiempo muerto, llamadas de emergencia, costos altos y menor estabilidad operativa.

Este proyecto responde a la pregunta:

**¿Podemos usar lecturas operativas para detectar equipos con mayor riesgo de falla en los próximos 7 días?**

## Objetivos

- Analizar variables como Delta T, presión de succión, presión de descarga, amperaje, vibración, presión diferencial del filtro, horas de operación y consumo energético.
- Identificar señales relacionadas con fallas próximas.
- Construir un modelo de clasificación para predecir riesgo de falla.
- Presentar resultados visuales que ayuden a tomar decisiones de mantenimiento.

## Tecnologías utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Estructura del repositorio

```text
hvac-predictive-maintenance/
├── data/
│   └── hvac_equipment_readings.csv
├── notebooks/
│   └── hvac_predictive_maintenance.ipynb
├── assets/
│   ├── delta_t_failure.png
│   ├── energy_vs_outdoor_temp.png
│   ├── feature_importance.png
│   └── confusion_matrix.png
└── README.md
```

## Proceso de análisis

1. **Carga de datos**: se revisó el dataset de lecturas HVAC, incluyendo variables de operación, energía y condición de falla.
2. **Limpieza y preparación**: se trataron valores faltantes con imputación por mediana y se seleccionaron variables numéricas relevantes.
3. **Análisis exploratorio**: se analizaron patrones entre consumo energético, temperatura exterior, Delta T y eventos de falla.
4. **Modelado predictivo**: se propone un modelo Random Forest con pesos balanceados para manejar la diferencia entre equipos con falla y sin falla.
5. **Evaluación**: el notebook calcula métricas como Accuracy, F1-score, AUC-ROC y matriz de confusión.

## Indicadores del dataset

| Indicador | Valor |
|---|---:|
| Registros analizados | 1,800 |
| Equipos incluidos | 15 |
| Tasa de falla simulada | 7.5% |
| Delta T promedio sin falla | 17.5 °F |
| Delta T promedio con falla | 14.9 °F |

## Visualizaciones

### Delta T promedio por condición de falla
<img width="1280" height="800" alt="delta_t_failure" src="https://github.com/user-attachments/assets/7a45af40-76cd-4382-a61a-948bc7268aaa" />



### Consumo energético vs temperatura exterior
<img width="1280" height="800" alt="energy_vs_outdoor_temp" src="https://github.com/user-attachments/assets/0a201efa-efd6-402b-abd3-eab54e7557f4" />



### Variables relacionadas con riesgo de falla
<img width="1280" height="800" alt="delta_t_failure" src="https://github.com/user-attachments/assets/b4162e70-014d-44f4-9d78-8ce9e00d98c8" />



### Matriz de confusión
<img width="800" height="640" alt="confusion_matrix" src="https://github.com/user-attachments/assets/a85e7530-9937-4dc5-a538-015e48e0a50f" />



## Conclusión

El análisis muestra que variables como Delta T, presión de descarga, amperaje, vibración, presión diferencial del filtro y consumo energético pueden ayudar a identificar equipos con mayor probabilidad de falla.

Este tipo de análisis puede apoyar decisiones de mantenimiento preventivo, ayudando a reducir fallas inesperadas, priorizar inspecciones y mejorar la eficiencia operativa.

## Posibles mejoras futuras

- Conectar datos reales desde un sistema BMS, sensores IoT o registros de mantenimiento.
- Crear un dashboard en Power BI, Tableau o Streamlit.
- Agregar costos de reparación para estimar ahorro potencial.
- Probar modelos adicionales como Gradient Boosting, XGBoost o CatBoost.
- Incorporar explicación de modelos con SHAP.
