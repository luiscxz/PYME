# Predicción de Riesgo de Incumplimiento crediticio


El objetivo de este proyecto fue **desarrollar un modelo de predicción de riesgo de incumplimiento crediticio** para clientes PYME, con un horizonte de 12 meses posteriores a la aprobación del crédito.  

Los resultados iniciales muestran que el modelo puede **identificar correctamente 8 de cada 10 clientes que incumplen**, lo que representa un avance significativo hacia una gestión de riesgo más eficiente.

**Recomendaciones clave:**
- Antes de usarlo en producción, se recomienda **refinar el modelo con más datos**, especialmente de clientes que hayan incumplido.  
- Si se aplicara en su estado actual, la estrategia más conservadora sería:
  - **Aprobar solo el 52.8% de los clientes** cuya probabilidad de incumplimiento sea menor a **0.5%**.  
  - Bajo este umbral, **1 de cada 6 aprobados** presentaría incumplimiento.  
  - **Dar prioridad** a clientes con **calificación buró A o B**, quienes muestran **tasas de cumplimiento superiores al 96%**.

---

## Factores Predictivos Clave

El modelo identificó tres variables como las más determinantes en la predicción del riesgo de incumplimiento:

1. **Historial de pagos:**  
   Los clientes con antecedentes de atrasos presentan una probabilidad significativamente mayor de incumplir.  

2. **Calificación buró:**  
   Los segmentos con calificaciones **C y D** concentran los mayores riesgos, mientras que **A y B** se asocian con perfiles de muy alto cumplimiento.  

3. **Nivel de endeudamiento:**  
   La relación entre el **monto solicitado + deudas totales / ingresos** refleja la capacidad real de pago del cliente.  

*En síntesis:* el **historial**, la **calificación crediticia** y el **nivel de deuda relativa** son los predictores más influyentes del riesgo crediticio.

---

## Rendimiento del Modelo

El modelo demuestra un **buen equilibrio entre sensibilidad y especificidad**, logrando detectar la mayoría de los incumplimientos sin rechazar innecesariamente a clientes solventes.  

No obstante, dado que fue entrenado con una base de datos **reducida**, sus resultados deben considerarse **exploratorios** y no definitivos.

**Posibles impactos si se consolida con más datos:**
- **Reducción de pérdidas por impago**, al recomendar aprobaciones más seguras.  
- **Segmentación de cartera optimizada**, priorizando clientes A y B, los más rentables.  
- **Estrategia de crecimiento más robusta**, maximizando utilidades y minimizando exposición al riesgo.

---

## Tecnologías y Herramientas Utilizadas

- **Lenguaje:** Python  
- **Librerías principales:** `pandas`, `scikit-learn`, `numpy`, `matplotlib`, `xgboost`  
- **Modelo base:** Clasificador supervisado (árboles de decisión / boosting)  
- **Métricas de evaluación:** `Precision`, `Recall`, `F1-score`  
- **Gestión de datos:** `CSV / SQL`  
- **Entorno de desarrollo:** Jupyter Notebook / VS Code  

---
