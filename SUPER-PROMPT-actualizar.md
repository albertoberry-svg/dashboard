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

**HIPOTECAS Y FINANCIACIÓN (pestaña Hipotecas 🏦)**
- Euríbor 12M valor actual y mínimo desde cuándo → fuente: Banco de España
- Tipo fijo medio mejor oferta mercado (TIN) → fuente: HelpMyCash / iAhorro
- Diferencial variable medio (Euríbor + X%) → fuente: AHE / entidades
- LTV máximo habitual (%) → sin cambio salvo normativa nueva
- Plazo medio hipotecas España → fuente: INE / AHE
- Tipos por entidad: Kutxabank, Openbank, ING, Bankinter, CaixaBank, Santander, BBVA, Sabadell (TIN fijo, diferencial variable, TAE, comisión apertura) → fuente: webs oficiales / comparadores
- Cuotas mensuales actualizadas (recalcular con nuevo tipo fijo si ha variado)
- Esfuerzo financiero por ciudad (% salario destinado a hipoteca) → fuente: BdE / INE
- Novedades Aval ICO jóvenes (dotación, condiciones actualizadas) → fuente: ICO / Ministerio Vivienda

**OKUPACIÓN & INQUIOKUPACIÓN (pestaña Jetas 🦹)**
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

1. **Ticker superior** → todos los valores del ticker (Madrid, Barcelona, España media, Alquiler, IPV, Hipoteca, Rentabilidad, Compraventas, Vivienda nueva, IPC, Euríbor, Bono 10Y, BCE, Construcción, Okupación)

2. **KPIs del panel Resumen** → los 6 KPI cards con sus valores y variaciones

3. **KPIs del panel Ciudades** → precios por ciudad y variaciones

4. **KPIs del panel Alquiler** → precio alquiler, meses de récord, subida acumulada 2 años, IRAV

5. **KPIs del panel Inversión** → rentabilidad total, bruta, subida real, % extranjeros

6. **KPIs del panel Macro/IPC** → IPC, IPC subyacente, Euríbor, BCE, Bono 10Y

7. **KPIs sección Costes de Construcción** → coste €/m², acumulado, índices de mano de obra y materiales

8. **KPIs del panel Hipotecas** → Euríbor 12M, tipo fijo medio, diferencial variable, LTV, plazo medio. Claves data-tip: `hip-euribor`, `hip-fijo`, `hip-variable`, `hip-ltv`, `hip-plazo`

9. **KPIs del panel Jetas** → denuncias, viviendas ocupadas, tiempo de desalojo, % Cataluña, viviendas en portales

10. **Datos de los gráficos de Hipotecas** → actualiza los arrays en `initHipotecasCharts()`:
    - Serie histórica Euríbor (canvas ID: `hipChartEuribor`)
    - Tipos por entidad fijo y variable (canvas ID: `hipChartTiposEntidad`)
    - Cuotas mensuales recalculadas con nuevo tipo fijo (canvas ID: `hipChartCuotaMensual`)
    - Esfuerzo financiero por ciudad (canvas ID: `hipChartEsfuerzo`)
    - Tabla comparativa entidades: array `hipData` en `initHipotecasCharts()`

11. **Datos de los gráficos de Jetas** → actualiza los arrays en `initJetasCharts()`:
    - Serie histórica de denuncias
    - Distribución por CCAA de ocupación
    - Cualquier gráfico temporal con nuevos trimestres

12. **Cualquier gráfico temporal** en otras pestañas con nuevos trimestres publicados

13. **Tooltips** → actualiza el objeto TIPS en el JS si los valores han cambiado:
    - Claves Hipotecas: `hip-euribor`, `hip-fijo`, `hip-variable`, `hip-ltv`, `hip-plazo`, `hip-chart-euribor`, `hip-chart-entidades`, `hip-chart-cuota`, `hip-chart-esfuerzo`, `hip-chart-tabla`
    - Claves Jetas: `jetas-denuncias`, `jetas-viviendas`, `jetas-desalojo`, `jetas-cataluna`, `jetas-portales`, `jetas-chart-historico`, `jetas-chart-ccaa`, `jetas-chart-tipo`, `jetas-chart-percepcion`, `jetas-chart-tabla`

