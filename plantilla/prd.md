# PRD · <nombre del producto>

> Mini-PRD de la Estación 2. Diseñado para llenarse en 45 minutos.
> Las secciones 1 a 5 son **obligatorias**; la 6 y la 7 son **deseables** (súmalas si les da el tiempo).
> Borra los comentarios `<!-- -->` cuando termines una sección.
> Regla de oro: **cero tecnologías en este documento**. Nada de React, LangChain, Postgres ni "un endpoint". Eso es el CÓMO y llega en la E5.

| Campo | Valor |
|---|---|
| Producto | <!-- nombre corto --> |
| Equipo | <!-- equipo-0N --> |
| Segmento | <!-- copia el segmento del brief --> |
| Track | <!-- PVB (cliente externo) o ISB (solución interna) --> |
| Autores | <!-- nombres y rol: facilitador, escriba, abogado del diablo... --> |
| Fecha | <!-- AAAA-MM-DD --> |
| Estado | Borrador |

---

## 1. Resumen en una línea  ⏱ 3 min

<!--
Formato:
Para <usuario> que <problema>, <producto> es un <categoría> que <beneficio clave>.
A diferencia de <lo que hacen hoy>, <diferenciador>.
Si no cabe en dos líneas, todavía no saben qué están construyendo.
-->

## 2. Problema y evidencia  ⏱ 7 min

<!--
- El problema en 2 o 3 frases, desde el punto de vista del usuario. Sin mencionar la solución.
- Evidencia: al menos 2 datos del brief y 1 cita de usuario.
- Costo de no hacer nada: ¿qué pasa si en 6 meses seguimos igual? Pónganle un número.
Prueba: si la frase "no tenemos un agente" aparece como problema, vuelvan a empezar.
-->

**Problema:**

**Evidencia:**

-
-
-

**Costo de no hacer nada:**

## 3. Usuario, cliente y JTBD  ⏱ 7 min

<!--
- Usuario: quién lo usa. Concreto: rol, contexto y frecuencia. "Todos los clientes" no es un usuario.
- Cliente: quién paga o decide que esto exista. A veces es otra persona.
- JTBD: Cuando <situación>, quiero <motivación>, para <resultado esperado>.
- Alternativa actual: qué hace HOY el usuario para resolverlo (esa es tu verdadera competencia).
-->

| | |
|---|---|
| Usuario principal | |
| Cliente (paga o decide) | |
| Job to be done | Cuando …, quiero …, para … |
| Alternativa actual | |

## 4. Métricas  ⏱ 8 min

<!--
- North Star: el valor que recibe el usuario y que predice el negocio. Una sola.
- Métricas de entrada: 2 palancas que el equipo puede mover y que empujan la North Star.
- Guardrail: lo que NO puede empeorar mientras optimizan (margen, CSAT, errores...).
Cada métrica lleva línea base (del brief), meta y plazo. Sin número no es métrica.
"Número de conversaciones con el agente" es vanidad: mide uso, no valor.
-->

| Tipo | Métrica | Línea base | Meta | Plazo |
|---|---|---|---|---|
| North Star | | | | |
| Entrada | | | | |
| Entrada | | | | |
| Guardrail | | | | |

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
