# Setup IA Nomadic — Guía de inicio

> Esta carpeta contiene los archivos de contexto del setup de IA de Nomadic.
> Si llegaste acá, empezá por acá.

---

## ¿Qué es esto?

Son seis archivos que le explican a la herramienta de IA que uses quiénes somos, cómo trabajamos, qué tono usamos y cuáles son los límites. Los configurás una sola vez y desde ahí la IA ya sabe de Nomadic antes de tu primera pregunta.

El setup funciona con cualquier herramienta del stack. No estás atado a una sola opción.

---

## Los archivos de esta carpeta

| Archivo | Qué contiene |
|---------|--------------|
| `GEMINI.md` | Instrucciones globales para Gemini y Antigravity. Se carga automáticamente. |
| `CLAUDE.md` | Instrucciones globales para Claude Cowork y Claude Code. Se carga automáticamente. |
| `about-nomadic.md` | Contexto de la empresa: áreas, roles, herramientas, cultura, Ruta de Valor |
| `working-preferences.md` | Cómo trabaja el agente con vos. **Completá la sección de tu área.** |
| `brand-guidelines.md` | Tono, colores, tipografía, nomenclatura y protocolos de comunicación |
| `safety.md` | Reglas de seguridad no negociables para cualquier herramienta |

---

## Dos ecosistemas, un mismo setup

### Arranque — Ecosistema Google
*Nomadic te lo provee. No hace falta contratar nada extra.*

| Herramienta | Para qué | Setup |
|-------------|----------|-------|
| **Gemini** | Chat inteligente con contexto de Nomadic. Pensar, redactar, consultar. | 5 minutos |
| **Antigravity** | Agente con acceso a tus archivos y conectores. Ejecuta tareas en tu nombre. | 10 minutos |

→ Si es tu primera vez, arrancá por Gemini. Funciona con tu cuenta de Google de Nomadic sin instalar nada.

---

### Level up — Ecosistema Claude
*Para quienes ya usan el Arranque y quieren ir más lejos: más autonomía, más integración, capacidad de ejecutar tareas más complejas.*

| Herramienta | Para qué | Setup |
|-------------|----------|-------|
| **Claude Chat** | Chat con proyectos y contexto persistente | 5 minutos |
| **Claude Cowork** | Agente de escritorio con acceso a archivos y conectores | 10 minutos |
| **Claude Code** | Agente de terminal para automatizaciones y procesamiento de datos | 20 minutos |

→ Requiere cuenta Claude Pro ($20/mes). Consultá con Wilson antes de suscribirte.

---

## Por dónde empezar

### Gemini — Arranque (arrancá acá)

1. Entrá a [gemini.google.com](https://gemini.google.com) con tu cuenta de Nomadic
2. En el panel izquierdo → **Gems** → **New Gem**
3. Nombre: `Nomadic IA — [tu nombre]`
4. En el campo de instrucciones, pegá el contenido del archivo `GEMINI.md`
5. Subí `about-nomadic.md`, `working-preferences.md` y `brand-guidelines.md` como archivos del Gem
6. Guardá y abrí una nueva conversación desde el Gem

Desde ahora, cada vez que uses este Gem va a arrancar con todo el contexto de Nomadic ya cargado.

**Primer prompt para verificar que funcionó:**
```
Leé los archivos de contexto que tenés cargados y explicame en tres oraciones qué sabés sobre Nomadic.
```

---

### Antigravity — Arranque

Antigravity es el agente de Google. A diferencia de Gemini Chat, puede ejecutar tareas en tu nombre: leer archivos de tu Drive, buscar en Slack, preparar documentos.

1. Descargá Antigravity desde [antigravity.google](https://antigravity.google)
2. Iniciá sesión con tu cuenta de Nomadic
3. Creá una carpeta en tu computadora: `~/nomadic-workspace/`
4. Copiá todos los archivos de este setup ahí dentro
5. En Antigravity → **Settings** → seleccioná `~/nomadic-workspace/` como carpeta de trabajo
6. El archivo `GEMINI.md` se carga automáticamente

**Primer prompt para verificar:**
```
¿Qué podés hacer por mí como integrante del equipo Nomadic? Listame 5 casos de uso concretos para mi rol.
```

---

### Claude Chat — Level up

1. Entrá a [claude.ai](https://claude.ai) o descargá la app
2. En el sidebar → **New Project** → nombre: `Nomadic — [tu nombre]`
3. En **Project Instructions**, pegá el contenido de `CLAUDE.md`
4. Subí `about-nomadic.md`, `working-preferences.md` y `brand-guidelines.md` como archivos del proyecto
5. Guardá. Cada nueva conversación dentro del proyecto arranca con el contexto de Nomadic listo.

---

### Claude Cowork — Level up

1. Descargá la app desde [claude.com/download](https://claude.com/download) (requiere Claude Pro)
2. Abrí el tab **Cowork** → **Select Folder** → elegí `~/nomadic-workspace/`
3. En **Settings > Connectors**, conectá: Google Drive, Gmail (modo Ask), Google Calendar, Slack (modo Ask)
4. El archivo `CLAUDE.md` se carga automáticamente al seleccionar la carpeta

---

### Claude Code — Level up

1. Instalá Node.js desde [nodejs.org](https://nodejs.org) → versión LTS
2. En la terminal: `npm install -g @anthropic-ai/claude-code`
3. Autenticate: `claude` (abre el navegador para login)
4. Navegá a tu workspace: `cd ~/nomadic-workspace/`
5. Lanzá una sesión: `claude`

El archivo `CLAUDE.md` se carga automáticamente al abrir Claude Code dentro de esa carpeta.

---

## Personalizá tu setup

Abrí `working-preferences.md` y completá la sección de tu área:

```
Área: [tu área — ej: Medios Editorial, CX, Growth]
Rol: [tu rol — ej: Analista SEO, CS, Editor]
Clientes o proyectos activos: [lista o "no aplica"]
Tipo de outputs que produzco más seguido:
  - [ej: reportes mensuales de SEO, estrategias de contenido]
  - [ej: mails a clientes, minutas de reunión]
```

---

## Si ya usabas ChatGPT u otra herramienta

Podés seguir usándola — convive sin problema. Los archivos de este setup son compatibles con cualquier herramienta que lea archivos de contexto. La recomendación de Nomadic para escalar es el ecosistema de este setup, pero no es un reemplazo obligatorio.

---

## Dudas y soporte

- Canal principal: **#inteligencia-artificial** en Slack — dudas, casos de uso, tips
- Blocker crítico: DM a Wilson (AI & Automation Lead)

---

*Setup construido por el equipo de IA & Automation de Nomadic — marzo 2026*
