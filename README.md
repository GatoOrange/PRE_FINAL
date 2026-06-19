# Socialización del Proyecto Final

Presentación interactiva en formato PowerPoint-style con navegación por diapositivas, desarrollada en HTML/CSS/JS puro.

## Estructura

```
genially_slide/
├── index.html          # Presentación completa (12 diapositivas)
├── README.md           # Este archivo
└── images/
    ├── logo-sena-blanco.png   # Logo SENA (blanco/verde)
    └── logo_0.png             # Logo SENA original (legacy)
```

## Slides

| # | Nombre | Contenido |
|---|--------|-----------|
| 1 | **Portada** | Título, subtítulos, logo SENA, redes sociales, partículas decorativas |
| 2 | **Objetivos** | Objetivo general + 5 botones expandibles con objetivos específicos (Síntesis, Caracterización, Balances, P&ID, Biosolvente) |
| 3 | **Fase 1: Preparación y Caracterización** | 4 bloques interactivos (Recolección, Caracterización, Estandarización, Catalizador) con modal paso a paso |
| 4 | **Fase 2: Transformación** | 3 bloques interactivos (Esterificación Ácida, Transesterificación Alcalina, Centrifugación) con modal paso a paso |
| 5 | **Fase 3: Purificación y Caracterización** | 6 bloques en 2 grupos (Purificación: Lavado/Centrifugación/Secado — Caracterización: Ésteres/Humedad/Desempeño) con modal paso a paso |
| 6 | **Escalamiento Industrial** | Diagrama P&ID interactivo: 3 fases conectadas (Caracterización MP → Transformación → Caracterización Producto) + Balance M&E + botón SCADA. Cada fase abre modal con imagen, descripción y variables asociadas |
| 7 | **Balance M&E** | Tablas de balance de materia (122.7 kg/batch) y energía (65.6 MJ/batch) con métricas de rendimiento y escalamiento |
| 8 | **HMI / SCADA** | Variables monitoreadas (temperatura, presión, caudal, nivel, pH, RPM) |
| 9 | **Balance** | Rendimiento del proceso (92% másico, 1:6 molar, 45°C) |
| 10 | **Aplicación** | Software de caracterización con cálculo de propiedades y generación de informe PDF |
| 11 | **Conclusiones** | Resultados del proyecto (6 puntos clave) |
| 12 | **Cierre** | Dato curioso (biosolvente vs biodiesel) + créditos |

## Paleta de colores

| Color | Uso | Código |
|-------|-----|--------|
| Negro | Fondos | `#121212` |
| Verde | Acentos, títulos, iconos | `#39b54a` |
| Blanco | Texto principal | `#e0e0e0` / `#ffffff` |
| Gris | Subtítulos, metadatos | `#999` / `#888` / `#bbb` |
| Card | Fondo de tarjetas | `#1a1a1a` |
| Borde | Separadores sutiles | `rgba(255,255,255,0.05)` |

## Navegación

- **Flechas izquierda/derecha**: diapositiva anterior/siguiente
- **Espacio**: siguiente diapositiva
- **Home**: primera diapositiva
- **End**: última diapositiva
- **ESC**: abrir/cerrar vista general
- **Rueda del mouse**: navegación vertical
- **Touch swipe**: navegación táctil
- **Botones inferiores**: anterior, siguiente, vista general
- **Dots**: acceso directo a cada diapositiva
- **Click en diapositiva**: desactivado (no avanza)

## Decoraciones

Todas las diapositivas incluyen:
- Patrón de fondo hexagonal (verde tenue)
- Partículas flotantes (círculos verdes, blancos, grises)
- Hexágonos decorativos simples y dobles
- Cadenas moleculares (carbonadas)
- Fragmentos de ecuaciones químicas (R-COO-R', NaOH, KOH, CH₃OH, etc.)

## Modales

Las cards con `"Ver más"` abren modales con información detallada:
- Objetivos (General / Específicos)
- Fases de laboratorio (Fase 1 / 2 / 3)
- Industrial (Fase 1 / 2 / 3 + Balance M&E)
- Aplicación (Entrada / Salida)
- Conclusiones
- P&ID detallado (equipos V-101, P-101, E-101, R-101, V-102, S-101, T-101, Productos, Diagrama)
- HMI detallado
- Balance detallado (Materia / Energía / Escalamiento)
- Industrial (Fase 1 / 2 / 3 + Balance M&E)
- App detalle (Entrada / Salida)
- App informe

## Responsive

- **≤900px**: grid de 3 columnas, decoraciones ocultas, logo 72px
- **≤600px**: grid de 2 columnas, logo 48px, tipografía reducida
