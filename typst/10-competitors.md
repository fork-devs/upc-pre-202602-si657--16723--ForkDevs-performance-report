# Capítulo II: Requirements & Analysis

## 2.1. Competidores

En esta sección se identifican, analizan y comparan las principales soluciones existentes en el mercado frente a nuestra propuesta de valor **DriveOS**. Este estudio comparativo permite evaluar las fortalezas, debilidades y modelos operativos de los competidores actuales, con el objetivo de identificar oportunidades estratégicas y ventajas competitivas que permitan resolver eficientemente las necesidades de nuestros segmentos objetivo.

```{=typst}
#set page(
  paper: "a4",
  flipped: true,
  margin: (x: 1.5cm, top: 1.8cm, bottom: 1.8cm)
)

#set text(size: 8.5pt)
#set par(leading: 0.5em, spacing: 0.8em)

=== 2.1.1. Análisis Competitivo

#v(0.5em)
#table(
  columns: (70pt, 85pt, 1fr, 1fr, 1fr, 1fr),
  align: (center + horizon, left + horizon, left + top, left + top, left + top, left + top),
  stroke: 0.4pt + rgb("#cbd5e1"),
  fill: (x, y) => if y == 0 { rgb("#1e3a8a") } else if calc.even(y) { rgb("#f8fafc") } else { rgb("#ffffff") },
  inset: (x: 6pt, y: 6pt),

  // Encabezado
  table.cell(colspan: 2)[#text(fill: white, weight: "bold")[Competidor]],
  align(center)[#image("assets/logo-driveos.jpg", width: 65pt)],
  align(center)[#image("assets/logo-mi-taller.png", width: 65pt)],
  align(center)[#image("assets/logo-ok-car.png", width: 65pt)],
  align(center)[#image("assets/logo-taller-gp.png", width: 65pt)],

  // Perfil - Overview
  table.cell(rowspan: 2)[*Perfil*],
  [*Overview*],
  [ForkDevs es una startup tecnológica peruana originada en la Universidad Peruana de Ciencias Aplicadas (UPC) en 2026, dedicada a profesionalizar y digitalizar el mantenimiento automotriz mediante datos, transparencia y rentabilidad operativa. Nuestro producto estrella *DriveOS* es un ecosistema digital integral (web + móvil + hardware) diseñado para cambiar el paradigma del mantenimiento vehicular de reactivo a predictivo con SUNAT nativo.],
  [Startup peruana fundada en 2022 en Lima, especializada en digitalizar talleres mecánicos independientes. Resuelve el caos administrativo (papel, Excel, mensajería desordenada) centralizando órdenes de trabajo, inventario y caja en una sola plataforma en la nube.],
  [Startup mexicana fundada en 2019, líder en Latam con presencia en 6 países (México, Colombia, Perú, Chile, Argentina, Ecuador). Digitaliza talleres medianos y grandes, eliminando el papel y centralizando la operación completa (administrativa + comercial).],
  [Empresa española fundada en 2008 en Valencia, con +15 años de trayectoria. ERP robusto para cadenas de talleres y grandes operadores. Resuelve la complejidad administrativa de multi-sucursales con consolidado financiero y control centralizado.],

  // Perfil - Ventaja Competitiva
  [*Ventaja Competitiva*],
  [Somos la única solución en Perú que combina un ERP/MRO multi-tenant con *ingesta telemática IoT hardware-agnostic* (compatible con cualquier escáner OBD2) para lectura en tiempo real de PIDs y códigos DTC. Ofrecemos facturación electrónica SUNAT nativa (Régimen MYPE), control de inventario bajo principio FIFO estricto por lote, órdenes móviles con respaldo fotográfico inmutable (Direct-to-Cloud) y control de mano de obra verificado por geocerca perimetral, con el respaldo académico de la UPC.],
  [*Adaptación 100% a la realidad peruana*: facturación electrónica SUNAT nativa, alertas ilimitadas de servicio y soporte local en tiempo real (menos de 2h de respuesta). Su curva de aprendizaje es mínima (menos de 15 min de onboarding).],
  [*App móvil para clientes finales* muy pulida (historial del vehículo, citas, pagos en línea) que genera fidelización. Su módulo de "Proyección de Servicios" usa IA básica para predecir mantenimientos por historial, no por telemetría.],
  [*Escalabilidad enterprise*: soporta 50+ sucursales con roles granulares, alertas de ITV/mantenimiento preventivo y consultas a la DGT (en España). Certificación de seguridad ISO 27001, algo crítico para cadenas grandes.],

  // Perfil de Marketing - Mercado Objetivo
  table.cell(rowspan: 2)[*Perfil de\ Marketing*],
  [*Mercado Objetivo*],
  [Talleres multimarca independientes de pequeño y mediano tamaño (1 a 5 elevadores/bahías) en Lima Metropolitana y principales ciudades del Perú, que atienden vehículos particulares y ligeros (modelo 2008+ con puerto OBD2), con facturación entre S/ 8,000 y S/ 40,000 mensuales y que buscan profesionalizar sus operaciones y diferenciarse con diagnóstico telemétrico proactivo.],
  [Talleres multimarca independientes de *pequeño y mediano tamaño* en Lima Metropolitana (1–5 elevadores), que atienden vehículos particulares y motos, con facturación entre S/ 5,000 y S/ 30,000 mensuales.],
  [Talleres multimarca de *mediano y gran tamaño* (2–10 elevadores) en zonas urbanas de Latinoamérica, que facturan más de \$8,000 USD mensuales y tienen entre 5 y 20 empleados.],
  [*Cadenas de talleres* y grupos automotrices (3–50 sucursales) en España y Latinoamérica, que facturan más de €50,000 mensuales y requieren consolidado financiero y control centralizado.],

  // Perfil de Marketing - Estrategias
  [*Estrategias de Marketing*],
  [Marketing digital B2B enfocado en gestores de taller (Facebook, Instagram, LinkedIn, Google Ads), demos en vivo con escaneo telemétrico en tiempo real, alianzas estratégicas con importadoras de scanners OBD2 y repuestos, programa de prueba gratuita de 14 días y programa de referidos ("1 mes gratis por cada taller invitado"). Participación en eventos del sector automotriz y ferias de innovación de la UPC.],
  [*Marketing digital B2B*: fuerte presencia en Facebook/Instagram con casos de éxito de talleres locales (San Borja, MotoPro). Demos gratuitas por Zoom, programa de referidos (1 mes gratis por cada taller invitado) y SEO en Google para "software para taller mecánico Perú".],
  [*Estrategia híbrida*: publicidad pagada en Google Ads y Facebook, presencia en ferias automotrices (Expo Mecánica México, Automecánica Bogotá), webinars semanales y programa de embajadores (talleres que recomiendan la herramienta a cambio de descuentos).],
  [*Venta consultiva B2B*: participación en ferias industriales (Feria de Barcelona, Automecánica São Paulo), partnerships con consultoras de gestión automotriz, casos de estudio de cadenas exitosas. Sin publicidad masiva; enfoque en referidos y eventos del sector.],

  // Perfil de Producto - Productos y Servicios
  table.cell(rowspan: 3)[*Perfil de\ Producto*],
  [*Productos y Servicios*],
  [Ecosistema multiplataforma (Dashboard Web gerencial + App Móvil Offline-First para mecánicos en bahía + App Móvil *DriveOS* para conductores): módulo de ingesta telemática IoT (PIDs y DTCs), ERP completo (órdenes de servicio con respaldo fotográfico Direct-to-Cloud, inventario FIFO por lote, caja, agendamiento de bahías), facturación electrónica SUNAT nativa (RMT), alertas telemáticas automáticas vía app/email y medición de tiempos con validación perimetral (geocerca). Implementación rápida en menos de 48h con capacitación remota y soporte técnico local.],
  [Software web y móvil (responsive) de gestión: órdenes de servicio, inventario, caja, agenda, facturación electrónica SUNAT, alertas de servicio. *No incluye hardware OBD2*. Soporte técnico por chat de lunes a sábado (8am–8pm).],
  [Software web y app móvil (iOS/Android) para taller y cliente: órdenes de servicio, inventario, facturación (MX/CO), pasarela de pagos, módulo de lealtad, proyección de servicios. *No incluye hardware OBD2*. Soporte por chat y email (lunes a viernes, 9am–6pm CDMX).],
  [ERP web (desktop-first): agenda multi-sucursal, órdenes de reparación, facturación, stock avanzado, campañas de marketing (email/SMS), integración con contabilidad externa (Sage, ContaPlus). *No incluye hardware OBD2*. Soporte por email y teléfono (lunes a viernes, 9am–6pm CET).],

  // Perfil de Producto - Precios y Costos
  [*Precios y Costos*],
  [Modelo SaaS por suscripción mensual por niveles: *Plan Básico desde S/ 149/mes* (ERP completo + órdenes de trabajo + SUNAT nativo) y *Plan Pro desde S/ 279/mes* (incluye ingesta telemática IoT OBD2 + respaldo fotográfico ilimitado + módulo FIFO avanzado). Sin costos ocultos de implementación en planes anuales. Onboarding guiado, capacitación remota y soporte local incluidos.],
  [Suscripción mensual desde *S/ 129.99* (Plan Básico) hasta *S/ 249.99* (Plan Empresarial). No hay costo de implementación (onboarding gratuito). No cobran comisión por pasarela de pagos, pero las alertas SMS premium y el módulo avanzado de reportes son add-ons de ~S/ 30/mes.],
  [Suscripción desde *\$37 USD/mes* (~S/ 140) hasta *\$97 USD/mes* (~S/ 370) según número de órdenes de trabajo. *Costo de implementación: \$150 USD* (capacitación inicial). Módulo de contabilidad avanzada es add-on de \$25 USD/mes. Sin comisiones por pasarela.],
  [*Precio no publicado* (cotización personalizada). Estimado: *€80–€200/mes* (~S/ 320–S/ 800). *Implementación: €500–€1.500* (configuración + capacitación). Módulos extra son add-ons de €30–€50/mes.],

  // Perfil de Producto - Canales de Distribución
  [*Canales de Distribución*],
  [Modelo 100% SaaS en la nube con ventas directas digitales B2B (sitio web oficial forkdevs.pe, demos por Zoom/Google Meet) y canal de venta consultiva para talleres medianos. Onboarding guiado en 24–48 horas. Alianzas estratégicas con distribuidoras de herramientas de diagnóstico y gremios automotrices locales. Soporte técnico local digital y telefónico.],
  [*100% SaaS (nube)*. El cliente se registra en mitaller.com.pe, paga con tarjeta/Yape y empieza a usarlo en menos de 15 min. Venta directa digital + demos por Zoom. Sin distribuidores físicos.],
  [*SaaS en la nube* con venta híbrida: web directa + distribuidores locales en algunos países (en Perú, venta 100% digital). Onboarding de 3 días incluido en plan Premium.],
  [*SaaS en la nube*, pero con venta consultiva (demo + cotización). Partners/distribuidores en España; en Perú, venta directa web + Zoom. Implementación de 2–4 semanas.],

  // Análisis SWOT - Fortalezas
  table.cell(rowspan: 4)[*Análisis\ SWOT*],
  [*Fortalezas*],
  [
    - *Plataforma ERP/MRO 100% peruana* con integración telemática IoT hardware-agnostic (compatible con cualquier escáner OBD2 del mercado).
    - Facturación electrónica SUNAT nativa (Régimen MYPE Tributario) integrada al cierre de órdenes.
    - Respaldo fotográfico inmutable en órdenes móviles (Direct-to-Cloud) para blindaje contra reclamos.
    - Valorización de inventario contable bajo principio FIFO estricto por lote de compra.
    - Interfaces adaptadas por rol: Dashboard Web gerencial + App Móvil Offline-First para mecánicos en bahía.
    - Respaldo institucional y académico de estudiantes de Ingeniería de Software de la UPC.
  ],
  [
    - *Marca 100% peruana* con soporte local en tiempo real (respuesta en menos de 2h).
    - Facturación electrónica SUNAT 100% integrada y actualizada.
    - +80 talleres activos en Lima (casos de éxito visibles: San Borja, MotoPro).
    - Interfaz muy intuitiva para dueños no técnicos.
  ],
  [
    - *Presencia en 6 países* (economías de escala).
    - App móvil muy pulida para clientes (historial, citas, pagos).
    - Módulo de "Proyección de Servicios" (predictivo básico por historial).
    - Capacitación ilimitada incluida en todos los planes.
  ],
  [
    - *ERP enterprise-grade* (escalable a 50+ sucursales).
    - Alertas de ITV/Mantenimiento preventivo (por tiempo/km).
    - Integración con contadores externos (Sage, ContaPlus).
    - +15 años en el mercado (trayectoria sólida).
  ],

  // Análisis SWOT - Debilidades
  [*Debilidades*],
  [
    - Startup en etapa inicial sin una base masiva de usuarios activos aún.
    - Presupuesto de marketing inicial más acotado en comparación con competidores internacionales (OK CAR, Taller GP).
    - Requiere un proceso inicial de capacitación para adaptar el hábito operativo de los mecánicos al uso de la app móvil en bahía.
  ],
  [
    - *Cero integración con hardware OBD2* (no hacen diagnóstico predictivo, solo recordatorios manuales).
    - Módulo de contabilidad básico (no genera asientos automáticos).
    - No tiene app nativa móvil (solo web responsive).
    - Sin IA para ayudar en diagnósticos.
  ],
  [
    - *Sin integración OBD2* (el predictivo es por kilometraje/tiempo, no por telemetría).
    - Facturación electrónica *no adaptada a SUNAT* (solo México/Colombia).
    - Soporte en español pero desde México (huso horario -6, lento para urgencias peruanas).
    - Interfaz sobrecargada para talleres pequeños.
  ],
  [
    - *Enfoque 100% administrativo* (cero diagnóstico técnico).
    - *Precio alto* para talleres independientes peruanos (pyme).
    - Sin facturación electrónica SUNAT.
    - Implementación lenta (semanas vs. minutos).
  ],

  // Análisis SWOT - Oportunidades
  [*Oportunidades*],
  [
    - Crecimiento acelerado del parque automotor en Perú con puerto OBD2 accesible (vehículos post-2008).
    - Demanda creciente de digitalización y formalización tributaria (SUNAT) en talleres Pyme independientes.
    - Posibilidad de alianzas con aseguradoras y empresas de flotas (taxis, logística) para monitoreo preventivo telemétrico.
    - Acceso a fondos de innovación y aceleradoras tecnológicas (Innóvate Perú, StartUP Perú, UPC Launchpad).
  ],
  [
    - Crecimiento de vehículos híbridos/eléctricos en Lima (requieren nuevos flujos de trabajo).
    - Adopción masiva de Yape/Plin en talleres pequeños.
    - Alianzas con aseguradoras para talleres certificados.
  ],
  [
    - Expandir a talleres de cadena (multi-sucursal) en Perú.
    - Integrar pasarelas locales (Yape, Plin, Niubiz).
    - Alianzas con importadoras de scanners OBD2 (para competir contigo).
  ],
  [
    - Crecimiento de cadenas de talleres en Lima (AutoFast, Speedy).
    - Demanda de ERPs multi-sucursal con consolidado financiero.
    - Alianzas con aseguradoras para talleres de red.
  ],

  // Análisis SWOT - Amenazas
  [*Amenazas*],
  [
    - Competidores regionales o locales (Mi Taller CRM, OK CAR) que adopten módulos telemétricos o bajen precios agresivamente.
    - Cambios imprevistos en las normativas tributarias o APIs de SUNAT que requieran refactorización técnica rápida.
    - Resistencia cultural al cambio por parte de dueños de talleres tradicionales acostumbrados a registros en papel o Excel.
  ],
  [
    - *Entrada de DriveOS con OBD2 + SUNAT nativo* (propuesta de valor superior).
    - Cambios bruscos en normativa SUNAT (ej. nueva versión de facturación electrónica).
    - Competidores internacionales (OK CAR, Bujia) bajando precios para ganar share.
  ],
  [
    - *ForkDevs con ingesta telemática IoT + SUNAT nativo*.
    - Fortalecimiento de competidores locales (Mi Taller) con mejor adaptación tributaria.
    - Devaluación del sol que encarezca su suscripción en USD.
  ],
  [
    - *ForkDevs con modelo más ágil y adaptado* para el 90% del mercado peruano.
    - Competidores locales (Mi Taller) escalando a multi-sucursal.
    - Brecha horaria (España -6h) que dificulta soporte en tiempo real.
  ]
)

#pagebreak()
#set page(
  paper: "a4",
  flipped: false,
  margin: (x: 2.5cm, top: 2.8cm, bottom: 2.5cm)
)
```


