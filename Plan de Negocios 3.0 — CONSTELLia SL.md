# Plan de Negocios 3.0 — CONSTELLia SL

**Versión:** 3.0 · **Fecha:** Marzo 2026  
**Clasificación:** Estratégico — Confidencial hasta lanzamiento  
**Audiencia:** Fundadores, Equipo Técnico, Aceleradoras, Inversores, Comité Ético

***

## Resumen Ejecutivo

CONSTELLia SL es una plataforma digital de **claridad emocional sistémica** que combina IA explicable (XAI), facilitadores humanos certificados y producción audiovisual personalizada para ayudar a las personas a ver sus patrones familiares y tomar decisiones vitales con mayor conciencia.

**Lo que hace único a CONSTELLia:**
- No es psicoterapia, coaching genérico ni app de meditación.
- Es un **ciclo de servicio completo** de 12–15 minutos: formulario sistémico → análisis IA → guía revisada por facilitador → vídeo personalizado.
- Opera en el espacio de **bienestar digital preventivo** (e-health), fuera del marco sanitario regulado, cumpliendo plenamente con el Plan del Ministerio de Sanidad contra pseudoterapias.[^1]

**Posición 3.0:** Con la incorporación de las APIs de Perplexity como núcleo de inteligencia (ya dispone de Perplexity Enterprise Pro activo) y WordPress + SiteGround como capa web (contrato anual vigente), el stack se simplifica y se concentra alrededor de un único motor de búsqueda, razonamiento, embeddings y orquestación de agentes.[^2][^3][^4]

**Proyección financiera:**
- Mercado digital de salud mental en España: USD 988 M en 2025 → USD 5.400 M en 2035 (CAGR 18,5%).[^5]
- Mercado wellness apps España: USD 238 M (2024) → USD 571 M (2030), CAGR 15,7%.[^6]
- Mercado corporate wellness España: USD 1.207 M (2025) → USD 2.015 M (2034), CAGR 5,9%.[^7]

***

## Capítulo 1 — Problema y Oportunidad

### 1.1 El Problema Raíz

Millones de personas conviven con bloqueos emocionales y patrones relacionales (dinero, vínculos, autoridad) que no pueden ver desde dentro del sistema en el que viven. Las alternativas actuales presentan barreras estructurales:[^8]

- **Terapia convencional:** cara (60–120 €/sesión), listas de espera, estigma, 60 minutos de profundidad no siempre necesaria.[^8]
- **Apps de wellness genéricas** (Calm, Headspace): sin contacto humano, sin resultado tangible personalizado, sin perspectiva sistémica.[^8]
- **Marketplaces médicos** (Doctolib, Teladoc): buscan profesional clínico, no claridad mental rápida.[^8]

El 47% de los consumidores prefieren sesiones de apoyo emocional basadas en IA para obtener ayuda inmediata, y más del 62% muestran mayor participación cuando las apps ofrecen contenido personalizado. Sin embargo, ninguna plataforma actual combina IA sistémica + facilitador humano + output audiovisual único por usuario.[^9]

### 1.2 Por Qué Ahora

- **Tendencia macro:** microservicios de bienestar + IA generativa como nuevo estándar de salud preventiva accesible.[^10][^8]
- **Mercado receptivo:** el e-Health es el segmento de mayor crecimiento en salud digital en España (CAGR 26,8%).[^11]
- **Tecnología lista:** APIs de búsqueda + razonamiento + embeddings + vídeo IA disponibles a bajo coste y con capacidad de producción.[^2][^8]
- **Legitimidad social:** España destinó más de 800 M€ a su Estrategia de Salud Digital; la prevención y la atención temprana son prioridad política.[^12]

***

## Capítulo 2 — Propuesta de Valor y Diferenciación

### 2.1 Beneficio Central

> **"Ver tu sistema familiar en orden, sin jerga, en 12 minutos."**[^8]

| Dimensión | Competencia Típica | CONSTELLia 3.0 |
|---|---|---|
| Modelo | App de meditación / journaling | Ciclo micro-sesión + audiovisual personalizado |
| Entrada | Genérica (tips, cursos) | Formulario sistémico estructurado (11 preguntas RSSA) |
| Motor IA | Modelo único, sin búsqueda | Perplexity Agent API (búsqueda + razonamiento + RAG) |
| Output | Contenido estático | Vídeo simbólico único por usuario |
| Validación | Sin contacto humano | Facilitador certifica cada pieza |
| Datos propios | No (queda en plataforma tercera) | Sí (100% en tu stack) |
| Coste | Alto (€50+/mes SaaS) | Bajo (€0,50–1,00/usuario automatizado) |[^8][^13][^2]

### 2.2 Los Tres Pilares Diferenciales

1. **XAI sistémica:** la IA detecta patrones narrativos con hipótesis trazables y citadas; no una caja negra.[^14]
2. **Facilitador humano como árbitro:** el humano valida el guion antes de que se genere el vídeo; la IA propone, el humano aprueba.[^1][^8]
3. **Output audiovisual único:** el usuario recibe su propia pieza visual, no un consejo genérico; esto genera identidad, retención y viralidad orgánica.[^13][^8]

***

## Capítulo 3 — Arquitectura Tecnológica 3.0

### 3.1 Stack Concentrado en Perplexity

La versión 3.0 elimina la dispersión de proveedores de IA y concentra el motor inteligente en las APIs de Perplexity, reduciendo acoplamientos frágiles y costes de integración.[^3][^4][^2]

```
┌─────────────────────────────────────────────────────┐
│ CAPA WEB / COMERCIAL (WordPress + SiteGround)       │
│  Landing · Blog · SEO · Checkout (WooCommerce/Stripe)│
│  Contrato anual vigente — mantener íntegro           │
└──────────────────────┬──────────────────────────────┘
                       │ Pago confirmado → URL formulario
┌──────────────────────▼──────────────────────────────┐
│ CAPA INTAKE (Formulario RSSA Propio)                │
│  HTML + Apps Script / Gravity Forms (en WP)         │
│  11 preguntas sistémicas → JSON al backend          │
└──────────────────────┬──────────────────────────────┘
                       │ Webhook
┌──────────────────────▼──────────────────────────────┐
│ CAPA DE INTELIGENCIA (Perplexity — Motor Central)   │
│                                                     │
│  Agent API → Análisis RSSA: clasifica, detecta      │
│              patrones, genera guía + guion           │
│  Search API → Evidencia web en tiempo real          │
│              (para soporte a facilitadores)          │
│  Embeddings API → RAG sobre corpus CONSTELLia       │
│              (protocolos, glosario, materiales)      │
└──────────────────────┬──────────────────────────────┘
                       │ Guion revisado + aprobado por facilitador
┌──────────────────────▼──────────────────────────────┐
│ CAPA AUDIOVISUAL (Satélites especializados)         │
│  DALL-E / Midjourney → imágenes simbólicas por tema │
│  Synthesia / HeyGen → vídeo avatar personalizado    │
│  SendGrid → entrega email + link al usuario         │
└──────────────────────┬──────────────────────────────┘
                       │
┌──────────────────────▼──────────────────────────────┐
│ CAPA DATOS / OPERACIÓN                              │
│  Notion / Google Drive → almacenamiento sesiones    │
│  Make / Zapier → automatizaciones y conexiones      │
│  Google Workspace → operación interna del equipo    │
└─────────────────────────────────────────────────────┘
```


