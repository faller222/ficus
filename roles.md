estoy armando una empresa de sw y marketing digital a puro agend IA y engineering prompting.

sin entrar en detalles, que skilles necesito?

preVenta, un skill que dado un poco dw contexto del problema empatiza con el leed y agrega valor a su solucion entendiendo el dolor que representa su problema.

diseñadorWeb - hace las ux ui siguiento w3c a11y i18n entre otros

BusinessAnalist es aquel que entiende la primera entrevista e indaga que otros requisitoss necesita agregando otros implicitos como seguridad, alta disponibilidad, i18n etc...

copyWriter - este es fundamental, es quien decide que textos van en cada seccion. piede inculir varias idas y vueltas con el uxUi para coordinar, habla de hero, CTA entre otros.

developer - es quien siguiendo la arquitectura propuesta desarrolla toda la solucion, tests, linter, todas law buenas practicas

fixer - este es vital, corrige errores o hace mejoras sobre el sistema, a diferencia del developer este hace un botom up en la documentacion actualozando el copy, la ux ui, las decisiones de arquitectura y anotandolo en un changelog.

auditor - este recorre todos los documentos y el codigo implementado para saver si hay gaps y da un informe exaustivo de la situacion del proyecto

arquitecto - sefun el proyecto tendra mas o menos participacion, pero decide que stack es mejor dentro de los que ya manejamos, suguiere incuir otras tecnologias que nuesto stack no contempla con la debida justificacion, quenra ADRs con los trade offs

---

que otros roles incuirias? contestame incluyendo todos los que mencione y mejorando la desceipcion de sus roles. 


Sí. Y te diría algo importante: no pienses estos roles como “personas” sino como capacidades especializadas que tus agentes deben ejecutar. Algunos pueden combinarse en proyectos chicos, pero conceptualmente conviene mantenerlos separados porque tienen objetivos y criterios de éxito distintos.

Tu set inicial está bastante bien. Yo lo llevaría a algo así:

1. PreSales / Discovery

Objetivo: convertir una conversación comercial en una comprensión clara del problema y una oportunidad de negocio.

No debería limitarse a “vender”.

Hace:

Entiende el contexto del lead y su industria.
Identifica el dolor explícito y el dolor subyacente.
Hace preguntas que el cliente probablemente no sabe que debería hacerse.
Detecta oportunidades de automatización, digitalización e IA.
Traduce problemas técnicos a impacto de negocio.
Estima complejidad y riesgos preliminares.
Detecta si el proyecto es realmente viable.
Propone una dirección inicial de solución sin comprometer arquitectura prematuramente.
Identifica stakeholders y decisores.
Detecta presupuesto, urgencia y criterios de éxito.
Prepara el handoff hacia Business Analyst.

Output: Discovery Brief / Opportunity Brief.

2. Business Analyst / Product Analyst

Objetivo: transformar el problema de negocio en requisitos completos, coherentes y verificables.

Este es uno de los agentes más importantes.

No debería simplemente transcribir lo que dijo el cliente.

Debe preguntarse:

“¿Qué tendría que ser cierto para que este sistema realmente funcione en producción?”

Por eso debe descubrir requisitos implícitos:

seguridad
permisos
auditoría
disponibilidad
escalabilidad
performance
observabilidad
internacionalización
accesibilidad
privacidad
backups
recuperación ante fallos
integración con terceros
compliance
manejo de errores
edge cases
roles de usuario
workflows
estados
reglas de negocio

También debe detectar contradicciones entre requisitos.

Output: PRD / Requirements Specification / User Stories / Acceptance Criteria.

3. Product Manager / Product Strategist

Este rol lo agregaría explícitamente.

El BA responde:

“¿Qué necesita el sistema?”

El PM responde:

“¿Qué deberíamos construir y por qué?”

Debe:

definir objetivos del producto
priorizar funcionalidades
separar MVP de nice-to-have
definir personas
definir journeys
definir métricas
definir KPIs
evaluar impacto vs esfuerzo
evitar scope creep
definir roadmap
cuestionar features innecesarias
asegurar que la solución resuelva un problema real

Esto es particularmente importante si tu empresa va a vender producto + ingeniería, no solamente desarrollo.

