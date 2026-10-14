# Brief · Equipo 02 · Suscriptor de Grano Club

**Segmento:** la persona suscrita a Grano Club (una bolsa al mes) que quiere pausar, cambiar su café o su dirección.
**Track:** PVB (cliente externo). **Lee también:** `contexto/grano-hoy.md`.

## Contexto

Grano Club salió en julio y ya tiene 820 suscriptores, pero pierde el 11 % cada mes (la meta es 6 %). Hoy, para cualquier cambio, el suscriptor escribe por WhatsApp o correo y espera a que alguien de soporte lo atienda a mano. Finanzas dice que la suscripción es el negocio más rentable de Grano. El CEO quiere "un agente en WhatsApp que retenga gente".

## Lo que escuchamos (entrevistas)

1. "Quería pausar un mes porque me iba de viaje. Tardaron en contestar y mejor cancelé." (Andrea, 35, ex-suscriptora)
2. "Me gustaría decirle 'el de este mes estuvo muy ácido' y que el siguiente sea distinto." (Raúl, 41)
3. "Todo por WhatsApp, por favor. No voy a bajar otra app." (Sofía, 28)
4. "Si me ofrecen 20 % para quedarme, me quedo… y cancelo al mes siguiente." (Daniel, 33)
5. Laura, de Finanzas: "Cada descuento de retención sale de nuestro margen, no del del tostador."

## Datos

| Dato | Valor |
|---|---|
| Suscriptores activos | 820 |
| Churn mensual | 11 % (meta: ≤ 6 %) |
| Tickets de cambios de suscripción | ≈ 270 al mes · resolución promedio: 22 h |
| Motivo de cancelación: "me llegó un café que no me gustó" | 38 % |
| Motivo: "se me acumula el café" | 27 % |
| Motivo: precio | 19 % |
| Prefieren WhatsApp como canal (encuesta) | 72 % |
| Valor de vida: suscriptor vs. comprador único | $3,900 vs. $910 MXN |

## Restricciones de tu segmento

- Política comercial: descuento de retención máximo de 15 %, una vez por cliente al año.
- Cancelar, o cambiar el método de pago, requiere confirmación explícita del cliente.
- WhatsApp: fuera de la ventana de 24 h solo se envían plantillas aprobadas.

## Preguntas guía

1. ¿La gente se va por el **café**, por la **fricción** o por el **precio**? ¿Cuál ataca su MVP y cuál deja fuera?
2. ¿El agente puede ofrecer descuentos? ¿Con qué umbral? Piensen en Daniel.
3. Si la North Star es "churn", ¿cómo evitan que el agente simplemente dificulte cancelar?
4. ¿Qué pasa si el agente entiende "pausa" cuando el cliente dijo "cancela"? ¿Es reversible?
5. ¿Pausar en 1 minuto requiere IA, o basta con un botón?

## Entregable

`equipos/equipo-02/prd.md` con las secciones 1 a 5 completas (6 y 7 si les da el tiempo), entregado como Pull Request a las **8:35 pm COT**.

## Prompt para Claude (voz del usuario)

```text
Actúa como Andrea, 35 años, que estaba suscrita a un club de café por WhatsApp y canceló
porque quería pausar un mes y nadie le contestó a tiempo. Responde mis preguntas como ella:
concreta, un poco molesta, sin proponer soluciones. Si te pregunto algo que ella no sabría,
dilo. Espera mi primera pregunta.
```
