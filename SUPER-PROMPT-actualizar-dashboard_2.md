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

**OCUPACIÓN & INQUIOKUPACIÓN (pestaña Jetas)**
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

### PASO 3 — ACTUALIZACIÓN DEL CÓDIGO

Una vez confirmado el informe (yo te diré "procede" o haré correcciones), actualiza el archivo HTML del dashboard tocando **todos** los siguientes elementos:

1. **Ticker superior** → todos los valores del ticker (Madrid, Barcelona, España media, Alquiler, IPV, Hipoteca, Rentabilidad, Compraventas, Vivienda nueva)

2. **KPIs del panel Resumen** → los 6 KPI cards con sus valores y variaciones

3. **KPIs del panel Ciudades** → precios por ciudad y variaciones

4. **KPIs del panel Alquiler** → precio alquiler, meses de récord, subida acumulada 2 años, IRAV

5. **KPIs del panel Inversión** → rentabilidad total, bruta, subida real, % extranjeros

6. **KPIs del panel Macro/IPC** → IPC, IPC subyacente, Euríbor, BCE, Bono 10Y

7. **KPIs sección Costes de Construcción** → coste €/m², acumulado, índices de mano de obra y materiales

8. **KPIs del panel Jetas** → denuncias, viviendas ocupadas, tiempo de desalojo, % Cataluña, viviendas en portales

9. **Datos de los gráficos** → actualiza los arrays de datos en los charts de Chart.js que correspondan, incluyendo:
   - Serie histórica de denuncias (pestaña Jetas)
   - Distribución por CCAA de ocupación (pestaña Jetas)
   - Cualquier gráfico temporal con nuevos trimestres publicados

10. **Tooltips** → actualiza el texto de los tooltips (objeto TIPS en el JS) si los valores han cambiado. Las claves de Jetas son: `jetas-denuncias`, `jetas-viviendas`, `jetas-desalojo`, `jetas-cataluna`, `jetas-portales`, `jetas-chart-historico`, `jetas-chart-ccaa`, `jetas-chart-tipo`, `jetas-chart-percepcion`, `jetas-chart-tabla`

11. **Tabla CCAA de demandas judiciales** → actualiza el array `ccaaData` en la función `initJetasCharts()` con los datos del último trimestre del CGPJ disponible

12. **Tarjetas informativas de análisis profundo Jetas** → actualiza cualquier estadística o dato normativo que haya cambiado en los 4 bloques del análisis ampliado:
    - `Ocupación vs Inquiokupación`: plazos, artículos del CP, novedades LO 1/2025
    - `Coste real para el propietario`: rango de rentas impagadas, costes legales y de reparación
    - `Qué hacer si te ocupan`: si hay cambios en procedimiento policial o novedades legales
    - `El proceso judicial — cronología`: plazos reales según últimos datos CGPJ

13. **Texto "Actualizado: [mes] [año]"** en el pie de página → pon el mes y año actuales

---

### PASO 4 — NUEVAS PESTAÑAS (si procede)

Si en el futuro se crea una nueva pestaña, el proceso de actualización debe incluir también:

- Buscar los datos relevantes para esa pestaña en el PASO 1 (añadir bloque de búsqueda)
- Actualizar sus KPIs en el PASO 3
- Actualizar sus gráficos y tablas en el PASO 3
- Actualizar sus tooltips (claves `data-tip`) en el objeto TIPS del JS
- Actualizar este SUPER-PROMPT para que la nueva pestaña quede documentada aquí de forma permanente

> 📌 **Instrucción de auto-mantenimiento:** Cada vez que se añada una pestaña nueva al dashboard, actualiza también este archivo SUPER-PROMPT-actualizar-dashboard.md para reflejar los nuevos datos que hay que buscar y los nuevos elementos que hay que actualizar. Así este prompt siempre estará al día sin intervención manual.

---

### PASO 5 — VERIFICACIÓN

Al terminar, indícame:
- ✅ Cuántos valores has podido actualizar
- ⚠️ Cuáles no encontraste y dejaste sin cambiar
- 📅 El rango de fechas de los datos usados
- 🔗 Las fuentes principales consultadas

---

### CONTEXTO DEL PROYECTO

- El archivo se llama `index.html` y se sirve desde `https://dashboard.sebastiangil.app`
- Repo GitHub: `https://github.com/albertoberry-svg/dashboard` (rama `main`, archivo `index.html` en raíz)
- Es un HTML single-file con Chart.js, diseño oscuro, **8 pestañas**: Resumen · Ciudades · Alquiler · Inversión · Macro/IPC · 🏦 Hipotecas · 🦹 Jetas · 📡 Noticias
- Array interno de tabs: `['overview','ciudades','alquiler','inversion','macro','hipotecas','jetas','noticias']`
- El sistema de tooltips usa el objeto `TIPS` en el JS con claves `data-tip` en los elementos HTML
- La pestaña Jetas se inicializa con la función `initJetasCharts()` y tiene panel `id="panel-jetas"`
- La barra de navegación en móvil usa grid 6 cols: tabs 1–6 → `span 2` (3 por fila), tabs 7–8 → `span 3` (2 por fila)
- Las fuentes principales del dashboard son: **Idealista, Fotocasa, INE, Banco de España, Bankinter, Sociedad de Tasación, UVE Valoraciones, ACR, MITMA, Colegio de Registradores, Ministerio del Interior, CGPJ, Institut Cerdà**
- Tras actualizar, guarda el archivo en `/mnt/user-data/outputs/index.html`
- Si actualizas también este SUPER-PROMPT, guárdalo en `/mnt/user-data/outputs/SUPER-PROMPT-actualizar-dashboard_2.md`

