# Prompt para llevar STATUS LAB a VS Code + GitHub

## 1) Prompt para pegar en el asistente de IA de VS Code
> (Copilot Chat en modo Agente, o Claude en VS Code. Pégalo tal cual.)

```
Quiero montar una landing page estática llamada "STATUS LAB" en este proyecto de VS Code y subirla a GitHub. Ya tengo un archivo index.html con todo el HTML/CSS/JS en un solo archivo (landing dark monocromática: blanco, negro y grises, con hero, servicios de IA y Marketing, proceso y formulario de contacto).

Haz lo siguiente paso a paso:

1. Crea la siguiente estructura de carpetas en el proyecto:
   - index.html  (mi archivo principal, ya lo voy a pegar / ya está)
   - /assets/    (carpeta para imágenes y el logo)
   - README.md
   - .gitignore

2. Genera un README.md profesional que explique:
   - Qué es STATUS LAB (empresa de tecnología con IA y Marketing para empresas)
   - Que es una landing page estática (HTML/CSS/JS, sin dependencias)
   - Cómo verla en local (abrir index.html o usar Live Server)
   - Cómo desplegarla (Netlify, Vercel o GitHub Pages)

3. Genera un .gitignore apropiado para un proyecto web estático
   (incluye .DS_Store, node_modules/, .vscode/ opcional, *.log).

4. Inicializa git en el proyecto, haz el primer commit con el mensaje
   "feat: landing inicial STATUS LAB" y deja todo listo para subir.

5. Dame los comandos exactos para crear el repositorio en GitHub y
   hacer el push (tanto con GitHub CLI `gh` como con git tradicional),
   y explícame cómo activar GitHub Pages para publicarla gratis.

6. Recomiéndame extensiones útiles de VS Code para este proyecto
   (Live Server, Prettier, etc.).

Mantén el código en un solo archivo index.html por ahora. No agregues
frameworks ni build tools: debe seguir siendo HTML estático puro.
```

---

## 2) Comandos manuales (si prefieres hacerlo tú)

### A. Abrir el proyecto en VS Code
1. Crea una carpeta, por ejemplo `status-lab`, y copia dentro tu `index.html`.
2. En VS Code: `File > Open Folder...` y selecciona `status-lab`.
3. Instala la extensión **Live Server** y haz clic derecho en `index.html > Open with Live Server` para verla en vivo.

### B. Inicializar Git y primer commit
```bash
cd ruta/a/status-lab
git init
git add .
git commit -m "feat: landing inicial STATUS LAB"
git branch -M main
```

### C. Subir a GitHub

**Opción rápida con GitHub CLI (`gh`):**
```bash
gh repo create status-lab --public --source=. --remote=origin --push
```

**Opción manual:** crea el repo vacío en github.com (botón *New*),
copia su URL y luego:
```bash
git remote add origin https://github.com/TU-USUARIO/status-lab.git
git push -u origin main
```

### D. Publicar gratis con GitHub Pages
1. En tu repo de GitHub: **Settings > Pages**.
2. En *Source* elige la rama **main** y carpeta **/(root)**.
3. Guarda. En 1–2 min tu sitio estará en:
   `https://TU-USUARIO.github.io/status-lab/`
4. Para usar tu dominio propio: en *Pages > Custom domain* escribe tu dominio
   y configura el DNS (un registro CNAME apuntando a `TU-USUARIO.github.io`).

---

## 3) Extensiones recomendadas de VS Code
- **Live Server** — recarga en vivo mientras editas.
- **Prettier** — formatea el código automáticamente.
- **HTML CSS Support** / **IntelliSense for CSS** — autocompletado.
- **GitLens** — historial y control de cambios de Git.
- **GitHub Pull Requests** — gestionar el repo desde VS Code.
