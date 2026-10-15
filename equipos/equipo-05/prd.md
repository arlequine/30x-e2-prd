# PRD · Grano Inventario al Día

> Mini-PRD de la Estación 2 · Equipo 05.
> Regla de oro: cero tecnologías en este documento. Define el QUÉ y el PORQUÉ, no el CÓMO.

| Campo | Valor |
|---|---|
| Producto | Grano Inventario al Día |
| Equipo | equipo-05 |
| Segmento | Operaciones: inventario y reabastecimiento con los tostadores |
| Track | ISB (solución interna) |
| Autores | Cristiam Martínez · Harold Campo · Oscar Cantero · Wilson Rivera · Rafael Nenninger · Jaime Díaz |
| Fecha | 2026-10-14 |
| Estado | Borrador |

---

## 1. Resumen en una línea

Para Rafa, el coordinador de operaciones que cada lunes persigue a 18 tostadores por WhatsApp para saber cuánto café les queda, Inventario al Día es un asistente interno que pide, lee y confirma el inventario por el mismo WhatsApp que los tostadores ya usan, y avisa antes de que un café se agote. A diferencia del Google Sheet semanal, el dato llega varias veces por semana sin que el tostador tenga que llenar otro sistema.

## 2. Problema y evidencia

**Problema:** Grano no sabe cuánto café le queda a cada tostador hasta que es tarde. El dato llega una vez por semana y a mano, así que la tienda sigue vendiendo cafés que ya se acabaron; el cliente paga, el pedido no se puede surtir y Soporte tiene que reembolsar. Cuando Rafa se entera de que algo se agotó, el tostador ya tostó esa semana y no alcanza a reponer.

**Evidencia:**

- 11 % de los pedidos (≈ 236 al mes) tienen un café agotado después de pagar; cada uno cuesta ≈ $120 MXN más un ticket de soporte. *(brief)*
- El inventario se actualiza 1 vez por semana, y 7 de los 18 tostadores no usan el Sheet: solo contestan por WhatsApp. Rafa dedica 4 h por semana a conciliarlo. *(brief)*
- El top 10 de cafés suma 23 días-producto agotados al mes. *(brief)*
- "Los lunes me la paso persiguiendo tostadores por WhatsApp para saber cuánto les queda." (Rafa, Operaciones)
- "Yo tuesto los martes. Si me avisan el jueves que se acabó, ya no llego." (tostador de Veracruz)

**Costo de no hacer nada:** en 6 meses serían ≈ 1.416 sobreventas, ≈ $170.000 MXN en reembolsos y cupones (236 × $120 × 6), ≈ 1.416 tickets que Karla llama "nuestros peores tickets" y ≈ 100 horas de Rafa conciliando a mano. Además, la tienda pierde ventas en los 23 días-producto que el top 10 pasa agotado cada mes.

## 3. Usuario, cliente y JTBD

| | |
|---|---|
| Usuario principal | **Rafa**, coordinador de operaciones (único en el equipo), que concilia inventario cada semana (hoy 4 h, sobre todo los lunes). **Usuario secundario:** los 18 tostadores, que reportan su inventario 1 vez por semana y no quieren otro sistema. |
| Cliente (paga o decide) | **Valeria, CEO**: decide el presupuesto y absorbe el costo de las sobreventas y de una orden de compra equivocada. |
| Job to be done | Cuando se acerca el día de tueste de cada tostador, quiero saber con certeza cuánto le queda de cada café, para avisarle a tiempo y que la tienda no venda lo que no existe. |
| Alternativa actual | Google Sheet semanal, más WhatsApp uno a uno con los 7 tostadores que no lo usan, más la memoria de Rafa. |

**Tensión usuario ↔ cliente:** Rafa quiere el dato más seguido y que el sistema actúe; Valeria no quiere que nada compre solo ("si se equivoca por 50 kilos, la que paga soy yo"); los tostadores no quieren llenar nada nuevo. El producto tiene que dar el dato sin pedirle esfuerzo al tostador y sin quitarle a una persona la decisión de compra.

