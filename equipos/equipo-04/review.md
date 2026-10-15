Fecha: 2026-10-15 · PRD: equipos/equipo-04/prd.md

## Revisión · Soporte post-venta: rastreo, daños y reembolsos (equipo-04) · 5/15

**Todavía no está listo para la E3.** Se necesitan 10 puntos o más, y hoy tiene 5. El PRD sigue siendo la plantilla vacía: no hay ninguna sección escrita, solo el segmento y la fecha.

| Criterio | Nivel | Evidencia (cita del PRD) | Qué falta para subir |
|---|---|---|---|
| A. Problema con evidencia | 1 | Sección 2 vacía: "**Problema:**" y "**Evidencia:**" sin texto. | Está vacía, así que es nivel 1. El brief ya trae datos para llenarla: 1,900 tickets al mes con 3 personas, 34 % de "¿dónde está mi pedido?", primera respuesta de 9 h, CSAT de 3.9, $58,000 MXN al mes en reembolsos, ≈ $45 por ticket. También trae citas (Karla, Beto y dos clientes). |
| B. Usuario, cliente y JTBD | 1 | Sección 3 vacía: "Usuario principal \| \|", "Cliente (paga o decide) \| \|". | Está vacía, así que es nivel 1. Hay que elegir usuario (¿el cliente que escribe o Karla y Beto?) y justificarlo, nombrar al cliente (el brief dice que Marisol decide si el producto se queda), escribir el JTBD completo y nombrar la alternativa actual. |
| C. Métricas | 1 | Sección 4: tabla con North Star, Entrada, Entrada y Guardrail sin contenido. | Está vacía, así que es nivel 1. Cada métrica necesita línea base, meta y plazo, y la North Star debe medir valor y no actividad. |
| D. Alcance y no-objetivos | 1 | Sección 5: CU1, CU2 y CU3 en blanco, y la tabla de no-objetivos sin filas llenas. | Está vacía, así que es nivel 1. Faltan hasta 3 casos de uso con criterio observable y al menos 3 no-objetivos con su porqué. |
| E. AI Strategic Lens | 1 | Sección 6: las 6 lentes en blanco. | Está vacía, así que es nivel 1. Aunque es "deseable", la rúbrica la puntúa. |

**Banderas rojas:**
- 🚩 No hay ningún no-objetivo.
- Las otras tres no aplican porque no hay contenido. Al escribir, vigila la política de reembolsos: los mayores a $500, o de clientes con más de 2 reclamos en 90 días, los aprueba una persona. Esos umbrales deben aparecer escritos.

**Datos sin fuente:** ninguno, porque el PRD no contiene datos. El título sigue como `<nombre del producto>`, y los campos Producto y Autores están sin llenar. La sección 1 está vacía.

### 3 mejoras de mayor impacto
1. **A, de 1 a 3 (hasta +2): escribe el problema desde el usuario que elijas y cuantifica el costo de no hacer nada.** Usa los datos del brief y 1 cita. No menciones la solución ni digas "no tenemos un agente". Ponle número al costo en 6 meses. El brief da con qué hacerlo: $58,000 al mes en reembolsos y ≈ $45 por ticket.
2. **C, de 1 a 3 (hasta +2): llena las 4 métricas con línea base del brief, meta y plazo.** Las bases ya existen: 9 h de primera respuesta, CSAT de 3.9, $58,000 de reembolsos. La North Star debe medir lo que gana el usuario elegido. El guardrail debe ser el que dejaría tranquila a Marisol ("si un bot regala reembolsos, lo apago"), con un número.
3. **D, de 1 a 3 (hasta +2): define hasta 3 casos de uso con criterios comprobables y al menos 3 no-objetivos con su porqué.** Aquí entra el umbral exacto de autonomía en reembolsos. El no-objetivo más valioso es lo que alguien del equipo sí quería hacer, como dejar que el agente decida reembolsos solo.

Para llegar a 10 hacen falta +5, así que hay que subir al menos tres criterios. B y E también suman y se llenan rápido con el brief.

**Pregunta incómoda:** Marisol dice "si un bot regala reembolsos, lo apago al día siguiente", y Beto admite que hoy los reembolsos se deciden "a ojo". ¿Cómo sabrás que el agente decide mejor que Beto, si hoy nadie tiene un criterio escrito contra el cual compararlo? ¿Y el usuario que eliges es el cliente que escribe o Karla y Beto? Cambia todo el PRD.
