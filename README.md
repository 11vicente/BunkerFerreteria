# Proyecto Taller de Programación

Repositorio de seguimiento del proyecto. Contiene la documentación, gestión y un enlace al repositorio del producto.

## Estructura

- `Documentacion/` — entregables y material de referencia (Estado del Arte, Tabla de Homologación, Recomendaciones de Stack, etc.).
- `Gestion/` — información del equipo y gestión del proyecto.
- `Producto/` — **submódulo** que apunta al repositorio del producto: [FelphM/Ferromat_Proyecto](https://github.com/FelphM/Ferromat_Proyecto). Aquí está el código fuente real del sistema.

## Clonar el repositorio

Como `Producto/` es un submódulo, hay que clonarlo con el flag `--recurse-submodules` para que descargue también el contenido del repo del producto:

```bash
git clone --recurse-submodules https://github.com/11vicente/Proyecto_taller_programacion.git
```

Si ya lo clonaste sin ese flag y la carpeta `Producto/` aparece vacía:

```bash
git submodule update --init --recursive
```

## Trabajar con el repositorio

### Traer los últimos avances del producto

Cuando se hagan cambios en `Ferromat_Proyecto`, para que este repo apunte a la versión más nueva:

```bash
git -C Producto pull origin main
git add Producto
git commit -m "Actualizar avance del producto"
git push
```

### Trabajar dentro del producto

Si quieres editar el código del producto desde aquí, entra a `Producto/` y trabaja normalmente — es el repositorio de Ferromat_Proyecto:

```bash
cd Producto
# editar, commit, push como siempre
git add .
git commit -m "tu mensaje"
git push
```

Luego vuelve a la raíz y actualiza la referencia del submódulo (pasos de la sección anterior).

### Sincronizar tu copia local

Para traer cambios del repo padre **y** del submódulo en un solo paso:

```bash
git pull
git submodule update --remote --merge
```

## Integrantes

Ver [`Gestion/Integrantes.txt`](Gestion/Integrantes.txt).
