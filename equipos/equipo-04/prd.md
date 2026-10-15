# PRD · Asistente de soporte post-venta

> Mini-PRD de la Estación 2. Diseñado para llenarse en 45 minutos.
> Las secciones 1 a 5 son **obligatorias**; la 6 y la 7 son **deseables** (súmalas si les da el tiempo).
> Borra los comentarios `<!-- -->` cuando termines una sección.
> Regla de oro: **cero tecnologías en este documento**. Nada de React, LangChain, Postgres ni "un endpoint". Eso es el CÓMO y llega en la E5.

| Campo | Valor |
|---|---|
| Producto | Asistente de soporte post-venta |
| Equipo | equipo-04 |
| Segmento | Equipo de soporte post-venta: rastreo, daños y reembolsos |
| Track | ISB (solución interna) |
| Autores | <!-- PENDIENTE: nombres y rol de cada integrante del equipo --> |
| Fecha | 2026-10-14 |
| Estado | Borrador |

---

## 1. Resumen en una línea  ⏱ 3 min

Para Karla y Beto, del equipo de soporte de Grano, que pierden la mañana copiando el estatus de la paquetería y deciden los reembolsos "a ojo", el asistente de soporte post-venta es un copiloto interno que responde al instante el "¿dónde está mi pedido?" y deja cada reclamo de daño listo para aprobar con criterios claros.
A diferencia de hoy (copiar y pegar, y decidir caso por caso con 9 horas de espera), ningún reembolso se paga sin una persona y nunca se promete una fecha que la paquetería no haya confirmado.

## 2. Problema y evidencia  ⏱ 7 min

**Problema:**

Tres personas atienden 1,900 tickets al mes. Más de la mitad son trabajo repetitivo: copiar el estatus de una guía o juntar evidencia de un daño. Mientras tanto, el cliente espera 9 horas una primera respuesta y, si su bolsa llegó rota, le piden foto, ticket y video. Los reembolsos no tienen un criterio escrito: cada agente decide por su cuenta, y la Head de Operaciones no tiene forma de confiar en esas decisiones.

**Evidencia:**

- El 34 % de los tickets (≈ 650 al mes) es "¿dónde está mi pedido?" y el 18 % (≈ 340) son daños y reembolsos. Juntos son el 52 % de la carga (brief y `grano-hoy.md`).
- La primera respuesta tarda 9 horas en promedio y el CSAT es de 3.9 / 5 (brief).
- Grano paga $58,000 MXN al mes en reembolsos, decididos "a ojo" (brief).
- Karla, de Soporte: "El '¿dónde está mi pedido?' me come la mañana. Es copiar la guía de la paquetería y pegarla."
- Beto, de Soporte: "Los reembolsos los decido a ojo. A veces siento que me están viendo la cara."
- Cliente: "Mi bolsa llegó rota y me pidieron foto, ticket y video. Me cansé."

**Costo de no hacer nada:**

Con la operación de hoy, atender los tickets cuesta ≈ $85,500 MXN al mes (1,900 × $45), de los cuales ≈ $29,000 son consultas de rastreo. En 6 meses son ≈ $513,000 MXN en atención y ≈ $348,000 MXN en reembolsos sin criterio. Además, el volumen crece con los pedidos (2,150 al mes) sobre un equipo de 3 personas, y Marisol (Head de Operaciones) no tiene cómo auditar los reembolsos.

## 3. Usuario, cliente y JTBD  ⏱ 7 min

| | |
|---|---|
| Usuario principal | Karla y Beto, agentes del equipo de soporte de Grano (3 personas en total). Atienden tickets de rastreo, daños y reembolsos todos los días, con 1,900 tickets al mes entre el equipo. El cliente final que escribe es beneficiario, no usuario. |
| Cliente (paga o decide) | Marisol, Head de Operaciones: decide si el producto se queda ("Si un bot regala reembolsos, lo apago al día siguiente"). El presupuesto de IA lo define Valeria, CEO ($40,000 MXN al mes para todo Grano). |
| Job to be done | Cuando me llega un ticket de rastreo o de un daño, quiero resolver o preparar el caso sin copiar datos a mano ni decidir a ojo, para responder rápido al cliente y que cada reembolso se pueda defender ante Operaciones. |
| Alternativa actual | Copiar y pegar a mano el estatus de la guía de la paquetería. Para daños, pedir foto, ticket y video por mensaje y decidir el reembolso caso por caso sin criterio escrito. Tensión: el usuario (Karla y Beto) quiere ahorrarse el trabajo repetitivo; el cliente (Marisol) solo lo acepta si no pierde control del dinero. |