4. UX Researcher

También lo separaría del diseñador.

Antes de diseñar:

analiza usuarios
analiza contexto de uso
identifica jobs-to-be-done
identifica frustraciones
analiza competencia
analiza patrones existentes
identifica riesgos de UX
propone hipótesis
define qué debería validarse

En proyectos pequeños puede fusionarse con UX/UI.

En proyectos importantes, no.

5. UX/UI Designer

Tu descripción va bien, pero agregaría una responsabilidad importante:

no diseña pantallas; diseña una experiencia.

Debe trabajar sobre:

information architecture
user flows
wireframes
UI
responsive design
design system
componentes
estados vacíos
loading
errores
success states
formularios
navegación
mobile/desktop
accesibilidad WCAG
internacionalización
RTL cuando corresponda
consistencia visual

Y debe colaborar iterativamente con Copywriter y Developer.

Además debería producir design decisions, no solamente imágenes.

6. Copywriter / UX Writer

Este lo considero crítico, especialmente para marketing.

No es simplemente “escribir textos lindos”.

Debe decidir:

headline
subheadline
CTA
navegación
beneficios
features
social proof
formularios
errores
empty states
onboarding
mensajes transaccionales
microcopy
FAQs
metadata
SEO copy
tono de marca

Y debe trabajar en loop con UX/UI.

Ejemplo:

UX:

“Necesitamos un CTA acá.”

Copywriter:

“¿Qué acción queremos realmente que tome el usuario?”

Eso cambia el diseño.

7. Brand / Marketing Strategist

Si vas a hacer SW + marketing, yo agregaría este sí o sí.

Determina:

posicionamiento
ICP
buyer personas
propuesta de valor
diferenciadores
tono de marca
messaging
oferta
pricing strategy
funnel
canales
estrategia de contenido
SEO
campañas
conversión

El Copywriter ejecuta buena parte del mensaje.

Este rol decide qué mensaje debería existir y para quién.

8. Solution Architect

Tu Arquitecto debería tener una responsabilidad más amplia que elegir tecnologías.

Debe definir:

arquitectura
boundaries
componentes
integraciones
APIs
persistencia
infraestructura
seguridad
escalabilidad
observabilidad
deployment
resiliencia
estrategia de testing
estrategia de datos
stack

Y especialmente:

ADRs

Cada decisión importante debería poder responder:

qué problema estamos resolviendo
qué alternativas consideramos
qué elegimos
por qué
qué trade-offs aceptamos
qué consecuencias tiene

También debe ser capaz de decir:

“No necesitamos microservicios.”

Eso es tan importante como saber diseñarlos.

9. Security Engineer

Yo no lo dejaría como responsabilidad implícita del arquitecto.

Debe existir como skill independiente.

Analiza:

authentication
authorization
RBAC/ABAC
secrets
OWASP
injection
XSS
CSRF
SSRF
rate limiting
session management
encryption
data exposure
dependency vulnerabilities
supply chain
API security
tenant isolation
audit logs

Y hace threat modeling.

Idealmente:

Security by design, no security al final.

10. Developer / Software Engineer

Tu definición está bien, pero lo haría responsable del implementation contract.

Debe:

implementar arquitectura
respetar ADRs
escribir código mantenible
tests unitarios
integration tests
E2E cuando corresponda
lint
formatting
type safety
documentación técnica
manejo de errores
observabilidad
performance
seguridad
migrations
CI/CD

Y algo importante:

el Developer no debería tener libertad para cambiar silenciosamente decisiones arquitectónicas.

Si descubre algo que invalida una decisión:

Developer → Architect → ADR actualizado → implementación.

11. QA / Test Engineer

Este te falta y es importante.

No debería ser simplemente:

“corro los tests.”

Debe pensar:

“¿Cómo puedo demostrar que esto está mal?”

Trabaja con:

test strategy
unit tests
integration tests
E2E
regression
boundary testing
negative testing
exploratory testing
API testing
browser testing
accessibility testing
compatibility testing

Y valida acceptance criteria.

12. DevOps / Platform Engineer

Otro que agregaría.

Responsable de que:

