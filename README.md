# Game Zone 🎮

Sitio web de 4 páginas para una tienda/zona gamer, construido **solo con HTML5 y CSS**
(sin JavaScript, sin frameworks de estilos), cumpliendo las indicaciones de la asignación:

- HTML5 (`<!DOCTYPE html>`), sin etiquetas obsoletas/no soportadas (`<center>`, `<font>`, etc.).
- Sin `<style>` ni atributos `style=""` en línea: todo el CSS va en archivos `.css` externos
  enlazados con `<link>`.
- Sin JavaScript: el menú móvil se resuelve con el truco de CSS puro
  (`<input type="checkbox">` + `<label>` + selector `:checked ~`), no con un `<script>`.
- Exactamente 4 páginas: Inicio, Consolas, Experiencia y Contacto.

**Fecha de entrega:** domingo 20 de septiembre de 2026 (sábado 12 de septiembre + 8 días).

## Estructura

```
Taller_html/
├── index.html              # Página de inicio
├── index.css                # Estilos de inicio (incluye header/nav/footer base)
├── html/
│   ├── consolas.html         # Catálogo interactivo de consolas (mosaico con hover)
│   ├── experiencia.html      # Zonas de la tienda (torneos, VIP, streaming, retro)
│   └── contacto.html         # Formulario e información de contacto
└── css/
    ├── consolas.css
    ├── experiencia.css
    ├── contacto.css
    └── animaciones.css       # Animaciones (@keyframes) compartidas entre páginas
```

## Notas de diseño

- Todo el arte visual (logos, iconos, fondos de las tarjetas) está hecho con CSS puro
  (gradientes, `box-shadow`, pseudo-elementos), sin imágenes externas.
- Cada página enlaza su propia hoja de estilos más `css/animaciones.css`.
- El header, la navegación y el footer se repiten con la misma estructura en las 4 páginas
  para mantener consistencia visual.
- El menú hamburguesa en móvil funciona sin JavaScript, usando un `<input type="checkbox">`
  oculto controlado por CSS (`:checked ~ .menu`).
