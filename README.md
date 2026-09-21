Creas un proyecto nuevo, por ejemplo logopeda, pegas el prompt maestro y Codex prepara la estructura base. Después tú metes los materiales donde corresponda: referencias visuales en referencias/estilo/, información del negocio en referencias/negocio/, imágenes reales en assets/images/, logotipo en assets/logos/, etc.

A partir de ahí, Codex debería trabajar en este orden:

Inspecciona el proyecto y crea solo las carpetas/archivos que falten.
Lee las referencias visuales.
Lee los documentos del negocio que hayas añadido.
Si le das una URL antigua, la analiza con Firecrawl si está disponible.
Extrae todo lo que ya puede saber sin preguntarte.
Te entrevista solo sobre lo que falta.
Con toda esa información genera BRIEF.md, PRODUCT.md, CONTENT.md y DESIGN.md.
Con esos documentos ya consolidados diseña e implementa la web.
Finalmente revisa responsive, accesibilidad, enlaces, formularios y coherencia visual.

La estructura conceptual sería esta:

PROYECTO LOGOPEDA
│
├── PROMPT MAESTRO
│
├── referencias/
│   ├── estilo/
│   │   ├── capturas
│   │   ├── DESIGN.md de referencia
│   │   ├── tokens
│   │   └── CSS de referencia
│   │
│   └── negocio/
│       ├── dossier.pdf
│       ├── servicios.docx
│       └── notas
│
├── assets/
│   ├── images/
│   ├── logos/
│   └── icons/
│
├── BRIEF.md
├── PRODUCT.md
├── CONTENT.md
├── DESIGN.md
├── AGENTS.md
│
└── web

Y puedes arrancar proyectos de tres maneras distintas sin cambiar el sistema:

Solo conversación
→ «Es una clínica de logopedia de Valencia, estos son los servicios...»

Con documentación
→ metes PDF, Word, textos, logos, fotos, etc.

Con web antigua
→ «Esta es la web actual: ... Analízala antes de preguntarme.»

O combinar las tres, que probablemente será lo habitual.

Hay solo un ajuste que haría al prompt que te di antes: no crearía automáticamente carpetas vacías como capturas/, icons/, logos/, etc. si todavía no hacen falta. Para un proyecto nuevo sí crearía la estructura documental principal y referencias/, pero dejaría que vaya creando subcarpetas conforme aparezcan recursos. Así el repositorio no empieza lleno de carpetas vacías.

Y otra cosa importante: DESIGN.md dentro de la raíz debería ser el diseño del proyecto actual. Si tú quieres pasarle un DESIGN.md de otra web para inspirarse, ese debería ir en:

referencias/estilo/DESIGN.md

Así Codex no confunde la referencia con las decisiones definitivas del nuevo proyecto.

En resumen: sí, el prompt sirve para lo que quieres montar. Lo que estamos construyendo realmente es una plantilla de inicio de proyecto para Codex, no una plantilla de landing. Y esa distinción es la correcta.