“el software pueda vivir.”

Incluye:

Docker
CI/CD
environments
infrastructure as code
cloud
networking
secrets
deployment
rollback
backups
disaster recovery
observability
logging
metrics
tracing
cost management

Especialmente importante si tus agentes generan aplicaciones completas.

13. SRE / Reliability Engineer

Puede parecer exagerado, pero conceptualmente es diferente de DevOps.

Se preocupa por:

SLO
SLA
SLI
availability
latency
error budgets
resilience
failure modes
capacity
incident response
disaster recovery
graceful degradation

En proyectos chicos puede ser un skill que el Architect/DevOps active solamente cuando corresponde.

14. Data / Analytics Engineer

Para proyectos con datos.

Responsable de:

modelado de datos
pipelines
ETL/ELT
calidad de datos
analytics
tracking
eventos
métricas
dashboards
data retention
reporting

Y para marketing es especialmente importante.

Porque si construís campañas pero no medís:

estás haciendo diseño, no marketing.

15. SEO Specialist

Para sitios comerciales debería ser una capability explícita.

Debe revisar:

technical SEO
semantic HTML
metadata
structured data
sitemap
robots
canonical
Open Graph
performance
Core Web Vitals
internal linking
search intent
keyword strategy

Y coordinarse con Copywriter + UX + Developer.

16. CRO / Conversion Specialist

Este también es muy interesante para tu modelo.

Su pregunta es:

“¿Por qué alguien visitaría esta página y no convertiría?”

Analiza:

funnel
CTA
friction
forms
trust
social proof
pricing
objections
landing pages
experiments
A/B testing
conversion metrics

No es UX y tampoco es Copywriting.

17. AI Engineer / AI Solutions Architect

En tu caso lo pondría como core, no como accesorio.

Debe decidir cuándo tiene sentido:

LLM
RAG
agents
embeddings
vector DB
structured outputs
tool calling
MCP
multimodal
speech
OCR
classification
extraction
fine-tuning

Y, fundamentalmente:

cuándo NO usar IA.

Debe diseñar:

prompts
context strategy
evaluation
hallucination mitigation
guardrails
cost control
latency
model selection
fallback models
observability
privacy
18. Prompt / Agent Engineer

Este sería particularmente propio de tu empresa.

No es exactamente AI Engineer.

Se dedica a diseñar los agentes internos que producen el software.

Por ejemplo:

PreSales
↓
Business Analyst
↓
Product Manager
↓
UX Research
↓
UX/UI
↕
Copywriter
↓
Architect
↓
Developer
↓
QA
↓
Security
↓
Auditor

Pero además controla:

contexto
memoria
handoffs
tools
instrucciones
artefactos
validaciones
feedback loops
critic agents
evaluators
stopping conditions

Esto puede convertirse en tu verdadera ventaja competitiva.

19. Fixer / Maintainer

Tu concepto me gusta mucho y lo mantendría separado del Developer.

Porque el Developer construye desde una especificación.

El Fixer trabaja sobre:

la realidad existente.

Debe hacer reverse engineering:

Código actual
↓
Comportamiento actual
↓
Documentación existente
↓
Contradicciones
↓
Corrección
↓
Actualización documental

Y actualizar:

requirements
PRD
UX
copy
arquitectura
ADRs
tests
documentación
changelog

Es básicamente el agente que evita que el sistema acumule documentation drift.

20. Auditor / Technical Reviewer

También lo mantendría.

Pero no debería modificar nada.

Debe ser independiente.

Audita:

requirements
UX
copy
arquitectura
seguridad
código
tests
infraestructura
SEO
accesibilidad
performance
documentación
coherencia entre artefactos

Y produce:

Finding
Severity
Evidence
Impact
Recommendation

Por ejemplo:

PRD dice que usuarios pueden tener múltiples organizaciones.

pero:

DB tiene user.organization_id.

Eso es un gap.

21. Release Manager

Para proyectos medianos/grandes.

Decide si el producto está listo para salir.

Valida:

todos los acceptance criteria
tests
migrations
rollback
changelog
version
deployment
environment
secrets
monitoring
alerts
documentation

Y finalmente:

GO / NO-GO.

22. Project Manager / Delivery Manager

No confundir con Product Manager.

Product: qué construir y por qué.

Project/Delivery: cómo y cuándo entregarlo.

Gestiona:

milestones
dependencias
riesgos
bloqueos
scope
deadlines
entregables
estado del proyecto

En un sistema multiagente puede incluso controlar el workflow de los agentes.

23. Client Success / Account Manager

Este es más comercial.

Después de vender:

mantiene relación
recoge feedback
detecta nuevas necesidades
identifica oportunidades
mide satisfacción
coordina cambios
evita churn

Es el puente entre cliente y la fábrica.

24. Cost / FinOps Analyst

Para una empresa basada en agentes IA esto puede ser muchísimo más importante que en una software factory tradicional.

Debe controlar:

tokens
modelos
llamadas
infraestructura
storage
bandwidth
CI/CD
cloud
terceros
costo por proyecto
costo por feature
costo por agente

Y eventualmente calcular:

Revenue
-
AI inference
-
Cloud
-
Tools
-
Engineering
=
Gross Margin

Si no medís esto, podés estar vendiendo proyectos que aparentemente son rentables mientras los agentes se comen el margen.

Y agregaría uno más: Knowledge Manager

Este puede ser el pegamento de todo tu sistema.

Responsable de mantener la memoria institucional del proyecto:

documentación
decisiones
ADRs
convenciones
glossary
domain knowledge
changelog
lessons learned
referencias
dependencias entre artefactos

Su función principal es evitar que cada agente "reinvente" el proyecto.

La arquitectura que yo terminaría usando

No tendría 25 agentes corriendo siempre.

Tendría skills especializados + orchestrator.

Algo así:

                    ┌──────────────────┐
                    │   ORCHESTRATOR   │
                    └────────┬─────────┘
                             │
        ┌────────────────────┼────────────────────┐
        │                    │                    │
COMMERCIAL             PRODUCT             DELIVERY
│                    │                    │
PreSales             Product Manager      Project Manager
Account Manager      Business Analyst     Release Manager
UX Research
UX/UI
Copywriter
Marketing
SEO
CRO
│                    │                    │
└────────────────────┼────────────────────┘
│
ENGINEERING
│
┌──────────────┼──────────────┐
│              │              │
Architect       AI Engineer    Security
│              │              │
Developer      Agent Engineer   QA
│              │              │
DevOps/SRE      Data Engineer
│
Fixer
│
Auditor

Y hay algo todavía más importante:

No todos los agentes deberían tener autoridad para modificar todo.

Yo establecería una especie de ownership matrix.

Por ejemplo:

Artefacto	Owner	Reviewers
Discovery	PreSales	BA
Requirements	BA	Product
PRD	Product	BA
UX	UX/UI	UX Research
Copy	Copywriter	Marketing + UX
Architecture	Architect	Security + Dev
ADR	Architect	Dev
Code	Developer	QA + Architect
Tests	QA	Developer
Infrastructure	DevOps	Architect + Security
Security	Security	Architect
SEO	SEO	Developer + Copy
Analytics	Data	Marketing
Changelog	Fixer	Knowledge Manager
Final audit	Auditor	—

Eso evita un problema enorme de sistemas multiagente:

todos opinan, todos modifican y al final nadie sabe cuál es la verdad.

Tu sistema debería tener una Single Source of Truth por artefacto, ownership, versionado y reglas claras de quién puede modificar qué.

Y una última observación: tu producto no debería venderse internamente como "una empresa que usa agentes IA para programar". Eso es una implementación.

Tu verdadero producto puede ser una software factory agentic, donde el diferencial es que tenés un proceso reproducible que transforma:

problema → discovery → requisitos → producto → diseño → arquitectura → implementación → validación → deployment → mantenimiento → evolución.

Ahí sí hay algo defendible. El prompt en sí es fácilmente copiable; el sistema operativo de agentes, los workflows, los artefactos, las evaluaciones y el conocimiento acumulado son mucho más difíciles de copiar.

---

ok yo le agregaria entonces a los agents que son read only y los que editan, que files editan.