## 4. Métricas  ⏱ 8 min

> Las metas son propuestas del equipo, no datos del brief. Hay que validarlas con Soporte y con Marisol.

| Tipo | Métrica | Línea base | Meta | Plazo |
|---|---|---|---|---|
| North Star | Tiempo promedio de primera respuesta al cliente | 9 h | ≤ 1 h | 8 semanas después del lanzamiento |
| Entrada | % de tickets de rastreo que el cliente resuelve sin intervención de una persona | 0 % (hoy todo es manual; ≈ 650 tickets al mes) | ≥ 70 % | 8 semanas después del lanzamiento |
| Entrada | % de casos de daño que llegan a una persona con el expediente completo (sin pedir evidencia más de una vez al cliente) | No medido hoy (se piden foto, ticket y video) | ≥ 90 % | 8 semanas después del lanzamiento |
| Guardrail | Reembolsos pagados sin aprobación humana, o fuera de la política ($500 / 2 reclamos en 90 días) | 0 aprobados por el sistema; hoy no se audita | 0, sin excepciones | Siempre |
| Guardrail | CSAT | 3.9 / 5 | ≥ 3.9 (no empeora) | Siempre |

## 5. Alcance del MVP y no-objetivos  ⏱ 10 min

### Flujo del MVP

```
Llega un ticket
├─ "¿Dónde está mi pedido?" (34 %)
│   └─ El agente consulta el estatus de la paquetería
│       ├─ Sin incidencia → responde el estatus, sin prometer fecha
│       └─ Con incidencia → pasa a una persona de soporte
├─ Daño o reembolso (18 %)
│   └─ El agente arma el expediente (historial, evidencia, una sola solicitud al cliente)
│       ├─ ≤ $500 y ≤ 2 reclamos en 90 días → con recomendación; una persona aprueba
│       └─ > $500 o > 2 reclamos en 90 días → sin recomendación; una persona decide
│       (el agente nunca paga)
└─ Otros motivos (48 %) → fuera del MVP, siguen como hoy
```

### Casos de uso

| # | Caso de uso | Criterio de aceptación (observable) |
|---|---|---|
| CU1 | **Rastreo:** el cliente pregunta por su pedido y recibe el estatus actual de la paquetería. | El cliente recibe respuesta en menos de 1 minuto con el estatus que reporta la paquetería. La respuesta no incluye ninguna fecha de entrega que la paquetería no haya confirmado. Si el estatus indica un problema (retraso o extravío), el caso llega a una persona de Soporte marcado como tal. |
| CU2 | **Expediente de daño:** el cliente reporta un producto dañado y el asistente reúne lo necesario en una sola conversación. | Al cliente se le pide la evidencia una sola vez. La persona de Soporte recibe el caso con pedido, evidencia y número de reclamos del cliente en los últimos 90 días, sin pedir nada más al cliente. |
| CU3 | **Reembolso con aprobación humana:** el asistente prepara una recomendación dentro de la política y una persona la aprueba. | Hasta $500 y con 2 reclamos o menos en 90 días, el caso llega con recomendación y una persona la aprueba antes de pagar. Sobre $500, o con más de 2 reclamos, el caso llega marcado como "escalado" sin monto recomendado. Ningún reembolso se paga sin aprobación de una persona. |

### No-objetivos

| No vamos a… | Porque… |
|---|---|
| Dejar que el asistente apruebe o pague reembolsos por sí solo, ni siquiera los de $500 o menos | Es lo que el CEO y la política actual permitirían, pero las reglas de Grano exigen confirmación humana para todo reembolso, y Marisol apaga el producto si regala dinero. Se revisa después de medir el MVP. |
| Prometer o estimar fechas de entrega | La paquetería da el estatus pero no garantiza fechas; prometer una es un compromiso que Grano no puede cumplir. |
| Atender cambios de suscripción (14 % de los tickets) ni recomendaciones de café (12 %) | Pertenecen a otros segmentos (equipo 02 y equipo 01) y diluyen el foco en lo que mueve la North Star. |
| Tocar datos de tarjetas ni ejecutar cobros | Restricción del segmento: el agente no tiene acceso a datos de tarjetas. |

