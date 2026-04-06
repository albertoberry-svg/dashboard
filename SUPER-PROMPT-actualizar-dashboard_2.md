# 🔄 SUPER PROMPT — Actualización Dashboard Inmobiliario España

> Copia y pega este prompt completo cada vez que quieras actualizar el dashboard.
> Añade al final la fecha en que lo pides para que Claude sepa qué datos buscar.

---

## ✂️ PROMPT A COPIAR

---

Necesito que actualices todos los datos del **Dashboard Mercado Inmobiliario España** con la información más reciente disponible. Sigue estos pasos en orden:

---

### PASO 1 — BÚSQUEDA DE DATOS (usa web search)

Busca los datos más recientes disponibles de las siguientes variables. Para cada una, anota el valor encontrado, la fuente y la fecha de publicación:

**PRECIOS DE VENTA**
- Precio medio venta España (€/m²) y variación interanual → fuente: Idealista o Fotocasa
- Precio Madrid venta (€/m²) y variación interanual
- Precio Barcelona venta (€/m²) y variación interanual
- Precio Málaga venta (€/m²) y variación interanual
- Precio Valencia venta (€/m²) y variación interanual
- Precio Sevilla venta (€/m²) y variación interanual
- Precio Bilbao venta (€/m²) y variación interanual
- Precio Palma venta (€/m²) y variación interanual
- Precio vivienda nueva España (€/m²) y variación interanual
- **Precio Brent (USD/barril)** → fuente: Bloomberg / EIA / Expansión

**PRECIOS DE ALQUILER**
- Precio medio alquiler España (€/m²/mes) y variación interanual → Idealista o Fotocasa
- Precio alquiler Madrid (€/m²/mes) y variación
- Precio alquiler Barcelona (€/m²/mes) y variación
- Ciudad con mayor subida de alquiler y su % variación
- Ciudad con bajada de alquiler (si existe) y su % variación
- IRAV (Índice de Referencia de Alquiler de Vivienda) valor vigente → fuente: Ministerio de Vivienda / BOE

**ÍNDICES OFICIALES**
- IPV (Índice de Precios de Vivienda) último trimestre publicado, variación anual y trimestral → fuente: INE
- IPV 2ª mano variación anual
- IPV vivienda nueva variación anual
- Número de compraventas último dato publicado → fuente: INE / Notarios

**DATOS MACRO Y FINANCIEROS**
- Euríbor 12 meses (media mensual más reciente) → fuente: Banco de España / Bankinter
- Tipo de interés BCE (último valor) → fuente: BCE
- Bono español 10 años (yield actual) → fuente: prensa financiera
- IPC general España (último dato interanual) → fuente: INE
- IPC subyacente España (último dato) → fuente: INE
- Hipoteca fija media mejor oferta del mercado → fuente: HelpMyCash o iAhorro
- **Precio Brent (USD/barril)** más reciente y eventos geopolíticos relevantes que lo hayan movido

**INVERSIÓN Y RENTABILIDAD**
- Rentabilidad bruta media alquiler España (%) → fuente: Idealista / Fotocasa / Bankinter
- Rentabilidad neta estimada (si disponible)
- % compras por extranjeros no residentes (último dato anual) → fuente: Colegio Registradores

**CONSTRUCCIÓN**
- Coste ejecución material vivienda plurifamiliar (€/m²) → fuente: UVE Valoraciones / MITMA / ACR
- Variación interanual coste construcción
- Visados de obra nueva últimos 12 meses → fuente: Ministerio de Transportes / Fomento

**HIPOTECAS** *(pestaña 🏦 Hipotecas)*
- Euríbor 12M media mensual más reciente y variación vs mes anterior
- Tipo fijo medio mercado (TIN) → fuente: HelpMyCash / iAhorro / Bankinter
- Tipo variable medio (diferencial sobre Euríbor)
- LTV máximo estándar para primera y segunda vivienda
- Plazo medio de concesión hipotecaria
- Esfuerzo hipotecario nacional (% salario bruto) → fuente: Banco de España / AHE
- Comparativa de tipos fijos y variables por entidad (CaixaBank, BBVA, Santander, Sabadell, Bankinter, ING, Openbank, Myinvestor)
- Cuota mensual estimada por rango de precio (200K, 300K, 400K, 500K, 600K)

