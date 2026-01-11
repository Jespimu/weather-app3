# WeatherApp — Refactor de UI (Módulo 3)

Aplicación de clima refactorizada para mejorar la experiencia visual y la mantenibilidad del CSS. Se aplican BEM, SASS (7-1), modelo de cajas y Bootstrap 4 para un layout claro y responsivo.

## Características
- Home con grilla de lugares en cards (`place-card`) mostrando icono, temperatura y estado.
- Vista de detalle con información ampliada y breadcrumb.
- Header/navbar consistente y footer con información del proyecto.
- Layout responsivo: 1 columna en móvil, múltiples columnas en pantallas grandes.

## Tecnologías y Metodologías
- BEM para nombrado de bloques, elementos y modificadores.
- SASS con patrón 7-1: variables, mixins, funciones, layout, componentes, páginas, temas, vendors.
- Bootstrap 4 (CDN) para grid, navbar, formularios y breadcrumb.

## Estructura del proyecto
```
.
├─ index.html
├─ detail.html
├─ css/
│  └─ main.css
└─ scss/
   ├─ abstracts/      # variables, mixins, funciones
   ├─ base/           # reset/base, tipografía, utilidades
   ├─ layout/         # header, footer, grid
   ├─ components/     # buttons, cards (place-card)
   ├─ pages/          # estilos por página (home)
   ├─ themes/         # temas (default, dark)
   └─ vendors/        # normalize
```

## BEM (ejemplos usados)
- App: `weather-app`, `weather-app__header`, `weather-app__hero`, `weather-app__search`, `weather-app__results`.
- Card: `place-card`, `place-card__icon`, `place-card__name`, `place-card__temp`, `place-card__state`, `place-card__action`.
- Modificadores: `place-card--sunny`, `place-card--rainy`, `place-card--cloudy`.

## Cómo ejecutar
- Opción simple: abrir `index.html` en tu navegador.
- Vista de detalle: navegar a `detail.html` desde las cards o directo en el navegador.

## Compilar SASS (opcional)
Si deseas recompilar desde `scss/main.scss` hacia `css/main.css`:
- Con Sass CLI: `sass scss/main.scss css/main.css --watch`
- Con Dart Sass (npx): `npx sass scss/main.scss css/main.css --watch`

Nota: El repo incluye `css/main.css` ya compilado para visualizar sin build.

## Bootstrap 5
- Inclusión por CDN en `index.html` y `detail.html`.
- Grid usado: `col-12 col-md-6 col-lg-4` para cards.
- Componentes: `navbar`, `form-inline`, `breadcrumb` y utilidades (`container`, `row`, `mb-4`).

## Próximos pasos
- Conectar API de clima (por ejemplo OpenWeather) y poblar `place-card` dinámicamente.
- Añadir manejo de estados de carga/errores y favoritos.
- Incorporar temas (claro/oscuro) usando `themes/`.

## Autor
- Autor: Jaime Espinoza

