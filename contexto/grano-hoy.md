# Grano hoy · octubre 2026

> Contexto común para los 5 equipos. Los datos son ficticios pero consistentes entre sí: úsalos como si fueran reales.

## Qué es Grano

Grano es un marketplace curado de café de especialidad de **microtostadores mexicanos**. Es la tienda que construimos en la demo de la Estación 1: salió a producción en abril de 2026 con 6 cafés, catálogo con notas de cata, carrito con total en vivo y el cupón `BIENVENIDA10`.

Seis meses después, el negocio creció y se complicó.

## Números de hoy

| Área | Dato | Comentario |
|---|---|---|
| Catálogo | 18 microtostadores · 64 cafés | Eran 6 cafés en abril |
| Tráfico | 120,000 visitas al mes | 64 % son visitantes nuevos |
| Ventas | 2,150 pedidos al mes · conversión 1.8 % | La meta del PVB era 2 %; la del año es 2.5 % |
| Ticket | $640 MXN promedio | Meta del PVB: ≥ $600 ✓ |
| Ingreso | Grano cobra 25 % de comisión al tostador | ≈ $344,000 MXN de ingreso al mes |
| Grano Club | 820 suscriptores · churn mensual 11 % | Lanzado en julio. Meta: churn ≤ 6 % |
| B2B | 35 cafeterías compran por WhatsApp y Excel | 22 % del GMV; 9 cafeterías en lista de espera |
| Soporte | 3 personas · 1,900 tickets al mes | Primera respuesta: 9 h · CSAT 3.9 / 5 |
| Operaciones | 11 % de pedidos con un café agotado después de pagar | El inventario vive en un Google Sheet que se actualiza 1 vez por semana |

### De qué tratan los tickets de soporte

| Motivo | % | Tickets / mes |
|---|---|---|
| "¿Dónde está mi pedido?" | 34 % | ≈ 650 |
| Daños, faltantes y reembolsos | 18 % | ≈ 340 |
| Cambios de suscripción (pausar, cambiar café o dirección) | 14 % | ≈ 270 |
| "¿Qué café me recomiendan?" | 12 % | ≈ 230 |
| Otros | 22 % | ≈ 410 |

## El pedido del CEO

> "Para el Q1 de 2027 quiero un agente de IA en Grano. Tenemos **$40,000 MXN al mes** de presupuesto para IA y **2 devs durante 8 semanas**. No me traigan una lista de deseos: tráiganme un producto que mueva un número."
> — Valeria, CEO de Grano

Fíjate en que el CEO pidió una **solución** ("un agente"). Su trabajo hoy es averiguar **para quién, para qué problema y con qué número** tiene sentido, y también si de verdad hace falta IA.

## Equipo de Grano

12 personas: CEO (hace de PM), 3 devs, 3 en soporte, 2 en ventas B2B, 1 coordinador de operaciones, 1 en finanzas y 1 en marketing.

## Restricciones que aplican a todos

- **Precios solo en la API.** Ningún agente inventa, calcula ni promete un precio que la API de Grano no haya devuelto. Es la misma regla del `CLAUDE.md` de la E1.
- **Datos personales.** Grano opera en México y está sujeto a la ley de protección de datos personales (LFPDPPP): aviso de privacidad, consentimiento y uso limitado al fin declarado.
- **WhatsApp Business.** Fuera de la ventana de 24 h desde el último mensaje del cliente solo se pueden enviar plantillas aprobadas por Meta.
- **Pagos.** Ningún agente cobra, reembolsa ni cambia un método de pago sin una confirmación explícita (del cliente o de un humano de Grano, según el caso).
- **Paquetería.** La API de la paquetería da el estatus del envío, pero no garantiza fechas. Nadie promete una fecha que la paquetería no haya confirmado.
- **Presupuesto.** $40,000 MXN al mes para costos de IA. Cada equipo debe estimar si su producto cabe.

## Los 5 segmentos

| Equipo | Segmento | Track |
|---|---|---|
| 01 | Comprador nuevo que no sabe qué café elegir | PVB · cliente externo |
| 02 | Suscriptor de Grano Club que gestiona su suscripción | PVB · cliente externo |
| 03 | Cafeterías B2B: cotizaciones y pedidos de mayoreo | PVB · cliente externo |
| 04 | Equipo de soporte post-venta: rastreo, daños y reembolsos | ISB · solución interna |
| 05 | Operaciones: inventario y reabastecimiento con los tostadores | ISB · solución interna |