### 3.2 Rol Específico de Cada API de Perplexity

**Search API — Búsqueda web en tiempo real:**
- Dentro del panel de facilitadores: botón "contrastar con evidencia" → genera resumen citado de estudios o guías sobre el patrón detectado en la sesión.[^15][^16]
- Para generación de contenido editorial (artículos, FAQs, materiales educativos) con fuentes actualizadas y citadas.[^16]

**Agent API — Orquestación de flujos RSSA:**
- Recibe las 11 respuestas del formulario sistémico.[^13]
- Ejecuta pasos: (1) clasificar tema y riesgo, (2) recuperar del RAG los protocolos aplicables, (3) enriquecer con búsqueda web si es necesario, (4) generar guion + guía estructurada, (5) preparar brief de prompts para imagen + vídeo.[^17][^4][^14]
- Actúa como backend inteligente detrás del front WordPress, respondiendo webhooks desde Make/Zapier.[^14][^17]

**Embeddings API — Base de conocimiento CONSTELLia:**
- Indexa todo el corpus propietario: protocolos sistémicos, glosario, materiales de facilitadores, casos de referencia (anonimizados).[^18]
- Permite búsqueda semántica: el facilitador escribe en lenguaje natural y recupera los fragmentos más relevantes aunque no coincidan las palabras exactas.[^18]
- Soporte para RAG ético: las respuestas de la IA solo usan el contexto interno previamente aprobado por el Comité Ético.[^1][^18]

### 3.3 Proveedores Satélite (Periféricos)

| Función | Proveedor | Alternativa |
|---|---|---|
| Imágenes simbólicas | DALL-E (OpenAI API) | Midjourney API |
| Vídeo avatar | Synthesia | HeyGen, D-ID |
| Email transaccional | SendGrid | Brevo (ex Sendinblue) |
| Automatización | Make (Integromat) | Zapier |
| Base de datos / backoffice | Notion | Airtable |
| Almacenamiento | Google Drive | AWS S3 |
| Pagos | WooCommerce + Stripe | Stripe Checkout directo |[^13][^8]

### 3.4 Estimación de Costes Tecnológicos por Ciclo de Servicio

| Componente | Coste estimado por usuario |
|---|---|
| Perplexity Agent API (análisis RSSA ~5.000 tokens) | ~0,08–0,15 USD |
| Perplexity Embeddings (RAG consultas) | ~0,001 USD |
| DALL-E imagen simbólica | ~0,04–0,08 USD |
| Synthesia vídeo 2–3 min | ~0,30–0,50 USD |
| SendGrid email | ~0,001 USD |
| Make automatizaciones | ~0,01 USD |
| **Total por usuario** | **~0,45–0,75 USD** |[^19][^13]

Esto mantiene el coste de producción bien por debajo del precio de venta (€15–25/sesión), garantizando un margen bruto superior al 95% una vez automatizado el ciclo.[^8]

***

## Capítulo 4 — Flujo de Servicio Detallado

### 4.1 El Ciclo RSSA Completo

El ciclo de servicio de CONSTELLia 3.0 sigue el principio de **pago primero, acceso después**, como principio de confirmación y filtro de usuarios comprometidos.[^20]

```
1. ATRACCIÓN
   └── Landing WP (blog, SEO, piezas educativas gratuitas)

2. PAGO (WooCommerce / Stripe)
   └── Solo usuarios que pagan acceden al formulario
   └── URL del formulario se genera tras confirmación de pago

3. FORMULARIO RSSA (11 preguntas sistémicas, 12-15 min)
   Bloque 1: Historia y relaciones familiares (5-7 min)
   Bloque 2: Simbolismos personales (3-4 min)
   Bloque 3: Narrativas y patrones (4-5 min)
   Bloque 4: Inventario personal + consentimiento (1-2 min)

4. PROCESAMIENTO IA (Perplexity Agent API, automático)
   └── RAG sobre corpus CONSTELLia (Embeddings API)
   └── Clasificación de tema (dinero/relaciones/autoridad/transformación)
   └── Detección de riesgo (protocolo SOS 3 capas si es necesario)
   └── Generación de guión sistémico + brief de imagen
   └── Búsqueda web (Search API) si se necesita evidencia externa

5. REVISIÓN HUMANA (Facilitador, 10-15 min)
   └── Checklist de 4 preguntas (sin dogmas, sin promesas, sin ruido)
   └── Aprueba o ajusta guión antes de generar vídeo

6. PRODUCCIÓN AUDIOVISUAL (automática tras aprobación)
   └── DALL-E genera imagen simbólica por tema
   └── Synthesia genera vídeo avatar (1,5-5 min según intensidad)
   └── SendGrid envía email con link al vídeo

7. ENTREGA + FEEDBACK
   └── Usuario ve su pieza única personalizada
   └── Encuesta post-vídeo (NPS + 1 pregunta de claridad)
   └── Oferta clara de siguiente paso (pack, serie, grupo)
```


### 4.2 Tipología de Piezas Audiovisuales

| Tipo | Duración | Uso | Intensidad |
|---|---|---|---|
| Píldora de Orden | 60 seg | Claridad conceptual | 1–2 |
| Visual Sistémico | 60 seg | Ver dinámicas familiares | 1–2 |
| Narrativa Personal | 2–3 min | Reconocimiento de patrón | 3 |
| Prototipo de Transformación | 3–5 min | Profundización sistémica | 4–5 |
| Mini-serie (5 episodios) | 2–3 min c/u | Exploración extendida | 3–5 |[^8]

***

## Capítulo 5 — Modelo de Negocio

### 5.1 Segmentos de Clientes

**B2C — Personas (canal principal):**
- Usuario curioso (top of funnel): accede a piezas educativas gratuitas, evalúa compra.
- Usuario comprometido (cliente activo): compra sesión o pack, recibe vídeo personalizado.
- Usuario fidelizado: suscripción comunidad, packs avanzados, mini-series.[^8]

**B2B2C — Empresas (canal de escalado):**
- RR. HH. de empresas del Campo de Gibraltar, logística, servicios, puerto: programa de bienestar laboral sistémico.
- Sello "Empresa CONSTELLia – Entorno Sistémico Saludable".[^21]

**B2B — Facilitadores (canal de licencias):**
- Escuelas sistémicas, institutos de constelaciones, coaches: licencias mensuales para usar la plataforma con sus propios clientes.[^21][^8]

### 5.2 Fuentes de Ingreso por Fase

