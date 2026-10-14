# PRD · Grano, tienda en línea v1

> **Ejemplo resuelto.** Es el PRD de la tienda que construimos en la demo de la E1, reescrito con la plantilla de la E2.
> Sirve de referencia de **nivel y forma**. Su producto de hoy es otro (Grano Asistente), así que no copien el contenido.
> Las notas al margen (`> 💡`) explican por qué cada sección está escrita así.

| Campo | Valor |
|---|---|
| Producto | Grano · tienda en línea v1 |
| Equipo | Demo E1 |
| Segmento | Bebedor curioso de café que compra en línea por primera vez |
| Track | PVB (cliente externo) |
| Autores | Mentor (demo E1) |
| Fecha | 2026-04-01 |
| Estado | Aprobado; en producción desde abril de 2026 |

---

## 1. Resumen en una línea

Para el bebedor curioso que quiere probar café de especialidad pero no entiende la jerga ni sabe cuánto va a pagar, Grano es una tienda en línea de microtostadores que explica cada café en lenguaje simple y muestra el total real antes de pagar. A diferencia del supermercado y de las tiendas de cada tostador, reúne a varios tostadores con la misma experiencia de compra.

> 💡 Tiene usuario, problema, categoría, beneficio y contra quién compite. Si quitas una pieza, la frase deja de decidir algo.

## 2. Problema y evidencia

**Problema:** el bebedor curioso quiere salir del café de supermercado, pero las tiendas de especialidad le hablan en jerga ("lavado", "honey", "notas de panela") y no le dicen el costo total hasta el último paso. Termina comprando lo de siempre o abandona el carrito.

**Evidencia:**

- En 12 entrevistas, 9 personas dijeron que "no saben qué café elegir" en una tienda de especialidad.
- 5 de 6 microtostadores entrevistados no tienen tienda en línea; venden por Instagram y WhatsApp.
- "Me salió en $480 el café y luego $150 de envío. Lo dejé ahí." (Mariana, 29)

**Costo de no hacer nada:** los microtostadores siguen vendiendo uno a uno por Instagram y el bebedor curioso sigue en el supermercado. El mercado existe, pero nadie lo junta.

> 💡 El problema no menciona la solución. "No hay una tienda de microtostadores" sería una solución disfrazada de problema.

## 3. Usuario, cliente y JTBD

| | |
|---|---|
| Usuario principal | Bebedor curioso de 25 a 40 años que compra 1 o 2 bolsas al mes y prepara en casa (prensa francesa, V60 o moka) |
| Cliente (paga o decide) | El usuario paga su pedido; el microtostador paga a Grano 25 % de comisión por venta. **Grano tiene dos clientes.** |
| Job to be done | Cuando quiero probar un café mejor que el del súper, quiero entender qué voy a recibir y cuánto voy a pagar, para comprar sin miedo a equivocarme |
| Alternativa actual | Café de supermercado o mandar DM al tostador por Instagram |

> 💡 Usuario ≠ cliente. Si el tostador no vende, se va; por eso el catálogo respeta sus notas de cata tal cual.

## 4. Métricas

| Tipo | Métrica | Línea base | Meta | Plazo |
|---|---|---|---|---|
| North Star | Pedidos completados al mes | 0 (lanzamiento) | 100 | Primer mes |
| Entrada | Conversión visita → pedido | n/a (benchmark del sector: 1.5 %) | ≥ 2 % | Primer mes |
| Entrada | Ticket promedio | n/a | ≥ $600 MXN | Primer mes |
| Guardrail | Pedidos con total distinto al mostrado en el carrito | n/a | 0 | Siempre |

> 💡 El guardrail cuida la promesa central ("el total real antes de pagar"). Si se rompe, el producto pierde su razón de existir aunque los pedidos suban.

## 5. Alcance del MVP y no-objetivos

### Casos de uso

| # | Caso de uso | Criterio de aceptación (observable) |
|---|---|---|
| CU1 | Explorar el catálogo y entender cada café | Cada café muestra origen, tostador, precio y notas de cata en lenguaje simple |
| CU2 | Armar el carrito y ver el total real | El total incluye envío: $99, o gratis desde $600. 2 Huila + 1 Chiapas con `BIENVENIDA10` = **$837** con envío gratis |
| CU3 | Aplicar el cupón de bienvenida | `BIENVENIDA10` descuenta 10 %; un cupón inválido muestra un mensaje y no cambia el total |

### No-objetivos

| No vamos a… | Porque… |
|---|---|
| Hacer cuentas de usuario ni login | Queremos medir si compran antes de pedirles un registro |
| Hacer suscripciones | Primero hay que probar la compra única; la suscripción depende de la recompra |
| Dar a los tostadores un panel para editar su catálogo | Con 6 cafés, el catálogo se mantiene a mano en un CSV |
| Manejar inventario | Riesgo aceptado para el MVP. Llegó en la v1.1 (lo vimos en el D6 de la demo) |

> 💡 Cada criterio se puede comprobar sin leer código. El $837 se volvió un test automático en la demo: así un PRD alimenta directamente al agente.

## 6. AI Strategic Lens

| Lente | Respuesta |
|---|---|
| 1. ¿Por qué IA? | **La tienda no usa IA.** Catálogo, carrito y cupón se resuelven con reglas. La IA estuvo en cómo la construimos (Claude Code), no en el producto. |
| 2. Datos y ventaja | Notas de cata y relación directa con los tostadores: un dato propio que crece con cada tostador nuevo |
| 3. Autonomía | No aplica (no hay agente en el producto) |
| 4. Costo del error | Un total mal calculado cobra de más o de menos y rompe la confianza. Por eso hay tests en la API |
| 5. Humano en el circuito | El equipo de Grano revisa cada pedido antes de enviarlo a los tostadores |
| 6. Evaluación | 19 tests de API y un E2E con Playwright que compra el caso de $837 en producción |

> 💡 Una respuesta válida a "¿por qué IA?" es **"no hace falta"**. Que hoy les digan "hagan un agente" no los obliga a que todo sea un agente.

## 7. Riesgos, supuestos y preguntas abiertas

**Supuesto más riesgoso:** el bebedor curioso le cree a un catálogo de varios tostadores y compra sin probar.

**Cómo lo validamos (≤ 2 semanas, sin código):** una landing con 6 cafés y un botón "Lo quiero" que abre un formulario; medimos clics y correos dejados con $2,000 de anuncios.

**Riesgos:**

- Sobreventa sin inventario (aceptado para la v1).
- Un tostador sube precios sin avisar y el catálogo queda desactualizado.

**Preguntas abiertas:**

- ¿Cobramos la comisión al tostador por venta o por mes?
