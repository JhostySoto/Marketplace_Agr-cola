# Especificación de requisitos (SRS)

## Introducción

**Propósito:** acordar con el equipo y el docente qué hará el Marketplace Agrícola en su primer incremento.

**Alcance:** publicación de productos, búsqueda, carrito, pedidos y notificaciones al productor. Los pagos en línea y las calificaciones quedan para incrementos posteriores.

## Descripción general y modelo de proceso

- **Usuarios:** productores agrícolas locales, compradores finales y administrador de la plataforma.
- **Estabilidad de los requisitos:** estables en publicación, búsqueda y pedidos. Inciertos en pagos y entregas.
- **Riesgo:** bajo en el primer incremento porque los pagos quedan fuera. Medio en la definición de entregas.
- **Urgencia de uso:** media. Los productores necesitan publicar su oferta en cuanto el primer incremento funcione.
- **Modelo elegido:** incremental. Cada incremento entrega valor usable y los pagos y las entregas se prototipan antes de construirlos.

## Requisitos funcionales

| ID | Requisito | Prioridad |
|---|---|---|
| RF-01 | Un productor autenticado puede publicar un producto con nombre, precio por unidad, cantidad disponible y al menos una fotografía. | Debe |
| RF-02 | Un comprador puede buscar productos por categoría y ordenar los resultados por distancia al productor. | Debe |
| RF-03 | Un comprador puede agregar productos a un carrito y confirmar un pedido indicando la dirección de entrega. | Debe |
| RF-04 | Un productor autenticado puede cambiar el estado de un pedido entre recibido, preparado y entregado. | Debería |
| RF-05 | El sistema envía al productor una notificación por correo electrónico cuando recibe un pedido nuevo. | Debería |

## Requisitos no funcionales

| ID | Categoría | Requisito con métrica y umbral | Prioridad |
|---|---|---|---|
| RNF-01 | Rendimiento | La búsqueda de productos responde en menos de 2 segundos en el percentil 95 con 500 usuarios concurrentes. | Debe |
| RNF-02 | Seguridad | Ninguna contraseña se almacena en texto plano y el 100 por ciento usa un algoritmo de hash seguro como bcrypt o argon2. | Debe |
| RNF-03 | Disponibilidad | El sitio mantiene una disponibilidad mensual de al menos 99 por ciento, medida con un monitor externo. | Debería |

## Pendientes y riesgos

| Pendiente | Riesgo | Cómo se reducirá |
|---|---|---|
| Condiciones de entrega con transportistas: tiempos, costos y zonas | Las reglas de entrega pueden cambiar el diseño del pedido y retrasar la confirmación de compras | Entrevistar a dos productores y a un transportista local antes de planificar el segundo incremento |
| Medio de pago en línea y condiciones de la integración bancaria | Si se incluye antes de tiempo, el segundo incremento podría retrasarse | Mantener el pago contra entrega en el primer incremento y construir un prototipo de integración antes de decidir |
