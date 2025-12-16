# ecommerce-customer-analysis-powerbi
Análisis del comportamiento y la fidelidad de clientes en un e-commerce utilizando Power BI, con foco en la dependencia de ingresos, detección de riesgos y apoyo a la toma de decisiones.

🔍 Resumen del Proyecto
Este caso analiza el comportamiento de clientes en un ecommerce para identificar:
qué segmento aporta mayor valor,


cuántos clientes están en riesgo de abandono,


qué patrones definen a los clientes fieles,


y qué decisiones pueden mejorar la retención y los ingresos.


El objetivo principal fue diseñar un dashboard capaz de responder las preguntas clave del negocio en pocos segundos, sin necesidad de interpretación técnica.

Objetivos del Análisis
Medir el nivel de dependencia del negocio respecto a clientes fieles.


Detectar clientes valiosos que muestran señales de abandono.


Identificar patrones de recencia, frecuencia y valor.


Proponer acciones concretas para mejorar retención y ventas.



Preguntas Clave
Fidelidad:
¿Cómo definimos a un cliente “fiel” en este modelo?


¿Qué porcentaje de las ventas depende realmente de los clientes fieles?


¿Cómo se comportan los clientes de mayor valor comparado con el resto?


¿Qué segmento tiene más potencial de crecimiento?


¿Qué pasaría si el top 10% de clientes deja de comprar mañana?
SALUD DE LA BASE
¿Cómo evoluciona la base total de clientes mes a mes?

¿Cómo cambian las tasas de adquisición, retención y recurrencia?

¿Qué parte del crecimiento depende de nuevos clientes vs repetidores?

ESTRATEGIA COMERCIAL
¿Dónde conviene invertir para aumentar ingresos o evitar pérdidas?

¿Qué canales o productos generan clientes de mayor calidad?

¿Qué iniciativas aumentan la repetición de compra?

RIESGO Y FUTURO
¿Cuántos clientes están en riesgo de irse?


¿Qué patrones anticipan abandono antes de que suceda?


¿Qué señales de comportamiento permiten detectar churn temprano?


¿Qué segmentos muestran una caída en su actividad reciente?



Hipótesis Iniciales
Una pequeña proporción de clientes genera la mayoría de los ingresos.


Los clientes fieles poseen patrones claros de frecuencia y recencia.


El abandono puede anticiparse observando cambios de comportamiento.


La falta de segmentación dificulta acciones de retención efectivas.



 Datos Utilizados
Fuentes principales:
Tabla de pedidos (monto, fecha, cliente).


Tabla de clientes (ID, historial).


KPIs generados:
Ingresos por tipo de cliente.


Ticket promedio.


Recencia y frecuencia.


Segmentos de fidelidad (nuevo, recurrente, fiel, en riesgo).


% de ingresos según segmento.


Variación de compras en el tiempo.



Modelo de Datos
El modelo sigue un esquema estrella simple, con el objetivo de permitir:
segmentaciones rápidas,


medidas DAX consistentes,


análisis limpio sin ambigüedades.


Estructura:
FactOrders


ID pedido


ID cliente


Fecha


Monto


Cantidad


DimCustomers


ID cliente


Información histórica


Segmentos generados por DAX


DimDate


Calendario completo


Jerarquías de tiempo


Razonamiento:
 Una estrella simple facilita cálculos de fidelidad (RFM) y comparaciones entre segmentos, evitando relaciones complejas o bidireccionales innecesarias.

Metodología y Métricas
Segmentación RFM simplificada


Recencia → última compra.


Frecuencia → nº de compras.


Valor → monto acumulado.


Categorización de clientes


Recurrente


Fiel


Super Fiel


Medidas DAX principales (ejemplos):


Diseño del Dashboard

El dashboard fue diseñado para responder en segundos:
“¿Estamos ganando o perdiendo con nuestros clientes fieles?”
Principios de diseño:
Jerarquía visual clara (salud general, segmentación, riesgo, oportunidad).



 Insights Principales
 