**OKUPACIÓN & INQUIOKUPACIÓN** *(pestaña 🦹 Jetas)*
- Nº de denuncias por ocupación ilegal último año disponible → fuente: Ministerio del Interior / Portal Estadístico de Criminalidad
- Variación respecto al año anterior (%)
- Estimación total viviendas ocupadas en España (si hay estudio actualizado) → fuente: Institut Cerdà u otros
- Tiempo medio de desalojo en meses → fuente: CGPJ
- Comunidad autónoma con más casos y su % del total
- Nº de viviendas en proceso en portales inmobiliarios (si hay dato actualizado)
- Evolución de demandas judiciales por CCAA (último trimestre CGPJ disponible)
- Alguna novedad legislativa o judicial relevante sobre inquiokupación o desahucios

---

### PASO 2 — INFORME PREVIO

Antes de tocar el código, preséntame una tabla con todos los datos encontrados en este formato:

| Variable | Valor anterior (dashboard) | Valor nuevo encontrado | Fuente | Fecha dato |
|----------|---------------------------|----------------------|--------|------------|
| ... | ... | ... | ... | ... |

Señala con ⚠️ los datos que NO hayas podido encontrar o que no hayan cambiado significativamente.

---

### PASO 3 — ACTUALIZACIÓN DEL DASHBOARD (HTML)

Una vez confirmado el informe (yo te diré "procede" o haré correcciones), actualiza el archivo HTML del dashboard tocando **todos** los siguientes elementos:

1. **Ticker superior** → todos los valores del ticker (Madrid, Barcelona, España media, Alquiler, IPV, Hipoteca, Rentabilidad, Compraventas, Vivienda nueva)

2. **KPIs del panel Resumen** → los KPI cards con sus valores y variaciones

3. **KPIs del panel Ciudades** → precios por ciudad y variaciones

4. **KPIs del panel Alquiler** → precio alquiler, meses de récord, subida acumulada 2 años, IRAV

5. **KPIs del panel Inversión** → rentabilidad total, bruta, subida real, % extranjeros

6. **KPIs del panel Macro/IPC** → IPC, IPC subyacente, Euríbor, BCE, Bono 10Y

7. **KPIs sección Costes de Construcción** → coste €/m², acumulado, índices de mano de obra y materiales

8. **KPIs y tabla del panel Hipotecas** → Euríbor, tipo fijo/variable, LTV, plazo, esfuerzo financiero, comparativa entidades

9. **KPIs del panel Jetas** → denuncias, viviendas ocupadas, tiempo de desalojo, % Cataluña, viviendas en portales

10. **Datos de los gráficos** → actualiza los arrays de datos en los charts de Chart.js que correspondan, incluyendo:
    - Serie histórica de denuncias (pestaña Jetas)
    - Distribución por CCAA de ocupación (pestaña Jetas)
    - Charts de Hipotecas (Euríbor histórico, cuotas, esfuerzo por ciudad)
    - **chartBrent** (pestaña Macro): añadir nuevo punto mensual a `brentData[]` y `brentLabels[]`, y revisar si hay nuevos eventos geopolíticos para añadir a `brentEvents[]`
    - Cualquier gráfico temporal con nuevos trimestres publicados

11. **Tooltips** → actualiza el texto de los tooltips (objeto `TIPS` en el JS) si los valores han cambiado

12. **Tabla CCAA de demandas judiciales** → actualiza el array `ccaaData` en `initJetasCharts()` con datos del último trimestre del CGPJ

13. **Tarjetas informativas de contexto** → actualiza estadísticas o datos normativos que hayan cambiado (nuevas leyes, nuevos plazos, etc.)

14. **Texto teletipo (pantalla fósforo del Resumen)** → si hay una noticia relevante nueva, actualiza el contenido del `DESPACHO` en el JS. Incrementa el número de despacho (Nº 003/2026, etc.) y actualiza las 4 líneas: TITULAR, CONTEXTO, TESIS, CONCLUSIÓN. No cites personas ni portales por su nombre en la CONCLUSIÓN.

15. **Texto `Actualizado: [mes] [año]`** en el pie de página → pon el mes y año actuales

---

### PASO 4 — REGENERACIÓN DEL INFORME PDF

**⚠️ Este paso es obligatorio cada vez que se actualicen datos del dashboard.**

Una vez actualizado el HTML, regenera también el informe PDF con los mismos datos nuevos. El script está en `/home/claude/build_informe_mercado.py`.

**Elementos del PDF que deben actualizarse en paralelo al dashboard:**