| Fase | Fuente | Precio | Volumen estimado | Ingreso |
|---|---|---|---|---|
| **EARLY** (Meses 1–3) | Sesión 12 min + vídeo | €15–25 | 5–10/semana | €75–250/semana |
| | Pack 4 sesiones | €50–80 | 1–2/semana | €50–160/semana |
| **MID** (Meses 4–9) | Sesión individual | €20–30 | 15–20/semana | €300–600/semana |
| | Serie prototipo (5 piezas) | €50–80 | 2–3/semana | €100–240/semana |
| | Grupo sistémico | €25–40/persona | 10–15/mes | €250–600/mes |
| **SCALE** (Mes 10+) | Comunidad privada | €10–15/mes | 200–500 usuarios | €2.000–7.500/mes |
| | Licencias a facilitadores | €200–500/mes | 5–10 facilitadores | €1.000–5.000/mes |
| | Cursos educativos | €30–100 | 5–20/mes | €150–2.000/mes |
| | B2B empresas | Negociado | 2–5 empresas | €500–3.000/mes |[^8]

### 5.3 Principio Ético de Monetización

**No se cobra:**
- Contenido educativo básico (piezas de prospección gratuitas).
- Formulario de bienvenida e información básica.
- Primer feedback post-vídeo.

**Razón estratégica:** Generar confianza antes que fricción. El dinero entra cuando hay valor probado (vídeo + sesión). Este principio protege también frente a las regulaciones de publicidad engañosa (Ley 3/1991).[^1][^8]

***

## Capítulo 6 — Ecosistema de Partners Estratégicos

### 6.1 Mapa de Partners por Función

| Capa | Partner | Rol para CONSTELLia |
|---|---|---|
| Práctica sistémica | AECFS / AEBH | Red de facilitadores, código ético, sello simbólico |
| Práctica sistémica | Escuelas (La Montera, Cosmosistémica) | Pilotos, validación de lenguaje, espacios presenciales |
| Marco conceptual | IoPT (Franz Ruppert) | Lenguaje contemporáneo sobre trauma e identidad |
| Salud comunitaria | AFEMEN Algeciras | Piloto prioritario, psicoeducación sistémica familiar |
| Salud comunitaria | FAEM / Federación Salud Mental Andalucía | Escalado provincial y autonómico |
| Salud comunitaria | USMC Algeciras | Interlocutor sanitario, protocolos de derivación |
| Innovación | Andalucía Open Future (AOF) | Aceleración, mentores, visibilidad, financiación |
| Corporativo | Empresas Campo de Gibraltar | Pilotos B2B, validación modelo laboral |
| Profesionales | Facilitadores sistémicos locales | Comité asesor clínico local, primeros pilotos |[^21]

### 6.2 Prioridades de Alianzas (0–12 Meses)

1. **Mes 1–3:** Cerrar acuerdo de piloto con AFEMEN Algeciras (psicoeducación familiar) y grupo de facilitadores sistémicos locales (3–5 personas).[^21]
2. **Mes 3–6:** Presentar CONSTELLia a Andalucía Open Future con PMV funcional y primeros datos de uso y NPS.[^21]
3. **Mes 6–9:** Activar programa B2B con 1–2 empresas del entorno (logística, servicios, puerto de Algeciras).[^21]
4. **Mes 9–12:** Formalizar acuerdos con 2–3 escuelas sistémicas para integrar CONSTELLia como herramienta de preparación y seguimiento.[^21]

***

## Capítulo 7 — Marco Legal, Ético y de Gobernanza

### 7.1 Posicionamiento Legal (Fuera del Marco Sanitario)

CONSTELLia opera como **plataforma de bienestar, autoconocimiento y claridad emocional**, no como servicio sanitario, evitando el registro REGCESS y manteniéndose dentro del marco de coaching sistémico y formación emocional.[^1]

**CONSTELLia NO es:** psicoterapia · diagnóstico · prescripción · tratamiento clínico · servicio sanitario.[^1]
**CONSTELLia SÍ es:** herramienta de autoconocimiento · educación emocional · coaching sistémico · bienestar relacional preventivo.[^1]

### 7.2 Marco Regulatorio Aplicable

| Norma | Aplicación a CONSTELLia |
|---|---|
| RGPD (2016/679) | Máxima protección: datos emocionales = datos de salud (art. 4.15) |
| LOPDGDD | Implementación RGPD nacional, obligatoria |
| Ley 3/1991 Competencia Desleal | Prohibición de promesas terapéuticas falsas |
| Código Penal art. 172 | Obligación de no incitar riesgo suicida, deber de derivar |
| Plan Ministerio Sanidad vs pseudoterapias | 6 criterios cumplidos (ver §7.4) |
| DSA (2022/2065) | Moderación de contenido, transparencia, gestión de riesgos |
| LSSI-CE (34/1988) | Obligaciones de transparencia digital |[^1]

### 7.3 Protección de Datos (RGPD)

**Medidas obligatorias implementadas o en proceso:**

- TLS 1.3 en tránsito + AES-256 en reposo.
- DPO designado (interno o externo).
- DPIA (Evaluación de Impacto) completado.
- Consentimiento granular: separado para sesión, grabación, IA, marketing.
- Contratos de encargo de tratamiento (art. 28) con todos los proveedores (Perplexity, Synthesia, SendGrid, etc.).
- Auditoría GDPR anual + procedimiento de brechas (notificación AEPD en 72h).
- Autenticación multi-factor (MFA) para facilitadores.[^1]

### 7.4 Cumplimiento de los 6 Criterios del Ministerio de Sanidad

| Criterio | Cómo lo cumple CONSTELLia |
|---|---|
| Sin finalidad sanitaria | Declaración explícita "no es servicio sanitario" en T&C, landing y onboarding |
| No sustituye tratamientos eficaces | Disclaimer en cada sesión; facilitadores no recomiendan abandonar medicación/terapia |
| Información veraz y publicidad honesta | Sin claims terapéuticos ni "garantizado"; resultados descritos en términos realistas |
| Compromiso con la evidencia | Recolección de datos de NPS + claridad percibida; colaboración con universidades |
| Gestión responsable de riesgos | Protocolo SOS 3 capas (IA + facilitador + derivación 024/112) |
| Gobernanza y colaboración | Comité Ético independiente (7–9 miembros), informe anual de transparencia público |[^1]

### 7.5 Protocolo SOS — 3 Capas

- **Capa 1 (IA):** Análisis textual en tiempo real (<5 segundos); flag automático ante palabras clave de riesgo.[^1]
- **Capa 2 (Facilitador):** Evaluación clínica mini (4 preguntas); documentación en checklist.[^1]
- **Capa 3 (Usuario):** Botón SOS disponible en cualquier momento → activa protocolo inmediato, derivación a 024 / 112.[^1]

### 7.6 Gobernanza Ética

**Comité Ético Independiente (7–9 miembros):**
- Presidente/a senior salud mental (externo).
- Psicólogo/a clínico/a.
- Abogado/a RGPD + derecho sanitario.
- Bioeticista.
- Representante de usuarios (remunerado €200/reunión).
- Facilitador/a de CONSTELLia.
- CEO/Fundador (con voto, sin veto).[^1]

