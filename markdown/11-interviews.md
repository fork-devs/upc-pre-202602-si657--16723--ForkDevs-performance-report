## 2.2. Entrevistas

En esta sección se detalla el diseño metodológico de las guías de entrevista estructuradas por bloques temáticos, dirigidas a validar las necesidades, fricciones operativas y la disposición de adopción tecnológica de los dos segmentos de clientes B2B definidos en el proyecto.

### 2.2.1. Diseño de Entrevistas

#### Matriz de Alineación del Diseño de Entrevistas

**Segmento 1: Personal de Gestión y Propietarios del Taller (Decisores B2B)**

| Bloque Temático | Objetivo de Investigación | Artefacto / Módulo Impactado |
| :--- | :--- | :--- |
| **Bloque 1: Datos Demográficos** | Caracterizar el perfil del decisor y contexto operativo del taller. | User Persona (Gestor B2B) |
| **Bloque 2: Operatividad y Cuellos de Botella** | Identificar fricciones y tiempos muertos en la gestión de órdenes. | As-Is Scenario Mapping |
| **Bloque 3: Inventario y Finanzas** | Evaluar pérdidas por descontrol de stock y costeo empírico vs FIFO. | Módulo FIFO & Rentabilidad |
| **Bloque 4: Facturación y SUNAT** | Analizar el nivel de formalización tributaria y tiempos de liquidación. | Facturación SUNAT Nativa |
| **Bloque 5: Telemetría y Adopción** | Validar la disposición de pago por diagnóstico predictivo IoT OBD2. | Ecosistema SaaS Proactivo |

**Segmento 2: Personal Operativo del Taller (Técnicos Mecánicos en Bahía)**

| Bloque Temático | Objetivo de Investigación | Artefacto / Módulo Impactado |
| :--- | :--- | :--- |
| **Bloque 1: Perfil Técnico** | Identificar nivel de alfabetización digital y uso de smartphones. | User Persona (Técnico B2B) |
| **Bloque 2: Recepción y Diagnóstico** | Evaluar el tiempo de diagnóstico e interpretación de códigos DTC. | Ingesta Telemática PIDs/DTCs |
| **Bloque 3: Trazabilidad y Evidencia** | Identificar vulnerabilidad ante disputas por daños preexistentes. | Respaldo Fotográfico Direct-to-Cloud |
| **Bloque 4: Conectividad y Entorno** | Evaluar la necesidad de funcionamiento continuo sin internet. | Arquitectura Offline-First |
| **Bloque 5: Tiempos e Incentivos** | Medir la transparencia en la remuneración por productividad. | Control por Geocerca |

---

#### Guía de Entrevistas — Segmento 1: Personal de Gestión y Propietarios del Taller (Decisores B2B)

**Objetivo General:** Identificar cómo gestionan administrativamente el taller, los métodos de control de inventario y costeo de repuestos, las dificultades de facturación/formalización tributaria ante SUNAT y su disposición a adoptar un modelo de mantenimiento predictivo vía telemetría.

**Bloque 1: Datos Demográficos y Contexto del Negocio**
1. ¿Cuál es su nombre, edad y cargo dentro del taller?
2. ¿Cuántos años lleva operando el taller y cuántas bahías/elevadores y personal técnico tiene a su cargo?
3. ¿Cuál es el promedio mensual de vehículos que ingresan y qué tipo de clientes atienden mayoritariamente (particulares, flotas comerciales, empresas)?
4. ¿Qué herramientas o software utiliza actualmente para administrar el negocio (cuadernos físicos, Excel, ERP, WhatsApp, otro)?

**Bloque 2: Operatividad Diaria y Cuellos de Botella**
5. ¿Cómo es el proceso desde que un cliente llega al taller hasta que se aprueba y finaliza una orden de trabajo?
6. ¿Cuáles son los principales motivos de retraso en la entrega de vehículos y cómo maneja las quejas de clientes por tiempos no cumplidos?
7. ¿Cómo realiza la asignación de vehículos y el control de la carga de trabajo entre sus técnicos mecánicos?

