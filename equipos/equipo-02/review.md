Fecha: 2026-10-15 · PRD: equipos/equipo-02/prd.md

## Revisión · Grano Club, gestión de suscripción (equipo-02) · 6/15

**Todavía no está listo para la E3.** Se necesitan 10 puntos o más, y hoy tiene 6.

| Criterio | Nivel | Evidencia (cita del PRD) | Qué falta para subir |
|---|---|---|---|
| A. Problema con evidencia | 2 | "Motivo de cancelación: 'me llegó un café que no me gustó' - 38 % usuarios". Y en el costo: "en 6 meses se perderia aproximadamente la mitad de los suscriptores". | Tiene 3 datos del brief, pero ninguna cita de usuario (el brief trae a Andrea y a Raúl). El costo de no hacer nada no muestra cómo se calculó y no está en pesos. El brief da el valor de vida: $3,900 de un suscriptor contra $910 de un comprador único. |
| B. Usuario, cliente y JTBD | 1 | Usuario: "Suscriptor". Cliente: "CEO - Grano Club". JTBD: "Adaptar la suscripción para ser más flexible…". | El usuario es genérico: no tiene contexto ni frecuencia. El JTBD no sigue el formato "Cuando…, quiero…, para…". La tabla quedó con una columna de más. La alternativa actual (WhatsApp y atención manual) sí está nombrada. |
| C. Métricas | 1 | "North Star — Churn: queremos que menos clientes abandonen Grano Club." | Ninguna de las 4 métricas tiene línea base, meta ni plazo. Sin números, la rúbrica las deja en nivel 1. |
| D. Alcance y no-objetivos | 1 | CU2: "El usuario recibe una confirmación". CU3 está vacío. Un solo no-objetivo: "Bajar más del 15% el precio por una única vez". | Falta el tercer caso de uso. Los criterios solo piden "una confirmación" y no prueban nada de lo que importa. Hay 1 no-objetivo y se piden al menos 3. |
| E. AI Strategic Lens | 1 | La sección 6 tiene las 6 lentes en blanco. | Está vacía, así que es nivel 1. Aunque es "deseable", la rúbrica la puntúa. |

**Banderas rojas:**
- Ninguna de las cuatro se activa del todo. No hay tecnologías, la North Star no es de vanidad y existe un no-objetivo.
- Riesgo a vigilar: el PRD no dice si el agente puede ofrecer descuentos de retención. Si lo hace, la regla del brief (máximo 15 %, una vez por cliente al año) tiene que quedar escrita como umbral.

**Datos sin fuente:**
- Los porcentajes 38 %, 27 %, 19 %, el 11 % y el 6 % vienen del brief.
- "Aproximadamente la mitad de los suscriptores en 6 meses" no trae su cálculo. Sale de aplicar 11 % mensual durante 6 meses, pero el PRD no lo dice.
- La sección 1 no usa el formato de la plantilla. Habla de un problema de la compañía y no del usuario, y todavía dice `<nombre del producto>`. Los campos Producto y Autores están sin llenar.

### 3 mejoras de mayor impacto
1. **C, de 1 a 3 (hasta +2): ponle línea base, meta y plazo a cada métrica.** El brief ya trae varias: churn 11 % con meta ≤ 6 %, resolución de 22 h, ≈ 270 tickets al mes y 72 % que prefiere WhatsApp. Falta el plazo, y decidir si "churn" es la North Star o una consecuencia de algo que el usuario sí percibe. Al guardrail de cancelación libre ponle un número que se pueda auditar.
2. **D, de 1 a 3 (hasta +2): completa CU3 y haz comprobables los criterios.** Define qué debe pasar cuando el cliente dice "cancela" y el agente entiende "pausa", porque el brief exige confirmación explícita para cancelar. Agrega al menos 2 no-objetivos más, cada uno con su porqué. El más valioso es algo que el equipo sí quería hacer, como los descuentos o el agente en WhatsApp.
3. **B, de 1 a 2 (+1): vuelve concreto al usuario y reescribe el JTBD completo.** Di qué suscriptor es (por ejemplo, alguien que se va de viaje, como Andrea) y qué hace hoy. Después nombra la tensión entre lo que quiere el suscriptor (Daniel: "me quedo… y cancelo al mes siguiente") y lo que protege Grano (Laura: el descuento sale del margen).

Llenar la sección 6 también suma +1 y cierra el hueco más grande. Con las mejoras 1 y 2 en nivel 3 (+4) llegarías a 10, que es el mínimo para la E3.

**Pregunta incómoda:** Dos de las dos funciones de tu alcance son pausar y cambiar el café. ¿Por qué necesitan IA y no un botón o un menú en WhatsApp? El PRD nunca dice qué parte del problema solo puede resolver un agente. Y si el 19 % se va por precio, ¿qué parte de la North Star estás dejando fuera, y lo escribiste como no-objetivo?
