Fecha: 2026-10-15 · PRD: equipos/equipo-05/prd.md

## Revisión · Grano Inventario al Día (equipo-05) · 15/15

**Listo para la E3** (el mínimo es 10). Tiene el máximo en los cinco criterios. Lo que sigue son afinaciones, no puntos pendientes.

| Criterio | Nivel | Evidencia (cita del PRD) | Qué falta para subir |
|---|---|---|---|
| A. Problema con evidencia | 3 | "Grano no sabe cuánto café le queda a cada tostador hasta que es tarde." Costo de no hacer nada: "≈ 1.416 sobreventas, ≈ $170.000 MXN en reembolsos y cupones (236 × $120 × 6)… ≈ 100 horas de Rafa". | Ya está en el máximo. La sección 2 no menciona la solución. Los datos y las citas son del brief, y las cuentas cuadran (236 × 6 = 1,416; 236 × $120 × 6 = $169,920; 4 h × 26 semanas = 104 h). |
| B. Usuario, cliente y JTBD | 3 | "Tensión usuario ↔ cliente: Rafa quiere el dato más seguido y que el sistema actúe; Valeria no quiere que nada compre solo… los tostadores no quieren llenar nada nuevo." | Ya está en el máximo. Usuario concreto, cliente identificado, JTBD completo, alternativa actual ("Google Sheet semanal, más WhatsApp uno a uno… más la memoria de Rafa") y la tensión escrita. |
| C. Métricas | 3 | "% de pedidos con un café agotado después de pagar · 11 % (≈ 236/mes) · ≤ 3 % (≈ 65/mes) · 3 meses después del lanzamiento". | Ya está en el máximo. Las 4 métricas tienen línea base, meta y plazo, y la North Star mide valor y no uso. Afinación: ver mejora 1. |
| D. Alcance y no-objetivos | 3 | CU3: "ninguna orden sale sin su clic". No-objetivo: "Generar ni enviar órdenes de compra de forma automática… Es lo que Rafa sí quería". | Ya está en el máximo. Son 3 casos de uso con criterio observable y 5 no-objetivos con su porqué, uno de ellos algo que el equipo sí quería hacer. |
| E. AI Strategic Lens | 3 | Lente 1: "Casi todo es regla… La IA solo hace falta para leer respuestas libres de WhatsApp". Lente 6: "100 mensajes reales… Meta: ≥ 95 % leídos bien y 100 % de los mensajes sin unidad detectados como ambiguos". | Ya está en el máximo. Las 6 lentes tienen umbrales concretos para el humano (2 h, 50 %, café en negativo) y plan de evaluación. Afinación: ver mejora 3. |

**Banderas rojas:** ninguna. No hay tecnologías ni arquitectura: WhatsApp, el Sheet y las plantillas de Meta vienen del brief y del contexto. No hay precios ni compras que el agente decida sin umbral: la sugerencia la aprueba Rafa y el brief fija los $5,000. La North Star no es de vanidad. Hay 5 no-objetivos.

**Datos sin fuente:**
- Los datos del brief y del contexto cuadran todos: 11 %, 236, $120, 4 h, 7 de 18, 23 días-producto, 1.8 % de conversión, $5,000 y $40,000.
- Estos números son parámetros de diseño que propone el equipo y no vienen del brief. Está bien que sean decisiones suyas, pero ninguno tiene justificación escrita: el plazo de 15 minutos de CU2, las 2 h de espera, el 50 % de cambio, el 95 % de acierto y los "3 mensajes por semana" del costo.
- "0 de 18" como línea base de tostadores que reportan 2 veces por semana es una deducción razonable del brief, que solo dice que el Sheet se actualiza 1 vez por semana.
- El PRD usa "1.416" y "$170.000" con punto como separador de miles, y "1,8 %" con coma. El brief usa "$5,000" y "1.8 %". Conviene unificar para que nadie lea 1.416 como uno coma cuatro.

### 3 mejoras de mayor impacto
Ninguna sube puntos, porque ya está todo en 3. Estas son afinaciones, ordenadas por riesgo.
1. **Guardrail de la métrica C.** "Conversión de la tienda ≥ 1,8 %" se mueve por mil causas ajenas a este producto, así que no te dirá si hay falsos agotados. Considera un guardrail más directo, como los cafés marcados agotados que sí tenían existencias, o añade un segundo guardrail. Así el guardrail detecta el riesgo que tú mismo nombras en la sección 7.
2. **Formato del archivo.** El PRD perdió la estructura de markdown: no hay encabezados `#`, las tablas se convirtieron en líneas sueltas y se ve como pegado desde otro editor. En el repositorio se leerá mal. Restaura las tablas y los encabezados de la plantilla.
3. **Costo de IA (lente 6).** Dices que "queda muy por debajo de los $40.000 MXN, pero el número exacto lo confirman los devs". Para el nivel 3 está bien, pero una cifra aproximada por mes (con el supuesto de 230 mensajes) deja el PRD sin hueco. Que el número lo afinen los devs en la E5.

**Pregunta incómoda:** Si llegas a la meta de ≤ 3 %, evitas unas 171 sobreventas al mes (236 − 65), que son ≈ $20,500 MXN al mes en reembolsos y cupones, más las horas de Rafa. ¿Eso justifica 2 devs durante 8 semanas, y qué parte de esa mejora depende de tostadores que reportan 2 veces por semana mientras siguen vendiendo por Instagram o en su local? Tu propio riesgo 1 puede limitar la meta de 3 %, y no dices cuánto.
