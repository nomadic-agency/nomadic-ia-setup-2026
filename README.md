# Setup IA Nomadic — Guía de inicio

> Para Claude Chat, Claude Cowork y Claude Code.
> Si llegaste acá, estás en el lugar correcto para arrancar.

---

## ¿Qué es esto?

Esta carpeta es tu **"cerebro de IA"** para el trabajo en Nomadic. Contiene archivos de contexto que Claude lee automáticamente al inicio de cada sesión — para que no tengas que explicar quién sos, dónde trabajás y cómo querés que te ayude cada vez que abrís una nueva conversación.

El concepto es simple: **una vez que lo configurás, Claude ya sabe cómo trabajar con vos.**

---

## Archivos de esta carpeta

| Archivo | Qué contiene |
|---------|--------------|
| `CLAUDE.md` | Instrucciones globales. Claude lo lee primero, siempre. |
| `about-nomadic.md` | Contexto de la empresa: áreas, roles, herramientas, cultura |
| `working-preferences.md` | Cómo querés que Claude trabaje con vos |
| `brand-guidelines.md` | Tono y estilo de comunicación Nomadic |
| `safety.md` | Reglas de seguridad para sesiones de Cowork y Claude Code |

---

## Las tres herramientas

En Nomadic usamos Claude en tres capas. No son opciones — son niveles. Arrancás por el primero y vas sumando:

| # | Herramienta | Para qué | Tiempo de setup |
|---|-------------|----------|-----------------|
| 1 | **Claude Chat** (web o app) | Pensar, redactar, consultar | 5 minutos |
| 2 | **Claude Cowork** (desktop) | Trabajar con tus archivos, automatizar sin código | 10 minutos |
| 3 | **Claude Code** (terminal) | Construir automatizaciones, procesar datos, crear herramientas | 20 minutos |

---

## 1 — Claude Chat (arrancá acá)

La base. Chat inteligente con contexto de Nomadic siempre cargado.

### Setup (5 minutos)