## 6. AI Strategic Lens  ⏱ 7 min (deseable)

| Lente | Respuesta |
|---|---|
| 1. ¿Por qué IA? ¿Una regla, un filtro o un formulario lo resolvería? | Consultar el estatus de una guía es una consulta directa, no necesita IA. La IA aporta donde el cliente escribe en lenguaje libre: entender qué pregunta, redactar una respuesta clara, detectar que el estatus indica un problema y armar el expediente de un daño sin formularios largos. |
| 2. Datos y ventaja: ¿qué sabe Grano que un competidor con el mismo modelo no sabe? | Grano conoce el historial de pedidos y de reclamos por cliente y cómo se resolvieron antes sus casos de daño. Un competidor con el mismo modelo no tiene esa historia ni la política de reembolsos de Grano. |
| 3. Autonomía: nivel 0 a 3 y por qué | Rastreo: nivel 2, responde solo porque el riesgo es bajo y no promete fechas. Reembolsos: nivel 1 hasta $500 (redacta, una persona aprueba) y nivel 0 sobre $500 o con más de 2 reclamos (solo arma el expediente). |
| 4. Costo del error: ¿qué pasa si se equivoca? ¿Es reversible? ¿Quién lo paga? | Un estatus mal informado es reversible y cuesta CSAT. Un reembolso mal recomendado no se paga sin aprobación, así que el error lo atrapa la persona. El peor caso es un cliente ofendido o una fecha prometida, que no es reversible; por eso ambas están prohibidas. |
| 5. Humano en el circuito: ¿en qué momento y con qué umbral entra una persona? | Siempre antes de cualquier reembolso. Sobre $500, o con más de 2 reclamos en 90 días, la persona decide sin recomendación del asistente. También entra cuando el estatus indica un retraso o extravío. |
| 6. Evaluación: ¿cómo sabrán que funciona antes de lanzarlo? | Con un conjunto de tickets históricos reales que Karla y Beto revisan antes del lanzamiento. Criterio: cero recomendaciones fuera de la política, cero fechas prometidas y cero respuestas que ellos juzguen ofensivas. |

## 7. Riesgos, supuestos y preguntas abiertas  ⏱ 3 min (deseable)

**Supuesto más riesgoso:**

Que la mayoría de los tickets de "¿dónde está mi pedido?" son solo una consulta de estatus y no un problema real (retraso, extravío). Si no es así, el 70 % de resolución sin persona es inalcanzable.

**Cómo lo validamos (≤ 2 semanas, sin código):**

Que Karla revise con el equipo una muestra de tickets de rastreo de un mes (por ejemplo, 50) y clasifique cuántos eran solo estatus y cuántos terminaron en un problema. Con eso se corrige la meta de la North Star.

**Riesgos:**

- Marisol apaga el producto a la primera señal de un reembolso fuera de política: por eso el guardrail es 0 y no un porcentaje.
- Datos personales y fotos de clientes: Grano está sujeto a la LFPDPPP (aviso de privacidad, consentimiento y uso limitado).
- Fuera de la ventana de 24 h de WhatsApp solo se pueden enviar plantillas aprobadas, lo que limita las respuestas proactivas.
- El costo de IA por ticket no está estimado y debe caber en los $40,000 MXN al mes de todo Grano.
- Si los ahorros se miden en pesos sin estimar ese costo, la meta de ahorro podría quedar sobrestimada.

**Preguntas abiertas:**

- Para el CEO y Operaciones: ¿se permite que el asistente apruebe solo los reembolsos de $500 o menos en una segunda etapa, aunque hoy se exige confirmación humana?
- Para Operaciones: ¿cuántos reembolsos hay al mes y cuántos superan $500? No están en el brief.
- Para el brief: el 6 % de "clientes con más de 2 reclamos", ¿es el 6 % de los reembolsos o del monto?
- Para Legal: ¿qué consentimiento se necesita para guardar las fotos que envía el cliente?
- Para Soporte: ¿de dónde sale el CSAT de 3.9 y cuánto se debe a la espera frente a malas resoluciones?
