# Brief · Equipo 01 · Comprador nuevo

**Segmento:** la persona que llega por primera vez a Grano y no sabe qué café elegir.
**Track:** PVB (cliente externo). **Lee también:** `contexto/grano-hoy.md`.

## Contexto

El 64 % de las visitas a Grano son de gente nueva. El catálogo pasó de 6 a 64 cafés y las fichas usan el lenguaje de los tostadores: "lavado", "honey", "notas de jamaica y panela". Marketing cree que el catálogo asusta. El CEO cree que un agente que "platique" con el comprador va a subir la conversión.

## Lo que escuchamos (entrevistas)

1. "Entré, vi 'notas de frutos rojos y panela' y no supe si me iba a gustar. Me fui al súper." (Mariana, 29, primera visita)
2. "Tengo una prensa francesa y ya. No quiero aprender de procesos." (Jorge, 34)
3. "Pedí uno que decía 'floral' y me supo a té. No regresé." (Paola, 31, compró una vez)
4. "Me encantaría que alguien me dijera: si te gusta el de la cafetería de la esquina, empieza por este." (Iván, 26)
5. "No quiero hablar con un bot. Quiero filtros que sirvan." (Luis, 38)
6. Un tostador de Oaxaca: "Si el sistema siempre recomienda a los tostadores grandes, yo no vendo."

## Datos

| Dato | Valor |
|---|---|
| Visitantes nuevos | 64 % de 120,000 visitas al mes |
| Rebote en el catálogo | 58 % |
| Carritos abandonados (compradores nuevos) | 41 % |
| Búsquedas sin resultados ("suave", "no amargo", "para prensa francesa") | 3,100 al mes |
| Tickets "¿qué café me recomiendan?" | ≈ 230 al mes |
| Recompra a 60 días de compradores nuevos | 19 % |

## Restricciones de tu segmento

- Las notas de cata son las que escribe el tostador. El agente no inventa sabores ni atributos.
- No se piden datos personales sensibles para recomendar.
- Costo de IA estimado: ≤ $1.50 MXN por sesión de recomendación.

## Preguntas guía

1. ¿El problema es **elegir** o es **confiar** en lo que eligió? ¿Qué cambia en cada caso?
2. Luis no quiere un bot. ¿Esto se resuelve con mejores filtros? Respondan honestamente la lente 1.
3. ¿Qué número le importa más a Grano: la conversión de hoy o la recompra a 60 días? ¿Cuál es su North Star?
4. El tostador también es su cliente. ¿Qué guardrail lo protege?
5. ¿Qué pasa si el agente recomienda un café que no le gusta a la persona? ¿Quién paga ese error?

## Entregable

`equipos/equipo-01/prd.md` con las secciones 1 a 5 completas (6 y 7 si les da el tiempo), entregado como Pull Request a las **8:35 pm COT**.

## Prompt para Claude (voz del usuario)

```text
Actúa como Mariana, 29 años, que entró por primera vez a una tienda en línea de café de
especialidad y se fue sin comprar porque no entendió las notas de cata. Responde mis
preguntas como ella: con detalles concretos de su vida, sin jerga y sin proponer soluciones.
Si te pregunto algo que ella no sabría, dilo. Espera mi primera pregunta.
```