| Sección PDF | Variables a actualizar |
|-------------|----------------------|
| Portada (KPIs) | Precio medio España, variación interanual, compraventas, Euríbor |
| S01 · Resumen Ejecutivo | Todos los KPIs del resumen, párrafo introductorio con datos actuales |
| S02 · Ciudades y CCAA | Tabla ranking 12 ciudades (venta, alquiler, rentabilidad, variaciones), tabla CCAA |
| S03 · Alquiler | KPIs alquiler, tabla carga financiera por ciudad, datos regulatorios IRAV |
| S04 · Inversión | KPIs inversión, tabla yield por ciudad, tabla comparativa de activos |
| S05 · Macro / IPC | KPIs macro, tabla IPC por componentes, tabla histórico BCE/Euríbor |
| S06 · Hipotecas | KPIs hipotecas, tabla comparativa entidades, tabla esfuerzo por ciudad |
| S07 · Ocupación | KPIs jetas, tabla CCAA ocupación, tabla comparativa ocupación/inquiokupación |
| S08 · Previsiones | Tabla previsiones organismos — actualiza si salen nuevas previsiones |
| Fecha del informe | Actualiza "Marzo 2026" → mes y año actuales en portada, header y footer |

**Procedimiento:**
1. Abre `/home/claude/build_informe_mercado.py`
2. Actualiza los datos numéricos de todas las tablas y KPIs con los valores nuevos del PASO 1
3. Actualiza la fecha del informe (portada, header, footer, sección disclaimer)
4. Ejecuta el script: `python3 /home/claude/build_informe_mercado.py`
5. Copia el PDF generado a `/mnt/user-data/outputs/informe_mercado_inmobiliario_2026.pdf`
6. Presenta el archivo al usuario con `present_files`

---

### PASO 5 — NUEVAS PESTAÑAS (si procede)

Si en el futuro se crea una nueva pestaña, el proceso de actualización debe incluir también:

- Buscar los datos relevantes para esa pestaña en el PASO 1 (añadir bloque de búsqueda)
- Actualizar sus KPIs en el PASO 3
- Actualizar sus gráficos y tablas en el PASO 3
- Actualizar sus tooltips (claves `data-tip`) en el objeto `TIPS` del JS
- Añadir su sección correspondiente en el PDF (`build_informe_mercado.py`): nueva sección con `sec_header`, KPIs, tablas y párrafos narrativos
- Actualizar este SUPER-PROMPT para que la nueva pestaña quede documentada aquí de forma permanente

> 📌 **Instrucción de auto-mantenimiento:** Cada vez que se añada una pestaña nueva al dashboard, actualiza también este SUPER-PROMPT para reflejar los nuevos datos que hay que buscar, los nuevos elementos que hay que actualizar, y la nueva sección del PDF. Así este prompt siempre estará al día sin intervención manual.

---

### PASO 6 — VERIFICACIÓN FINAL

Al terminar, indícame:
- ✅ Cuántos valores del **dashboard HTML** has podido actualizar
- ✅ Cuántos valores del **informe PDF** has podido actualizar
- ⚠️ Cuáles no encontraste y dejaste sin cambiar
- 📅 El rango de fechas de los datos usados
- 🔗 Las fuentes principales consultadas

---

### CONTEXTO DEL PROYECTO

**Archivos principales:**
| Archivo | Ruta | Descripción |
|---------|------|-------------|
| Dashboard HTML | `/home/claude/dashboard.html` | Archivo principal — single file HTML/CSS/JS |
| Output HTML | `/mnt/user-data/outputs/index.html` | Copia para descarga / deploy a GitHub Pages |
| Script PDF | `/home/claude/build_informe_mercado.py` | Script Python (reportlab) que genera el informe PDF |
| Output PDF | `/mnt/user-data/outputs/informe_mercado_inmobiliario_2026.pdf` | PDF generado |
| Super-prompt | `/mnt/user-data/outputs/SUPER-PROMPT-actualizar-dashboard_2.md` | Este archivo actualizado |

**Estructura del dashboard — 8 pestañas:**
```
array switchTab: ['overview','ciudades','alquiler','inversion','macro','hipotecas','jetas','noticias']
```

| # | ID | Emoji | Nombre | Panel HTML ID |
|---|----|----|---------|---------------|
| 1 | overview | — | Resumen | `#panel-overview` |
| 2 | ciudades | — | Ciudades | `#panel-ciudades` |
| 3 | alquiler | — | Alquiler | `#panel-alquiler` |
| 4 | inversion | 💰 | Inversión | `#panel-inversion` |
| 5 | macro | 📉 | Macro / IPC | `#panel-macro` |
| 6 | hipotecas | 🏦 | Hipotecas | `#panel-hipotecas` |
| 7 | jetas | 🦹 | Jetas | `#panel-jetas` |
| 8 | noticias | 📡 | Noticias | `#panel-noticias` |