## 4. Métricas

| Tipo | Métrica | Línea base | Meta | Plazo |
|---|---|---|---|---|
| North Star | % de pedidos con un café agotado después de pagar | 11 % (≈ 236/mes) | ≤ 3 % (≈ 65/mes) | 3 meses después del lanzamiento |
| Entrada | Tostadores que reportan inventario al menos 2 veces por semana | 0 de 18 (hoy es 1 vez por semana) | 16 de 18 | 6 semanas después del lanzamiento |
| Entrada | Horas de Rafa conciliando inventario | 4 h/semana | ≤ 1 h/semana | 6 semanas después del lanzamiento |
| Guardrail | Conversión de la tienda (no debe caer por cafés marcados como agotados por error) | 1,8 % | No baja de 1,8 % | Siempre |

> La North Star mide el valor (pedidos que sí se pueden surtir), no el uso del asistente. El guardrail evita "ganar" apagando cafés de más: si para cero sobreventas marcamos agotado lo que sí hay, perdemos ventas.

## 5. Alcance del MVP y no-objetivos

### Casos de uso

| # | Caso de uso | Criterio de aceptación (observable) |
|---|---|---|
| CU1 | **Pedir y registrar inventario por WhatsApp.** El día antes del tueste de cada tostador (y a mitad de semana) le llega un mensaje; responde con texto libre y el inventario queda registrado. | El tostador nunca abre otro sistema. Si la respuesta no trae unidad ("me quedan 5"), el asistente pregunta "¿5 bolsas de 250 g o 5 kilos?" **antes** de registrar. El tostador recibe un resumen ("Registré: Pluma 12 bolsas, Chiapas 0") y puede corregirlo. Ningún tostador ve el inventario de otro. |
| CU2 | **Dejar de vender lo que se acabó.** Cuando el inventario confirmado de un café llega a cero, la tienda lo muestra agotado. | Un café con 0 bolsas confirmadas no se puede pagar a más tardar 15 minutos después de la confirmación. El café vuelve a venderse cuando el tostador reporta existencias. |
| CU3 | **Avisar a tiempo para reabastecer.** Si con el ritmo de venta un café se va a agotar antes del próximo día de tueste, Rafa recibe un aviso con una cantidad sugerida. | El aviso llega **antes** del día de tueste del tostador (ej.: si tuesta el martes, el aviso sale a más tardar el lunes). La sugerencia se envía al tostador solo cuando Rafa la aprueba; ninguna orden sale sin su clic. |

### No-objetivos

| No vamos a… | Porque… |
|---|---|
| Generar ni enviar órdenes de compra de forma automática, ni siquiera las menores de $5.000 MXN | La CEO lo descartó y un error de 50 kg lo paga Grano. Es lo que Rafa sí quería: lo dejamos para cuando el asistente lleve meses de aciertos medidos. |
| Darles a los tostadores un portal, una app o un formulario nuevo | "No voy a llenar otro sistema" (tostadora de Oaxaca). Si el reporte cuesta esfuerzo, no llega el dato y no hay producto. |
| Integrarnos con los sistemas de los tostadores | La restricción del segmento es que solo hay WhatsApp y el Sheet. |
| Pronosticar la demanda por temporada o por campaña | Con un dato que hoy llega 1 vez por semana, primero hay que tenerlo a tiempo; el pronóstico viene después. |
| Mostrar comparativos o rankings de inventario entre tostadores | El inventario de cada tostador es confidencial frente a los demás. |

## 6. AI Strategic Lens

