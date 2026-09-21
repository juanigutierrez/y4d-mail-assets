# Estructura de carpetas

```text
y4d-mail-assets/
├── index.html
├── .nojekyll
├── README.md
├── GUIA-PASO-A-PASO.md
├── ESTRUCTURA-DE-CARPETAS.md
├── brand/
│   ├── y4d/
│   └── kairos/
├── regions/
│   ├── metro/
│   ├── cuyo/
│   ├── patagonia/
│   ├── pampeana/
│   ├── noreste/
│   └── noroeste/
├── partners/
├── editions/
│   └── 2026/
├── flyers/
└── general/
```

## Convención de nombres

Usar nombres claros, estables y sin versiones ambiguas.

Recomendado:

- `y4d-logo-horizontal-azul.png`
- `kairos-logo-negro.png`
- `chubut-2026-convocatoria.png`
- `mendoza-2026-seleccionados.png`
- `embajada-eeuu-logo.png`

Evitar:

- `final.png`
- `final2.png`
- `nuevo nuevo.png`
- `IMG_4728.png`

Los espacios son válidos, pero para simplificar URLs conviene utilizar minúsculas, guiones y caracteres sin tildes.

## Qué formato usar

Para correos HTML, priorizar:

1. PNG para logos, recursos con transparencia y gráficos.
2. JPG/JPEG para fotografías.
3. WebP solo si existe una razón concreta y se comprobó compatibilidad con el flujo de envío.

No usar archivos locales ni rutas `file:///` dentro de correos HTML.