**Bloque 3: Control de Inventario, Costeo y Finanzas**
8. ¿Cómo registra y valoriza el stock de repuestos e insumos en su almacén? ¿Aplica algún método formal de costeo (como FIFO) o un cálculo empírico?
9. ¿Ha experimentado pérdidas económicas por descontrol de stock, mermas o repuestos utilizados cuyo costo real no fue cobrado al cliente? ¿Con qué frecuencia ocurre?
10. ¿Cómo calcula el margen de ganancia neto real de cada servicio prestado considerando el costo exacto del repuesto y la mano de obra?

**Bloque 4: Facturación, Formalización y Relación con el Cliente**
11. ¿Cómo maneja la emisión de comprobantes de pago electrónicos ante la SUNAT y cuánto tiempo le toma liquidar una orden de trabajo?
12. ¿Qué porcentaje de sus clientes regresa de forma periódica para mantenimientos preventivos frente a los que solo acuden cuando el vehículo ya presenta una avería grave?
13. ¿Qué canales utiliza para comunicarse con sus clientes y cómo les notifica el presupuesto o el avance de la reparación?

**Bloque 5: Telemetría, Innovación y Adopción Tecnológica**
14. ¿Conoce o ha evaluado la posibilidad de monitorear de forma remota el estado mecánico del vehículo de sus clientes mediante dispositivos OBD-II?
15. Si existiera una plataforma en la nube que le permita anticipar fallas mecánicas de sus clientes antes de que ocurran, controlar su inventario bajo FIFO y facturar electrónicamente en menos de 2 minutos, ¿qué valor le aportaría a su taller y qué le preocuparía respecto a su costo o curva de aprendizaje?

---

#### Guía de Entrevistas — Segmento 2: Personal Operativo del Taller (Técnicos Mecánicos en Bahía)

**Objetivo General:** Explorar el flujo de inspección y diagnóstico vehicular, las fricciones al interactuar con órdenes de trabajo físicas, la vulnerabilidad ante reclamos por daños preexistentes y la necesidad de una herramienta móvil ágil con soporte *Offline-First*.

**Bloque 1: Datos Demográficos y Perfil Técnico**
1. ¿Cuál es su nombre, edad y cuántos años de experiencia tiene trabajando en mecánica automotriz?
2. ¿Cuenta con formación técnica superior (Senati, Tecsup, etc.) o su aprendizaje ha sido empírico?
3. ¿Qué tipo de dispositivo móvil utiliza diariamente en el taller (sistema operativo, tamaño de pantalla, uso con guantes o manos con grasa)?

**Bloque 2: Proceso de Recepción, Diagnóstico y Escaneo**
4. Cuando ingresa un vehículo a su bahía de trabajo, ¿cuál es el procedimiento que sigue para realizar el diagnóstico preliminar?
5. ¿Utiliza escáneres automotrices OBD-II multimarca en su trabajo diario? ¿Qué marcas o modelos suele emplear y qué dificultades encuentra al interpretar códigos DTC o parámetros en vivo?
6. ¿Cuánto tiempo le toma en promedio identificar la causa raíz de una avería y plasmar el diagnóstico en la orden de servicio?

**Bloque 3: Trazabilidad, Evidencia y Disputas con Clientes**
7. Al recibir un vehículo, ¿cómo registra el estado estético inicial (rayones, golpes, pertenencias en el auto)? ¿Se utiliza registro fotográfico o formatos en papel?
8. ¿Alguna vez ha tenido reclamos injustificados por parte de clientes acusándolo de haber dañado una pieza o de no haber realizado un reemplazo? ¿Cómo se defendió frente a esa situación?
9. ¿Consideraría útil contar con una aplicación móvil que permita tomar fotos inmutables del estado del auto y subirlas directamente a la orden de trabajo digital en la nube?

**Bloque 4: Conectividad y Condiciones del Entorno de Trabajo**
10. ¿En las fosas de trabajo, elevadores o áreas cerradas del taller cuenta con buena cobertura de internet Wi-Fi o datos móviles?
11. Si una aplicación móvil se quedara sin señal a mitad del registro de un diagnóstico o servicio, ¿qué impacto tendría en su ritmo de trabajo? ¿Qué tan indispensable considera que funcione sin conexión a internet (Offline-First)?
12. ¿Qué características debería tener una interfaz móvil para que no le resulte incómoda o pesada de usar mientras trabaja en el vehículo?

