# Proyecto eléctrico paso a paso

App web instalable (PWA) con la guía de proyecto eléctrico del curso Categoría III (ERSeP Córdoba, AEA 90364-7-770): 19 pasos con calculadoras, planilla de PMU, editor de plano con simbología IRAM 2010, PDF del proyecto para entregar y base de clientes.

Desarrollado por © Silva Jonás

## Archivos

| Archivo | Para qué es |
|---|---|
| `index.html` | La app completa (HTML, estilos y código en un solo archivo) |
| `manifest.webmanifest` | Nombre, colores e íconos para instalarla en el celular |
| `sw.js` | Service worker: deja usar la app sin conexión |
| `icon-192.png`, `icon-512.png` | Íconos de la app |

## Cómo subirla

1. Subí los cinco archivos **juntos, en la misma carpeta** del servidor (por ejemplo un repositorio nuevo en GitHub Pages).
2. El servidor tiene que usar **https** (GitHub Pages ya lo hace). Sin https el celular no la deja instalar ni usar sin conexión.
3. Abrí la dirección en Chrome del celular → menú ⋮ → **Agregar a la pantalla principal** / **Instalar app**.

## Dónde se guardan los datos

- El proyecto en curso se guarda solo en el navegador (localStorage).
- **Clientes**: cada cliente con su PDF se guarda en el mismo dispositivo y navegador (IndexedDB). No se comparte entre el celular y la compu. Si borrás los datos del navegador o desinstalás la app, se pierden: descargá los PDF importantes.
- Para tener los clientes en todos tus dispositivos hace falta un servidor con base de datos (por ejemplo Supabase).

## Actualizar

Reemplazá `index.html` en el servidor. Si cambiás otros archivos, subí también la versión de `CACHE` en `sw.js` (por ejemplo `proy-elec-v2`) para que el celular tome la versión nueva.
