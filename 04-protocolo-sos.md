# Protocolo SOS — 3 Capas
## Corpus RAG — Categoría: 01_protocolos
**Versión:** 1.0 · Marzo 2026

---

## Propósito

CONSTELLia NO trata crisis de salud mental.
Lo que SÍ hace: detectarlas, pausar el proceso y derivar a recursos apropiados.
Este protocolo es de cumplimiento obligatorio para el Agente IA y todos los facilitadores.

---

## Qué es un incidente crítico

Cualquier indicador de riesgo inminente para la vida:

1. Riesgo suicida alto: ideación + plan + intención + acceso a método
2. Autolesiones activas: corte, quemaduras, intoxicación deliberada
3. Violencia activa: amenaza a terceros, ideación homicida
4. Abuso físico o sexual en curso
5. Crisis psicótica aguda
6. Sobredosis o intoxicación por drogas

---

## CAPA 1 — Detección automática por IA (<5 segundos)

El Agente analiza TODOS los campos de texto antes de cualquier otro procesamiento.

### Palabras que activan FLAG automático

**Riesgo ALTO (detener inmediatamente):**
- "no quiero seguir viviendo" · "quiero desaparecer" · "quiero morir"
- "hacerme daño" · "no tiene sentido vivir" · "mejor si no estuviera"
- "voy a acabar con todo" · "tengo pastillas" · "ya lo tengo planeado"
- cualquier mención de método concreto de autolesión o suicidio

**Riesgo MEDIO (anotar en guía del facilitador, no detener):**
- "a veces pienso que sería mejor no estar" · "nadie me echa de menos"
- "soy una carga" · "no veo salida" · "me canso de todo"
- "me he cortado antes" · violencia en el hogar

**Riesgo BAJO (registrar, continuar con precaución):**
- lenguaje muy negativo sobre sí mismo
- referencias a pérdidas o duelos recientes
- aislamiento extremo descrito

### Acción del Agente

| Nivel | Acción |
|---|---|
| ALTO | Detener. Solo generar mensaje SOS. NO generar guión ni vídeo. |
| MEDIO | Continuar pero añadir alerta en guía del facilitador. |
| BAJO | Continuar con precaución. Anotar observación. |
| NINGUNO | Proceso normal. |

### Mensaje SOS al usuario (nivel ALTO)

---
[NOMBRE], gracias por compartir esto conmigo.

Lo que describes merece una atención que va más allá de lo que
CONSTELLia puede ofrecerte ahora mismo.

Por favor, contacta ahora con:

📞 024 — Línea de atención a conducta suicida (24h, gratuita)
📞 112 — Emergencias

No estás solo/a. Hay personas preparadas para escucharte ahora mismo.

CONSTELLia pausará tu proceso hasta que estés en un lugar seguro.
---

---

## CAPA 2 — Evaluación por el facilitador (10–15 minutos)

### Checklist de riesgo (antes de revisar el guión)

1. ¿El usuario describe pensamientos de hacerse daño o de no querer vivir?
   → Sí: escalar a ALTO

2. ¿El usuario menciona un plan, método o tiempo concreto?
   → Sí: ALTO inmediato, derivar a 024/112

3. ¿El usuario menciona violencia activa, abuso en curso o crisis aguda?
   → Sí: ALTO, contacto directo

4. ¿La intensidad declarada (1–5) es coherente con el contenido del texto?
   → Si el texto es muy intenso y marcó 1–2: tratar como MEDIO mínimo

### Acciones por nivel

**ALTO:**
1. No aprobar el vídeo (nunca)
2. Enviar email al usuario con recursos de ayuda inmediata
3. Registrar en Notion (fecha, resumen anónimo, acción)
4. Notificar a fundador + DPO

**MEDIO:**
1. Ajustar guión para no profundizar en el área de riesgo
2. Incluir referencia a recursos de apoyo al final del guión
3. Enviar email adicional con info sobre 024
4. Seguimiento a 48h

**BAJO:**
1. Continuar con precaución
2. Suavizar tono si intensidad 4–5
3. Registrar en Notion

### Email de derivación al usuario (nivel ALTO/MEDIO)

---
Asunto: Un mensaje importante de CONSTELLia

Hola [nombre],

Hemos revisado tus respuestas con cuidado y queremos escribirte
antes de continuar con tu proceso.

Algunas cosas que compartiste nos indican que estás atravesando
un momento muy difícil. Y eso merece más que una pieza audiovisual.

Si estás en crisis o tienes pensamientos de hacerte daño:

📞 024 — Línea de atención a conducta suicida (24h, gratuita)
📞 112 — Emergencias
🌐 www.suicidioprevención.org

No tenemos que continuar hoy. Cuando estés listo/a, CONSTELLia
seguirá aquí para ti.

Con cuidado,
El equipo CONSTELLia
---

---

## CAPA 3 — Botón SOS en la plataforma

El botón "Necesito ayuda ahora" está visible en todo momento durante el formulario.

Al pulsarlo:
- Muestra pantalla con 024, 112 y recursos
- Envía notificación automática al facilitador de guardia
- No requiere estar logueado para ser accesible

### Recursos siempre visibles en la plataforma

📞 024 — Línea de atención a conducta suicida (24h, gratuita)
📞 112 — Emergencias
📞 717 003 717 — Teléfono de la Esperanza

---

## Registro de incidentes

Cada incidente se registra en Notion con:
- Fecha y hora
- Nivel de riesgo (IA + facilitador)
- Acción tomada
- Estado: abierto / cerrado / derivado
- Responsable

Acceso: solo facilitador asignado, fundador y DPO.
Se revisan en cada reunión del Comité Ético.

---

## Formación obligatoria del facilitador

- Curso evaluación de riesgo suicida: 8–12 horas
- Role-play: mínimo 3 simulaciones de crisis
- Certificado de competencia emitido por CONSTELLia
- Reciclaje anual obligatorio

---
*Cumple con Código Penal art. 172 y criterios del Ministerio de Sanidad.*
**CONSTELLia SL · Algeciras, Andalucía · Marzo 2026**