**Detalles técnicos importantes:**
- HTML single-file con Chart.js (CDN), tipografías Google Fonts (Bebas Neue, DM Mono)
- Sistema de tooltips: objeto `TIPS` en JS, claves `data-tip` en elementos HTML
- Tema claro/oscuro: toggle 🌙/☀️ en header, función `toggleTheme()` — **NUNCA destruir charts**, solo `chart.update('none')`
- Pestaña Jetas inicializada con `initJetasCharts()`
- Teletipo fósforo verde: objeto `DESPACHO` en el JS, pantalla `id="phosphor-screen"`, solo visible en escritorio (>768px)
- Número de despacho actual: `DESPACHO Nº 002/2026` → incrementar en cada actualización de noticia
- **Última actualización de datos: 6 abr 2026** — IPC +3.3% mar 26, Euríbor 2.565% mar 26, Alquiler 15.0 €/m² +7.1% Q1, BCE 2.00%, IRAV +2.16%, 49 meses récord, Venta +17.7% (2.673 €/m² feb 26, mar 26 estimado 2.710)
- Widgets BTC y EUR/USD: refresco cada 30s, fuentes en cascada, badge LIVE con `display: 'flex'`
- Noticias RSS: `fetch()` con `{ cache: 'no-store' }` + timestamp `&_t=${Date.now()}`. Cadena de **5 proxies en cascada** por este orden: `rss2json.com` (JSON estructurado) → `allorigins.win/get` (JSON con XML) → `corsproxy.io` (raw XML) → `codetabs.com` (raw XML) → `allorigins.win/raw` (raw XML). Si todos fallan pero hubo un fetch previo exitoso, muestra **caché** en lugar del fallback estático. **Auto-refresco cada 20 minutos** mientras la pestaña está visible.
- **Botón descarga PDF en el header:** clase `.pdf-download-btn`, es un `<a>` con `href="informe_mercado_inmobiliario_2026.pdf" download`. **NO eliminar ni mover.**
- **Botón Herramientas en el header:** clase `.pdf-download-btn`, es un `<a>` con `href="https://sebastiangil.app/herramientas"`. **NO eliminar ni mover.**

**Layout primera fila del Resumen:**
```
grid-template-columns: 2fr 0.65fr 1fr 1fr
├── [1] chartVenta (gráfico evolución precio venta)
├── [2] chartDonut (tipo de vivienda — card separado)
├── [3] Indicadores Clave (indicator-grid)
└── [4] BITCOIN WIDGET (id: btc-*)   — Binance → CoinGecko → Kraken
```
EUR/USD widget: id: fx-* — visible en escritorio a la derecha del BTC.

**Layout pestaña Macro/IPC — 6 cuadros en 3 filas de 2 columnas:**
```
Fila 1 (grid-2): chartIPC (Evolución IPC)  |  chartIpcVsVivienda (IPC vs Vivienda)
Fila 2 (grid-2): chartEuribor (Euríbor)    |  chartIpcComponentes (IPC Componentes)
Fila 3 (grid-2): chartPoderAdquisitivo     |  chartBrent (Brent petróleo) ← NUEVO
```

**Canvas IDs por pestaña:**
- **Resumen:** `chartVenta`, `chartDonut`, `chartCiudades`
- **Macro/IPC:** `chartIPC`, `chartIpcVsVivienda`, `chartEuribor`, `chartIpcComponentes`, `chartPoderAdquisitivo`, `chartBrent`
- **Hipotecas:** `hipChartEuribor`, `hipChartTiposEntidad`, `hipChartCuotaMensual`, `hipChartEsfuerzo`
- **Jetas:** `chartOkupHistorico`, `chartOkupCCAA`, `chartOkupTipo`, `chartOkupPercepcion`

**Variable compartida `labels8`:**
Usada por `chartIPC`, `chartIpcVsVivienda` y `chartPoderAdquisitivo`. Actualmente 9 puntos: `['2018','2019','2020','2021','2022','2023','2024','2025','Mar 26']`. **Cuando se añada un punto nuevo a labels8, hay que añadirlo también en TODOS los datasets de los 3 gráficos que la usan** (12 datasets en total — 3 por chartIPC + 4 por chartIpcVsVivienda + 4 por chartPoderAdquisitivo + 1 implícito).

