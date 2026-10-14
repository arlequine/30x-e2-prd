# Brief · Equipo 03 · Cafeterías B2B

**Segmento:** cafeterías que le compran a Grano café por kilo (mayoreo) para servirlo en su barra.
**Track:** PVB (cliente externo). **Lee también:** `contexto/grano-hoy.md`.

## Contexto

Sin planearlo, Grano empezó a venderle a cafeterías. Hoy son 35 y ya representan el 22 % del GMV. Todo pasa por WhatsApp y un Excel: la cafetería pide una cotización, Ana o Toño (ventas) consultan disponibilidad con el tostador, calculan el precio por volumen y contestan. Hay 9 cafeterías en lista de espera porque "no damos abasto". El CEO quiere "un agente que cotice solo".

## Lo que escuchamos (entrevistas)

1. "Necesito saber hoy si me surtes 15 kilos de Chiapas para el lunes. Si no, le compro a otro." (Dueño de cafetería, Guadalajara)
2. "El precio cambia según quién me conteste el WhatsApp." (Barista jefa, CDMX)
3. "Quiero mis facturas sin pedirlas tres veces." (Administradora de cafetería, Puebla)
4. Toño, de Ventas: "La mitad del trabajo es negociar. Si un bot da el precio de lista, perdemos a los mejores clientes."
5. Un tostador de Veracruz: "Para mayoreo necesito 5 días para tostar. No me prometan en 2."

## Datos

| Dato | Valor |
|---|---|
| Cafeterías activas | 35 · más 9 en lista de espera |
| Participación en el GMV | 22 % (≈ $300,000 MXN al mes) |
| Tiempo promedio para cotizar | 26 h |
| Cotizaciones con error de precio o de disponibilidad | 30 % |
| Pedido B2B promedio | 12 kg |
| Tiempo de ventas dedicado a cotizar | 60 % de 2 personas |

## Restricciones de tu segmento

- Precio por volumen en 3 niveles (1–9 kg, 10–24 kg, 25 kg o más). Cualquier precio fuera de la tabla requiere aprobación de Ventas.
- La disponibilidad depende de la capacidad semanal de cada tostador (tuestan 1 o 2 días por semana).
- Grano no da crédito: el pedido se paga antes de tostar.

## Preguntas guía

1. ¿El dolor de la cafetería es el **precio**, la **velocidad** o la **certeza** de que le van a surtir?
2. ¿Quién es su usuario: la cafetería o Ventas? Elijan uno y justifiquen.
3. ¿El agente cotiza solo, o redacta y Ventas aprueba? ¿Con qué umbral?
4. ¿Qué no van a hacer? (Facturas, negociación, crédito…)
5. ¿Qué pasa si el agente promete 15 kg para el lunes y el tostador no puede? ¿Quién paga?

## Entregable

`equipos/equipo-03/prd.md` con las secciones 1 a 5 completas (6 y 7 si les da el tiempo), entregado como Pull Request a las **8:35 pm COT**.

## Prompt para Claude (voz del usuario)

```text
Actúa como Memo, dueño de una cafetería en Guadalajara que compra 12 kg de café al mes por
WhatsApp a un marketplace de tostadores. Responde mis preguntas como él: práctico, con
prisa, con ejemplos de su operación diaria y sin proponer soluciones. Si te pregunto algo
que él no sabría, dilo. Espera mi primera pregunta.
```
