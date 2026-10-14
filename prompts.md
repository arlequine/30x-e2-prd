# Prompts para trabajar con Claude en la sala

**Regla del ejercicio:** Claude **entrevista y critica**; el equipo **decide y escribe**.
No le pidan "escríbeme el PRD". Un PRD que no pensaron ustedes no lo van a poder defender en la plenaria, y la plenaria es justo eso: defenderlo.

Peguen primero el contexto (`contexto/grano-hoy.md` y su `brief.md`) y después el prompt.

## 1. Voz del usuario · rol: voz del usuario

Está al final de su `brief.md`. Úsenlo para **entrevistar** a la persona: pregunten por hechos ("¿qué hiciste la última vez que…?"), no por opiniones ("¿te gustaría un agente?").

## 2. Prueba de la regla · lente 1

```text
Este es nuestro problema y nuestros casos de uso: <pega las secciones 2 y 5>.
Para cada caso de uso, dime si se puede resolver sin IA (con una regla, un filtro, un
formulario o una plantilla) y qué se perdería. Sé honesto: si no hace falta IA, dilo.
No propongas tecnologías.
```

## 3. Revisor de métricas · rol: analista de negocio

```text
Estas son nuestras métricas: <pega la sección 4>.
Para cada una dime: ¿es de valor o de vanidad? ¿La puede mover el equipo? ¿Tiene línea
base y meta? Luego dime qué podría salir mal si optimizamos solo la North Star, y si
nuestro guardrail lo detectaría.
```

## 4. Abogado del diablo · rol: abogado del diablo

```text
Actúa como Valeria, CEO de Grano: escéptica, con poco presupuesto y poca paciencia.
Lee nuestro PRD: <pega el PRD>.
Hazme las 3 preguntas más incómodas que harías antes de aprobarlo. No reescribas el PRD y
no me des las respuestas.
```

## 5. Revisión contra la rúbrica · al final (8:30)

```text
Esta es la rúbrica: <pega rubrica.md>. Este es nuestro PRD: <pega el PRD>.
Califica cada criterio de 1 a 3 citando la frase del PRD que lo justifica, y dime la
única mejora que más puntos nos daría en 5 minutos. No reescribas el PRD.
```

> Después de clase: si usan Claude Code en este repo, el skill `prd-review` hace esta revisión por ustedes (ver el README).