**chartBrent — estructura técnica:**
```javascript
// Dentro del IIFE macro (function() { ... })();
// Variables disponibles en ese scope: gold, gold2, red, green, blue2, text2, gridC, tipOpts
// ⚠️ NO usar 'border' — la variable de rejillas es 'gridC'

const brentLabels = [ /* 'Abr 23', 'May 23', ..., 'Abr 26' */ ];  // 37 puntos actuales
const brentData   = [ /* 84, 75, 75, ..., 109 */ ];                // 37 puntos actuales
const brentEvents = [
  { idx: 6,  line1: 'Hamas',        line2: '7 Oct 23',  color: 'rgba(220,60,60,0.9)'  },
  { idx: 12, line1: 'Iran->Israel', line2: '13 Abr 24', color: 'rgba(220,140,0,0.9)'  },
  { idx: 21, line1: 'Alto fuego',   line2: 'Gaza',      color: 'rgba(60,180,100,0.9)' },
  { idx: 35, line1: 'Guerra Iran',  line2: '28 Feb 26', color: 'rgba(200,30,30,0.95)' }
];
// Plugin de anotaciones inline: drawRoundRect() + brentAnnotationPlugin
// ⚠️ NO usar ctx.roundRect() — no disponible en todos los navegadores
// ⚠️ NO usar emojis en strings JS dentro de este bloque — solo ASCII
```
Para añadir un mes nuevo: push en `brentLabels` y `brentData`. Para añadir evento: push en `brentEvents` con el índice correcto.

**Auditoría obligatoria de gráficos:**
Después de cualquier cambio en arrays de datos, ejecutar siempre la auditoría automática:
```python
# Verificar que labels y datos tienen el mismo número de puntos en todos los gráficos
# Si labels usa variable (labels8, brentLabels), verificar longitud por separado
# Residuo cero en valores de datos anteriores antes de entregar
```
**Regla de oro:** si un gráfico usa `labels: labels8`, todos sus datasets deben tener exactamente `len(labels8)` puntos. Actualmente 9 puntos (hasta `Mar 26`).

**Scope JS — variables por IIFE:**
| IIFE / scope | Variables definidas |
|---|---|
| IIFE macro `(function(){ ... })();` L4205 | `gold, gold2, red, green, blue2, text2, gridC, tipOpts, labels8, labels8e` |
| IIFE BTC `(function(){ ... })();` L4551 | `$, fmt, fmtB, sparkPrices, btcPrev, liveTimer, activeSource` |
| `initHipotecasCharts()` | `hipColor, hipColor2, hipAlpha` |
| `initJetasCharts()` | `red, redFade, gold, blue, green` (redefinidas localmente) |

**SEO — NO TOCAR NUNCA:**
```html
<meta name="google-site-verification" content="fm-yZR6gPCYEu1uQwdhxBPHlPMAi6d78yzgVw_krv14" />
<link rel="canonical" href="https://dashboard.sebastiangil.app">
<link rel="sitemap" type="application/xml" href="https://dashboard.sebastiangil.app/sitemap.xml">
```

**Deploy:**
- URL pública: `https://dashboard.sebastiangil.app`
- Repo GitHub: `https://github.com/albertoberry-svg/dashboard` (rama `main`, archivo `index.html` en raíz)
- Tras cada actualización: subir `index.html` al repo para que GitHub Pages lo publique automáticamente

**Fuentes principales del dashboard:**
Idealista · Fotocasa · INE · Banco de España · BCE · Bankinter · Sociedad de Tasación · UVE Valoraciones · ACR · MITMA · Colegio de Registradores · Ministerio del Interior · CGPJ · Institut Cerdà · CaixaBank Research · HelpMyCash · iAhorro · Bloomberg / EIA (Brent)

**Estructura del script PDF (`build_informe_mercado.py`):**
```
Portada custom (draw_cover)
S01 · Resumen Ejecutivo
S02 · Precios por Ciudad y CCAA
S03 · Mercado del Alquiler
S04 · Inversión y Rentabilidades
S05 · Entorno Macroeconómico e IPC
S06 · Mercado Hipotecario
S07 · Ocupación e Inquiokupación
S08 · Previsiones 2026
S09 · Aviso Legal y Descargo de Responsabilidad
```

---

**Fecha en que hago esta solicitud: [ESCRIBE AQUÍ LA FECHA, ej: Junio 2026]**

---

*Fin del prompt*
