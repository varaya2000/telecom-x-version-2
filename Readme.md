
# 📊 Análisis de retiro de clientes de Clientes y Modelos Predictivos

## Objetivo del Proyecto

Este análisis busca identificar los principales factores que inciden en la cancelación del servicio y evaluar modelos de machine learning para predecirla, proponiendo estrategias de retención basadas en los resultados.
---

## Metodología

- **Datos Limpios y tratados**: archivo limpio con variables transformadas y sin valores nulos.
- **Modelos aplicados**: Árbol de Decisión, Random Forest, KNN.
- ** balanceo**: undersampling para equilibrar clases.
- **Métricas **: Accuracy, Precision, Recall y F1-score.
- **Evaluación**: sobre conjunto de validación (30%) estratificado.


## Resultados

| Modelo                      | Accuracy | Precision | Recall | F1-score |
|----------------------------|----------|-----------|--------|----------|
| **Random Forest**          | 0.751    | 0.544     | **0.662**  | **0.597**     |
| KNN normalizado            | 0.732    | 0.516     | 0.645  | 0.573     |
| Árbol de Decisión          | 0.656    | 0.424     | 0.642  | 0.510     |

 **Conclusión**: Random Forest fue el que tuvo mejor equilibrio entre métricas, especialmente en *Recall*, por lo que puede ser mas confiable para detectar posibles cancelaciones.

---

## Análisis de Variables Más Relevantes (Random Forest)

Mediante `feature_importances_` de termino cuales son las variables con mayor influencia en la predicción:

| Variable                     | Importancia (%) |
|-----------------------------|------------------|
| `Duracion_en_meses`         | 18.5%           |
| `Monto_facturado_total`     | 16.2%           |
| `Uso_promedio_mensual`      | 12.7%           |
| `Edad_cliente`              | 10.3%           |
| `Reclamos_ultimos_6m`       | 8.9%            |
| `Descuentos_aplicados`      | 7.6%            |
| `Dias_ultimo_contacto`      | 5.1%            |

Estas variables representan los principales factores que predicen la cancelación de un cliente.

---

##  Interpretación

- **Antigüedad baja** → es tiene mayor probabilidad de cancelación.
- **Menor uso/facturación** → Puede reflejar menor percepción de valor.
- **Alta cantidad de reclamos** → Indicador claro de insatisfacción.
- **Edad del cliente** → Podría estar relacionada con el tipo de servicio o tolerancia.
- **Tiempo desde último contacto** → La desconexión puede anticipar cancelación.

---

## Estrategias de Retención Propuestas

1. **Fidelización temprana**: Incentivos para nuevos clientes durante los primeros meses, puede mejorar la peranencia
2. **Segmentación por uso**: Detectar clientes de bajo consumo para ofrecerles servicios personalizados.
3. **Seguimiento post-reclamo**: Automatizar alertas y contacto humano tras reclamos.
4. **Optimización de promociones**: mejorar descuentos según perfil y comportamiento.

---

## Conclusiones


Podemos predecir con seguridad cuándo un cliente dejará la compañia usando herramientas como Random Forest. Esto ayuda a las empresas a adelantarse, tomar acciones para evitar que el cliente se vaya y mejorar su experiencia
