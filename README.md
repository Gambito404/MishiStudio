# 🐱 Mishi Studio - Catálogo Digital PWA

Catálogo interactivo y progresivo (PWA) para productos personalizados: pins, stickers, llaveros y más. Gestionado 100% desde Google Sheets.

## ✨ Características Técnicas

- 🛍️ **Catálogo Dinámico** - Sincronizado en tiempo real con Google Sheets.
- 📊 **Gestión Fácil** - Administra productos, precios y fotos desde Excel sin tocar código.
- 🛒 **Carrito de Compras** - Cotización automática y envío de pedidos a WhatsApp.
- 🤝 **Modo Vendedor** - Enlaces personalizados para distribuidores con sus propios precios y contacto.
- ❤️ **Favoritos** - Guarda tus productos preferidos localmente.
- 📱 **Diseño Responsive** - Optimizado para móviles y escritorio.
- ⚡ **PWA Instalable** - Funciona como una app nativa, incluso sin conexión (modo offline básico).
- 🔄 **Auto-Actualización** - Detecta cambios en tiempo real y avisa al usuario.
- 🖼️ **Soporte Drive** - Carga imágenes directamente desde enlaces de Google Drive.

## 🚀 Cómo comprar (Para Clientes)

1. Explora el catálogo por categorías.
2. Haz clic en "Cotizar" o agrega al carrito 🛒.
3. Revisa tu pedido y selecciona las cantidades.
4. Haz clic en "Finalizar Pedido" para enviar el detalle automáticamente por WhatsApp.

## 🤝 Modo Vendedor (Para Distribuidores)

Esta funcionalidad permite que cada vendedor tenga su propia versión del catálogo:
- **Precios Propios**: Pueden definir escalas de precios distintas a las de la tienda principal.
- **Contacto Directo**: Los pedidos realizados a través de su enlace llegan directamente a su WhatsApp personal.
- **Identidad**: El catálogo muestra el nombre del vendedor en la cabecera.
- **Filtrado Estricto**: Solo se muestran los productos que el vendedor ha decidido vender (aquellos con precio asignado en su lista).

## 🛠️ Guía de Administración (Para el Dueño)

El catálogo se controla desde una Hoja de Cálculo de Google con las siguientes pestañas:

### Estructura del Excel (4 Hojas Obligatorias)

#### 1. Hoja `Productos`
- **Categoria**: ID de la categoría (ej: `pins`).
- **Titulo**: Título visible de la sección.
- **Subtitulo**: Descripción corta de la sección.
- **Id_producto**: ID único del producto (ej: `pin1`).
- **Nombre_Producto**: Nombre del ítem.
- **Descripcion**: Detalles del producto.

#### 2. Hoja `Imagenes`
- **Id_producto**: El mismo ID usado en la hoja Productos.
- **Imagenes**: Enlace de la imagen (Google Drive o URL directa).
  - *Tip:* Deja el ID vacío en filas siguientes para agregar más fotos al mismo producto (Galería).

#### 3. Hoja `Precios`
- **Id_producto**: El mismo ID usado en la hoja Productos.
- **Cantidades**: Cantidad mínima (ej: 1, 12, 50).
- **Precios**: Precio total para esa cantidad.

#### 4. Hoja `Vendedores` (Nueva)
- **idVendedor**: ID único (ej: `V-001`).
- **nombre**: Nombre del vendedor.
- **numero**: WhatsApp con código de país (ej: `59170000000`).
- **idProducto**: El mismo ID usado en `Productos`.
- **cantidad**: Cantidad para la escala de precio.
- **precio**: Precio total para esa cantidad.

> **Tip de Llenado**: No es necesario repetir el ID, nombre y número en cada fila. El sistema "hereda" los datos de la fila superior hasta encontrar un nuevo vendedor o producto.

## 🔗 Generación de Enlaces para Vendedores

Para entregar el catálogo a un vendedor, usa la siguiente estructura de URL:
`https://tu-catalogo.com/?id=[ID_DEL_VENDEDOR]`

**Ejemplo:**
`https://gambito404.github.io/MishiStudio/?id=V-001`

El sistema buscará automáticamente el nombre y teléfono del vendedor en la hoja `Vendedores`.

### 📸 Imágenes desde Google Drive
1. Sube la foto a Drive.
2. Clic derecho > Compartir > **"Cualquier persona con el enlace"**.
3. Copia el enlace y pégalo en la hoja `Imagenes`.

## 📞 Contacto

- **WhatsApp**: +591 77424842
- **Email**: gabrielberriosmendoza@gmail.com

---

Hecho con ❤️ por **Gambito404** | © 2026 Mishi Studio