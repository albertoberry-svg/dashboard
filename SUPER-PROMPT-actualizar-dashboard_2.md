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
- Euríbor 12 meses (valor actual) → fuente: Banco de España o prensa financiera
- Tipo de interés BCE (último valor) → fuente: BCE
- Bono español 10 años (yield actual) → fuente: prensa financiera
- IPC general España (último dato interanual) → fuente: INE
- IPC subyacente España (último dato) → fuente: INE
- Hipoteca fija media mejor oferta del mercado → fuente: HelpMyCash o iAhorro

**INVERSIÓN Y RENTABILIDAD**
- Rentabilidad bruta media alquiler España (%) → fuente: Idealista / Fotocasa / Bankinter
- Rentabilidad neta estimada (si disponible)
- % compras por extranjeros no residentes (último dato anual) → fuente: Colegio Registradores

**CONSTRUCCIÓN**
- Coste ejecución material vivienda plurifamiliar (€/m²) → fuente: UVE Valoraciones / MITMA / ACR
- Variación interanual coste construcción
- Visados de obra nueva últimos 12 meses → fuente: Ministerio de Transportes / Fomento

**HIPOTECAS** *(pestaña 🏦 Hipotecas)*
- Euríbor 12M valor actual y variación vs máximo del ciclo
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
- Widgets BTC y EUR/USD: refresco cada 30s, fuentes en cascada, badge LIVE con `display: 'flex'`
- Noticias RSS: `fetch()` con `{ cache: 'no-store' }` + timestamp `&_cb=${Date.now()}`
- **Botón descarga PDF en el header:** clase `.pdf-download-btn`, es un `<a>` con `href="informe_mercado_inmobiliario_2026.pdf" download`. Contiene un SVG de icono documento+flecha y un `<span class="pdf-tooltip">Descargar Informe</span>`. Está situado a la izquierda del toggle de tema. **NO eliminar ni mover.**

**Layout primera fila del Resumen (grid-3):**
```
grid-template-columns: 2.2fr 0.85fr 0.85fr 0.85fr
├── [1] chartVenta + chartDonut integrado (90×90px)
├── [2] Indicadores Clave (indicator-grid)
├── [3] BITCOIN WIDGET (id: btc-*)   — Binance → CoinGecko → Kraken
└── [4] EUR/USD WIDGET (id: fx-*)    — Kraken OHLC → Binance → ExchangeRate-API
```

**Canvas IDs por pestaña:**
- **Resumen:** `chartVenta`, `chartDonut`, `chartCiudades`
- **Hipotecas:** `hipChartEuribor`, `hipChartTiposEntidad`, `hipChartCuotaMensual`, `hipChartEsfuerzo`
- **Jetas:** `chartOkupHistorico`, `chartOkupCCAA`, `chartOkupTipo`, `chartOkupPercepcion`

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
Idealista · Fotocasa · INE · Banco de España · BCE · Bankinter · Sociedad de Tasación · UVE Valoraciones · ACR · MITMA · Colegio de Registradores · Ministerio del Interior · CGPJ · Institut Cerdà · CaixaBank Research · HelpMyCash · iAhorro

**Estructura del script PDF (`build_informe_mercado.py`):**
```
Portada custom (draw_cover)   ← fondo oscuro NAVY, banda dorada lateral, texto "sebastiangil.ai"
                                 en blanco 38pt centrado con líneas doradas decorativas.
                                 NO usar imágenes ni logos — solo texto tipográfico.
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
El script usa `reportlab` (ya instalado). Los datos están hardcodeados como tablas Python. Para actualizar: editar los arrays `*_data` de cada sección y los `kpis*` de cada `kpi_row()`.

---

**Fecha en que hago esta solicitud: [ESCRIBE AQUÍ LA FECHA, ej: Junio 2026]**

---

*Fin del prompt*
