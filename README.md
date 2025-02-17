# Mejorar la retención de clientes en "Model Fitness"

**Descripción del Proyecto**  
Este proyecto tiene como objetivo pronosticar los factores determianntes en la pérdida de clientes del gimnasio "Model Fitness", para que posteriormente sea posible elaborar una estrategia de retención de clientes.  
Utilicé algortimos de Machine Learning para elaborar un modelo predictivo que permita estimar la cancenlación de la suscripción de sus usuarios.  

**Motivación**  
Uno de los problemas más comunes que enfrentan diferentes servicios es la pérdida de clientes. Los indicadores de abandono pueden variar de un campo a otro, sin embargo; para el caso de los gimnasios si un cliente no asiste durante un mes, es poco probable que regrese. Este proyecto busca ayudar a que la cadena de gimnasios pueda desarrollar una estrategia que logre aumentar la retención de sus clientes.  

**Características del Dataset**  

Datos del usuario del mes anterior:
- *gender*: género del usuario
- *Near_Location*: 1 si el/la usuario/a vive o trabaja en el vecindario donde se encuentra el gimnasio
- *Partner*: 1 si el/la usuario/a trabaja en una compañía asociada (el gimnasio tiene empresas asociadas cuyos empleados obtienen descuentos; en estos casos el gimnasio almacena información sobre los empleadores de los clientes)
- *Promo_friends*: 1 si el/la usuario/a originalmente se inscribió mediante una oferta "traer un amigo/a" (se utilizó un código promocional de un amigo/a cuando pagaron el primer abono)
- *Phone*: 1 si el/la usuario/a aportó el número de teléfono
- *Age*: edad del usuario
- *Lifetime*: el tiempo (meeses) desde que el/la usuario/a llegó por primera vez al gimnasio

Datos del registro de visitas, compras, y sobre el estado actual de la membresía:
- *Contract_period*: 1 mes, 3 meses, 6 meses o 1 año
- *Month_to_end_contract*: los meses faltantes para que expire el contrato
- *Group_visits*: 1 si el/la usuario/a participa en sesiones grupales
- *Avg_class_frequency_total*: frecuencia media de visitas por semana a lo largo de la vida del cliente
- *Avg_class_frequency_current_month*: frecuencia media de visitas por semana durante el mes en curso
- *Avg_additional_charges_total*: cantidad total de dienro gastado en otros servicios del gimnasio; cafetería, productos deportivos, cosméticos, masajes, etc
- *Churn*: cancelación para el mes en curso; 1 si ha cancelado la suscripción

**Herramientas utilizadas**  
Lenguaje: Python 3  
Librerias:
- Pandas para la manipulación de datos
- Matplotlib y Seaborn para visualizaciones
- Sklearn para la creaación y evaluación de modelos de Machine Learning
- Scipy; módulo cluster para el análisis de conglomerados
- Jupiter Notebook para la documentación del análisis

**Proceso del Proyecto**  

**1. Carga y Exploración de Datos**  
- Análisis inicial del dataset: revisión del tamaño del dataset, valores faltantes, duplicados y tipos de datos.
- Análisis Exploratorio de Datos (EDA): para entender las relaciones entre las variables y aquellos usuarios que cancelaron su suscripción.

**2. Limpieza y Preprocesamiento**  
- Modificación de nombres de columnas para cumplir con formato PEP8.
- No existen valores ausentes ni duplicados.

**3. Construcción del Modelo**  
- Se probaron los siguientes modelos de Machine Learning:
    - Logistic Regression
    - Random Forest
- El modelo con mejor rendimiento fue Logistic Regression.
- Además, se relizó clustering para identificar diferentes grupos de usuarios y relacionar la cancelación con las diferentes características de estos grupos.

**4. Evaluación del Modelo**  
- Se utilizó *Train/Test Split* para validar la robustez del modelo.
- Las métricas de evaluación utilzadas fueron:
    - Exactitud: 0.92
    - Precisión: 0.85
    - Recuperación: 0.83
 
**5. Resultados**  
- Se identificaron los factores que se relacionan con una mayor fidelización de los clientes; contratar un plan anual, asistir a sesiones grupales, llegar al gimnasio por un amigo o por ser de una empresa asociada.
- Se hace relevante apuntar a estas variables para generar estrategias de marketing que contribuyan a disminuir la tasa de cancelación de los clientes, algunas recomendaciones:
    - Crear un "programa de referidos" con un descuento exclusivo en el plan anual.
    - Ofreciendo beneficios exclusivos para los usuarios del plan anual (clases grupales, descuentos en productos/servicios adicionales).
    - Evaluar la experiencia del cliente (hallar factores que determinen su continuidad, posibles mejoras y cambios).