1. Entrá a [claude.ai](https://claude.ai) o descargá la app desde [claude.com/download](https://claude.com/download)
2. En el sidebar izquierdo → **New Project** → ponerle nombre (ej: "Nomadic — [tu nombre]")
3. En **Project Instructions**, pegá el contenido del archivo `CLAUDE.md`
4. Subí `about-nomadic.md`, `working-preferences.md` y `brand-guidelines.md` como archivos del proyecto
5. Listo. Cada nueva conversación dentro del proyecto arranca con todo el contexto de Nomadic ya cargado.

### Qué podés hacer desde el día uno

Claude Chat es para pensar, no para ejecutar. Usalo para estructurar problemas, generar criterios, explorar enfoques y preparar el terreno antes de actuar.

**Estructurar un problema antes de resolverlo:**
```
Tengo que [describir situación compleja con un cliente / proyecto / decisión].
Ayudame a pensar el problema: ¿cuáles son las variables relevantes,
qué me falta saber, y cuáles son los enfoques posibles?
```

**Generar criterios de decisión:**
```
Necesito decidir [qué herramienta usar / cómo priorizar / cómo estructurar algo].
Dame un framework de criterios para evaluarlo, con pros y contras de cada camino.
```

**Preparar el contexto para una sesión de Cowork o Claude Code:**
```
Voy a automatizar [descripción del proceso]. Antes de arrancar,
ayudame a definir: inputs, outputs esperados, casos borde, y criterios de calidad.
Con eso estructurado, puedo pasarle el brief al agente.
```

> **Nota:** Claude Chat con Projects no lee archivos de tu computadora ni ejecuta tareas en tu máquina. Es chat con contexto persistente. Para trabajar con tus archivos reales, pasá a Cowork.

---

## 2 — Claude Cowork (el siguiente nivel)

Cowork vive en la app de escritorio y tiene acceso directo a tu carpeta de trabajo. Le delegás tareas y las ejecuta en tu máquina — sin que tengas que estar presente.

### Setup (10 minutos)

**Paso 1: Descargá la app de escritorio**
→ [claude.com/download](https://claude.com/download)

Necesitás cuenta Claude Pro ($20/mes) para acceder a Cowork.

**Paso 2: Creá tu workspace**

Creá esta carpeta en tu computadora:
```
~/nomadic-workspace/
```
Copiá todos los archivos de este setup ahí dentro (CLAUDE.md, about-nomadic.md, working-preferences.md, brand-guidelines.md).

**Paso 3: Seleccioná tu carpeta**

Abrí la app → tab **Cowork** → **Select Folder** → elegí `~/nomadic-workspace/`.

**Paso 4: Configurá las instrucciones globales**

En **Settings > Cowork > Global Instructions**, pegá esto:
```
Antes de cualquier tarea, leé CLAUDE.md, about-nomadic.md, working-preferences.md y brand-guidelines.md.
Mostrá un plan breve antes de ejecutar tareas que toquen múltiples archivos.
Esperá mi aprobación antes de ejecutar.
Nunca borrés archivos sin mi confirmación explícita.
```

**Paso 5: Conectá Google Workspace y Slack**

Estas dos conexiones son las más importantes para el trabajo diario en Nomadic. Hacelas antes de cualquier otra.

En **Settings > Connectors**:

- **Google Drive** → permite leer y escribir en tus documentos, buscar entregables, trabajar con archivos de cliente directamente
- **Gmail** → para redactar, buscar y gestionar mails *(configurar en modo **Ask**, nunca Allow — no querés que mande mails solo)*
- **Google Calendar** → para revisar agenda, preparar reuniones y crear eventos
- **Slack** → para buscar contexto de conversaciones anteriores y postear *(modo **Ask** para postear, Allow solo para lectura)*

> Conectá las cuatro desde el arranque. Son el núcleo del trabajo en Nomadic.

**Paso 6: Instalá plugins y configurá skills**

**Plugins** — En **Customize > Browse Plugins**:
- Instalá **Productivity** primero (útil para cualquier rol)
- Según tu área: **Marketing**, **Sales**, **Operations**, o el que aplique
- Una vez instalado, escribí `/` en Cowork para ver los slash commands disponibles

**Skills** — En **Customize > Skills**:

Las skills son archivos de instrucciones para tareas específicas y repetibles. Son uno de los multiplicadores de calidad más grandes de Cowork. Ejemplos para Nomadic:

- `skill-reporte-mensual` → genera reportes con el formato y tono correcto cada vez
- `skill-outline-seo` → outlines de contenido con la estructura que aprobó el cliente
- `skill-minuta` → minutas con decisiones, owners y fechas en formato Nomadic
- `skill-mail-cliente` → mails con el tono cercano-profesional de la agencia

Para crear una skill: **Customize > Skills > New Skill**. Describí qué hace, cómo debe sonar, y pegá 1-2 ejemplos de output bueno que ya hayas producido. Claude va a replicar ese estándar en cada tarea futura.

**MCPs (conectores avanzados)** — para sumar más herramientas del stack Nomadic:
- **Asana** → crear y consultar tareas directamente desde Claude
- **Airtable** → acceder a datos operativos sin abrir la app

Los MCPs se configuran en **Settings > Integrations > MCP Servers**. Pedile ayuda a Wilson si llegás a este punto.

### Flujo de trabajo recomendado

Para tareas no triviales, siempre en dos pasos:
1. Pedile que **planifique** antes de ejecutar
2. Revisá el plan, aprobalo, y recién ahí dejalo correr

```
Necesito [descripción de tarea].
Primero mostrá el plan completo, esperá mi aprobación y después ejecutá.
```

---

## 3 — Claude Code (para los que quieren construir)

Claude Code corre en la terminal. No necesitás saber programar — necesitás perderle el miedo a una ventana negra. A partir de ahí, podés construir automatizaciones reales.

### Setup (20 minutos)

**Paso 1: Instalá Node.js**

Descargá desde [nodejs.org](https://nodejs.org) → versión **LTS**.

Verificá que funcionó abriendo la terminal y corriendo:
```bash
node --version
```
Tiene que aparecer algo como `v20.x.x`.

> **¿Dónde está la terminal?**
> - Mac: buscá "Terminal" en Spotlight (Cmd + Espacio)
> - Windows: buscá "PowerShell" en el menú inicio

**Paso 2: Instalá Claude Code**

```bash
npm install -g @anthropic-ai/claude-code
```

**Paso 3: Autenticate**

```bash
claude
```

La primera vez te va a abrir el navegador para loguearte con tu cuenta Claude Pro. Hacés login, volvés a la terminal, y listo.

**Paso 4: Copiá los archivos de contexto**

Si ya hiciste el setup de Cowork, la carpeta ya existe. Si no:
```bash
mkdir ~/nomadic-workspace
```

Copiá los archivos de este setup ahí (CLAUDE.md, about-nomadic.md, working-preferences.md, brand-guidelines.md).

**Paso 5: Lanzá tu primera sesión**

```bash
cd ~/nomadic-workspace
claude
```

Desde ahora, cada vez que abras Claude Code dentro de esta carpeta, va a leer el `CLAUDE.md` automáticamente y arrancar con todo el contexto de Nomadic listo.

### Los 3 modos — entendelos antes de arrancar

Dentro de Claude Code, **Shift+Tab** cambia el modo de operación:

| Modo | Qué hace | Cuándo usarlo |
|------|----------|---------------|
| **Normal** | Pregunta antes de cada acción | Cuando explorás algo nuevo |
| **Auto-Accept** (Shift+Tab × 1) | Ejecuta sin pedir confirmación | Cuando revisaste el plan y confiás |
| **Plan Mode** (Shift+Tab × 2) | Solo planifica, no ejecuta nada | Para tareas complejas — siempre arrancá acá |

**Flujo recomendado para empezar:**
1. **Plan Mode** → pedile que planifique la tarea
2. Revisá que el plan tiene sentido
3. **Auto-Accept** → dejalo ejecutar

### Comandos útiles

```bash
claude              # Arrancar una sesión
/compact            # Compactar contexto cuando la sesión se hace larga (ahorra tokens)
/clear              # Limpiar la conversación y arrancar fresco
/exit               # Cerrar la sesión
```

### Cuánto cuesta

| Plan | Precio | Para quién |
|------|--------|------------|
| Claude Pro | $20/mes | Para arrancar — suficiente para la mayoría |
| Claude Max 5x | $100/mes | Uso intensivo diario |
| Claude Max 20x | $200/mes | Proyectos de automatización pesados |

### IDE recomendado: Cursor o VSCode

En vez de usar la terminal sola, podés usar un IDE que te da una interfaz más amigable y tiene la terminal integrada:

- **[Cursor](https://cursor.com)** — el IDE recomendado para trabajar con IA. Tiene plan gratuito y Claude Code corre directo en su terminal integrada. La experiencia es mucho más visual que la terminal pura.
- **[VSCode](https://code.visualstudio.com)** — opción gratuita de Microsoft, muy popular. Instalás la extensión oficial de Claude Code desde el marketplace y tenés todo en un mismo lugar.

Para arrancar: descargá Cursor, abrí la carpeta `~/nomadic-workspace/` desde ahí, y usá la terminal integrada (Ctrl+\` o Cmd+\`) para correr `claude`.

### Alternativas gratuitas a Claude Code

Si todavía no tenés cuenta paga:
- **Antigravity** — herramienta de Google para agentes de IA, tiene tier gratuito
- **OpenCode** — alternativa open source a Claude Code

Los archivos de contexto de este setup (CLAUDE.md y compañía) funcionan con cualquiera de estas herramientas.

---

## Personalizá tu setup

El archivo `working-preferences.md` tiene una sección que completás vos. Abrilo y llenala:

```
Área: [tu área — ej: Medios Editorial, CX, Growth]
Rol: [tu rol — ej: Analista SEO, CS, Editor]
Clientes que manejo: [lista o "no aplica"]
Tareas más frecuentes:
  1. [descripción]
  2. [descripción]
  3. [descripción]
```

**Primer prompt para arrancar** (copiá y pegá en tu primera sesión):

```
Leé los archivos CLAUDE.md, about-nomadic.md, working-preferences.md, brand-guidelines.md y safety.md.

Después preguntame de a una:
1. ¿En qué área trabajás y cuál es tu rol?
2. ¿Qué tipo de outputs producís más seguido?
3. ¿Hay clientes o proyectos activos que debería conocer?

Con esas respuestas, completá la sección "Personalización por área" de working-preferences.md y guardala.
```

---

## Primeras tareas que podés delegar

Los prompts de abajo están organizados por herramienta. Usá la que corresponde a tu nivel de setup actual.

### Claude Chat — para pensar y redactar

**Armar una estrategia de contenido:**
```
Soy [rol] en Nomadic trabajando con [tipo de cliente / vertical].
Basándote en el contexto de la empresa, armá una estrategia de contenido SEO
para el mes de [mes] enfocada en [objetivo]. Incluí pilares temáticos,
formatos recomendados y criterios de priorización.
```

**Revisar un entregable antes de mandar:**
```
Revisá este [reporte / mail / estrategia] antes de que lo mande al cliente.
Checkeá: tono Nomadic, claridad, próximo paso definido, términos bien escritos.
[pegá el texto]
```

### Claude Cowork — para trabajar con tus archivos

**Procesar un archivo y generar un entregable:**
```
Tengo en la carpeta el archivo [nombre del archivo] con los datos de Search Console del mes.
Generá la sección de análisis del reporte mensual en formato .docx con template Nomadic.
Tono directo, datos primero, conclusión accionable al final.
```

**Preparar una reunión buscando contexto en Slack y Calendar:**
```
Tengo una reunión mañana con [cliente] a las [hora].
Buscá en Slack los últimos mensajes relevantes sobre esta cuenta,
revisá si hay algo en Calendar sobre reuniones previas,
y armame un doc de preparación con: contexto reciente, puntos a cubrir
y preguntas clave para hacerles.
```

**Resumir una semana de updates de un cliente:**
```
Buscá en Slack todas las menciones de [cliente] de la última semana.
Organizalas en: decisiones tomadas, pendientes, alertas o problemas abiertos.
Guardalo en /outputs/resumen-[cliente]-semana-[número].md
```

### Claude Code — para construir y automatizar

**Procesar múltiples archivos en lote:**
```
Tengo 20 artículos en la carpeta /drafts que necesitan revisión de estilo Nomadic.
Leé brand-guidelines.md, pasá cada archivo, aplicá las correcciones y guardá
los resultados en /outputs con el mismo nombre de archivo.
Mostrá primero el plan y esperá mi aprobación.
```

**Automatizar un reporte recurrente:**
```
Necesito automatizar la generación del reporte semanal de [cliente].
Los datos de entrada están en [descripción de fuente].
El formato de salida es el de /templates/reporte-semanal.md.
Armá el plan primero, sin ejecutar nada todavía.
```

---

## Reglas de seguridad

Están en `safety.md`. Leé ese archivo antes de arrancar con Cowork o Claude Code.

La regla que resume todo: **leer siempre está permitido, escribir o enviar siempre requiere aprobación.**

---

## Dudas y soporte

- Canal principal: **#inteligencia-artificial** en Slack
- Tips, casos de uso y automatizaciones que funcionaron: se comparten ahí
- Bloqueador crítico: DM a Wilson (AI & Automation Lead)

---

---

*Setup construido por el equipo de IA & Automation de Nomadic — marzo 2026*
