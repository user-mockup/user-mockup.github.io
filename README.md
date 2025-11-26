# Sistema de Gestión de Pedidos de Inventario NIA

Una aplicación web progresiva (PWA) sencilla para sistematizar la toma de pedidos de inventario por vendedores externos.

## Características

- **Administrar Vendedores**: Agregar y eliminar vendedores.
- **Crear Clientes**: Agregar nuevos clientes con nombre y email.
- **Gestión de Productos**: Importar productos desde archivos Excel (.xlsx, .xls, .csv), actualizar cantidades.
- **Tomar Pedidos**: Seleccionar vendedor, cliente y productos con cantidades.
- **Reportes**: Descargar reporte de transacciones en CSV por rango de fechas.
- **PWA**: Funciona offline, instalable en dispositivos móviles.

## Instalación y Uso

1. Abre `index.html` en un navegador web moderno.
2. Para instalar como PWA: En Chrome/Edge, haz clic en "Instalar" cuando aparezca el prompt.
3. Los datos se almacenan localmente en el navegador.

## Estructura de Archivos Excel para Importar Productos

El archivo debe tener columnas para nombre, cantidad y precio. Nombres de columnas aceptados (case-insensitive, basado en "INVENTARIObase NIA"):

- Nombre: Nombre, nombre, Name, name, Producto, producto, Articulo, articulo, Item, item, Descripción, descripción, Descripcion, descripcion, Nombre Producto, nombre producto, Descripción Producto, descripción producto, Codigo, codigo
- Cantidad: Cantidad, cantidad, Quantity, quantity, Stock, stock, Disponible, disponible, Qty, qty, Cantidad Disponible, cantidad disponible, Stock Disponible, stock disponible
- Precio: Precio, precio, Price, price, Costo, costo, Valor, valor, Precio Unitario, precio unitario, Costo Unitario, costo unitario, Precio1, precio1, UltCosto, ultcosto

Al importar, se mostrará un alert con las columnas encontradas para verificar. Si no se encuentra una columna válida, se usa un valor por defecto (ej. 'Sin Nombre' para nombre, 0 para cantidad/precio).

Ejemplo:

| Codigo | Descripcion | Cantidad | Precio1 |
|--------|-------------|----------|---------|
| 001 | Producto A | 100 | 10.50 |
| 002 | Producto B | 50 | 25.00 |

## Tecnologías

- HTML5, CSS3, JavaScript (Vanilla)
- PWA con Service Worker
- Librería XLSX para manejo de Excel
- Almacenamiento local (localStorage)

## Gestión de Datos

Los datos se almacenan localmente en el navegador, pero puedes exportarlos a un archivo JSON editable para backup o edición externa:

- **Exportar Datos**: Descarga un archivo `datos.json` con toda la información.
- **Importar Datos**: Sube un archivo JSON para cargar datos previamente exportados o editados.

Edita el JSON externamente con un editor de texto y luego impórtalo para actualizar la app.