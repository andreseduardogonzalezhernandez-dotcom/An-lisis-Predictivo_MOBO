Estrategia de Optimización de Inventarios y Predicción de Demanda - MOBO
Desarrollado por: Andrés González — Actuario & Data Analyst

Propósito del Proyecto
Este proyecto fue desarrollado como parte de la evaluación práctica para la posición de Científico de Datos. El objetivo central es transformar datos históricos de ventas (2022-2023) en una herramienta estratégica de toma de decisiones que permita a MOBO:

Reducir el capital inmovilizado mediante segmentación inteligente de inventarios.

Predecir la demanda futura con alta precisión técnica mediante modelos de aprendizaje automatizado.

Optimizar el gasto promocional basándose en la elasticidad real de los productos y segmentos de tienda.

Metodología y Ejecución
1. Análisis Exploratorio y Calidad de Datos (EDA)
Se realizó una limpieza de los datos, estandarizando tipos y tratando valores nulos. El hallazgo crítico en esta fase fue la identificación de la ubicación de la tienda como el predictor con mayor peso correlativo en el éxito de las ventas, por encima de otras variables demográficas iniciales.

2. Clasificación y Clustering de Productos y Tiendas
Clasificación de Productos (Modelo ABC): Se categorizó el catálogo para identificar los productos Clase A (Elite) que generan la mayor parte del valor, permitiendo priorizar el presupuesto de compras.

Clustering de Tiendas: Mediante algoritmos de K-Means, se agruparon las sucursales por volumen de ventas, frecuencia de transacciones y ticket promedio.

Validación: Se utilizó el Silhouette Score y el Análisis de Inercia (Método del Codo) para determinar que 4 clusters representaban la estructura óptima de negocio para MOBO.

3. Diagnóstico de Tendencias y Estacionalidad
Se identificaron los picos orgánicos de demanda relacionados con festividades como el Día de las Madres y el Buen Fin. Un descubrimiento fundamental fue la baja correlación (0.01) global entre ventas y promociones, revelando que:

Los productos Clase A (Elite) son inelásticos: el descuento no genera un aumento significativo en la demanda.

Los productos Clase C (Baja Rotación) presentan una respuesta moderada (r=0.32), siendo el segmento idóneo para aplicar estrategias promocionales de liquidación.

4. Estrategia de Predicción (XGBoost)
Se implementó una arquitectura de Extreme Gradient Boosting (XGBoost) para predecir las ventas a 30 días. El modelo integra variables transaccionales, contexto geográfico de las tiendas y factores de estacionalidad mensual.

Resultados y Evaluación del Error
Desempeño del Modelo
Precisión (R²): 78.42%

Error Medio Absoluto (MAE): Aproximadamente $3,850 MXN.

Resistencia a Outliers: El modelo demostró capacidad para seguir picos de venta de hasta $40,000 sin perder estabilidad en la predicción base.

Conclusiones Estratégicas
Surtido Regional: Es necesario ajustar el stock según el perfil del cluster de la tienda para evitar quiebres de inventario en nodos de alto flujo.

Eficiencia de Margen: Se recomienda reasignar el presupuesto de descuentos de los productos Elite hacia los productos Clase C para maximizar el retorno de inversión.

Gestión de Riesgos: El MAE calculado permite a la dirección financiera establecer niveles de stock de seguridad estandarizados, reduciendo el exceso de inventario.

Stack Tecnológico
Lenguaje: Python 3.x

Librerías: Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn.

Entorno: Jupyter Notebook / VS Code.