### 2.1.2. Estrategias y Tácticas frente a Competidores

```{=typst}
#v(0.5em)
#table(
  columns: (90pt, 1fr, 1fr, 1fr),
  align: (center + horizon, left + top, left + top, left + top),
  stroke: 0.4pt + rgb("#cbd5e1"),
  fill: (x, y) => if y == 0 { rgb("#1e3a8a") } else if calc.even(y) { rgb("#f8fafc") } else { rgb("#ffffff") },
  inset: (x: 8pt, y: 7pt),

  // Encabezado
  [#text(fill: white, weight: "bold")[Competidores]],
  [#text(fill: white, weight: "bold")[Táctica diferenciadora]],
  [#text(fill: white, weight: "bold")[Fortalezas del rival que enfrentamos]],
  [#text(fill: white, weight: "bold")[Debilidad del rival que aprovecharemos]],

  // Fila 1: Mi Taller CRM
  align(center + horizon)[#image("assets/logo-mi-taller.png", width: 75pt)],
  [Ellos se posicionan como *la opción 100% peruana y la más fácil de usar*: "En 15 minutos tu taller está digitalizado". Su gancho es la *inmediatez* (sin implementación larga) y el *soporte local en tiempo real* que responde en menos de 2 horas, algo que los dueños de taller valoran más que cualquier funcionalidad avanzada.],
  [*Adaptación total a SUNAT y confianza local*: Llevan 4 años (2022–2026) en el mercado peruano con +80 talleres activos que son sus mejores embajadores. Su facturación electrónica nunca falla porque la actualizan con cada cambio de la SUNAT, y eso genera una *barrera de confianza* muy alta: ningún dueño quiere arriesgarse a multas por un software nuevo.],
  [*Somos técnicos, ellos solo administrativos*: Mi Taller CRM solo gestiona papeles (órdenes, facturas, inventario), pero *no se conecta al vehículo*. El mecánico sigue usando su escáner OBD2 por separado y luego escribe manualmente el diagnóstico en el sistema. *Nuestra oportunidad:* *DriveOS* elimina ese paso manual: nuestro módulo de ingesta OBD2 envía los datos directamente a la plataforma y genera la orden de trabajo automática. Les ganamos en *velocidad de diagnóstico* y *prevención real de fallas*.],

  // Fila 2: OK CAR
  align(center + horizon)[#image("assets/logo-ok-car.png", width: 75pt)],
  [Ellos se venden como *la plataforma más completa para crecer*: "Lleva tu taller a otro nivel". Su gancho es la *app móvil para clientes finales* (el conductor puede ver el historial, agendar citas y pagar desde su celular), lo que los talleres usan como herramienta de fidelización. También destacan su módulo de "Proyección de Servicios" que sugiere mantenimientos futuros basados en historial.],
  [*Presencia regional y app pulida*: Operan en 6 países con miles de talleres, lo que les da economías de escala para invertir en una app móvil muy bien diseñada y en capacitación continua (webinars, academia en línea). Su efecto red es fuerte: los talleres que ya usan OK CAR atraen a otros por la app del cliente, que se ve "profesional" y moderna.],
  [*Su "predictivo" es falso, el nuestro es real*: La "Proyección de Servicios" de OK CAR solo dice "le toca cambio de aceite en 3 meses" basado en la última visita, *no lee datos reales del auto*. Además, *no tienen facturación electrónica para SUNAT* (solo México/Colombia), lo que obliga a los talleres peruanos a usar un sistema paralelo para facturar. *Nuestra oportunidad:* *DriveOS* ofrece predictivo real (lee sensores en vivo) + SUNAT nativo. Les ganamos en *tecnología de diagnóstico* y *cumplimiento tributario todo-en-uno*.],

  // Fila 3: Taller GP
  align(center + horizon)[#image("assets/logo-taller-gp.png", width: 75pt)],
  [Ellos se venden como *el ERP enterprise para cadenas que quieren control total*: "Gestiona 50 talleres como si fuera uno solo". Su gancho es la *escalabilidad y el consolidado financiero*: roles granulares, permisos por sucursal, reportes consolidados y conexión con contadores externos (Sage, ContaPlus). Apuntan a grupos automotrices, no a talleres independientes.],
  [*Trayectoria de 15+ años y robustez*: Llevan desde 2008 en el mercado, con certificación ISO 27001 de seguridad y clientes enterprise (cadenas de 20 - 50 sucursales). Su sistema es extremadamente estable y seguro, lo que da confianza a grandes inversionistas. Nadie los vence en *control multi-sucursal*.],
  [*Son lentos, caros y nosotros ágiles, baratos y predictivos*: Su implementación toma 2 - 4 semanas y cuesta €500 - €1.500, algo impensable para un taller independiente peruano. Además, *no hacen diagnóstico técnico* (solo agenda, factura y controla stock) y *no tienen SUNAT*. *Nuestra oportunidad:* *DriveOS* se implementa en minutos, cuesta 5 - 10 veces menos y ofrece diagnóstico predictivo con OBD2. Les ganamos en *agilidad, precio y tecnología de diagnóstico* para el 90% del mercado (talleres independientes) que ellos ignoran.]
)
```