seriá esteicto con el nombre, de archivos o carpetas. un busnes analist maneja un archivo pero el uxUi maneja una carpeta donde estan todos los htmls estaticos para mostrar el diseño.

el developer solo modifica src

y asi...

peero tambien tendria en la carpeta .agents (donde viven todos estos skills) tendria un status.json, para saber si ya se hizo o falta hscer que? es la memoria del orchestrator... si el ux le pidio al copi algo, lo deja ahi, waiting for [copy and architect] por decir algo.

el orchestartor lee eso e invoca al arquitecto y al copier. una vez terminen le dice al ux que ya respondieron (o actualizaron sus files)

---

Eso ya es bastante más serio que simplemente tener una carpeta con prompts. Estás diseñando un sistema de agentes con ownership, permisos, estado y handoffs explícitos.

Y haría un ajuste conceptual importante: no pensaría solamente en read-only vs edit. Tendría tres dimensiones independientes:

Qué puede leer
Qué puede modificar
Qué puede solicitar a otros agentes

Porque un agente puede no tener permiso para editar arquitectura, pero perfectamente puede crear una solicitud para el Architect.

1. Cada skill debería declarar su contrato

Dentro de .agents/ yo tendría algo así:

.agents/
├── orchestrator/
│   ├── skill.md
│   └── rules.md
│
├── pre-sales/
│   └── skill.md
├── business-analyst/
│   └── skill.md
├── product-manager/
│   └── skill.md
├── ux-researcher/
│   └── skill.md
├── ux-ui/
│   └── skill.md
├── copywriter/
│   └── skill.md
├── architect/
│   └── skill.md
├── developer/
│   └── skill.md
├── qa/
│   └── skill.md
├── security/
│   └── skill.md
├── devops/
│   └── skill.md
├── fixer/
│   └── skill.md
├── auditor/
│   └── skill.md
│
├── status.json
├── requests.json
└── changelog.md

Pero no dejaría que los skills decidan libremente dónde pueden escribir.

El orchestrator debería conocer el contrato.

2. Cada agente debería declarar su ownership

Por ejemplo, ux-ui/skill.md podría declarar conceptualmente:

ROLE: UX/UI Designer


MODE:
read: true
write: true


READ:
- requirements/
- product/
- architecture/
- brand/


WRITE:
- design/


REQUEST:
- copywriter
- architect
- business-analyst

Pero incluso mejor:

READ:
requirements/**
product/**
architecture/**


WRITE:
design/**


FORBIDDEN:
src/**
infrastructure/**
architecture/**

Eso es mucho más robusto.

3. Y sí: archivos/carpetas concretos

Tu ejemplo del BA es perfecto.

Por ejemplo:

requirements/
└── requirements.md

BA:

READ:
discovery/**
product/**


WRITE:
requirements/requirements.md

Mientras UX:

design/
├── index.html
├── pricing.html
├── contact.html
├── dashboard.html
├── assets/
├── css/
└── js/

UX puede:

WRITE:
design/**

pero no:

WRITE:
src/**
4. Developer

Acá sería extremadamente estricto.

developer


READ:
requirements/**
product/**
design/**
architecture/**
security/**
qa/**


WRITE:
src/**
tests/**

Y yo agregaría:

FORBIDDEN:
requirements/**
design/**
architecture/**

¿Por qué?

Porque si el Developer descubre:

"Esto está mal diseñado."

no debería corregir silenciosamente el diseño.

Debe crear una solicitud:

REQUEST:
ux-ui

con:

reason:
"The current design requires a workflow that is incompatible
with the backend authorization model."


impact:
high

Eso genera trazabilidad.

5. El Fixer es distinto

Tu idea del Fixer se vuelve todavía más interesante con este sistema.

El Developer:

src/**

El Fixer:

src/**
requirements/**
design/**
architecture/**
product/**

pero no debería tener libertad absoluta.

Su trabajo es sincronizar realidad y documentación.

Por ejemplo:

src/checkout.ts

descubre que existe una regla que no está documentada.

Entonces actualiza:

requirements/requirements.md

y:

changelog.md

y eventualmente:

architecture/ADR-017.md

Pero debería registrar qué cambió y por qué.

6. Y acá entra tu status.json

Sí.

Pero yo no lo usaría solamente como:

{
"ux": "done",
"copy": "pending"
}

Eso se queda corto muy rápido.

Lo trataría como el estado de ejecución del proyecto, no como documentación.

Por ejemplo:

{
"project": {
"status": "in_progress",
"phase": "design"
},


"tasks": [
{
"id": "TASK-001",
"created_by": "ux-ui",
"description": "Need final CTA copy for hero",
"waiting_for": ["copywriter"],
"status": "blocked"
},
{
"id": "TASK-002",
"created_by": "ux-ui",
"description": "Need confirmation whether authentication is required",
"waiting_for": ["architect", "business-analyst"],
"status": "blocked"
}
]
}

El orchestrator lee eso.

Detecta:

waiting_for:
copywriter
architect
business-analyst

y ejecuta esos agentes.

7. Pero haría algo todavía mejor: requests/

No pondría toda la comunicación dentro de status.json.

Porque eventualmente va a explotar.

Tendría:

.agents/
├── status.json
├── requests/
│   ├── REQ-001.json
│   ├── REQ-002.json
│   └── REQ-003.json
└── ...

Entonces:

REQ-001.json
{
"id": "REQ-001",
"from": "ux-ui",
"to": ["copywriter"],
"type": "input_required",
"status": "pending",


"request": {
"topic": "Hero CTA",
"question": "What is the primary conversion action?"
},


"context": {
"file": "design/index.html",
"section": "hero"
}
}

Copywriter trabaja.

Cuando termina:

{
"id": "REQ-001",
"status": "resolved",
"resolved_by": "copywriter",
"resolution": {
"file": "content/home.md"
}
}

Y el orchestrator detecta:

REQ-001 → resolved

y despierta UX.

8. Esto te permite crear un verdadero event loop

Tu orchestrator podría funcionar conceptualmente así:

READ status.json
↓
FIND pending / blocked tasks
↓
CHECK dependencies
↓
SELECT eligible agents
↓
INVOKE AGENT
↓
AGENT READS OWN CONTRACT
↓
AGENT WORKS
↓
AGENT WRITES OWN FILES
↓
AGENT CREATES REQUESTS
↓
UPDATE STATUS
↓
ORCHESTRATOR RE-EVALUATES
↓
REPEAT

Hasta llegar a:

{
"project": {
"status": "completed"
}
}
9. Hay una cosa que NO dejaría hacer al agente

No confiaría solamente en:

"El skill dice que no puede editar src."

Eso es una regla semántica, no un mecanismo de seguridad.

Si tu infraestructura lo permite, el orchestrator debería ejecutar cada agente con un filesystem restringido.

Por ejemplo:

UX Agent
↓
write access:
design/**

Developer:

write access:
src/**
tests/**

Architect:

write access:
architecture/**

etc.

Así tenés:

Policy

El prompt dice qué debería hacer.

Enforcement

El runtime impide que haga otra cosa.

Esto es muchísimo más importante de lo que parece.

Porque eventualmente vas a tener agentes autónomos ejecutando comandos.

10. Yo agregaría manifest.json

Incluso tendría un registro central:

.agents/
└── manifest.json

Algo parecido a:

{
"agents": {
"business-analyst": {
"read": [
"discovery/**",
"product/**"
],
"write": [
"requirements/requirements.md"
]
},


    "ux-ui": {
      "read": [
        "requirements/**",
        "brand/**",
        "content/**"
      ],
      "write": [
        "design/**"
      ]
    },


    "copywriter": {
      "read": [
        "requirements/**",
        "design/**",
        "brand/**"
      ],
      "write": [
        "content/**"
      ]
    },


    "architect": {
      "read": [
        "requirements/**",
        "design/**",
        "security/**"
      ],
      "write": [
        "architecture/**"
      ]
    },


    "developer": {
      "read": [
        "requirements/**",
        "design/**",
        "content/**",
        "architecture/**"
      ],
      "write": [
        "src/**",
        "tests/**"
      ]
    }
}
}

Eso se convierte en una especie de ACL del sistema de agentes.

11. Y aparece una propiedad brutalmente buena

Podés hacer que cada artefacto tenga un owner único.

Por ejemplo:

requirements.md       → business-analyst
PRD.md                → product-manager
design/**             → ux-ui
content/**            → copywriter
architecture/**       → architect
src/**                → developer
tests/**              → qa/developer
infrastructure/**     → devops
security/**           → security
analytics/**          → data

Entonces cuando algo está mal:

"¿Quién es responsable de esto?"

la respuesta es determinística.

No:

"el agente que lo tocó último."

Sino:

el owner del artefacto.

12. Incluso podés detectar drift automáticamente

Esto es donde tu Fixer + Auditor + ownership empieza a ponerse realmente potente.

Ejemplo:

Architecture dice:

PostgreSQL

pero src/ usa MongoDB.

Auditor:

ARCH-DRIFT-001
severity: critical


architecture/architecture.md
says PostgreSQL


src/database/
uses MongoDB

Orchestrator:

AUDITOR → BLOCKED


WAITING FOR:
architect
developer

Architect decide:

ADR-023:
MongoDB replaces PostgreSQL

Developer adapta código.

Fixer actualiza documentación.

Y recién entonces:

AUDITOR → PASS

Eso ya no es simplemente "varios agentes programando".

Es un sistema de control de consistencia del software.

Y yo apuntaría exactamente hacia ahí.

Tu ventaja no debería ser:

"Tenemos agentes que escriben código."

Eso se va a commoditizar rapidísimo.

Tu ventaja debería ser:

"Tenemos un sistema agentic que mantiene sincronizados negocio, requisitos, UX, contenido, arquitectura, código, infraestructura y documentación, con ownership, permisos, dependencias, auditoría y trazabilidad."

Eso es bastante más difícil de replicar y, sobre todo, mucho más vendible a clientes que necesitan resultados y no simplemente código generado por IA

---

hay una skill mas... y es presupuestar...  una vez hecha la primera entrevista con el cliente o despues de unas rondas, hay que poder decirle, mira este proyecto se basa en un sw a medida customizado para vos con desarrollo de marca, marketing, seguimiento de conversion, etc etc...

y el precio, segun contexto, si es una pyme, una uniperonal, una empresa o que... si es mercado uruguayo, latino, anglo, europeo...

_---

Sí. Y no la llamaría simplemente pricing. En tu modelo es una capability bastante más sofisticada: tiene que convertir el alcance técnico + valor comercial + contexto del cliente en una propuesta económica defendible.

La agregaría como Estimator / Pricing Strategist.

Y ojo con algo: no debería calcular precio solamente sumando horas × tarifa. Si hacés eso, estás vendiendo capacidad de programación. Vos querés vender una solución integral.

Estimator / Pricing Strategist

Objetivo: determinar el posicionamiento económico y construir una estimación comercial del proyecto a partir del contexto del cliente, alcance, complejidad, riesgo y valor esperado.

Recibe como input:

Discovery
Requirements
PRD
alcance preliminar
arquitectura
UX/UI
Copy/Marketing
integraciones
necesidades de infraestructura
riesgos
urgencia
tipo de cliente
mercado/geografía
tamaño de empresa
madurez digital
capacidad de pago estimada
modelo de negocio
valor potencial de la solución
modalidad de contratación

Y produce algo como:

PROJECT ESTIMATION
────────────────────────────────


Client profile:
SMB
Uruguay
Professional services


Solution:
Custom web platform
Brand development
Marketing landing
Conversion tracking
Admin dashboard
CRM integration


Complexity:
Medium


Risk:
Medium


Estimated effort:
320–420 hours


Recommended commercial model:
Fixed project + monthly maintenance


Implementation:
USD 8,500


Monthly:
USD 450


Optional:
SEO              USD 300/mo
Marketing        USD 600/mo
Additional dev   USD 65/h

Pero hay una distinción que para mí es fundamental.

Tiene que calcular tres precios

No uno.

1. Cost

¿Cuánto te cuesta producirlo?

engineering
AI inference
cloud
third-party services
management
overhead

2. Market Price

¿Cuánto cobra aproximadamente el mercado por una solución comparable?

3. Value Price

¿Cuánto valor económico puede generar o proteger para el cliente?

Y después:

recommended_price =
f(cost, market, value, risk, client_profile, geography)

No necesariamente el máximo de los tres. Pero el agente debe conocer los tres.

Y sí: geografía importa

Yo no hardcodearía:

Uruguay = $X
USA = $Y
Europe = $Z

Eso sería demasiado burdo.

Crearía un pricing model con variables.

Por ejemplo:

country
region
currency
economic_segment
company_size
industry
client_maturity
purchasing_power
competitive_market
contract_type
expected_value
risk
urgency

Entonces el mismo proyecto podría producir:

Uruguay SMB
USD 6k–10k


Argentina SMB
USD 5k–9k


LATAM enterprise
USD 15k–30k


US SMB
USD 20k–35k


US enterprise
USD 50k+

No porque "los americanos pagan más" sino porque el mercado, los presupuestos, el costo de oportunidad y el valor capturable son diferentes.

Pero agregaría otro concepto: Pricing Policy

No dejaría que el agente invente precios.

Tendría algo como:

.agents/
└── pricing/
├── skill.md
├── policy.md
├── pricing-model.json
├── markets/
│   ├── uruguay.json
│   ├── latam.json
│   ├── usa.json
│   └── europe.json
└── history/

pricing-model.json podría tener reglas como:

base_cost
minimum_margin
risk_multiplier
urgency_multiplier
complexity_multiplier
market_multiplier
client_segment_multiplier

Así el agente razona dentro de una política comercial, en vez de alucinar un precio.

Y algo todavía más importante

El agente debería poder decir:

NO BID

Esto es fundamental.

Ejemplo:

Client:
unipersonal
Market:
Uruguay


Requirements:
custom ERP
mobile app
AI assistant
real-time integrations
24/7 availability
custom CRM


Budget:
USD 1,500

El Estimator debería decir:

RECOMMENDATION: DO NOT BID


Reason:
Expected project scope is incompatible with stated budget.


Alternative:
Offer discovery + MVP.


Estimated MVP:
USD 3,500–5,000

Eso evita que tu empresa se meta en proyectos que van a ser un desastre.

Y lo conectaría directamente con el Orchestrator

Tu workflow empieza a quedar muy bueno:

PreSales
↓
Business Analyst
↓
Product
↓
Architecture
↓
UX/UI
↓
Copywriter
↓
Estimator
↓
┌──────────────────────┐
│ COMMERCIAL PROPOSAL  │
└──────────┬───────────┘
↓
CLIENT
↓
APPROVED?
/      \
NO        YES
↓          ↓
revise     Delivery

Y Estimator no debería ser necesariamente el último paso.

Puede entrar varias veces.

Por ejemplo:

Discovery
↓
Estimator v1
↓
Cliente agrega:
"También quiero app mobile"
↓
Business Analyst
↓
Architect
↓
Estimator v2
↓
+ USD 7,000

Eso es importantísimo porque el presupuesto pasa a ser un artefacto versionado del proyecto, no un número que alguien tiró en una reunión.

Yo incluso lo llamaría Commercial Estimator

Porque su responsabilidad no es únicamente pricing.

Tiene que producir:

alcance comercial
exclusiones
supuestos
estimación
precio
modalidad
timeline
fases
opcionales
recurrentes
riesgos
condiciones

Y podría terminar generando algo como:

PROPOSAL
├── Executive Summary
├── Problem
├── Proposed Solution
├── Scope
├── Deliverables
├── Timeline
├── Investment
├── Optional Services
├── Monthly Services
├── Assumptions
├── Exclusions
└── Commercial Terms

Ahí ya tenés otra pieza del sistema.

Y te diría que no mezcles Commercial Estimator con PreSales. PreSales busca entender, posicionar y vender. Estimator determina cuánto vale comercialmente ejecutar lo que se entendió. Pueden conversar, pero deben tener responsabilidades distintas.

Además, tu Auditor debería poder auditar después la propuesta contra el proyecto: “se presupuestaron 8 módulos, pero el requirements terminó teniendo 13”. Eso te permite aprender de cada proyecto y alimentar el pricing futuro.

---