---

### ESTRUCTURA TÉCNICA — REFERENCIA RÁPIDA

#### Layout primera fila panel Resumen (grid-3)
```
grid-template-columns: 2.2fr 0.85fr 0.85fr 0.85fr
├── [1] Evolución del Precio de Venta (chartVenta)
│       └── Donut integrado al pie: chartDonut (2ª mano 73% / Obra nueva 19% / VPO 8%)
├── [2] Indicadores Clave (indicator-grid)
├── [3] BITCOIN WIDGET (id: btc-*)
│       Fuentes: Binance → CoinGecko → Kraken
│       Actualización: cada 30 segundos
│       Badge LIVE: id="btc-live-badge" (display: flex cuando activo)
└── [4] EUR/USD WIDGET (id: fx-*)
        Fuentes: Kraken OHLC → Binance EURUSDT → ExchangeRate-API
        Datos: intradiario 24h, velas de 1h
        Stats: MÁX 24H, MÍN 24H, APERTURA, VAR. 24H
        Actualización: cada 30 segundos
        Badge LIVE: id="fx-live-badge" (display: flex cuando activo)
```

#### Widgets de mercado en tiempo real
Ambos widgets (BTC y EUR/USD) siguen el mismo patrón:
- Estado `loading` → spinner + "Conectando..."
- Estado `error` → ⚠️ + mensaje
- Estado `data` → precio grande + badge % + sparkline SVG + 4 stats + footer con hora y fuente
- Badge LIVE verde con animación `pulse` (`.live-badge` + `.live-dot`)
- Flash de color al actualizar precio: verde si sube, rojo si baja
- `showState()` activa el badge con `display: 'flex'` (no `''` ni `'block'`)

#### Sparkline EUR/USD — detalles técnicos
- SVG `id="fx-spark-svg"` viewBox `0 0 240 50`
- Path línea: `id="fx-spark-fill"` y `id="fx-spark-line"`
- Gradiente: `id="fxSparkGrad"`
- Línea de apertura punteada: `id="fx-open-line"` (cyan `#00b4d8`, dasharray `3,3`)
- Cache de velas: variable `sparkCache` (permite añadir precio live al final del array)

#### Pestaña Jetas — sección "Análisis Profundo" (añadida Marzo 2026)
Cuatro bloques bajo el separador `ANÁLISIS PROFUNDO · DATOS · MARCO LEGAL`:

| Bloque | Color borde | Contenido clave |
|--------|-------------|-----------------|
| ⚖️ Ocupación vs Inquiokupación | rojo `#ff4d6d` | Tabla comparativa 6 filas, regla 48h, límites LO 1/2025 |
| 💸 Coste real propietario | dorado | Desglose línea a línea, total 20.000–40.000€ |
| 🛡️ Qué hacer si te ocupan | verde | 5 pasos numerados (denuncia → abogado → suministros → negociación → prevención) |
| ⏱️ Proceso judicial cronología | azul `var(--blue2)` | Timeline con puntos de color, mes a mes hasta los 23,2 meses |

#### Tooltip EUR/USD
```javascript
'chart-eurusd': {
  title: 'EUR/USD · Tipo de Cambio',
  body:  'Precio de cierre del euro frente al dólar...',
  source:'BCE · Frankfurter API · Actualización diaria'
}
```

#### CSS móvil clave
- `.jetas-fuentes` → `display:none !important` en `max-width: 480px`
- `.info-boxes-grid` → `grid-template-columns: 1fr !important` en `max-width: 480px`
- `.grid-3` → `grid-template-columns: 1fr 1fr` en `max-width: 1200px`

#### Canvas IDs por pestaña
- **Resumen:** `chartVenta`, `chartDonut`, `chartCiudades`, `chartPrevisiones`
- **Hipotecas:** `hipChartEuribor`, `hipChartTiposEntidad`, `hipChartCuotaMensual`, `hipChartEsfuerzo`
- **Jetas:** `chartOkupHistorico`, `chartOkupCCAA`, `chartOkupTipo`, `chartOkupPercepcion`

#### SEO — NO TOCAR NUNCA
```html
<meta name="google-site-verification" content="fm-yZR6gPCYEu1uQwdhxBPHlPMAi6d78yzgVw_krv14" />
<link rel="canonical" href="https://dashboard.sebastiangil.app">
<link rel="sitemap" type="application/xml" href="https://dashboard.sebastiangil.app/sitemap.xml">
```
Al actualizar, sí tocar:
- `dateModified` en el bloque JSON-LD (`<script type="application/ld+json">`)
- `<lastmod>` en `sitemap.xml`

---

**Fecha en que hago esta solicitud: [ESCRIBE AQUÍ LA FECHA, ej: Junio 2026]**

---

*Fin del prompt*
