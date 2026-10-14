# Brief · Equipo 05 · Operaciones e inventario

**Segmento:** Rafa, coordinador de operaciones, y los 18 tostadores que surten a Grano: inventario y reabastecimiento.
**Track:** ISB (solución interna). **Lee también:** `contexto/grano-hoy.md`.

## Contexto

En la demo de la E1 agregamos inventario a la API (v1.1), pero el dato sigue llegando a mano: los tostadores actualizan un Google Sheet una vez por semana, o se lo mandan a Rafa por WhatsApp. Grano vende café que ya no existe. El 11 % de los pedidos tiene un café agotado después de pagar. El CEO quiere "un agente que maneje el inventario".

## Lo que escuchamos (entrevistas)

1. Rafa, de Operaciones: "Los lunes me la paso persiguiendo tostadores por WhatsApp para saber cuánto les queda."
2. Un tostador de Veracruz: "Yo tuesto los martes. Si me avisan el jueves que se acabó, ya no llego."
3. Una tostadora de Oaxaca: "No voy a llenar otro sistema. Mándame un mensaje y te contesto."
4. Valeria, CEO: "No quiero un agente que haga órdenes de compra solo. Si se equivoca por 50 kilos, la que paga soy yo."
5. Karla, de Soporte: "Las sobreventas son nuestros peores tickets."

## Datos

| Dato | Valor |
|---|---|
| Pedidos con un café agotado después de pagar | 11 % (≈ 236 al mes) |
| Costo de cada sobreventa | ≈ $120 MXN (reembolso parcial + cupón) más un ticket de soporte |
| Frecuencia de actualización del inventario | 1 vez por semana (Google Sheet) |
| Tostadores que no usan el Sheet y solo contestan por WhatsApp | 7 de 18 |
| Tiempo de Rafa conciliando inventario | 4 h por semana |
| Días-producto agotados en el top 10 de cafés | 23 al mes |

## Restricciones de tu segmento

- No hay integración con los sistemas de los tostadores: solo WhatsApp y el Sheet.
- Las órdenes de compra mayores a $5,000 MXN requieren aprobación de una persona.
- El inventario de un tostador es confidencial frente a los demás tostadores.

## Preguntas guía

1. ¿El problema es **saber** cuánto hay, **avisar** a tiempo o **decidir** cuánto pedir?
2. ¿Quién es el usuario: Rafa o los tostadores? ¿Y quién es el cliente?
3. ¿Qué autonomía tiene el agente? Lean otra vez la cita 4.
4. ¿Qué pasa si el agente lee mal un WhatsApp ("me quedan 5" ¿bolsas o kilos?)? ¿Cuánto cuesta ese error?
5. ¿Qué se resuelve sin IA (una plantilla de WhatsApp, un recordatorio) y qué sí la necesita?

## Entregable

`equipos/equipo-05/prd.md` con las secciones 1 a 5 completas (6 y 7 si les da el tiempo), entregado como Pull Request a las **8:35 pm COT**.

## Prompt para Claude (voz del usuario)

```text
Actúa como Rafa, coordinador de operaciones de un marketplace de café que depende de 18
microtostadores para saber cuánto inventario hay. Responde mis preguntas como él: cuéntame
tu semana, qué haces a mano y qué sale mal, sin proponer soluciones. Si te pregunto algo
que él no sabría, dilo. Espera mi primera pregunta.
```
