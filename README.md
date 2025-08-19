# 📊 TelecomX Challenge — Análisis de Evasión de Clientes
Proyecto de análisis de datos desarrollado para el programa de formación ALURA G8 (2025), orientado a identificar patrones de cancelación de clientes en una empresa de telecomunicaciones.  

https://drive.google.com/drive/folders/1bmZem_erWEUn_E1Kq8Bsj9Cu1vr1QRsU?usp=sharing

## 📁 Estructura del proyecto

- `TelecomX_Data.json`: dataset original provisto.
- `notebooks/`: análisis exploratorio, visualizaciones y limpieza de datos.
- `df_limpio.csv`: dataset limpio resultante (opcional si lo exportás).
- `visualizaciones/`: gráficos generados.
- `README.md`: este archivo.
## 🛠️ Tecnologías utilizadas

- Python (pandas, seaborn, matplotlib, plotly)
- Google Colab
- Análisis exploratorio de datos
- Visualización de datos
- Limpieza avanzada de datos

📄Informe

Conclusiones Relevantes del Análisis
1. Los clientes que cancelan tienen patrones distintos
Suelen tener menos meses contratados, lo que sugiere una cancelación temprana.

Tienden a tener cobros mensuales más altos, lo que puede reflejar una sensibilidad al precio.

En algunos casos, tienen Gasto_Total bajo por baja permanencia, pero Cobro_Mensual elevado por costo percibido alto en poco tiempo.

2. El gasto mensual y diario se relacionan con el abandono
clientes con mayor gasto diario, muestran una leve mayor propensión al churn.

Esto sugiere que una percepción de alto costo diario puede incidir en la decisión de cancelar, especialmente si no hay permanencia larga.

3. El tipo de contrato es un factor determinante contratos "Month-to-month" presentan una tasa de cancelación significativamente más alta.
Este grupo debe ser analizado o tratado como "de riesgo".

4. Distribuciones numéricas muestran insights valiosos,
Gasto_Total tiene una amplia dispersión: algunos clientes con montos muy altos (leales), otros con montos bajos (nuevos o recién cancelados).

Cobro Mensual tiende a concentrarse en rangos medios-altos, pero con outliers.

Meses contratados tiene acumulación en valores bajos y en máximos, indicando dos perfiles: clientes nuevos vs clientes fieles.

5. Transformaciones y limpieza fueron críticas, el tratamiento de nulos,
blancos y el renombrado de columnas fue clave para hacer el dataset interpretable y apto para análisis visual.

6. A considerar, que los valores vacios como clientes_cancelados = No,
fueron interpretados en base a que los contratos son mes a mes, por lo que en el momento del analisis, talvez no estaban activos en el momento y alternan su actividad mes a mes segun sus necesidades. Detectar y conservar registros incompletos pero valiosos (como contratos mes a mes con blancos) fue una buena decisión de negocio.

7. A futuro, propongo analizar el Metodo_Pago
(electronic check vs automático) como otra posible causa de churn.
