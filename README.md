# Bunker Ferreteria POS

Repositorio de seguimiento del proyecto **Bunker Ferretería POS**. Reúne la documentación, gestión y el código fuente del producto en un solo lugar.

## Estructura

- `Documentacion/` — entregables y material de referencia (Estado del Arte, Tabla de Homologación, Recomendaciones de Stack, diagramas de arquitectura/casos de uso/secuencia, ERD de Supabase, estado de avance, presentación parcial, etc.).
- `Gestion/` — información del equipo y gestión del proyecto.
- `Producto/` — **código fuente del sistema POS**. Aplicación React + Vite con backend Supabase (Postgres + Auth + Storage). Incluye los scripts SQL del ambiente de pruebas en `Producto/backup_supaBase/`.

## Clonar el repositorio

```bash
git clone https://github.com/11vicente/Proyecto_taller_programacion.git
cd Proyecto_taller_programacion
```

## Levantar el producto en local

```bash
cd Producto
npm install
npm run dev
```

La aplicación se sirve por defecto en `http://localhost:5173`. Requiere variables de entorno de Supabase configuradas (ver `Producto/src/lib/supabaseClient.js`).

## Sincronizar `Producto/` con el repositorio del proyecto

El código del producto vive originalmente en [FelphM/BunkerFerreteriaPOS_Proyecto](https://github.com/FelphM/BunkerFerreteriaPOS_Proyecto). Para traer los últimos cambios a este repo se reemplaza el contenido de `Producto/`:

```powershell
# Desde la raíz de Proyecto_taller
Remove-Item -Recurse -Force Producto
git clone https://github.com/FelphM/BunkerFerreteriaPOS_Proyecto Producto
Remove-Item -Recurse -Force Producto/.git
git add Producto/
git commit -m "Sincronizar Producto con ultima version de BunkerFerreteriaPOS_Proyecto"
git push
```

## Stack tecnológico

- **Frontend:** React 18, Vite, React Router, Bootstrap Icons
- **Backend:** Supabase (PostgreSQL + Auth + Storage)
- **Modo offline:** Dexie / IndexedDB
- **Deploy:** Vercel

## Módulos del sistema

Login/Auth, Punto de Venta (POS), Inventario, Productos, Variantes, Categorías, Proveedores, Clientes, Ventas, Compras, Cotizaciones, Facturas, Reportes, Configuración, Dashboard.

## Integrantes

Ver [`Gestion/Integrantes.txt`](Gestion/Integrantes.txt).

## Enlaces

- Repositorio del producto: https://github.com/FelphM/BunkerFerreteriaPOS_Proyecto
- Tablero Jira (SCRUM): https://duocuc-team-j7no4etr.atlassian.net/jira/software/projects/SCRUM/boards
