# Criterios de aceptación del sprint 1

Cada historia tiene cuatro criterios: flujo normal, excepción, límite y no funcional.

## HU-01 Registro de usuarios

| Tipo | Criterio |
|---|---|
| Flujo normal | Dado que una persona completa nombre, correo, contraseña y rol, cuando confirma, entonces se crea su cuenta y puede iniciar sesión. |
| Excepción | Si el correo ya existe o falta un campo, la app lo indica y no crea la cuenta. |
| Límite | La contraseña debe tener al menos 8 caracteres. Con 7 se rechaza y con 8 se acepta. |
| No funcional | La contraseña se guarda con hash seguro, nunca en texto plano (RNF-02). |

## HU-02 Publicar un producto

| Tipo | Criterio |
|---|---|
| Flujo normal | Dado que un productor tiene sesión, cuando publica un producto con tipo, cantidad y precio, entonces se guarda y aparece en el catálogo con sus datos. |
| Excepción | Si falta un campo, la app lo marca y no guarda nada. Si no hay conexión, avisa y conserva lo escrito. |
| Límite | Un precio de 0 o negativo y una cantidad negativa se rechazan. La cantidad 0 se acepta y marca el producto como agotado. |
| No funcional | Un productor nuevo publica su primer producto en menos de 3 minutos y sin ayuda. |

## HU-03 Buscar por categoría en el catálogo

| Tipo | Criterio |
|---|---|
| Flujo normal | Dado que hay productos publicados, cuando un comprador elige una categoría, entonces ve los productos de esa categoría con su precio y cantidad. |
| Excepción | Si la categoría no tiene productos, la app muestra un mensaje y no una lista vacía. |
| Límite | Un producto con cantidad 0 aparece marcado como agotado y no se puede pedir. |
| No funcional | La búsqueda responde en menos de 2 segundos en el percentil 95 con 500 usuarios concurrentes (RNF-01). |
