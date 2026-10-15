Fecha: 2026-10-15 · PRD: equipos/equipo-03/prd.md

## Revisión · Cafeterías B2B, cotizaciones y pedidos de mayoreo (equipo-03) · 5/15

**Todavía no está listo para la E3.** Se necesitan 10 puntos o más, y hoy tiene 5. El PRD sigue siendo la plantilla vacía: no hay ninguna sección escrita, solo el segmento y la fecha.

| Criterio | Nivel | Evidencia (cita del PRD) | Qué falta para subir |
|---|---|---|---|
| A. Problema con evidencia | 1 | Sección 2 vacía: "**Problema:**" y "**Evidencia:**" sin texto. | Está vacía, así que es nivel 1. El brief ya trae datos para llenarla: 26 h para cotizar, 30 % de cotizaciones con error de precio o disponibilidad, 60 % del tiempo de 2 personas de Ventas dedicado a cotizar, 9 cafeterías en lista de espera. También trae citas (el dueño de Guadalajara, la barista jefa de CDMX). |
| B. Usuario, cliente y JTBD | 1 | Sección 3 vacía: "Usuario principal \| \|", "Cliente (paga o decide) \| \|". | Está vacía, así que es nivel 1. Hay que elegir usuario (¿la cafetería o Ventas?) y justificarlo, nombrar al cliente, escribir el JTBD con el formato completo y nombrar la alternativa actual. |
| C. Métricas | 1 | Sección 4: tabla con North Star, Entrada, Entrada y Guardrail sin contenido. | Está vacía, así que es nivel 1. Cada métrica necesita línea base, meta y plazo, y la North Star debe medir valor y no actividad. |
| D. Alcance y no-objetivos | 1 | Sección 5: CU1, CU2 y CU3 en blanco, y la tabla de no-objetivos sin filas llenas. | Está vacía, así que es nivel 1. Faltan hasta 3 casos de uso con criterio observable y al menos 3 no-objetivos con su porqué. |
| E. AI Strategic Lens | 1 | Sección 6: las 6 lentes en blanco. | Está vacía, así que es nivel 1. Aunque es "deseable", la rúbrica la puntúa. |

**Banderas rojas:**
- 🚩 No hay ningún no-objetivo.
- Las otras tres no aplican porque no hay contenido. Hay que vigilar la restricción de precios: cualquier precio fuera de la tabla de 3 niveles requiere aprobación de Ventas.

**Datos sin fuente:** ninguno, porque el PRD no contiene datos. El título sigue como `<nombre del producto>`, y los campos Producto y Autores están sin llenar. La sección 1 está vacía.

### 3 mejoras de mayor impacto
1. **A, de 1 a 3 (hasta +2): escribe el problema desde la cafetería y cuantifica el costo de no hacer nada.** Usa los datos del brief y 1 cita. No menciones la solución. Decide si el dolor es el precio, la velocidad o la certeza de que le surtan, porque de esa respuesta depende todo lo demás. Ponle número al costo, por ejemplo qué pasa con las 9 cafeterías en espera.
2. **D, de 1 a 3 (hasta +2): define hasta 3 casos de uso con criterios comprobables y al menos 3 no-objetivos con su porqué.** El brief sugiere candidatos a descartar: facturas, negociación, crédito. El más valioso es el que alguien del equipo sí quería hacer, como "cotizar solo" a cualquier volumen.
3. **C, de 1 a 3 (hasta +2): llena las 4 métricas con línea base del brief, meta y plazo.** Las bases ya existen: 26 h de cotización, 30 % de error, 60 % del tiempo de Ventas. La North Star debe medir lo que gana la cafetería (por ejemplo, certeza de surtido) y no cuántas cotizaciones hace el agente.

Para llegar a 10 hacen falta +5, así que hay que subir al menos tres criterios. Los criterios B y E también suman, y son rápidos de llenar con el brief.

**Pregunta incómoda:** Toño dice "si un bot da el precio de lista, perdemos a los mejores clientes". ¿Quién es tu usuario, la cafetería o Ventas? Y si el agente cotiza solo y promete 15 kg para el lunes que el tostador no puede surtir (necesita 5 días), ¿quién paga ese error?