**Bloque 5: Gestión del Tiempo y Esquemas de Incentivos**
13. ¿Cómo registra actualmente el tiempo efectivo de mano de obra dedicado a cada reparación?
14. ¿Su remuneración incluye algún tipo de bono o incentivo basado en productividad u órdenes terminadas? ¿Considera que el sistema actual es transparente o se presta a confusiones?
15. ¿Cómo evaluaría una herramienta que mida sus tiempos reales de trabajo y le permita justificar de forma automática su productividad para bonificaciones meritocráticas?

### 2.2.2. Registro de Entrevistas

En esta sección se documenta el registro completo de las entrevistas realizadas a los representantes de nuestros segmentos objetivo, incluyendo la ficha técnica, la evidencia fotográfica y la estructuración ejecutiva del testimonio por ejes de análisis.

#### 2.2.2.1. Entrevista 1 — Kevin Ramírez Torres (Segmento 2: Personal Operativo del Taller)

| Evidencia Audiovisual | Ficha Técnica de Registro |
| :---: | :--- |
| ![Entrevista Kevin Ramírez Torres](../assets/interviews/kevin-ramirez-torres.png)<br>*Entrevista 1: Kevin Ramírez Torres* | **Nombres y Apellidos:** Kevin Ramírez Torres<br>**Segmento Objetivo:** Segmento 2: Personal Operativo del Taller (Técnicos Mecánicos)<br>**Edad / Ubicación:** 28 años \| Jesús María, Lima<br>**Cargo / Puesto:** Técnico en Mecatrónica Automotriz<br>**Formación:** Egresado de SENATI<br>**Experiencia:** 7 años en taller multimarca<br>**Entrevistador:** Barrenechea Bustamante, Rafael Andre<br>**Fecha:** 07/09/2026<br>**Tiempo / Video:** 00:00:05 – 00:11:53 ([Ver Grabación en YouTube](https://youtu.be/EuM09QvunOU)) |

**Resumen de la Entrevista**

Kevin Ramírez Torres (28 años), técnico en Mecatrónica Automotriz egresado de SENATI con 7 años de experiencia en un taller independiente multimarca, compartió información clave sobre la operatividad diaria en bahía. Destacó que utiliza diariamente un smartphone Android para comunicarse y tomar fotos, pero enfatizó que la manipulación del teléfono con guantes o manos con grasa dificulta la escritura extensa; por ello, una aplicación móvil para el técnico debe priorizar botones grandes, alto contraste y muy pocos toques.

Respecto al diagnóstico vehicular, inicia con la recepción del problema reportado, inspección visual y conexión de escáner OBD-II multimarca. Resaltó que los códigos DTC y parámetros en vivo son herramientas de orientación fundamentales, pero nunca deben sustituir el criterio profesional del técnico. La ingesta automática de códigos hacia la orden de trabajo reduciría tareas repetitivas, siempre que el mecánico conserve la responsabilidad final de confirmación.

En relación a la trazabilidad, señaló que actualmente las fotos de recepción quedan en la galería del teléfono o en WhatsApp sin asociarse formalmente a la orden de servicio. Validó la necesidad de contar con un registro fotográfico inmutable al momento del ingreso para blindar al taller ante reclamos por daños preexistentes.

Sobre conectividad, confirmó que las zonas cerradas o fosos del taller tienen cobertura inestable de Wi-Fi y datos. Ante una pérdida de señal, el técnico regresaría al papel si la app se bloquea, por lo que considera indispensable una arquitectura **Offline-First**. En cuanto a la gestión del tiempo, valoró positivamente el cronometraje de mano de obra por tarea siempre que sea transparente y respalde bonos de productividad, evitando que se perciba como vigilancia.

**Conclusiones Clave de la Entrevista**

| Aspecto Clave | Lección Aprendida para la Arquitectura de DriveOS |
| :--- | :--- |
| **UX en Bahía** | Priorizar interacción táctil simplificada y libre de tipeo extenso. |
| **Telemetría IoT** | Presentar datos telemétricos como recomendación con validación del técnico. |
| **Resiliencia Técnica** | Implementar base de datos local y sincronización asíncrona Offline-First. |
| **Blindaje Legal** | Captura fotográfica directa desde el móvil hacia la orden en la nube. |

### 2.2.3. Análisis de Entrevistas
