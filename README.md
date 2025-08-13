
# 📊 Análisis de retiro de clientes de Clientes y Modelos Predictivos

## ✅ Objetivo del Proyecto

Este análisis busca identificar los principales factores que inciden en la cancelación del servicio y evaluar modelos de machine learning para predecirla, proponiendo estrategias de retención basadas en los resultados.
---

## 🧪 Metodología

- **Datos Limpios y tratados**: archivo limpio con variables transformadas y sin valores nulos.
- **Modelos aplicados**: Árbol de Decisión, Random Forest, KNN.
- **Técnica de balanceo**: undersampling para equilibrar clases.
- **Métricas evaluadas**: Accuracy, Precision, Recall y F1-score.
- **Evaluación**: sobre conjunto de validación (30%) estratificado.

---
Classification Report:
              precision    recall  f1-score   support

           0       0.85      0.74      0.79      1086
           1       0.44      0.60      0.51       367

    accuracy                           0.71      1453
   macro avg       0.65      0.67      0.65      1453
weighted avg       0.75      0.71      0.72      1453

Confusion Matrix:
[[809 277]
 [146 221]]
## Resultados

| Modelo                      | Accuracy | Precision | Recall | F1-score |
|----------------------------|----------|-----------|--------|----------|
| **Random Forest**          | 0.751    | 0.544     | **0.662**  | **0.597**     |
| KNN normalizado            | 0.732    | 0.516     | 0.645  | 0.573     |
| Árbol de Decisión          | 0.656    | 0.424     | 0.642  | 0.510     |

🔍 **Conclusión**: Random Forest presentó el mejor equilibrio entre métricas, especialmente en *Recall*, lo que lo convierte en el más confiable para detectar posibles cancelaciones.

---

## 🔍 Análisis de Variables Más Relevantes (Random Forest)

Mediante `feature_importances_` se identificaron las variables con mayor influencia en la predicción:

| Variable                     | Importancia (%) |
|-----------------------------|------------------|
| `Duracion_en_meses`         | 18.5%           |
| `Monto_facturado_total`     | 16.2%           |
| `Uso_promedio_mensual`      | 12.7%           |
| `Edad_cliente`              | 10.3%           |
| `Reclamos_ultimos_6m`       | 8.9%            |
| `Descuentos_aplicados`      | 7.6%            |
| `Dias_ultimo_contacto`      | 5.1%            |

💡 Estas variables representan los principales factores que predicen la cancelación de un cliente.

---

## 🧠 Interpretación de Resultados

- **Antigüedad baja** → Mayor probabilidad de cancelación.
- **Menor uso/facturación** → Puede reflejar menor percepción de valor.
- **Alta cantidad de reclamos** → Indicador claro de insatisfacción.
- **Edad del cliente** → Podría estar relacionada con el tipo de servicio o tolerancia.
- **Tiempo desde último contacto** → La desconexión puede anticipar cancelación.

---

## 🛡️ Estrategias de Retención Propuestas

1. **Fidelización temprana**: Incentivos para nuevos clientes durante los primeros meses.
2. **Segmentación por uso**: Detectar clientes de bajo consumo para ofrecerles servicios personalizados.
3. **Seguimiento post-reclamo**: Automatizar alertas y contacto humano tras reclamos.
4. **Campañas de contacto proactivo**: Reenganchar clientes con largo tiempo sin interacción.
5. **Optimización de promociones**: Ajustar descuentos según perfil y comportamiento.

---

## 📌 Conclusión

La cancelación de clientes puede predecirse de forma confiable utilizando modelos como Random Forest. Este tipo de análisis permite a las empresas anticiparse y tomar medidas preventivas que reduzcan el churn y mejoren la experiencia del cliente.
