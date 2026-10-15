# PRD · <nombre del producto>


> Mini-PRD de la Estación 2. Diseñado para llenarse en 45 minutos.
> Las secciones 1 a 5 son **obligatorias**; la 6 y la 7 son **deseables** (súmalas si les da el tiempo).
> Borra los comentarios `<!-- -->` cuando termines una sección.
> Regla de oro: **cero tecnologías en este documento**. Nada de React, LangChain, Postgres ni "un endpoint". Eso es el CÓMO y llega en la E5.


| Campo | Valor |
|---|---|
| Producto | <!-- nombre corto --> |
| Equipo | equipo-02 |
| Segmento | Suscriptor de Grano Club que gestiona su suscripción |
| Track | PVB (cliente externo) |
| Autores | <!-- nombres y rol: facilitador, escriba, abogado del diablo... --> |
| Fecha | 2026-10-14 |
| Estado | Borrador |


---


## 1. Resumen en una línea  ⏱ 3 min


<!--
Formato:
Para <usuario> que <problema>, <producto> es un <categoría> que <beneficio clave>.
A diferencia de <lo que hacen hoy>, <diferenciador>.
Si no cabe en dos líneas, todavía no saben qué están construyendo.
-->
Para la compañía es un problema no cumplir la meta de churn mensual. Hoy se tiene 11% de churn y debería ser 6%.


## 2. Problema y evidencia  ⏱ 7 min


<!--
- El problema en 2 o 3 frases, desde el punto de vista del usuario. Sin mencionar la solución.
- Evidencia: al menos 2 datos del brief y 1 cita de usuario.
- Costo de no hacer nada: ¿qué pasa si en 6 meses seguimos igual? Pónganle un número.
Prueba: si la frase "no tenemos un agente" aparece como problema, vuelvan a empezar.
-->


**Problema:**
Los suscriptores de Grano Club cancelan su suscripción porque el café recibido no siempre se ajusta a sus preferencias y además se les dificulta gestionar los cambios de su suscripción.
**Evidencia:**


- Motivo de cancelación: "me llegó un café que no me gustó" - 38 % usuarios
- Motivo: "se me acumula el café" - 27 % usuarios
- Motivo: precio - 19 %


**Costo de no hacer nada:**
- El costo que tenemos de no tomar acciones es que los usuarios se vayan y en 6 meses se perderia aproximadamente la mitad de los suscriptores.


## 3. Usuario, cliente y JTBD  ⏱ 7 min


<!--
- Usuario: quién lo usa. Concreto: rol, contexto y frecuencia. "Todos los clientes" no es un usuario.
- Cliente: quién paga o decide que esto exista. A veces es otra persona.
- JTBD: Cuando <situación>, quiero <motivación>, para <resultado esperado>.
- Alternativa actual: qué hace HOY el usuario para resolverlo (esa es tu verdadera competencia).
-->


| | |
|---|---|
| Usuario principal | | Suscriptor
| Cliente (paga o decide) | | CEO - Grano Club
| Job to be done | Cuando …, quiero …, para … | Adaptar la suscripción para ser más flexible y se pueda gestionar de manera fácil y rápida.
| Alternativa actual | | Comunicación directa por whatsapp y atención manual de las peticiones.


## 4. Métricas  ⏱ 8 min


<!--
- North Star: el valor que recibe el usuario y que predice el negocio. Una sola.
- Métricas de entrada: 2 palancas que el equipo puede mover y que empujan la North Star.
- Guardrail: lo que NO puede empeorar mientras optimizan (margen, CSAT, errores...).
Cada métrica lleva línea base (del brief), meta y plazo. Sin número no es métrica.
"Número de conversaciones con el agente" es vanidad: mide uso, no valor.
-->


North Star — Churn: queremos que menos clientes abandonen Grano Club.


Entrada 1 — Tiempo de resolución: buscamos eliminar la demora que genera frustración.


Entrada 2 — Autogestión: queremos que el cliente resuelva sus necesidades sin depender de soporte.


Guardrail — Cancelación libre: debemos evitar que el agente reduzca artificialmente el churn al dificultar las cancelaciones.


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
| CU1 |El usuario puede pausar la suscripción|El usuario recibe una confirmación con el periodo de pausa para poder confirmar el cambio |
| CU2 |El usuario puede cambiar el tipo de café que le va a llegar| El usuario recibe una confirmación |
| CU3 | | |


### No-objetivos


| Bajar más del 15% el precio por una única vez | Porque sale del margen de Grano Club |
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
