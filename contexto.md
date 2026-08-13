# Contexto

Este repo no es un producto. Es un vómito.

Hay notas, chats pegados, roles de agencia, un chatbot, un modelo WaaS, un facturador DGI, un Kill Bill, SOC2 y dos hex de Instagram. Nada de eso es aún Ficus. Es una ensalada de frutas: cada mate agregó un sabor y nadie eligió el plato.

La regla de trabajo: **una cosa por vez**. No se diseña el sistema operativo de agentes, no se arma el motor de cobros, no se discute Gold a USD 200/h. Eso queda en `volcado.md`, `roles.md` y `vendedor.md` como archivo muerto hasta que la web exista.

El constraint de hoy: **ficus.uy desplegada en Vercel**. Todo lo que no empuje a esa URL se pospone.

---

## Qué hay en el repo (y para qué no usarlo hoy)

| Archivo | Qué es | Qué hacer con él |
|---|---|---|
| `volcado.md` | Dump de estrategia + productos + planes + billing | Mina de decisiones. No es spec. |
| `roles.md` | Organigrama de 25 agentes | Fuera de alcance hoy. |
| `vendedor.md` | Chatbot Gemini | Fuera de alcance hoy. Backend Vercel es la arquitectura correcta; el bot no entra en v1. |
| `README.md` | Nombre, Instagram, dos colores | Input visual ya procesado. La fuente es `docs/02-identidad.md`. |
| `docs/01-branding.md` | Párrafo + 5 “no somos” | Fuente del paso 1. Congelado. |
| `docs/02-identidad.md` | Paleta, tipo, hoja | Fuente del paso 2. Congelado. |
| `AGENTS.md` | Instrucciones para el agente | Cómo trabajar este repo. |

---

## Orden de ataque (hasta deploy)

Cada ítem tiene un “done”. No se pasa al siguiente sin cerrarlo.

### 1. Branding — qué es y qué no es Ficus

**Done.** Fuente: [`docs/01-branding.md`](docs/01-branding.md). Congelado. No se reabre en el copy.

Borrador previo (no usar; la fuente es el archivo):

**Es**
- Estudio / aceleradora digital boutique.
- Soluciones digitales a medida (sitio, plataforma, herramienta), operadas como servicio.
- Dueños del código. El cliente es dueño de dominio y datos.
- Una persona con seniority corporativo, presentada como marca Ficus.

**No es**
- “Hago páginas web” baratas.
- Software factory genérica (React, k8s, microservicios en la home).
- Netuy: hosting + WordPress a volumen.
- El facturador DGI, Kill Bill, ni una plataforma de campañas políticas. Productos futuros, no la marca de hoy.
- Un equipo de 15 con Valeria en el chat.

### 2. Identidad visual

**Done.** Fuente: [`docs/02-identidad.md`](docs/02-identidad.md). Congelado. Specimen: [`docs/02-identidad-preview.html`](docs/02-identidad-preview.html). Hoja: [`assets/leaf.svg`](assets/leaf.svg).

Input previo (no usar; la fuente es el archivo):

- Instagram: `ficus__uy`
- Acentos: `#c5e476` y `#87b343` (botones, hoja, hover). **No** como color de cuerpo sobre blanco: fallan contraste.
- Texto: casi negro sobre claro, o claro sobre oscuro. WCAG AA mínimo (4.5:1).
- Tono: plural de marca (“Ficus”, “nosotros”) en la web. Sin personajes falsos.

### 3. Oferta de la home (una)

Una frase. No cuatro planes con precios.

Ejemplo de dirección (se reescribe en el paso 4, no se publica así):
> Diseñamos y operamos la plataforma digital de tu negocio. Vos te ocupás de vender; nosotros de que el sistema funcione.

En la home **no** van USD 20, créditos, Starter/Pro/Star/Gold. Eso es conversación comercial, no landing.

CTA único: agendar reunión. Contacto como respaldo.

**Done:** oferta en 2 frases + CTA nombrado (Calendly / Calendar). Cero tabla de precios.

### 4. Copy en español

Secciones, en este orden:

1. Hero: qué es Ficus + CTA
2. Cómo trabajamos (problema → solución → operamos; WaaS en un párrafo)
3. Para quién (profesional / pyme / organización) — corto
4. Casos Ficus (periodista con link; el otro sin link si no hay URL pública)
5. Experiencia del fundador (Antel, BASF, Ticketmaster, etc.) **separada y honesta**: no son clientes de Ficus
6. CTA final
7. Footer: Instagram, contacto, “Ficus”

Sin i18n hoy. Sin SOC2. Sin stack en la portada.

**Done:** textos finales, no “borrador para pulir después”.

### 5. Diseño / HTML

Pilares de v1: mobile first, responsive, semántica, contraste, teclado.
Design-as-code: HTML (o Nuxt mínimo) que se pueda ver en el teléfono, no ASCII ni Figma eterno.

**Done:** una página que se entiende en 15 segundos en mobile.

### 6. Deploy Vercel

Dominio `ficus.uy` (o el preview de Vercel si el DNS no llega hoy). HTTPS. CTA clickeable. Footer con Instagram.

**Done:** URL pública. Eso cierra el día.

---

## Explicitamente después (no hoy)

- Chatbot Gemini (API en backend Vercel, nunca en el front)
- i18n
- Planes y precios en la web
- Skills / Ficus OS / orchestrator
- Motor de pagos, entitlements, facturador DGI
- Certificaciones

Esos archivos siguen en el repo. No se borran. **No se implementan hasta que exista la URL.**

---

## Cómo trabajar

1. Abrir este archivo.
2. Atacar el primer ítem sin done.
3. No mezclar el 3 con el 6.
4. Si aparece una idea nueva, va al final de “después”, no al medio del paso actual.
