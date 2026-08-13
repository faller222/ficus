# Identidad visual — Ficus

**Estado:** congelado. 13 de agosto de 2026.
El copy (paso 4) y el HTML de la home (paso 5) consumen este archivo. No lo reabren.

Specimen: [`02-identidad-preview.html`](02-identidad-preview.html).
Hoja: [`../assets/leaf.svg`](../assets/leaf.svg).
Lockup: [`../assets/logo.svg`](../assets/logo.svg) (hoja + FICUS). Sin el lema del PDF.

---

## Tokens

Light es el default. Dark es el mismo sistema mapeado (`prefers-color-scheme`). No es una segunda marca.

Los hex del logo (`#b6d77a`, `#7cb44c`) son chispa. No son texto. No son fondo.
Instagram (`#c5e476`, `#87b343`) era aproximación. La fuente es el PDF de Corel.

### Light

| Token | Hex | Uso |
|---|---|---|
| `--bg` | `#F4F5EE` | Papel. Cast verde, no menta. |
| `--surface` | `#FFFFFD` | Superficie / área del logo. |
| `--text` | `#1A1C16` | Cuerpo y títulos. |
| `--text-muted` | `#5C6154` | Secundario. |
| `--ink` | `#2F4218` | Links y focus. |
| `--leaf` | `#7cb44c` | Hoja oscura, fill del CTA. |
| `--lime` | `#b6d77a` | Hoja clara, hover del CTA, underline. |

CTA: fondo `--leaf`, texto `--text`, hover fondo `--lime`. El texto del botón no cambia.

### Dark

| Token | Hex | Uso |
|---|---|---|
| `--bg` | `#12140F` | Carbón. Cast verde, no bosque. |
| `--surface` | `#1A1D16` | Superficie. |
| `--text` | `#EDEFE6` | Cuerpo y títulos. Crema, no lima. |
| `--text-muted` | `#9AA090` | Secundario. |
| `--ink` | `#b6d77a` | Anillo de focus y underline. El texto del link sigue `--text`. |
| `--leaf` | `#7cb44c` | Igual que light. |
| `--lime` | `#b6d77a` | Igual que light. |

CTA: igual que light. El botón no cambia de piel.

---

## Tipografía

Una familia. Sin shopping.

- **Source Sans 3** (Google, variable). Cuerpo, UI, “Ficus” en semibold cuando no va el lockup.
- Lockup oficial: `assets/logo.svg`. FICUS está trazado, no es una fuente web. No se simula con otra type.
- Mono: no en v1.

---

## Reglas de uso

- Cuerpo: nunca `#b6d77a` ni `#7cb44c`.
- Link en light: `--ink` + underline `--lime`. No texto lima.
- Link en dark: `--text` + underline `--lime`. No párrafo en lima.
- Focus en light: anillo `--ink`. No `#7cb44c` solo (falla 3:1 sobre el papel).
- Focus en dark: anillo `--lime`.
- La hoja no se recolorea. En dark queda igual; el fondo oscuro la sostiene.
- Las venas son el hueco entre tres fills. Se ve el fondo. No son stroke blanco.
- El lema del PDF (“Make it happend”) no entra. Typo, inglés, no es la marca.

---

## Contraste (WCAG AA)

Texto normal: 4.5:1. UI no-texto (focus): 3:1.

| Par | Ratio | Pasa |
|---|---|---|
| `--text` `#1A1C16` sobre `--bg` `#F4F5EE` | 15.7:1 | AA |
| `--text-muted` `#5C6154` sobre `--bg` `#F4F5EE` | 5.8:1 | AA |
| `--ink` `#2F4218` sobre `--bg` `#F4F5EE` | 10.0:1 | AA |
| `--text` `#1A1C16` sobre `--leaf` `#7cb44c` | 7.0:1 | AA |
| `--text` `#1A1C16` sobre `--lime` `#b6d77a` | 10.6:1 | AA |
| `--text` `#EDEFE6` sobre `--bg` `#12140F` | 16.0:1 | AA |
| `--text-muted` `#9AA090` sobre `--bg` `#12140F` | 6.9:1 | AA |
| `--ink` `#2F4218` sobre `--bg` `#F4F5EE` (focus light) | 10.0:1 | AA UI |
| `--lime` `#b6d77a` sobre `--bg` `#12140F` (focus dark) | 11.5:1 | AA UI |

Fallan (por eso no se usan así):

| Par | Ratio | Por qué no |
|---|---|---|
| `#b6d77a` texto sobre blanco | 1.6:1 | Cuerpo / link lima en light |
| `#7cb44c` texto sobre blanco | 2.5:1 | Cuerpo / link hoja en light |
| Blanco sobre `#7cb44c` | 2.5:1 | CTA con texto blanco |
| `#7cb44c` outline sobre `#F4F5EE` | 2.3:1 | Focus ring solo en light |

---

## Bitácora

- Papel y carbón con *cast*, no página menta ni dark bosque.
- Los dos hex del logo no son sistema. Son chispa.
- Lima como color de link: no. Falla contraste.
- CTA blanco sobre `#7cb44c`: no. El botón lleva texto oscuro.
- Dark saturado tipo `#0B3B24`: no. Lee ONG / growshop.
- Inter, Geist, IBM Plex: no. Source Sans 3 cierra el día.
- Mono: espera. Una familia.
- PNG e Instagram: input. La hoja y el lockup salen del PDF Corel V02.
- “Make it happend”: muerto. No se imprime.