**Mandato:** Revisar políticas, auditar incidentes críticos (2–4 veces/año), aprobar nuevas funcionalidades con riesgo de datos, publicar informe anual de transparencia.[^1]

**Póliza de Responsabilidad Civil:**
- RC Profesional (E&O): €300.000–500.000 por persona / €1.000.000–2.000.000 agregado anual.
- Cobertura: ciberriesgo, privacidad, daño emocional.[^1]

***

## Capítulo 8 — Experiencia de Usuario y Contenido

### 8.1 Arquetipos de Usuario

| Arquetipo | Motivación | Entrada | Output Esperado |
|---|---|---|---|
| El Curioso | "¿Qué es esto? ¿Me ayudaría?" | Pieza educativa gratuita | Entiende sin jerga, considera compra |
| El Comprometido | Quiere ver su patrón sistémico | Compra sesión → formulario | Vídeo propio, claridad, próximo paso |
| El Fidelizado | Quiere profundizar | Pack, mini-serie, comunidad | Transformación narrativa progresiva |
| El Profesional | Quiere usar la herramienta con clientes | Licencia facilitador | Plataforma como extensión de su práctica |
| El Validador (inversor/aceleradora) | Evalúa el modelo | Demo + datos de uso | Confianza en escalabilidad y ética |[^8]

### 8.2 El Formulario RSSA — 11 Preguntas Sistémicas

El formulario es la entrada de datos al motor IA y la primera experiencia de valor para el usuario. Está estructurado en 4 bloques:[^13]

- **Bloque 1 — Historia y relaciones familiares (5–7 min):** familia de origen, experiencia significativa, lo no resuelto.
- **Bloque 2 — Simbolismos personales (3–4 min):** sueños recurrentes / imágenes, relato familiar repetido a lo largo de generaciones.
- **Bloque 3 — Narrativas y patrones (4–5 min):** patrón que se repite, cargas heredadas, intención de transformación.
- **Bloque 4 — Inventario personal (1–2 min):** tema principal (dinero / relaciones / autoridad / transformación), intensidad emocional (escala 1–5), consentimiento granular (4 checkboxes obligatorios).[^13]

Las variables extraídas por la IA incluyen: `family_myths`, `repeating_cycles`, `emotional_core`, `healing_theme`, `video_tone`, `recurring_symbol`, `family_key_figures`, y `primary_theme`, que alimentan directamente al agente de Perplexity y a los prompts de imagen y vídeo.[^13]

### 8.3 Contenido Educativo y Distribución

| Canal | Tipo de Contenido | Frecuencia | Objetivo |
|---|---|---|---|
| Blog WordPress | Artículos SEO sistémicos | 2/semana | Captación orgánica, autoridad |
| Instagram / Reels | Píldoras de Orden (60 seg) | 3/semana | Prospección, engagement |
| YouTube Shorts | Educativo Q&A sistémico | 2/semana | Alcance joven, educación |
| Email newsletter | Casos y reflexiones | 1/semana | Retención, comunidad |
| Comunidad privada | Contenido exclusivo + grupos | Continuo | Fidelización, upsell |[^8]

***

## Capítulo 9 — Operaciones y Equipo

### 9.1 Estructura de Facilitadores

**Requisitos de acceso:**
- Diplomado/Grado en Psicología, Trabajo Social, Pedagogía o Coaching; O certificación en Constelaciones Sistémicas (mín. 100 h).
- 2–3 años de experiencia con sistemas relacionales.
- Antecedentes penales negativos + 2 referencias profesionales.
- Formación interna complementaria: 20 h (protocolo, RGPD, riesgo, ética).[^1]

**Modelo contractual:**
- Profesional independiente (no empleado).
- Revenue share: 60% facilitador / 40% CONSTELLia.
- Código Ético CONSTELLia vinculante + RC propia.[^1]

**Supervisión:**
- Mensual: NPS usuarios ≥7,0, tasa de incidentes, velocidad de sesión.
- Trimestral: reunión 1:1, revisión de 2–3 sesiones anonimizadas.
- Anual: auditoría completa, decisión de renovación.[^1]

### 9.2 KPIs Operativos

| KPI | Meta | Acción si falla |
|---|---|---|
| Tasa de compra desde landing | ≥5–10% | Rediseñar landing / prompts educativos |
| Satisfacción con pieza (claridad) | ≥80% | Ajustar prompts o checklist del facilitador |
| Velocidad sesión → vídeo | ≤4 días | Optimizar Make / permisos Synthesia |
| Tema recurrente (foco) | ≥60% en 1–2 temas | Refinar entrevista para enfocar |
| NPS usuarios | ≥7,0 | Revisar flujo completo, facilitadores, piezas |
| Retry rate (2.º pack) | ≥5–10% | Mejorar propuesta de siguiente paso |[^8]

***

## Capítulo 10 — Fases de Desarrollo

### Fase 0 — PMV Funcional (Semanas 1–4)

**Objetivo:** Sistema end-to-end funcionando con 5–10 usuarios beta.

| Semana | Tarea | Propietario |
|---|---|---|
| 1 | Landing WordPress live + integración WooCommerce/Stripe | Tech/Fundador |
| 1 | Formulario RSSA en HTML/Gravity Forms (11 preguntas) | Tech |
| 2 | Backend ligero (Cloud Function / Make) → Perplexity Agent API | Tech |
| 2 | Corpus inicial indexado con Perplexity Embeddings (20–50 docs) | Fundador + Tech |
| 3 | Checklist de validación facilitador (4 preguntas) | Fundador |
| 3 | Prompts DALL-E (4 temas) + template Synthesia (1 genérico) | Audiovisual |
| 4 | 5 usuarios beta (amigos, conocidos) → feedback honesto | Fundador |
| 4 | Iteración de prompts, checklist y templates | Equipo |

**Entregables:** Landing live · Ciclo completo automatizado · 5 piezas testadas · Manual operativo · Corpus embeddings inicial.[^8]

### Fase 1 — Validación (Semanas 5–12)

**Objetivo:** 20 usuarios pagos. Satisfacción >60%. Viabilidad del modelo confirmada.[^8]

- Semanas 5–6: 5 compradores reales (red personal, landing, redes).
- Semanas 7–8: 10 compradores acumulados.
- Semanas 9–10: 15 compradores, primeros datos NPS.
- Semanas 11–12: 20 compradores, análisis semanal de temas recurrentes, primeras métricas de KPIs.

**Validaciones clave:**
- ¿Usuarios compran? ¿Están satisfechos (>60%)? ¿Coste < margen? ¿Tema recurrente claro?

**Checklist legal paralelo (Fases 0–1):**
- [ ] Sociedad constituida (SL/SLU), CIF asignado.
- [ ] DPO provisional designado.
- [ ] DPIA completado.
- [ ] Política de Privacidad + T&C + Código Ético de Facilitador redactados.
- [ ] Contratos de encargo de tratamiento con Perplexity, Synthesia, SendGrid.
- [ ] Póliza RC contratada.
- [ ] Comité Ético provisional convocado (3+ miembros iniciales).[^1]

