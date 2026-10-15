# PRD · Asistente de cotización de grano B2B

> Mini-PRD de la Estación 2. Diseñado para llenarse en 45 minutos.
> Las secciones 1 a 5 son **obligatorias**; la 6 y la 7 son **deseables** (súmalas si les da el tiempo).
> Borra los comentarios `<!-- -->` cuando termines una sección.
> Regla de oro: **cero tecnologías en este documento**. Nada de React, LangChain, Postgres ni "un endpoint". Eso es el CÓMO y llega en la E5.

| Campo | Valor |
|---|---|
| Producto | Asistente de cotización de grano B2B |
| Equipo | equipo-03 |
| Segmento | Cafeterías B2B: cotizaciones y pedidos de mayoreo |
| Track | PVB (cliente externo) |
| Autores | Patricio Reinoso / , Julian Grijalba / , Silvia Ram / , Rafael Prudencio / Andrés Lopez / ,Edgar Bonilla / , Pablo Hoyos / rol: |
| Fecha | 2026-10-14 |
| Estado | Borrador |

---

## 1. Resumen en una línea  ⏱ 3 min

Asistente de cotización de grano B2B, dirigido a las cafeterías (clientes) para reducir el tiempo de respuesta de las cotizaciones, adicionalmente estandarizar el tiempo de entrega para dar una infromación veridica (recolectar variables de decición), fecha de entrega confirmados en menos de 2 horas. 

## 2. Problema y evidencia  ⏱ 7 min

Se siente que el problema está en la estimación del tiempo de entrega.

- Evidencia, "Para mayoreo necesito 5 días para tostar. No me prometan en 2." Tostador de Veracruz

El precio en la tabla rígida con 25 o mas no da pie a decición de ventas.

- Evidencia, "La mitad del trabajo es negociar. Si un bot da el precio de lista, perdemos a los mejores clientes."

- Costo perdida de clientes.

Las facturas no se entregan a tiempo

- Evidencia "Quiero mis facturas sin pedirlas tres veces."

## 3. Usuario, cliente y JTBD  ⏱ 7 min

<!--
- Usuario: quién lo usa. Concreto: rol, contexto y frecuencia. "Todos los clientes" no es un usuario.
- Cliente: quién paga o decide que esto exista. A veces es otra persona.
- JTBD: Cuando <situación>, quiero <motivación>, para <resultado esperado>.
- Alternativa actual: qué hace HOY el usuario para resolverlo (esa es tu verdadera competencia).
-->

| | |
|---|---|
| Usuario principal |  Dueño o encargado de compras de una cafetería |
| Cliente (paga o decide) | decide comprar o no |
| Job to be done | Cuando necesito reabastecer café, quiero saber el mismo día el precio y si me entregan a tiempo, para decidir si le compro a Grano o a otro. |
| Alternativa actual | Queremos mejorar la experiencia del cliente al recibir una cotización mas acertada. |

## 4. Métricas  ⏱ 8 min

| Tipo | Métrica | Línea base | Meta | Plazo |
|---|---|---|---|---|
| North Star | % de cotizaciones entregadas en menos de 2 h con precio y fecha correctos | ≈ 0 % (26 h promedio, 30 % con error) | 80 % | 3 meses |
| Entrada | Tiempo promedio para cotizar | 26 h | < 2 h | 3 meses |
| Entrada | % de cotizaciones con error de precio o disponibilidad | 30 % | < 5 % | 3 meses |
| Guardrail | Ingreso mensual del canal B2B | $300,000 MXN | No baja de $300,000 MXN | 3 meses |

## 5. Alcance del MVP y no-objetivos  ⏱ 10 min

<!--
- Máximo 3 casos de uso. Si tienen 6, elijan los 3 que mueven la North Star.
- Cada caso de uso tiene un criterio de aceptación OBSERVABLE: algo que se puede comprobar
  sin leer el código ("el usuario recibe…", "el agente no…", "un humano aprueba…").
- No-objetivos: al menos 3 cosas razonables que decidieron NO hacer en el MVP, con el porqué.
  El no-objetivo más valioso es el que alguien del equipo sí quería hacer.
-->

### Casos de uso

| # | Caso de uso | Criterio de aceptación (observable) |
|---|---|---|
| CU1 | | |
| CU2 | | |
| CU3 | | |

### No-objetivos

| No vamos a… | Porque… |
|---|---|
| | |
| | |
| | |

## 6. AI Strategic Lens  ⏱ 7 min (deseable)

<!--
Seis preguntas. Contesten en una o dos líneas cada una.
Niveles de autonomía:
  0 = sugiere (el humano hace todo)
  1 = redacta (el humano revisa y aprueba cada acción)
  2 = actúa con límites (actúa solo debajo de un umbral; arriba, escala)
  3 = actúa solo
-->

| Lente | Respuesta |
|---|---|
| 1. ¿Por qué IA? ¿Una regla, un filtro o un formulario lo resolvería? | |
| 2. Datos y ventaja: ¿qué sabe Grano que un competidor con el mismo modelo no sabe? | |
| 3. Autonomía: nivel 0 a 3 y por qué | |
| 4. Costo del error: ¿qué pasa si se equivoca? ¿Es reversible? ¿Quién lo paga? | |
| 5. Humano en el circuito: ¿en qué momento y con qué umbral entra una persona? | |
| 6. Evaluación: ¿cómo sabrán que funciona antes de lanzarlo? | |

## 7. Riesgos, supuestos y preguntas abiertas  ⏱ 3 min (deseable)

<!--
- El supuesto más riesgoso: si es falso, el producto no sirve.
- Cómo lo validarían en 2 semanas o menos, sin escribir código.
- Preguntas abiertas para el CEO, para Legal o para los usuarios.
-->

**Supuesto más riesgoso:**

**Cómo lo validamos (≤ 2 semanas, sin código):**

**Riesgos:**

-

**Preguntas abiertas:**

-
