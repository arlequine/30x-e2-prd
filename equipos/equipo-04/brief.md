# Brief · Equipo 04 · Soporte post-venta

**Segmento:** el equipo de soporte de Grano (3 personas) y los tickets que atiende después de la venta: rastreo, daños y reembolsos.
**Track:** ISB (solución interna). **Lee también:** `contexto/grano-hoy.md`.

## Contexto

Soporte recibe 1,900 tickets al mes con 3 personas. La primera respuesta tarda 9 horas y el CSAT es de 3.9. Un tercio de los tickets es "¿dónde está mi pedido?", que se resuelve copiando el estatus de la paquetería. Los reembolsos se deciden "a ojo". El CEO quiere "un agente que conteste los tickets". Marisol, Head de Operaciones, es quien decide si el producto se queda.

## Lo que escuchamos (entrevistas)

1. Karla, de Soporte: "El '¿dónde está mi pedido?' me come la mañana. Es copiar la guía de la paquetería y pegarla."
2. Beto, de Soporte: "Los reembolsos los decido a ojo. A veces siento que me están viendo la cara."
3. Cliente: "Mi bolsa llegó rota y me pidieron foto, ticket y video. Me cansé."
4. Cliente: "Prefiero que me conteste un bot en 1 minuto que una persona en 9 horas."
5. Marisol, Head de Operaciones: "Si un bot regala reembolsos, lo apago al día siguiente."

## Datos

| Dato | Valor |
|---|---|
| Tickets al mes | 1,900 · 34 % "¿dónde está mi pedido?" · 18 % daños y reembolsos |
| Primera respuesta | 9 h promedio |
| CSAT | 3.9 / 5 |
| Reembolsos pagados | $58,000 MXN al mes |
| Reclamos de clientes con más de 2 reclamos en 90 días | 6 % de los reembolsos |
| Costo de un ticket atendido por una persona | ≈ $45 MXN |

## Restricciones de tu segmento

- Política actual: reembolsos mayores a $500, o de clientes con más de 2 reclamos en 90 días, los aprueba una persona.
- La API de la paquetería da el estatus pero no garantiza fechas: nadie promete un día de entrega.
- El agente no tiene acceso a datos de tarjetas.

## Preguntas guía

1. ¿Su usuario es el **cliente** que escribe o **Karla y Beto**? Cambia todo el PRD; elijan.
2. ¿Qué parte del "¿dónde está mi pedido?" necesita IA y qué parte es una consulta a la paquetería?
3. ¿Qué nivel de autonomía tiene el agente con los reembolsos? ¿Cuál es el umbral exacto?
4. ¿Cuál es el guardrail que dejaría tranquila a Marisol?
5. ¿Cómo evalúan, antes de lanzar, que el agente no regala dinero ni ofende a un cliente?

## Entregable

`equipos/equipo-04/prd.md` con las secciones 1 a 5 completas (6 y 7 si les da el tiempo), entregado como Pull Request a las **8:35 pm COT**.

## Prompt para Claude (voz del usuario)

```text
Actúa como Karla, agente de soporte en un e-commerce de café con 1,900 tickets al mes y
solo 3 personas en el equipo. Responde mis preguntas como ella: cuéntame cómo es un día
normal, qué te frustra y qué haces a mano, sin proponer soluciones. Si te pregunto algo
que ella no sabría, dilo. Espera mi primera pregunta.
```