### Fase 2 — Escalado (Meses 4–6)

**Objetivo:** 50–100 usuarios activos. Operación estable. Inicio de comunidad.[^8]

- Activar packs y series (retención y upsell).
- Contenido educativo regular (3–5 piezas/semana en redes).
- Segunda red social activa (YouTube Shorts o Instagram Reels).
- 1 facilitador adicional o soporte técnico parcial.
- Inicio de conversaciones con Andalucía Open Future.
- Primer acuerdo piloto con AFEMEN Algeciras o escuela sistémica.[^21]

### Fase 3 — Ecosistema (Meses 7–12)

**Objetivo:** Comunidad privada activa. Licencias a facilitadores. Programa B2B.[^8]

- Lanzamiento comunidad privada (suscripción €10–15/mes, plataforma tipo Circle o Mighty Networks).
- Programa de licencias: 5–10 facilitadores externos usando CONSTELLia.
- Cursos educativos sistémicos (€30–100).
- Presentación formal a AOF u otra aceleradora con datos reales.
- Inicio de programa B2B con 1–2 empresas del Campo de Gibraltar.
- Posible lanzamiento de app móvil si la tracción lo justifica.[^21][^8]

### Fase 4 — Internacionalización (Meses 13–24)

**Objetivo:** Expansión a Portugal, Francia, Alemania. Estudio académico publicado.[^1]

- Adaptación de contenidos y cumplimiento legal en mercados destino.
- Versión en portugués (primer mercado natural dado el contexto geográfico y lingüístico).
- Publicación de resultados de impacto en revista peer-reviewed.
- Convergencia con marco normativo europeo DSA + AI Act.[^1]

***

## Capítulo 11 — Proyecciones Financieras Orientativas

### 11.1 Estructura de Costes Recurrentes

| Concepto | Coste mensual estimado |
|---|---|
| SiteGround + WordPress (prorrateo contrato anual) | ~20–40 € |
| Perplexity Enterprise Pro (uso interno equipo) | ~40 € / asiento |
| Perplexity API (variable según volumen) | ~30–200 USD |
| Synthesia / HeyGen (vídeos) | ~50–200 USD |
| DALL-E API (imágenes) | ~10–30 USD |
| SendGrid (emails) | ~10–20 USD |
| Make / Zapier (automatizaciones) | ~10–30 USD |
| Notion / Google Workspace | ~20–40 € |
| RC Profesional (prorrateo) | ~80–150 € |
| **Total coste fijo + variable (mes 1–3)** | **~300–750 € + USD** |[^19][^3][^19]

### 11.2 Proyección de Ingresos

| Fase | Periodo | Ingresos Estimados |
|---|---|---|
| EARLY | Meses 1–3 | €150–400/semana (€600–1.600/mes) |
| MID | Meses 4–9 | €875–2.040/semana (€3.500–8.160/mes) |
| SCALE | Mes 10+ | €4.150–17.000/mes |[^8]

**Proyección objetivo Año 1:** Alcanzar breakeven operativo en mes 4–6, con ingresos mensuales de €3.000–5.000; llegar a €10.000–15.000/mes en mes 12 con comunidad + licencias activas.

### 11.3 Métricas de Éxito Financiero (Mes 3)

- [ ] Tasa de compra landing ≥5%.
- [ ] Coste de producción por usuario <€1.
- [ ] Margen bruto >90% en ciclo automatizado.
- [ ] NPS ≥7,0.[^8][^1]

***

## Capítulo 12 — Narrativa Estratégica y Posicionamiento

### 12.1 Para el Usuario

> *"CONSTELLia no es una app de meditación ni una plataforma de terapia.*  
> *Es una manera rápida y clara de VER tu sistema familiar.*  
> *En 12 minutos. Respondes unas preguntas. Un facilitador escucha.*  
> *Y genera un vídeo tuyo, donde aparecen las dinámicas invisibles que sostenías.*  
> *No es magia. Es observación sistémica hecha visible.*"*[^8]

### 12.2 Para Inversores y Aceleradoras

CONSTELLia es una **plataforma convergente de IA + bienestar sistémico** que ataca un mercado de USD 988 M en España (2025) con CAGR de 18,5% y resuelve en un ciclo automatizado de <15 minutos lo que la terapia convencional no puede hacer accesible ni rápido.[^5][^8]

- **Diferencial:** Híbrido IA + humano. Ético. Escalable. Output único (vídeo personalizado).
- **Motor tecnológico:** Perplexity API (Agent + Search + Embeddings) como núcleo de inteligencia concentrado en un único proveedor.[^4][^2]
- **PMV:** 2–4 semanas. Validación: 6 meses (20–50 usuarios pagos). Proyección: €10K–50K/mes en mes 12.[^8]
- **Barreras de entrada:** Protocolo ético sólido (Comité independiente, RGPD máximo), corpus propietario indexado (embeddings), red de facilitadores cualificados.[^1]

### 12.3 Para Partners y Facilitadores

> *"La salud mental del futuro es sistémica (ves tu familia, no solo tu 'yo'), audiovisual (ves, no solo entiendes), accesible (barata, rápida, online), ética (sin promesas, con límites claros) y escalable (IA + humano, no humano solo). CONSTELLia es el primer paso de ese futuro."*[^8]

***

## Supuestos Críticos y Riesgos

### Supuestos que Deben Ser Ciertos

1. Hay demanda real de "ver el sistema familiar de forma rápida y visual" → Validación: 5–20 usuarios pagos en mes 1.[^8]
2. Perplexity Agent API puede generar guiones sistémicos de calidad que pasen el checklist → Validación: 4/4 en checklist facilitador.[^8]
3. El ciclo sesión → vídeo se mantiene en <4 días (experiencia no frustrante) → Validación: tiempo promedio real.[^8]
4. Precio €15–25 es justo → Validación: tasa de compra >5% desde landing.[^8]
5. Facilitador puede validar 5–10 piezas/semana sin burnout → Monitorización semanal.[^8]

### Riesgos Principales y Mitigación

| Riesgo | Mitigación |
|---|---|
| Ser etiquetados como pseudoterapia | Lenguaje honesto, sin claims terapéuticos, Comité Ético, Informe de Transparencia anual |
| IA genera ruido sistémico (guión sin coherencia) | Doble capa: IA genera + facilitador valida; si >30% ruido, modo manual |
| Dependencia emocional del usuario | Texto en pieza: "El cambio ocurre en tu vida, no en el vídeo"; oferta de siguiente paso claro |
| Violación de privacidad (RGPD) | TLS 1.3 + AES-256 + DPO + DPIA + consentimiento granular + contratos proveedores |
| Facilitador negligente | Selección rigurosa, código ético vinculante, RC propia, supervisión trimestral |
| Dependencia de un proveedor IA (Perplexity) | Agent API permite orquestar modelos de terceros; plan B: migración a OpenAI/Claude si necesario |[^1][^8][^14]

