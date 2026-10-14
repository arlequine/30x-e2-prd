# 30x-e2-prd · Estación 2 · Descubrimiento y Definición

Material del ejercicio por equipos de la **Estación 2** del programa AI for Developers de 30X.
Hoy no escribimos código: escribimos el **PRD** (Product Requirements Document) de un agente de IA para Grano, la tienda de café de la demo de la E1.

## El ejercicio en 30 segundos

- El CEO de Grano pidió "un agente de IA". Cada equipo recibe un **segmento distinto** del negocio y escribe un **PRD completo pero acotado** para ese segmento.
- Tienen **45 minutos** (7:50 a 8:35 pm COT) en su sala de Zoom.
- Entregan su `prd.md` como **Pull Request** a las 8:35 pm COT.
- En la plenaria, cada equipo presenta en **2 minutos** y recibe feedback.

| Equipo | Segmento | Carpeta |
|---|---|---|
| 01 | Comprador nuevo que no sabe qué café elegir | [`equipos/equipo-01`](equipos/equipo-01) |
| 02 | Suscriptor de Grano Club | [`equipos/equipo-02`](equipos/equipo-02) |
| 03 | Cafeterías B2B | [`equipos/equipo-03`](equipos/equipo-03) |
| 04 | Soporte post-venta (interno) | [`equipos/equipo-04`](equipos/equipo-04) |
| 05 | Operaciones e inventario (interno) | [`equipos/equipo-05`](equipos/equipo-05) |

## Qué leer y en qué orden (5 minutos)

1. [`contexto/grano-hoy.md`](contexto/grano-hoy.md): la empresa, sus números y el pedido del CEO. **Todos.**
2. `equipos/equipo-0N/brief.md`: su segmento, sus datos y sus preguntas guía.
3. `equipos/equipo-0N/prd.md`: la plantilla que van a llenar.
4. De consulta: [`ejemplo/grano-tienda-prd.md`](ejemplo/grano-tienda-prd.md) (un PRD resuelto), [`rubrica.md`](rubrica.md) (cómo se evalúa) y [`prompts.md`](prompts.md) (cómo usar Claude).

## Roles en la sala

| Rol | Cuántos | Qué hace |
|---|---|---|
| Facilitador | 1 | Conduce la conversación, fuerza decisiones y presenta en la plenaria |
| Escriba | 1 | Es el **único** que edita el `prd.md`. Comparte pantalla todo el tiempo |
| Timekeeper | 1 | Lleva el reloj de los checkpoints y abre el Pull Request a las 8:32 |
| Abogado del diablo | 1 | Ataca cada decisión: "¿y si…?", "¿eso quién lo paga?" |
| Voz del usuario | 2 | Entrevistan a la persona del brief con Claude y traen citas y hechos |
| Analista de negocio | 2 | Métricas, costos y presupuesto; usan el prompt 3 |

Con menos gente: el facilitador también lleva el tiempo, y una sola persona hace de voz del usuario y de analista.

## Checkpoints (el mentor los anuncia por broadcast)

| Hora (COT) | Deberían tener |
|---|---|
| 7:55 | Roles asignados, brief leído y la entrevista con Claude andando |
| 8:05 | Secciones 1 y 2: resumen y problema con evidencia |
| 8:12 | Sección 3: usuario, cliente y JTBD |
| 8:20 | Sección 4: métricas con línea base y meta |
| 8:28 | Sección 5: alcance y no-objetivos. **El mínimo está completo.** |
| 8:32 | Secciones 6 y 7 si alcanzó el tiempo; revisión con el prompt 5. Se abre el PR |
| 8:35 | Regresan a la sala principal |

Con 8 personas, **paralelicen**: mientras el escriba cierra una sección, los analistas preparan la siguiente.

## Cómo entregar (2 minutos, sin git local)

Lo hace el escriba o el timekeeper, con su cuenta de GitHub:

1. Durante la sala, escriban el PRD en un editor local (VS Code, por ejemplo) sobre una copia de su `prd.md`.
2. A las 8:32, abran **su** `equipos/equipo-0N/prd.md` en este repo, en github.com.
3. Den clic en el lápiz ✏️ (*Edit this file*). GitHub crea un fork automáticamente.
4. Peguen el contenido completo y den clic en **Commit changes… → Propose changes**.
5. Den clic en **Create pull request**, con el título `Equipo 0N · <segmento>`.

**Plan B:** si GitHub falla, peguen el markdown en el chat de Zoom y mándenselo al mentor.

## Usar Claude en la sala

Claude **entrevista y critica**; ustedes **deciden y escriben**. Los prompts están en [`prompts.md`](prompts.md) y el de la voz del usuario viene al final de cada brief.

## Después de clase: revisar un PRD con Claude Code

Este repo trae el skill `prd-review` (`.claude/skills/prd-review/`), que revisa un PRD contra la rúbrica sin reescribirlo.

```bash
git clone https://github.com/arlequine/30x-e2-prd.git
cd 30x-e2-prd
claude
# y dentro de Claude Code:
#   revisa equipos/equipo-01/prd.md con el skill prd-review
```

Para revisar el PRD de su propio producto, copien la carpeta `.claude/skills/prd-review/` y `rubrica.md` a su repo.

## Tarea para la Estación 3

**El PRD de tu propio producto**, a partir del PVB o del ISB que entregaste en la E1.

1. Usa [`plantilla/prd.md`](plantilla/prd.md) y llena **las 7 secciones**.
2. Revísalo con el skill `prd-review` (o con el prompt 5) y corrige hasta llegar a **10 puntos o más** de la rúbrica.
3. Guárdalo como `docs/prd.md` en el repo de tu proyecto y comparte el link en el canal del programa.

**Fecha:** antes de la E3, lunes 19 de octubre, 7:00 pm COT. En la E3 vas a configurar tu entorno agéntico, y tu PRD es el contexto que le vas a dar.

## Estructura

```text
.
├── README.md
├── CLAUDE.md                     # contexto para Claude Code
├── contexto/grano-hoy.md         # la empresa y el pedido del CEO
├── plantilla/prd.md              # plantilla de 7 secciones (45 min)
├── ejemplo/grano-tienda-prd.md   # PRD resuelto de la tienda v1
├── rubrica.md                    # 5 criterios × 3 niveles
├── prompts.md                    # prompts para Claude en la sala
├── equipos/equipo-0N/            # brief.md + prd.md, uno por equipo
└── .claude/skills/prd-review/    # skill para revisar un PRD
```
