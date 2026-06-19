# Portfolio — Carlos Molina Martínez

Web porfolio estática y autocontenida: un solo `index.html` (CSS y JS embebidos) + carpeta `assets/` con imágenes y CV.

- `index.html` — versión **clara editorial** (Fraunces + azul cobalto). **Esta es la web principal.**
- `index-dark.html` — versión oscura tipo telemetría (alternativa, accesible en `/index-dark.html`).
- `cv/Carlos-Molina-Martinez-CV.tex` — fuente LaTeX del CV genérico descargable. Para regenerarlo:
  ```bash
  cd cv
  pdflatex Carlos-Molina-Martinez-CV.tex   # ejecutar dos veces para los hyperlinks
  ```
  y copia el PDF resultante a `assets/Carlos-Molina-Martinez-CV.pdf`.

## Desplegar en GitHub Pages (gratis)

1. Crea un repositorio en GitHub llamado **`carlosmolina55.github.io`** (con ese nombre exacto, la web quedará en la raíz: `https://carlosmolina55.github.io`).
2. Sube el contenido de esta carpeta (`index.html` + `assets/`):
   ```bash
   cd carlos-portfolio
   git init
   git add .
   git commit -m "Portfolio inicial"
   git branch -M main
   git remote add origin https://github.com/carlosmolina55/carlosmolina55.github.io.git
   git push -u origin main
   ```
3. En el repo: **Settings → Pages → Source: Deploy from a branch → main / (root)**.
4. En 1-2 minutos la web estará en `https://carlosmolina55.github.io`.

> Alternativa: si prefieres otro nombre de repo (p. ej. `portfolio`), la URL será `https://carlosmolina55.github.io/portfolio/`.

## Cómo actualizar la web

- **Nuevo proyecto** → duplica un bloque `<div class="proj">...</div>` en la sección `04 / Projects`.
- **Nueva publicación de LinkedIn** → duplica un bloque `<article class="slide">...</article>` en la sección `05 / Field Log` (carrusel), añade la imagen en `assets/img/` y ponla la primera para que salga al inicio.
- **CV nuevo** → reemplaza `assets/Carlos-Molina-Martinez-CV.pdf` (mismo nombre y no hay que tocar nada más).
- Después: `git add . && git commit -m "update" && git push` y la web se actualiza sola.

## Estructura

```
carlos-portfolio/
├── index.html              # toda la web (HTML + CSS + JS)
└── assets/
    ├── Carlos-Molina-Martinez-CV.pdf
    └── img/
        ├── ogathon.jpg
        ├── hackathon-caf.jpg
        ├── wats-floating-pv.jpg
        └── erasmus.jpg
```