14. **Tabla CCAA de demandas judiciales** → actualiza el array `ccaaData` en `initJetasCharts()` con el último trimestre del CGPJ

15. **Tarjetas informativas de Hipotecas** (Requisitos / Gastos asociados / Ayudas & Claves) → actualiza si han cambiado condiciones, normativa del Aval ICO, porcentajes de gastos, etc.

16. **Tarjetas informativas de Jetas** (Inquiokupación / Causas / Realidad vs Percepción) → actualiza estadísticas o novedades normativas

17. **Texto "Actualizado: [mes] [año]"** en el pie de página → pon el mes y año actuales

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

- El archivo se llama `index.html`
- Es un HTML single-file con Chart.js, **8 pestañas**: Resumen · Ciudades · Alquiler · Inversión · Macro/IPC · 🏦 Hipotecas · 🦹 Jetas · 📡 Noticias
- **Noticias siempre es la última pestaña** (posición 8)
- El orden en el array de `switchTab` es: `['overview','ciudades','alquiler','inversion','macro','hipotecas','jetas','noticias']`

**TEMA CLARO/OSCURO**
- Toggle switch en el header derecho (🌙 / ☀️), función `toggleTheme()`
- Aplica clase `body.light` y actualiza `Chart.defaults.color` + llama `chart.update('none')` sobre todas las instancias
- ⚠️ **NUNCA destruir los charts al cambiar de tema** — solo `chart.update('none')`
- La preferencia se guarda en `localStorage`

**LAYOUT MÓVIL PESTAÑAS**
- Grid de 6 columnas: cada tab ocupa `span 2` (→ 3 por fila)
- Tabs 7 y 8 (Jetas y Noticias) ocupan `span 3` → layout final: 3+3+2

**PESTAÑA HIPOTECAS 🏦**
- Función init: `initHipotecasCharts()`, flag: `hipotecasInitialized`, panel: `id="panel-hipotecas"`
- Color temático: `#00c2ff`
- Canvas IDs con prefijo `hip` para evitar duplicados con otras pestañas: `hipChartEuribor`, `hipChartTiposEntidad`, `hipChartCuotaMensual`, `hipChartEsfuerzo`
- Contiene: 5 KPIs · 4 gráficos · tabla comparativa entidades · 3 cajas informativas (Requisitos, Gastos, Ayudas)

**PESTAÑA JETAS 🦹**
- Función init: `initJetasCharts()`, flag: `jetasInitialized`, panel: `id="panel-jetas"`
- Color temático: `#ff4d6d`

**DETALLES VISUALES IMPORTANTES**
- Gauge needle (Alquiler, Demanda vs Oferta): clase CSS `gauge-needle` → blanca en dark, `#1a2540` en light
- Gráfico Rentabilidad por Activo (Inversión): 5 barras con colores distintos: dorado · azul · naranja teja `rgba(220,100,60,0.85)` · violeta `rgba(130,80,200,0.85)` · verde agua `rgba(60,190,140,0.85)`
- Noticias hora/fuente: amarillo `#f0c040` en tema oscuro, `var(--text3)` en tema claro

**PUBLICACIÓN**
- URL: **https://dashboard.sebastiangil.app**
- GitHub Pages, repo `albertoberry-svg/dashboard`, rama `main`, archivo `index.html` en raíz
- Para publicar: subir el `index.html` al repo de GitHub

**FUENTES PRINCIPALES**
Idealista · Fotocasa · INE · Banco de España · BCE · AHE · HelpMyCash · iAhorro · ICO · Bankinter · Sociedad de Tasación · UVE Valoraciones · ACR · MITMA · Colegio de Registradores · Ministerio del Interior · CGPJ · Institut Cerdà

**GUARDADO**
- Dashboard: `/mnt/user-data/outputs/index.html`
- Este super-prompt: `/mnt/user-data/outputs/SUPER-PROMPT-actualizar-dashboard.md`

---

**Fecha en que hago esta solicitud: [ESCRIBE AQUÍ LA FECHA, ej: Junio 2026]**

---

*Fin del prompt*