***

## Checklist de Lanzamiento PMV

### Semana 1–2: Fundación Técnica
- [ ] Landing WordPress live con copy CONSTELLia 3.0.
- [ ] Formulario RSSA (11 preguntas) en WordPress/Gravity Forms.
- [ ] Integración WooCommerce + Stripe (pago antes de acceso al formulario).
- [ ] Backend ligero conectado a Perplexity Agent API.
- [ ] Primeros 20–50 documentos corpus indexados con Embeddings API.

### Semana 3–4: IA + Audiovisual
- [ ] 5 prompts del agente RSSA definidos y testados.
- [ ] Prompts DALL-E (4 temas: dinero, relaciones, autoridad, transformación).
- [ ] Template Synthesia (1 genérico, adaptable por intensidad).
- [ ] Checklist de validación facilitador (4 preguntas).
- [ ] Flujo Make/Zapier completo (formulario → agente → imagen → vídeo → email).

### Semana 5–8: Legal + Ética
- [ ] Sociedad constituida (SL/SLU), CIF, alta en Hacienda.
- [ ] DPO provisional designado.
- [ ] DPIA completado.
- [ ] Política de Privacidad + T&C + Código Ético aprobados por abogado.
- [ ] Contratos encargo tratamiento con todos los proveedores API.
- [ ] Póliza RC Profesional contratada.
- [ ] Comité Ético provisional (mínimo 3 miembros).
- [ ] Protocolo SOS documentado y testado.

### Semana 9–12: Validación
- [ ] 5 usuarios beta con feedback completo.
- [ ] Iteración de prompts y checklist.
- [ ] Primeras 20 sesiones pagas.
- [ ] Datos de NPS y claridad percibida recogidos.
- [ ] Decisión: continuar · pivotar · escalar.[^8][^1]

***

*Documento vivo. Se actualiza en cada fin de fase con datos reales de uso, NPS, hallazgos del Comité Ético y cambios regulatorios.*  
*Próxima revisión prevista: Fin de Fase 1 (semana 12 desde lanzamiento PMV).*

***
**CONSTELLia SL · Algeciras, Andalucía · Marzo 2026**

---

## References

1. [Aspectos-Legales-Etica-CONSTELLia-2026.md](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/143983445/fbcde86d-7dec-4b1a-8010-6ad7bc6e3123/Aspectos-Legales-Etica-CONSTELLia-2026.md?AWSAccessKeyId=ASIA2F3EMEYEQE67SYT2&Signature=WDq%2BswmmTOCeYU7nLsJANlQoARI%3D&x-amz-security-token=IQoJb3JpZ2luX2VjEHMaCXVzLWVhc3QtMSJHMEUCIDLwF5B3mSKKfxcyl1yHcDLFEgCcxdc7H%2F5E8yt6rwWuAiEA5XA6m1FuZpXJ9z83or6oqX0Kv2NkMs%2FaW691HL50BJ4q8wQIOxABGgw2OTk3NTMzMDk3MDUiDAa%2BEkjaNPhSDaMkYirQBAa4eUnv2hUWDvTa5raLTMvEHOduvL4ZeOo9%2Bz4man%2FLmb6Y6UuvV5v%2F0H1pFswudHoWVn2jiR2kXg%2BVD32Xd65uQec9xsDks9tGtQkviDFR9OLCrJDk2KIm%2BdgXYBXc2nL2Hy%2FIz0Uy94ks4xbBxKmD%2F8M7Iiz7JaPlvurErdMbWavobIlMdNRF9HYLvNGc6aboPkEenhCa1osQXgKOEYgFfkssJE2HsWO0nw6xCj4Ql6f90vF9Sd%2FRFZ20VtisxhiHmaTU9wn%2FsYxaRWqiP0lhJ2B70IFQscRsAdChOKTlanbs%2B9cYhqIJulKE%2BIV5%2F3kh2ZDVfyKJ5FEbDbenZx6EO0DE22CtYXDnUpF5Nm1aRC35wqp%2ByH4su7W6L%2FChyVTWgvkLSC6CH7kCRKb5ASoyEtjc5v12tRqWiwDymEtyQF2%2BCFTT%2Fm0LUD4cz522PXWT9jHEHqmcXT6GTtfv120oOFsybcqSNZ%2FBkobtF%2FMuzlzqmedyRoPIrqZEHAyC1wUm3wly8GdV%2BmozTQhmV4i6YHDb9cHUAAGcM%2By7UhMPvw0klMHn%2B525F%2Btnm6NEQT9w05V5i2qka1wd6Zc3slHvpI7GUeB5KaXUp%2Fj282jHlqazFPtN7Wv0a8jskB%2Bjr1KDsfLaIwRIBqumFm9ew7L2%2B5Ov7KvNJnB6wtKO0RGGMiG1Nza62jWaWET1yPi62wpSFHFwNf%2FR4bBDv%2BekS17gCS15Ww%2FVv6tqvHiIUZDZ6lYdHfC6YEybEqHrgAamjYXDqaNHpPMjIDn7siQunbcwvJr2zQY6mAEp9Le9xxRUHwY%2FI7KapscIuCcmZWaEEdY6iO%2Bt8SCpP5j%2BjqsMCK1OuDLWR2pG0e8fqHrJdMlRK%2FfFLDag%2FHfsBFSGkSeO5yvb1cXEzFZoYKKVAUOrXu3EX%2BkJNIYKwY6Tb4TtKzzc190RUJJ%2BlNtLuPwdoObNCDbomVgchWS8nnPXr7cIzaBQoYt4IKof%2BNwwCpZWU3Ms8Q%3D%3D&Expires=1774033679) - # ASPECTOS LEGALES Y ÉTICO-OPERATIVOS DE CONSTELLia 2026
## Documento Integral de Cumplimiento y Gob...

