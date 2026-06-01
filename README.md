# STATUS LAB

Landing page de **STATUS LAB**, empresa de tecnología que crea soluciones con **Inteligencia Artificial** y **Marketing** para empresas.

🌐 **Sitio:** [statuslab.app](https://statuslab.app)

## Descripción

Sitio estático de una sola página (HTML + CSS + JS en un único archivo, sin dependencias ni build). Diseño monocromático (blanco, negro y grises) con estética dark y efectos de luz.

Incluye:
- Hero con captura de correo
- Servicios: Inteligencia Artificial y Marketing con datos
- Proceso de trabajo en 3 pasos
- Formulario de contacto / agendar llamada

## Ver en local

Opción 1: abre `index.html` directamente en el navegador.

Opción 2 (recomendada): en VS Code instala la extensión **Live Server**, haz clic derecho en `index.html` → *Open with Live Server*.

## Despliegue

El sitio se publica como hosting estático. Opciones gratuitas con HTTPS automático:
- **Netlify** — arrastra el archivo o conecta el repo.
- **Vercel** — importa el repo.
- **GitHub Pages** — *Settings → Pages → rama `main`*.

> Nota: el dominio `.app` exige HTTPS (lista HSTS), por lo que el host debe servir certificado SSL válido.

## Estructura

```
status-lab/
├── index.html      # Página principal (todo el HTML/CSS/JS)
├── assets/         # Imágenes y logo
├── README.md
└── .gitignore
```

---
© 2026 STATUS LAB. Todos los derechos reservados.
