# Backlog priorizado

## Enfoque de trabajo

El equipo trabaja de forma ágil con Scrum. Los requisitos van a cambiar durante el proyecto, porque los pagos y los envíos dependen de servicios externos. Son tres personas con las responsabilidades repartidas y se comunican con el cliente por una red social para mostrar avances y consultar cambios. Del enfoque dirigido por planes toma el SRS y un plan escrito de cada sprint.

## Historias en orden de prioridad

| Orden | Historia | MoSCoW y razón | Valor y esfuerzo | Stakeholder y requisito |
|---|---|---|---|---|
| 1 | Como productor o comprador, quiero registrarme, para acceder a la plataforma. | Debe. Sin cuenta no funciona ninguna otra historia. | Alto y bajo | Productor y comprador |
| 2 | Como productor, quiero publicar un producto con precio y cantidad, para ofrecerlo a los compradores. | Debe. Sin oferta no hay compra. | Alto y medio | Productor, RF-01 |
| 3 | Como comprador, quiero buscar productos por categoría, para encontrar lo que necesito. | Debe. Es la entrada principal al catálogo. | Alto y medio | Comprador, RF-02 |
| 4 | Como comprador, quiero agregar productos al carrito, para reunir mi pedido. | Debe. Es el paso previo al pedido. | Alto y medio | Comprador, RF-03 |
| 5 | Como comprador, quiero pagar mi pedido, para confirmar la compra. | Debe. Genera valor, pero depende del carrito y de la pasarela de pago. | Alto y alto | Comprador, pago en línea |
| 6 | Como productor, quiero ver los pedidos que recibí, para prepararlos. | Debe. Sin pedidos visibles no puede entregar. | Alto y medio | Productor, RF-04 |
| 7 | Como comprador, quiero recibir la confirmación de mi pedido, para tener respaldo de la compra. | Debe. Cierra el flujo de compra. | Medio y bajo | Comprador, RF-03 |
| 8 | Como proveedor logístico, quiero calcular el costo de envío según mi tarifa, para cobrar el servicio correctamente. | Debe. Es necesaria para la versión final, pero depende de la tarifa del transportista. | Alto y medio | Proveedor logístico |
| 9 | Como proveedor logístico, quiero consultar el estado del envío, para informar al comprador. | Debería. Mejora la experiencia, pero no bloquea la compra. | Medio y medio | Proveedor logístico |
| 10 | Como administrador, quiero gestionar las categorías de productos, para mantener el catálogo ordenado. | Debería. El catálogo puede funcionar con categorías fijas al inicio. | Medio y bajo | Administrador |

## Sprint 1

- **Objetivo:** un productor puede registrarse y publicar un producto con su tipo, cantidad y precio, y un comprador lo ve en el catálogo.
- **Historias:** 1 (registro), 2 (publicar) y 3 (buscar en el catálogo).
- **Pasan al sprint 2:** el carrito y la confirmación del pedido. El pago (5) y el cálculo de envío (8) quedan fuera porque dependen de servicios externos.
- **Cómo se comprueba:** en la revisión del sprint se muestra el flujo con un productor de prueba y se verifican los criterios de aceptación de las tres historias. Si un criterio falla, la historia vuelve al backlog con su nueva prioridad.

## Tratamiento de un cambio de requisito

**Cambio:** el transportista cambia su forma de cobrar a mitad del proyecto, de una tarifa fija por pedido a un cobro por peso y zona.

**Historias afectadas:** 8 (cálculo de envío), 5 (el total pagado incluye el envío) y 7 (la confirmación muestra el costo). Ninguna historia del sprint 1 se ve afectada.

**Decisión:** el Product Owner reescribe la 8 con criterios nuevos y revisa la 5 y la 7 en el backlog. La 8 entra al sprint 2 cuando el transportista confirme su nueva tarifa. Solo se interrumpe un sprint en curso si el cambio lo afecta en gran medida.
