## 1. Resumen en una línea

Para el comprador que llega por primera vez a Grano y no entiende las fichas de los tostadores, **Brújula de Grano** es un guía de elección que traduce cada café a su forma de prepararlo y a referencias que ya conoce, y respalda su primera compra.
A diferencia del catálogo actual (64 cafés descritos en lenguaje de tostador) o de irse al súper, le dice **por qué ese café le va a gustar** y qué pasa si no le gusta.

## 2. Problema y evidencia

**Problema:**
El comprador nuevo no puede predecir si un café le va a gustar: las fichas describen el café con palabras que no usa ("lavado", "honey", "notas de jamaica") y no se conectan con lo que sí sabe (cómo lo prepara, qué toma hoy). Cuando arriesga y el café no coincide con lo que imaginó, deja de confiar en Grano y no vuelve. El problema no es solo elegir: es **confiar en que eligió bien**.

**Evidencia:**

- **3,100 búsquedas al mes sin resultados** con el vocabulario real del usuario: "suave", "no amargo", "para prensa francesa". El usuario sabe pedir; el catálogo no sabe responder.
- **58 % de rebote** en el catálogo y **41 % de carritos abandonados** entre compradores nuevos (que son el 64 % de 120,000 visitas al mes ≈ 76,800 visitas).
- **Recompra a 60 días de solo 19 %**: 4 de cada 5 compradores nuevos no regresan.
- **≈ 230 tickets al mes** preguntando "¿qué café me recomiendan?".
- *"Entré, vi 'notas de frutos rojos y panela' y no supe si me iba a gustar. Me fui al súper."* — Mariana, 29, primera visita.
- *"Pedí uno que decía 'floral' y me supo a té. No regresé."* — Paola, 31, compró una vez.

**Costo de no hacer nada (6 meses):**
- ≈ 461,000 visitas nuevas, de las que ≈ 267,000 rebotan en el catálogo.
- ≈ 18,600 búsquedas fallidas y ≈ 1,380 tickets de recomendación atendidos a mano.
- De cada 100 compradores nuevos que logramos adquirir, 81 se pierden antes de su segunda compra: pagamos la adquisición y no recuperamos el valor de vida.
- Los tostadores pequeños, invisibles en un catálogo que nadie entiende, empiezan a irse de la plataforma (riesgo de oferta).

## 3. Usuario, cliente y JTBD

| | |
|---|---|
| Usuario principal | Adulto de 25 a 40 años, primera o segunda visita a Grano, toma café a diario en casa con un método sencillo (prensa francesa, cafetera de goteo, moka). Hoy compra café de súper o de una cafetería cercana. Decide en una sola visita, desde el celular, en menos de 5 minutos. |
| Cliente (paga o decide) | Grano (CEO y Marketing deciden y financian). Cliente secundario: **el tostador**, que necesita que su café se descubra y se venda de forma justa. |
| Job to be done | Cuando entro por primera vez a una tienda de café de especialidad y no entiendo las descripciones, quiero que me digan en mis palabras cuál me va a gustar con lo que ya tengo en casa, para comprar sin miedo a tirar mi dinero y sentir que acerté. |
| Alternativa actual | Irse al súper o a la cafetería de siempre; elegir al azar por precio o foto; mandar un ticket y esperar respuesta; preguntarle a un amigo que "sabe de café". |

## 4. Métricas

| Tipo | Métrica | Línea base | Meta | Plazo |
|---|---|---|---|---|
| North Star | % de compradores nuevos que hacen una segunda compra en ≤ 60 días | 19 % | 26 % | 6 meses |
| Entrada | Búsquedas sin resultados al mes (vocabulario del usuario) | 3,100 | ≤ 600 | 3 meses |
| Entrada | % de compradores nuevos que responden "sí, me gustó" a su primer café (encuesta post-entrega de 1 pregunta) | Por medir (semana 0) | ≥ 75 % | 4 meses |
| Guardrail | Participación de tostadores pequeños en las recomendaciones vs. su participación en el catálogo | Por medir (semana 0) | No menor a su participación en el catálogo | Continuo |
| Guardrail | Atributos o sabores mostrados que no están en la ficha del tostador | — | 0 (auditoría semanal de muestra) | Continuo |
| Guardrail | Costo de IA por sesión de recomendación | — | ≤ $1.50 MXN | Continuo |

> Métrica de soporte (no North Star): abandono de carrito de nuevos 41 % → 33 % en 3 meses. La conversión de hoy importa, pero sin recompra solo compramos clientes de una vez.

## 5. Alcance del MVP y no-objetivos

### Casos de uso

| # | Caso de uso | Criterio de aceptación (observable) |
|---|---|---|
| CU1 | **Buscar con mis palabras.** El usuario escribe o elige "suave", "no amargo", "para prensa francesa", "como el de mi cafetería" y obtiene cafés que corresponden. | Las 30 búsquedas sin resultado más frecuentes del último mes devuelven al menos 3 cafés cada una. Cada resultado muestra una frase de "por qué aparece", y esa frase solo usa atributos presentes en la ficha del tostador. |
| CU2 | **Guía de 3 preguntas, sin registro.** ¿Cómo lo preparas? ¿Qué tomas hoy? ¿Cómo lo quieres (suave, intenso, dulce, ácido)? → 3 recomendaciones explicadas en lenguaje simple con una referencia conocida. | El usuario recibe 3 opciones en ≤ 3 preguntas y sin dar nombre, correo ni datos sensibles. Cada opción indica para qué método sirve y traduce las notas del tostador a lenguaje simple aprobado por el propio tostador. Si hay un café de tostador pequeño que cumple, al menos una de las 3 opciones lo incluye. |
| CU3 | **Red de seguridad del primer café.** Tras la entrega, se pregunta "¿te gustó?". Si la respuesta es no, se ofrece una alternativa ajustada y un reemplazo o crédito. | El comprador nuevo recibe la pregunta entre 7 y 10 días después de la entrega. Si responde "no", recibe en ese mismo momento una nueva recomendación que explica qué cambia ("menos ácido", "más cuerpo") y un crédito para su siguiente bolsa, sin hablar con nadie, hasta el monto límite. El costo lo absorbe Grano, nunca el tostador. |

