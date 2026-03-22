# Protocolo RSSA Completo
## Corpus RAG — Categoría: 01_protocolos
**Versión:** 1.0 · Marzo 2026

---

## Qué es el proceso RSSA

RSSA son 4 fases secuenciales:

- **R — Recogida:** el usuario completa el formulario de 11 preguntas (12–15 min)
- **S — Síntesis:** el Agente IA analiza las respuestas y genera guía + guión
- **S — Supervisión:** el facilitador humano valida con el checklist de 4 preguntas
- **A — Audiovisual:** se genera el vídeo personalizado y se entrega al usuario

Ciclo completo desde pago hasta entrega: 1–4 días.

---

## FASE R — Formulario de 11 preguntas

### BLOQUE 1 — Historia y relaciones familiares

**Pregunta 1a — Familia de origen**
"¿Cómo describirías tu familia de origen? Quiénes han sido las figuras clave y qué tipo de vínculo tienes hoy con ellas."
→ Variable: input_familia_origen

**Pregunta 1b — Experiencia significativa**
"Recuerda una experiencia importante que hayas vivido con tu familia. ¿Qué ocurrió y qué la hace especial para ti?"
→ Variable: input_experiencia_importante

**Pregunta 1c — Lo no resuelto**
"¿Hay algo que sientas que no ha sido dicho o resuelto en tu familia?"
→ Variable: input_lo_no_resuelto

### BLOQUE 2 — Simbolismos personales

**Pregunta 2a — Sueños y símbolos**
"¿Has tenido sueños recurrentes, imágenes o símbolos que marcan tu historia?"
→ Variable: input_suenos_simbolos

**Pregunta 2b — Relato familiar repetido**
"¿Hay un relato, mito o historia familiar que se haya repetido a lo largo de generaciones?"
→ Variable: input_relato_familiar

### BLOQUE 3 — Patrones y narrativas

**Pregunta 3a — Patrón que se repite**
"¿Qué comportamiento, situación o resultado se repite una y otra vez en tu vida, aunque no lo quieras?"
→ Variable: input_patron_repetido

**Pregunta 3b — Cargas heredadas**
"¿Sientes que portas algo que no es tuyo? Un rol, una responsabilidad, un dolor que no elegiste."
→ Variable: input_cargas_heredadas

**Pregunta 3c — Intención de transformación**
"¿Qué quieres cambiar, soltar o conseguir a partir de explorar tu sistema familiar?"
→ Variable: input_intencion_transformacion

### BLOQUE 4 — Inventario personal

**Pregunta 4a — Tema principal** (selección única)
Opciones: DINERO · RELACIONES · AUTORIDAD · TRANSFORMACIÓN
→ Variable: input_tema_principal

**Pregunta 4b — Intensidad emocional** (escala 1–5)
1–2: "Lo noto pero no me afecta mucho ahora"
3: "Es un tema presente en mi vida"
4–5: "Me afecta con intensidad actualmente"
→ Variable: input_intensidad_emocional

**Consentimientos** (4 checkboxes obligatorios)
1. Consiento el análisis de mis respuestas por IA
2. Entiendo que esto no es un servicio sanitario
3. Acepto que mi facilitador revisará el guión
4. Acepto la Política de Privacidad y T&C

---

## FASE S — Síntesis del Agente IA

**Paso 1: Evaluación de riesgo** (SIEMPRE PRIMERO)
Si FLAG_RIESGO = ALTO → detener, activar protocolo SOS

**Paso 2: Clasificación temática**
Confirmar o corregir el tema declarado por el usuario

**Paso 3: Extracción de variables sistémicas**
family_key_figures · family_myth · repeating_pattern · inherited_burden · healing_intention · recurring_symbol · emotional_core

**Paso 4: Guía para el facilitador**
Resumen del patrón, figuras clave, áreas de sensibilidad, derivación Sí/No

**Paso 5: Guión del vídeo**
Duración: 90–120 seg (int.1-2) · 150–180 seg (int.3) · 240–300 seg (int.4-5)
Estructura: apertura → patrón → reconocimiento → intención → cierre

**Paso 6: Prompt de imagen DALL-E**
Imagen 16:9, sin texto, sin caras, metafórica, basada en recurring_symbol

**Paso 7: Metadatos de producción**
Nombre, email, asunto del email, idioma, timestamp

---

## FASE S — Checklist del Facilitador (4 preguntas)

| # | Pregunta | Criterio aprobación |
|---|---|---|
| 1 | ¿El guión tiene una sola idea central clara? | Sí → OK |
| 2 | ¿Usa únicamente lenguaje permitido CONSTELLia? | Sin palabras prohibidas |
| 3 | ¿El guión invita, no prescribe ni promete? | Sin verbos de obligación |
| 4 | ¿El prompt de imagen es metafórico (sin caras ni clínica)? | Sin referencias literales |

Pasa los 4 → APROBAR → activar Make → generar vídeo
Falla alguno → EDITAR o regenerar

---

## FASE A — Producción automatizada (Make)

1. DALL-E API → imagen simbólica
2. Synthesia / HeyGen → vídeo avatar con guión aprobado
3. Google Drive → almacena vídeo + guión + imagen (carpeta privada del usuario)
4. SendGrid → email al usuario con enlace al vídeo
5. Notion → sesión registrada como completada

---

## Tiempos de servicio

| Fase | Tiempo máximo | Responsable |
|---|---|---|
| R: Formulario recibido | Inmediato | Automático |
| S: Análisis IA | <5 minutos | Agente RSSA |
| S: Revisión facilitador | 24–48 horas | Facilitador |
| A: Producción audiovisual | <30 minutos | Make + Synthesia |
| **TOTAL** | **≤ 4 días** | CONSTELLia |

---
*Actualizar cuando cambie el formulario, stack tecnológico o tiempos de servicio.*
**CONSTELLia SL · Algeciras, Andalucía · Marzo 2026**
