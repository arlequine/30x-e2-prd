Fecha: 2026-10-15 · PRD: equipos/equipo-01/prd.md

## Revisión · Brújula de Grano (equipo-01) · 12/15

**Listo para la E3** (el mínimo es 10).

| Criterio | Nivel | Evidencia (cita del PRD) | Qué falta para subir |
|---|---|---|---|
| A. Problema con evidencia | 3 | "El problema no es solo elegir: es **confiar en que eligió bien**." Y en el costo de no hacer nada: "De cada 100 compradores nuevos que logramos adquirir, 81 se pierden antes de su segunda compra". | Ya está en el máximo. La sección 2 no menciona la solución, y el costo de no hacer nada está cuantificado (visitas, búsquedas, tickets, 81 de 100). |
| B. Usuario, cliente y JTBD | 2 | "Adulto de 25 a 40 años… toma café a diario en casa con un método sencillo". JTBD completo. Alternativa actual: "Irse al súper o a la cafetería de siempre…". | Nombra la alternativa y al tostador como cliente secundario, pero la sección 3 no dice dónde chocan usuario y cliente. Esa tensión solo aparece de pasada en los no-objetivos. |
| C. Métricas | 2 | North Star: "% de compradores nuevos que hacen una segunda compra en ≤ 60 días: 19 % → 26 % en 6 meses". | Mide valor, no actividad. Pero 2 de los 3 guardrails y una métrica de entrada tienen línea base "Por medir" o "—". La rúbrica pide todas con línea base. |
| D. Alcance y no-objetivos | 3 | Tres casos de uso. Seis no-objetivos con su porqué, entre ellos "Construir un asistente de conversación abierta" (lo que el CEO quería) y "Suscripciones o cajas de muestras en el MVP". | Ya está en el máximo. Un detalle: el criterio de CU3 ("hasta el monto límite") no es comprobable mientras el monto no exista. |
| E. AI Strategic Lens | 2 | "Soporte entra cuando un cliente pide un segundo crédito, cuando la búsqueda no encuentra nada con confianza suficiente…". La lente 1 es honesta ("Luis tiene razón: primero filtros que sirvan"). | Están las 6 lentes y hay plan de evaluación. Pero faltan umbrales concretos: "confianza suficiente" y "monto límite" no tienen número. La cata a ciegas con 30 compradores no dice qué resultado cuenta como aprobado. |

**Banderas rojas:** 🚩 parcial, el crédito de CU3. El agente lo otorga solo "hasta un crédito por cliente y un monto límite", y ese monto no está definido en ninguna parte (la pregunta a Finanzas sigue abierta). Hay regla (uno por cliente) pero falta el umbral. No hay tecnologías ni arquitectura. La North Star no es de vanidad. Hay no-objetivos.

**Datos sin fuente:**
- "algo como el del Oxxo pero mejor" (lente 1) no aparece en el brief ni en el contexto.
- "Luis **y otros** no quieren hablar con un bot": el brief solo registra a Luis.
- "no la tiene un competidor con el mismo modelo" (lente 2) es una afirmación sin respaldo.
- Las cifras de 6 meses (461,000, 267,000, 18,600, 1,380) cuadran con el brief: son multiplicaciones por 6, y 267,000 es 58 % de 461,000.
- Las metas (26 %, 33 %, ≤ 600, ≥ 75 %) son objetivos, no datos. Pero el PRD no explica de dónde sale que +7 puntos de recompra sea alcanzable.

### 3 mejoras de mayor impacto
1. **E, de 2 a 3 (+1): ponle número a los umbrales del humano y al criterio de aprobación.** Define cuándo escala a soporte, qué monto es el "límite" del crédito (o di que es un supuesto a validar con Finanzas), qué es "confianza suficiente" en una búsqueda y qué resultado de la cata a ciegas te deja lanzar. Eso también cierra la bandera parcial del crédito.
2. **C, de 2 a 3 (+1): cierra las líneas base que dicen "Por medir" o "—".** El brief no las trae, así que no las inventes. Pon quién las mide, en qué fecha y con qué método, o reemplaza la métrica por otra que sí tenga base. La semana 0 debe aparecer como un hito con fecha.
3. **B, de 2 a 3 (+1): escribe la tensión usuario-cliente en la sección 3.** El usuario quiere palabras simples, y el tostador y Grano necesitan que sus notas y su visibilidad no se distorsionen. Di qué se sacrifica cuando chocan.

Además, quita o respalda los tres datos sin fuente de arriba.

**Pregunta incómoda:** Tu supuesto más riesgoso es que los compradores no regresan porque no entienden las fichas, pero no escribiste qué resultado de las 2 semanas de validación te haría **abandonar** el producto. Si de los 20 carritos abandonados solo 3 dicen "no entendí las notas" y 12 dicen "el envío es caro", ¿sigues adelante con Brújula? ¿Y cuántos de esos 81 que no regresan lo hicieron por esa causa?
