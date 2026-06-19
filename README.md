# 🐱 Mishi Studio - Catálogo Digital PWA

Catálogo interactivo y progresivo (PWA) para productos personalizados: pins, stickers, llaveros y más. Gestionado 100% desde Google Sheets y con actualizaciones en tiempo real.

## ✨ Características Principales

- 🛍️ **Catálogo Dinámico**: Sincronizado con Google Sheets. Los cambios en precios, productos o stock se reflejan automáticamente.
- 🔄 **Actualización en Tiempo Real (Live Update)**: El catálogo detecta cambios y actualiza los productos de forma discreta, sin necesidad de recargar la página. Las tarjetas de los productos modificados se resaltan sutilmente para notificar al usuario.
- 🔍 **Búsqueda Inteligente**: Campo de búsqueda con sugerencias predictivas, botón de limpieza rápida y mensaje de "no encontrado" para una mejor experiencia.
- 🛒 **Carrito de Compras**: Cotización automática con cálculo de ahorros por volumen y envío de pedidos directamente a WhatsApp.
- 🤝 **Modo Vendedor**: Enlaces personalizados para distribuidores (`?id=V-001`) que cargan sus propios precios, contacto y disponibilidad de productos.
- ❤️ **Favoritos**: Funcionalidad para que los usuarios guarden sus productos preferidos localmente.
- 📱 **Diseño Responsivo y Moderno**: Optimizado para móviles y escritorio, con animaciones y una interfaz de usuario cuidada.
- ⚡ **PWA Instalable**: Funciona como una app nativa, con soporte offline básico y acceso rápido desde el dispositivo.
- 🚀 **Navegación Fluida**: Incluye un botón "Volver Arriba" para desplazarse cómodamente en catálogos extensos.
- 🖼️ **Soporte para Google Drive**: Permite cargar imágenes directamente desde enlaces compartidos de Google Drive.

## 🚀 Cómo comprar (Para Clientes)

1.  Explora el catálogo o usa la barra de búsqueda para encontrar productos.
2.  Añade productos al carrito 🛒 haciendo clic en "Cotizar" o "Añadir".
3.  Elige las cantidades deseadas. El sistema te mostrará si hay descuentos por volumen.
4.  Cuando termines, haz clic en el ícono del carrito y luego en "Finalizar Pedido" para enviar el detalle por WhatsApp.

## 🤝 Modo Vendedor (Para Distribuidores)

Esta funcionalidad permite que cada vendedor tenga su propia versión del catálogo:

-   **Precios Propios**: Pueden definir escalas de precios distintas a las de la tienda principal.
-   **Contacto Directo**: Los pedidos realizados a través de su enlace llegan directamente a su WhatsApp personal.
-   **Identidad Personalizada**: El catálogo muestra el nombre del vendedor en la cabecera.
-   **Disponibilidad Selectiva**: Solo se muestran los productos que el vendedor ha decidido vender (aquellos a los que les ha asignado un precio en su lista).

## 🛠️ Guía de Administración (Para el Dueño)

El catálogo se controla desde una Hoja de Cálculo de Google con 5 pestañas obligatorias:

### Estructura del Excel

1.  **`Productos`**: Define los productos y a qué categoría pertenecen.
    -   `Categoria`, `Titulo`, `Subtitulo`, `Id_producto`, `Nombre_Producto`, `Descripcion`, `Estado` (`activo`, `agotado`).
2.  **`Imagenes`**: Asigna una o más imágenes a cada producto.
    -   `Id_producto`, `Imagenes` (URL directa o de Google Drive).
3.  **`Precios`**: Define los precios para el público general.
    -   `Id_producto`, `Cantidades`, `Precios`.
4.  **`Vendedores`**: Define los precios y datos para cada vendedor.
    -   `idVendedor`, `nombre`, `numero` (WhatsApp), `idProducto`, `cantidad`, `precio`.
5.  **`Version`**: Controla las actualizaciones en tiempo real.
    -   `version`: Un número (ej: `1.0`, `1.1`, `1.2`). **Cada vez que cambies este número, el sistema forzará la actualización discreta en la app de los usuarios.**

> **Tip de Llenado**: No es necesario repetir el ID, nombre y número en cada fila de la hoja `Vendedores`. El sistema "hereda" los datos de la fila superior hasta encontrar un nuevo vendedor o producto.

### 🔗 Generación de Enlaces para Vendedores

Para entregar el catálogo a un vendedor, usa la siguiente estructura de URL:
`https://gambito404.github.io/MishiStudio/?id=[ID_DEL_VENDEDOR]`

**Ejemplo:**
`https://gambito404.github.io/MishiStudio/?id=V-001`

### 📸 Imágenes desde Google Drive

1.  Sube la foto a tu Google Drive.
2.  Haz clic derecho sobre la imagen > **Compartir** > **Compartir**.
3.  En "Acceso general", cambia a **"Cualquier persona con el enlace"**.
4.  Copia el enlace y pégalo en la hoja `Imagenes`.

## 📞 Contacto

-   **WhatsApp**: +591 77424842
-   **Email**: gabrielberriosmendoza@gmail.com

---

Hecho con ❤️ por **Gambito404** | © 2026 Mishi Studio
