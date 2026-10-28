# Proyecto Progreso 1 — Projects Listing (CDM Smith)

Una pantalla responsive construida a partir de un diseño de Figma.

## Tecnologías
- HTML5 semántico
- CSS Grid + Flexbox
- Media queries (mobile-first: 768 px y 1100 px)
- Nomenclatura BEM
- Sass (variables, nesting, parciales con `@use`, mixins)

## Estructura
```
proyecto/
├── index.html
├── package.json
├── css/main.css          # generado por Sass (no editar)
├── img/                  # fotos de las tarjetas
└── scss/
    ├── main.scss         # punto de entrada (unión de parciales + .layout)
    ├── _variables.scss   # colores, espaciados, breakpoints
    ├── _mixins.scss      # respond() y flex-center()
    ├── _base.scss        # reset, .container, .btn
    ├── _nav.scss
    ├── _hero.scss
    ├── _sidebar.scss
    ├── _card.scss        # resultados, tags, tarjeta, paginación
    ├── _cta.scss
    └── _footer.scss
```

## Cómo compilar
Requiere [Node.js](https://nodejs.org).

```bash
npm install        # instala Sass (solo la primera vez)
npm run build      # compila una vez
npm run watch      # recompila al guardar cambios
```

Luego abre `index.html` en el navegador (recarga con `Ctrl + F5` si no ves cambios).

## Dónde se usa cada técnica
| Técnica | Dónde |
|---|---|
| CSS Grid | `.layout`, `.results__list`, `.footer__top`, `.footer__cols` |
| Flexbox | `.nav`, `.card`, `.tag`, `.pagination`, `.cta__actions`, `.sidebar__group` |
| Media queries | mixin `respond()` en `_mixins.scss` |
| BEM | `.card__title`, `.tag--active`, `.btn--outline`, `.sidebar__option--child` |
| Sass | variables en `_variables.scss`, nesting con `&__` / `&--`, mixins `respond()` y `flex-center()` |

## Notas
- La fuente original del diseño ("cdm smith") no está disponible; se usa Segoe UI / Arial.
- Los íconos son símbolos de texto, no los del Figma.
