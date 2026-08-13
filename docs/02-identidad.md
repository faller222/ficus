# Identidad visual — Ficus

**Estado:** congelado. 13 de agosto de 2026.
El copy (paso 4) y el HTML de la home (paso 5) consumen este archivo. No lo reabren.

Specimen: [`02-identidad-preview.html`](02-identidad-preview.html).
Hoja: [`../assets/leaf.svg`](../assets/leaf.svg).

---

## Tokens

Light es el default. Dark es el mismo sistema mapeado (`prefers-color-scheme`). No es una segunda marca.

Los hex del logo (`#c5e476`, `#87b343`) son chispa. No son texto. No son fondo.

### Light

| Token | Hex | Uso |
|---|---|---|
| `--bg` | `#F4F5EE` | Papel. Cast verde, no menta. |
| `--surface` | `#FFFFFD` | Superficie / área del logo. |
| `--text` | `#1A1C16` | Cuerpo y títulos. |
| `--text-muted` | `#5C6154` | Secundario. |
| `--ink` | `#2F4218` | Links y focus. |
| `--leaf` | `#87b343` | Hoja oscura, fill del CTA. |
| `--lime` | `#c5e476` | Hoja clara, hover del CTA, underline. |

CTA: fondo `--leaf`, texto `--text`, hover fondo `--lime`. El texto del botón no cambia.

### Dark

| Token | Hex | Uso |
|---|---|---|
| `--bg` | `#12140F` | Carbón. Cast verde, no bosque. |
| `--surface` | `#1A1D16` | Superficie. |
| `--text` | `#EDEFE6` | Cuerpo y títulos. Crema, no lima. |
| `--text-muted` | `#9AA090` | Secundario. |
| `--ink` | `#C5E476` | Anillo de focus y underline. El texto del link sigue `--text`. |
| `--leaf` | `#87b343` | Igual que light. |
| `--lime` | `#c5e476` | Igual que light. |

CTA: igual que light. El botón no cambia de piel.

---

## Tipografía

Una familia. Sin shopping.

- **Source Sans 3** (Google, variable). Cuerpo, UI, wordmark “Ficus” en semibold.
- No hay wordmark dibujado. No se inventa una segunda voz.
- Mono: no en v1.

---

## Reglas de uso

- Cuerpo: nunca `#c5e476` ni `#87b343`.
- Link en light: `--ink` + underline `--lime`. No texto lima.
- Link en dark: `--text` + underline `--lime`. No párrafo en lima.
- Focus en light: anillo `--ink`. No `#87b343` solo (falla 3:1 sobre el papel).
- Focus en dark: anillo `--lime`.
- La hoja no se recolorea. En dark queda igual; el fondo oscuro la sostiene.
- Las venas de la hoja son recorte (se ve el fondo), no un stroke blanco. En el SVG: clip de la silueta + máscara. El PNG deja de ser la fuente.

---

## Contraste (WCAG AA)

Texto normal: 4.5:1. UI no-texto (focus): 3:1.

| Par | Ratio | Pasa |
|---|---|---|
| `--text` `#1A1C16` sobre `--bg` `#F4F5EE` | 15.7:1 | AA |
| `--text-muted` `#5C6154` sobre `--bg` `#F4F5EE` | 5.8:1 | AA |
| `--ink` `#2F4218` sobre `--bg` `#F4F5EE` | 10.0:1 | AA |
| `--text` `#1A1C16` sobre `--leaf` `#87b343` | 7.0:1 | AA |
| `--text` `#1A1C16` sobre `--lime` `#c5e476` | 12.1:1 | AA |
| `--text` `#EDEFE6` sobre `--bg` `#12140F` | 16.0:1 | AA |
| `--text-muted` `#9AA090` sobre `--bg` `#12140F` | 6.9:1 | AA |
| `--ink` `#2F4218` sobre `--bg` `#F4F5EE` (focus light) | 10.0:1 | AA UI |
| `--lime` `#c5e476` sobre `--bg` `#12140F` (focus dark) | 13.0:1 | AA UI |

Fallan (por eso no se usan así):

| Par | Ratio | Por qué no |
|---|---|---|
| `#c5e476` texto sobre blanco | ~1.4:1 | Cuerpo / link lima en light |
| `#87b343` texto sobre blanco | ~2.5:1 | Cuerpo / link hoja en light |
| Blanco sobre `#87b343` | ~2.5:1 | CTA con texto blanco |
| `#87b343` outline sobre `#F4F5EE` | ~2.3:1 | Focus ring solo en light |

---

## Bitácora

- Papel y carbón con *cast*, no página menta ni dark bosque.
- Los dos hex del logo no son sistema. Son chispa.
- Lima como color de link: no. Falla contraste.
- CTA blanco sobre `#87b343`: no. El botón lleva texto oscuro.
- Dark saturado tipo `#0B3B24`: no. Lee ONG / growshop.
- Inter, Geist, IBM Plex: no. Source Sans 3 cierra el día.
- Mono: espera. Una familia.
- PNG de la hoja: input. La fuente es `assets/leaf.svg`.