### No-objetivos

| No vamos a… | Porque… |
|---|---|
| Construir un asistente de conversación abierta ("que platique") | Luis y otros no quieren hablar con un bot; las 3,100 búsquedas muestran que el usuario sabe pedir en pocas palabras. Platicar aumenta costo y riesgo de inventar sabores sin evidencia de que suba la recompra. Se revisa si el MVP muestra que hace falta. |
| Pedir cuenta, edad, salud u otros datos personales para recomendar | Restricción del segmento y fricción: el usuario nuevo se va antes de registrarse. Con método y gusto basta. |
| Reescribir las fichas de los tostadores | Las notas son del tostador y el agente no inventa atributos. Agregamos una capa de traducción que el tostador aprueba; la ficha original queda intacta. |
| Personalizar por historial de compras | El 64 % es nuevo: no hay historial. Se vuelve relevante para la recompra en una fase 2. |
| Permitir que los tostadores paguen por aparecer más en las recomendaciones | Rompe la confianza del comprador y el guardrail de equidad con tostadores pequeños. |
| Suscripciones o cajas de muestras en el MVP | Buena idea para la recompra, pero cambia logística y precios; no es necesaria para validar si traducir y respaldar sube la confianza. |

## 6. AI Strategic Lens

| Lente | Respuesta |
|---|---|
| 1. ¿Por qué IA? ¿Una regla, un filtro o un formulario lo resolvería? | Honestamente, gran parte sí: filtros por método y por gusto en lenguaje del usuario más la guía de 3 preguntas son reglas. La IA se justifica solo en dos lugares: entender búsquedas libres ("algo como el del Oxxo pero mejor") y proponer traducciones simples de las notas de 64 cafés, que el tostador aprueba. Luis tiene razón: primero filtros que sirvan. |
| 2. Datos y ventaja | Grano sabe qué café compró cada comprador nuevo y si le gustó o no (CU3). Esa relación entre "lo que pidió en sus palabras" y "lo que de verdad le gustó" no la tiene un competidor con el mismo modelo, y mejora cada recomendación. |
| 3. Autonomía | Nivel 1 para traducciones de notas (el tostador revisa y aprueba cada una). Nivel 2 para recomendaciones y crédito del CU3: actúa solo hasta un crédito por cliente y un monto límite; por encima, escala a una persona. |
| 4. Costo del error | Si recomienda un café que no gusta: una bolsa (reversible con crédito) y, sobre todo, la confianza del cliente nuevo (difícil de revertir). Lo paga Grano con el crédito; nunca el tostador ni el comprador. Si inventa un sabor: daño a la reputación del tostador; por eso solo usa atributos de la ficha. |
| 5. Humano en el circuito | El tostador aprueba cada traducción antes de publicarla. Soporte entra cuando un cliente pide un segundo crédito, cuando la búsqueda no encuentra nada con confianza suficiente, o cuando un tostador reporta una descripción incorrecta. |
| 6. Evaluación | Antes de lanzar: (a) set de prueba con las 3,100 búsquedas fallidas reales y respuestas esperadas de un barista; (b) cata a ciegas con 30 compradores nuevos que eligen con la guía y califican; (c) auditoría de 100 recomendaciones: 0 atributos fuera de ficha; (d) medir distribución por tamaño de tostador. |

## 7. Riesgos, supuestos y preguntas abiertas

**Supuesto más riesgoso:**
Que la gente no compra (y no vuelve) porque no entiende las fichas, y que traducir a su método y a referencias conocidas sí predice que el café le va a gustar. Si el motivo real es precio, envío o desconfianza en la tienda, este producto no mueve la North Star.

**Cómo lo validamos (≤ 2 semanas, sin código):**
- **Mago de Oz:** durante 2 semanas un barista responde los ≈ 230 tickets usando solo el guion de 3 preguntas y las fichas; medimos compra y "¿te gustó?".
- **10 fichas reescritas a mano** (aprobadas por sus tostadores) contra las originales; comparamos clics y agregados al carrito.
- **20 llamadas** a carritos abandonados de compradores nuevos: ¿por qué no compraste?

**Riesgos:**
- La traducción simplifica de más y vuelve a fallar la expectativa (caso "floral" → "a té").
- El sistema concentra ventas en tostadores grandes porque tienen más fichas y datos.
- El crédito del CU3 se abusa o erosiona margen.
- Los tostadores no aprueban traducciones a tiempo y el MVP se retrasa.
- El CEO espera un "bot que platica" y percibe el MVP como poco ambicioso.

**Preguntas abiertas:**
- CEO: ¿aceptas la recompra a 60 días como North Star aunque la conversión de hoy suba menos?
- Finanzas: ¿cuál es el monto máximo de crédito por primer café que Grano puede absorber?
- Legal: ¿qué condiciones necesita la garantía del primer café? ¿Qué responsabilidad hay si la traducción contradice al tostador?
- Tostadores: ¿cuánto tiempo pueden dedicar a aprobar traducciones? ¿Qué consideran una recomendación justa?
- Usuarios: ¿qué referencias conocen de verdad (cafetería, marca de súper) para usar como ancla?