2. [Perplexity API Platform — AI Search & Grounded LLM APIs for ...](https://www.perplexity.ai/api-platform) - Access real-time web search results with Perplexity's Search API. Get ranked results, domain filteri...

3. [enterprise pro](https://www.perplexity.ai/search/46a87012-51bd-4407-a0d8-f92afc601476) - Parece que te refieres a Enterprise Pro de Perplexity, el plan para organizaciones (no alquiler de c...

4. [Agent API: A Managed Runtime for Agentic Workflows - Perplexity](https://www.perplexity.ai/hub/blog/agent-api-a-managed-runtime-for-agentic-workflows) - It replaces a model router, a search layer, an embeddings provider, a sandbox service, and a monitor...

5. [Spain Digital Mental Health Market Size, Growth Outlook ...](https://www.marketresearchfuture.com/reports/spain-digital-mental-health-market-43933) - Spain Digital Mental Health Market projected to grow at 18.54% CAGR, reaching USD 2.71 Billion by 20...

6. [Spain Wellness Apps Market Size & Outlook, 2025-2030](https://www.grandviewresearch.com/horizon/outlook/wellness-apps-market/spain) - The Spain wellness apps market generated a revenue of USD 238.4 million in 2024 and is expected to r...

7. [Spain Corporate Wellness Market Size, Forecast 2026-2034](https://www.imarcgroup.com/spain-corporate-wellness-market) - Spain corporate wellness market size reached USD 1207.0 Million in 2025 to reach USD 2015.4 Million ...

8. [CONSTELL-ia-Arquitectura-Sistema-PMV.docx](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/143983445/5bec6c90-c506-450e-9c33-43b28e14a30b/CONSTELL-ia-Arquitectura-Sistema-PMV.docx?AWSAccessKeyId=ASIA2F3EMEYEQE67SYT2&Signature=VA37XIzaxU22n51FLhIGIyrd0RA%3D&x-amz-security-token=IQoJb3JpZ2luX2VjEHMaCXVzLWVhc3QtMSJHMEUCIDLwF5B3mSKKfxcyl1yHcDLFEgCcxdc7H%2F5E8yt6rwWuAiEA5XA6m1FuZpXJ9z83or6oqX0Kv2NkMs%2FaW691HL50BJ4q8wQIOxABGgw2OTk3NTMzMDk3MDUiDAa%2BEkjaNPhSDaMkYirQBAa4eUnv2hUWDvTa5raLTMvEHOduvL4ZeOo9%2Bz4man%2FLmb6Y6UuvV5v%2F0H1pFswudHoWVn2jiR2kXg%2BVD32Xd65uQec9xsDks9tGtQkviDFR9OLCrJDk2KIm%2BdgXYBXc2nL2Hy%2FIz0Uy94ks4xbBxKmD%2F8M7Iiz7JaPlvurErdMbWavobIlMdNRF9HYLvNGc6aboPkEenhCa1osQXgKOEYgFfkssJE2HsWO0nw6xCj4Ql6f90vF9Sd%2FRFZ20VtisxhiHmaTU9wn%2FsYxaRWqiP0lhJ2B70IFQscRsAdChOKTlanbs%2B9cYhqIJulKE%2BIV5%2F3kh2ZDVfyKJ5FEbDbenZx6EO0DE22CtYXDnUpF5Nm1aRC35wqp%2ByH4su7W6L%2FChyVTWgvkLSC6CH7kCRKb5ASoyEtjc5v12tRqWiwDymEtyQF2%2BCFTT%2Fm0LUD4cz522PXWT9jHEHqmcXT6GTtfv120oOFsybcqSNZ%2FBkobtF%2FMuzlzqmedyRoPIrqZEHAyC1wUm3wly8GdV%2BmozTQhmV4i6YHDb9cHUAAGcM%2By7UhMPvw0klMHn%2B525F%2Btnm6NEQT9w05V5i2qka1wd6Zc3slHvpI7GUeB5KaXUp%2Fj282jHlqazFPtN7Wv0a8jskB%2Bjr1KDsfLaIwRIBqumFm9ew7L2%2B5Ov7KvNJnB6wtKO0RGGMiG1Nza62jWaWET1yPi62wpSFHFwNf%2FR4bBDv%2BekS17gCS15Ww%2FVv6tqvHiIUZDZ6lYdHfC6YEybEqHrgAamjYXDqaNHpPMjIDn7siQunbcwvJr2zQY6mAEp9Le9xxRUHwY%2FI7KapscIuCcmZWaEEdY6iO%2Bt8SCpP5j%2BjqsMCK1OuDLWR2pG0e8fqHrJdMlRK%2FfFLDag%2FHfsBFSGkSeO5yvb1cXEzFZoYKKVAUOrXu3EX%2BkJNIYKwY6Tb4TtKzzc190RUJJ%2BlNtLuPwdoObNCDbomVgchWS8nnPXr7cIzaBQoYt4IKof%2BNwwCpZWU3Ms8Q%3D%3D&Expires=1774033679) - **🏗️ CONSTELL-ia: ARQUITECTURA DE SISTEMA PMV**

**📊 Documento Estratégico**

**Versión**: 1.0\
**Fe...

9. [Tendencias del mercado de aplicaciones de salud mental](https://www.globalgrowthinsights.com/es/market-reports/mental-health-apps-market-123828) - Aproximadamente el 47% de los consumidores prefieren sesiones de terapia basadas en chat de IA para ...

10. [Tendencias en Salud y Bienestar 2026: eCommerce y ...](https://www.asendia.es/asendia-insights/tendencias-salud-bienestar-ecommerce-marketing) - Descubre cómo la tecnología, el eCommerce y la sostenibilidad están cambiando el bienestar en 2026. ...

11. [Spain Digital Health Market to 2032](https://www.databridgemarketresearch.com/nucleus/spain-digital-health-market) - The Spain Digital Health Market is expected to reach a 26.94 USD Billion by 2032 and is projected to...

12. [eHealth: un 'boom' que despega con legislación y ...](https://www.plantadoce.com/entorno/ehealth-un-boom-que-despega-con-legislacion-y-profesionales-como-frenos) - A mediados de noviembre nació en España el primer fondo europeo dedicado a la salud digital. Se trat...

13. [02_constellia-formulario-audiovisual-final.md](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/143983445/d2851592-912d-407e-878a-4c739e3cea44/02_constellia-formulario-audiovisual-final.md?AWSAccessKeyId=ASIA2F3EMEYEQE67SYT2&Signature=XUx4u4UJmgFGjcszB0Li5PFOVaE%3D&x-amz-security-token=IQoJb3JpZ2luX2VjEHMaCXVzLWVhc3QtMSJHMEUCIDLwF5B3mSKKfxcyl1yHcDLFEgCcxdc7H%2F5E8yt6rwWuAiEA5XA6m1FuZpXJ9z83or6oqX0Kv2NkMs%2FaW691HL50BJ4q8wQIOxABGgw2OTk3NTMzMDk3MDUiDAa%2BEkjaNPhSDaMkYirQBAa4eUnv2hUWDvTa5raLTMvEHOduvL4ZeOo9%2Bz4man%2FLmb6Y6UuvV5v%2F0H1pFswudHoWVn2jiR2kXg%2BVD32Xd65uQec9xsDks9tGtQkviDFR9OLCrJDk2KIm%2BdgXYBXc2nL2Hy%2FIz0Uy94ks4xbBxKmD%2F8M7Iiz7JaPlvurErdMbWavobIlMdNRF9HYLvNGc6aboPkEenhCa1osQXgKOEYgFfkssJE2HsWO0nw6xCj4Ql6f90vF9Sd%2FRFZ20VtisxhiHmaTU9wn%2FsYxaRWqiP0lhJ2B70IFQscRsAdChOKTlanbs%2B9cYhqIJulKE%2BIV5%2F3kh2ZDVfyKJ5FEbDbenZx6EO0DE22CtYXDnUpF5Nm1aRC35wqp%2ByH4su7W6L%2FChyVTWgvkLSC6CH7kCRKb5ASoyEtjc5v12tRqWiwDymEtyQF2%2BCFTT%2Fm0LUD4cz522PXWT9jHEHqmcXT6GTtfv120oOFsybcqSNZ%2FBkobtF%2FMuzlzqmedyRoPIrqZEHAyC1wUm3wly8GdV%2BmozTQhmV4i6YHDb9cHUAAGcM%2By7UhMPvw0klMHn%2B525F%2Btnm6NEQT9w05V5i2qka1wd6Zc3slHvpI7GUeB5KaXUp%2Fj282jHlqazFPtN7Wv0a8jskB%2Bjr1KDsfLaIwRIBqumFm9ew7L2%2B5Ov7KvNJnB6wtKO0RGGMiG1Nza62jWaWET1yPi62wpSFHFwNf%2FR4bBDv%2BekS17gCS15Ww%2FVv6tqvHiIUZDZ6lYdHfC6YEybEqHrgAamjYXDqaNHpPMjIDn7siQunbcwvJr2zQY6mAEp9Le9xxRUHwY%2FI7KapscIuCcmZWaEEdY6iO%2Bt8SCpP5j%2BjqsMCK1OuDLWR2pG0e8fqHrJdMlRK%2FfFLDag%2FHfsBFSGkSeO5yvb1cXEzFZoYKKVAUOrXu3EX%2BkJNIYKwY6Tb4TtKzzc190RUJJ%2BlNtLuPwdoObNCDbomVgchWS8nnPXr7cIzaBQoYt4IKof%2BNwwCpZWU3Ms8Q%3D%3D&Expires=1774033679) - # 🎬 CONSTELLIA FORMULARIO + AUDIOVISUAL PROMPTS
## VERSIÓN FINAL OPTIMIZADA PARA VIDEO GENERACIÓN
**...

14. [Perplexity AI API Access and Developer Use Cases Overview](https://www.datastudios.org/post/perplexity-ai-api-access-and-developer-use-cases-overview-platform-structure-key-capabilities-and) - Typical developer use cases span live web Q&A, enterprise research copilots, document intelligence s...

15. [Perplexity Search API](https://docs.perplexity.ai/docs/search/quickstart) - Perplexity's Search API provides developers with real-time access to ranked web search results from ...

16. [Introducing the Perplexity Search API](https://www.perplexity.ai/hub/blog/introducing-the-perplexity-search-api) - Introducing the Perplexity Search API · Providing access to the same global-scale infrastructure tha...

17. [Perplexity Agent API: Managed Runtime for AI Workflows](https://www.gend.co/blog/perplexity-agent-api-runtime) - Perplexity's Agent API is a managed runtime for building agentic workflows. It combines real-time we...

18. [Embeddings API - Perplexity](https://docs.perplexity.ai/docs/embeddings/quickstart) - Perplexity's Embeddings API generates high-quality text embeddings for semantic search and retrieval...

19. [Pricing - Perplexity](https://docs.perplexity.ai/docs/getting-started/pricing) - This page shows pricing information to help you understand API costs.For billing setup, payment meth...

20. [el pago debe ocurrir antes de empezar el formulario, yaque la tecnica RSSA debe quedar solo para aquellos que paguen, es el principio de confirmacion para que la ia mediante su algoritmo califique, filtre y emita un guien que sera revisado para luego crear una serie de imagenes que se montaran en un video personalizado.](https://www.perplexity.ai/search/3c8bfdbe-aad6-4e79-b67b-240ea83d4b6b) - Perfecto: entonces el flujo debe ser “primero pago, luego acceso a RSSA/intake”, y todo lo demás se ...

21. [Constellia-Partners.docx](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/143983445/d6d54c32-810e-4815-ab60-1e6d99f3fd97/Constellia-Partners.docx?AWSAccessKeyId=ASIA2F3EMEYEQE67SYT2&Signature=ZD%2FZZm1Fl59O23w3zolGetxhB3k%3D&x-amz-security-token=IQoJb3JpZ2luX2VjEHMaCXVzLWVhc3QtMSJHMEUCIDLwF5B3mSKKfxcyl1yHcDLFEgCcxdc7H%2F5E8yt6rwWuAiEA5XA6m1FuZpXJ9z83or6oqX0Kv2NkMs%2FaW691HL50BJ4q8wQIOxABGgw2OTk3NTMzMDk3MDUiDAa%2BEkjaNPhSDaMkYirQBAa4eUnv2hUWDvTa5raLTMvEHOduvL4ZeOo9%2Bz4man%2FLmb6Y6UuvV5v%2F0H1pFswudHoWVn2jiR2kXg%2BVD32Xd65uQec9xsDks9tGtQkviDFR9OLCrJDk2KIm%2BdgXYBXc2nL2Hy%2FIz0Uy94ks4xbBxKmD%2F8M7Iiz7JaPlvurErdMbWavobIlMdNRF9HYLvNGc6aboPkEenhCa1osQXgKOEYgFfkssJE2HsWO0nw6xCj4Ql6f90vF9Sd%2FRFZ20VtisxhiHmaTU9wn%2FsYxaRWqiP0lhJ2B70IFQscRsAdChOKTlanbs%2B9cYhqIJulKE%2BIV5%2F3kh2ZDVfyKJ5FEbDbenZx6EO0DE22CtYXDnUpF5Nm1aRC35wqp%2ByH4su7W6L%2FChyVTWgvkLSC6CH7kCRKb5ASoyEtjc5v12tRqWiwDymEtyQF2%2BCFTT%2Fm0LUD4cz522PXWT9jHEHqmcXT6GTtfv120oOFsybcqSNZ%2FBkobtF%2FMuzlzqmedyRoPIrqZEHAyC1wUm3wly8GdV%2BmozTQhmV4i6YHDb9cHUAAGcM%2By7UhMPvw0klMHn%2B525F%2Btnm6NEQT9w05V5i2qka1wd6Zc3slHvpI7GUeB5KaXUp%2Fj282jHlqazFPtN7Wv0a8jskB%2Bjr1KDsfLaIwRIBqumFm9ew7L2%2B5Ov7KvNJnB6wtKO0RGGMiG1Nza62jWaWET1yPi62wpSFHFwNf%2FR4bBDv%2BekS17gCS15Ww%2FVv6tqvHiIUZDZ6lYdHfC6YEybEqHrgAamjYXDqaNHpPMjIDn7siQunbcwvJr2zQY6mAEp9Le9xxRUHwY%2FI7KapscIuCcmZWaEEdY6iO%2Bt8SCpP5j%2BjqsMCK1OuDLWR2pG0e8fqHrJdMlRK%2FfFLDag%2FHfsBFSGkSeO5yvb1cXEzFZoYKKVAUOrXu3EX%2BkJNIYKwY6Tb4TtKzzc190RUJJ%2BlNtLuPwdoObNCDbomVgchWS8nnPXr7cIzaBQoYt4IKof%2BNwwCpZWU3Ms8Q%3D%3D&Expires=1774033679) - **CONSTELLia -- Mapa de actores, partners estratégicos y beneficios de colaboración**

**Índice**

1...