1. Dependencia de unos pocos clientes 
El 15% de los clientes aporta el 60% de los ingresos.
Este nivel de dependencia hace al negocio vulnerable: si esos clientes se van, el negocio cae.


2. Recurrencia marcada

La mayoría de los clientes leales vuelve a comprar dentro de los 60 días, definiendo una ventana clara de retención.


3.Existen clientes en riesgo

Se detectó un grupo de clientes con ticket 
promedio alto que:

Compraban varias veces
- Llevaban mucho tiempo sin hacerlo
Muestran señales de enfriamiento

4. Patrones de fidelidad

Los códigos de descuento no impulsan las compras repetidas: los clientes fieles compran de forma constante incluso sin incentivos.


5. Canal estrella

El sitio web es el canal más fuerte para el volumen de clientes fieles, superando a otros canales de adquisición.

6. Caminamos a ciegas

El negocio detecta tarde a los clientes valiosos que se están enfriando.

No es solo que haya clientes en riesgo, sino que el sistema actual no los detecta a tiempo.


7.Riesgo en fieles

Una gran proporción de clientes fieles está actualmente inactiva, representando $13.8M en ingresos en riesgo.

8. Aun así hay estabilidad

Los clientes fieles aportan estabilidad al negocio: sus ingresos se mantienen constantes incluso cuando las ventas totales fluctúan.







🧭 Recomendaciones
1- Proteger ingresos en los primeros 60 días
Priorizar acciones de retención durante los primeros 60 días del cliente para reducir el abandono temprano y proteger los ingresos recurrentes
2- Reducir la dependencia de descuentos en clientes fieles

Migrar de descuentos generalizados a mensajes basados en valor (beneficios, reconocimiento, experiencia) para clientes fieles.
3- Invertir en los canales que generan clientes de mayor calidad

Reforzar el marketing y el onboarding digital, ya que los clientes de mayor valor provienen principalmente del canal web.

4- Reactivar compradores fieles inactivos

Implementar activadores de re-engagement (emails, recordatorios, alertas de recompra) para clientes fieles que redujeron su actividad.

5- Monitorear el segmento en riesgo de forma continua

Establecer un seguimiento mensual del segmento en riesgo para anticipar la pérdida de fidelidad y evitar caídas de ingresos.
6-Fidelización basada en niveles y reconocimiento

Crear un sistema de niveles para clientes fieles, ofreciendo reconocimiento y beneficios progresivos para aumentar su valor en el tiempo.
7-
Mejorar la previsión de ingresos con foco en clientes fieles

Modelar la previsión de ingresos en función del comportamiento de clientes fieles, no solo del volumen total de clientes
8-Detectar caídas de frecuencia antes del abandono

Activar alertas mensuales para identificar caídas en la frecuencia de compra y actuar antes de que el cliente deje de comprar.
9-
Campañas segmentadas según etapa del cliente
Diseñar campañas diferenciadas para:
nuevos clientes (activación),
clientes fieles (valor),
clientes en riesgo (retención).





Impacto Potencial
1- Detección temprana de clientes en riesgo

Permite identificar señales de abandono antes de que el cliente deje de comprar.
Esto habilita acciones preventivas de retención, evitando la pérdida silenciosa de ingresos clave.
2- Mayor estabilidad en los ingresos
Al proteger y reactivar a los clientes fieles, los ingresos se vuelven más predecibles mes a mes.
El negocio reduce la volatilidad y deja de depender exclusivamente de picos de adquisición.
3- Estrategia comercial
Las acciones comerciales dejan de ser genéricas y se enfocan según el tipo de cliente y su momento.
Esto permite priorizar esfuerzos, reducir descuentos innecesarios y comunicar valor de forma más efectiva.

4- Riesgo y futuro
El negocio gana visibilidad sobre su nivel real de dependencia y los riesgos a mediano plazo.
Con esta información, es posible planificar crecimiento y retención con menos incertidumbre.