| Lente | Respuesta |
|---|---|
| 1. ¿Por qué IA? ¿Una regla, un filtro o un formulario lo resolvería? | **Casi todo es regla.** El recordatorio es una plantilla programada, pausar un café en cero es una regla y la cantidad sugerida sale de "venta promedio × días hasta el próximo tueste". La IA solo hace falta para **leer respuestas libres de WhatsApp** ("me quedan como 5 del Pluma y el Chiapas ya volé") de los 7 tostadores que no usan el Sheet y de los que prefieren escribir. |
| 2. Datos y ventaja: ¿qué sabe Grano que un competidor con el mismo modelo no sabe? | El historial de ventas por café, el calendario de tueste de cada uno de los 18 tostadores y la relación directa por WhatsApp con ellos. |
| 3. Autonomía: nivel 0 a 3 y por qué | **Nivel 2 para registrar inventario:** registra solo cuando el mensaje es claro (cantidad, unidad y café identificados); si no, pregunta o escala. **Nivel 1 para el reabastecimiento:** redacta la sugerencia y Rafa aprueba cada una. Nunca hay nivel 3. |
| 4. Costo del error: ¿qué pasa si se equivoca? ¿Es reversible? ¿Quién lo paga? | Leer "5 kilos" como "5 bolsas" causa una sobreventa (≈ $120 + un ticket, lo paga Grano) o un falso agotado (venta perdida, la pagan Grano y el tostador). El registro es reversible: el tostador ve el resumen y lo corrige. Una orden de compra mal hecha **no** es reversible, y por eso no la decide el asistente. |
| 5. Humano en el circuito: ¿en qué momento y con qué umbral entra una persona? | Rafa confirma el registro cuando: (a) el mensaje no trae unidad y el tostador no contestó en 2 h; (b) la cantidad cambia más de 50 % frente al reporte anterior sin ventas que lo expliquen; (c) el registro deja un café con pedidos ya pagados en negativo. Rafa aprueba **toda** sugerencia de compra, y las mayores de $5.000 MXN requieren además la aprobación que define la regla de Grano. |
| 6. Evaluación: ¿cómo sabrán que funciona antes de lanzarlo? | Antes de lanzar: 100 mensajes reales de inventario del WhatsApp de Rafa, con la cantidad correcta anotada a mano. Meta: ≥ 95 % leídos bien y 100 % de los mensajes sin unidad detectados como ambiguos (pregunta en vez de adivinar). Después, un piloto de 4 semanas con los 7 tostadores que solo usan WhatsApp. **Costo:** ≈ 18 tostadores × 3 mensajes por semana ≈ 230 mensajes al mes; estimamos que queda muy por debajo de los $40.000 MXN, pero el número exacto lo confirman los devs. |

## 7. Riesgos, supuestos y preguntas abiertas

**Supuesto más riesgoso:** los tostadores contestan un WhatsApp al menos 2 veces por semana con un dato confiable. Si no contestan, no hay producto, con o sin IA.

**Cómo lo validamos (≤ 2 semanas, sin código):** durante 2 semanas, Rafa manda a mano la misma plantilla los lunes y los jueves a los 18 tostadores y actualiza el Sheet con lo que respondan. Medimos la tasa de respuesta, el tiempo de respuesta y cuántas respuestas vienen sin unidad, y comparamos las sobreventas de esas 2 semanas con la línea base.

**Riesgos:**

- El tostador vende por fuera (Instagram, su local) entre un reporte y otro, y el inventario baja sin que Grano lo sepa.
- Fuera de la ventana de 24 h solo se pueden mandar plantillas aprobadas por Meta; los recordatorios dependen de que esa aprobación salga.
- Que un tostador reciba por error el inventario de otro rompe la confidencialidad y la relación.
- Falsos agotados por exceso de cautela (los vigila el guardrail).

**Preguntas abiertas:**

- ¿Quién aprueba las compras mayores de $5.000 MXN: Rafa o Valeria?
- ¿La sobreventa la absorbe Grano o se le descuenta al tostador? Eso cambia cuánto le importa reportar a tiempo.
- ¿Cuál es la unidad estándar de inventario (bolsa de cuántos gramos, o kilos de café tostado)?
