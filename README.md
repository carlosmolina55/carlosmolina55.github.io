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
