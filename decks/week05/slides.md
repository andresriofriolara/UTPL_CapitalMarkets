<section class="title-slide">
Semana 5 | Mapeo de Riesgos y VaR
<div class="subtitle">Mercados y Riesgos Financieros • <em>Noviembre 05, 2025</em></div>
</section>

---

## Agenda
1. Sobre la Semana Anterior
2. Contenido Semana 5

---

## Sobre la Semana Anterior
- **4.1 Definición de instrumentos derivados**
- **4.2 Mercado de opciones**
    - 4.2.1 Características y participantes en el mercado de opciones
    - 4.2.2 Clasificación de las opciones

--

    - 4.2.3 Representación gráfica y numérica opciones
- **4.3 Mercado de futuros**
- **4.4 Swaps de interés**
- **4.5 Forwards**

---

## Contenido Semana 5
Mapeo de Riesgos y VaR

- **5.1** Definiciones de Riesgo
- **5.2** Tipos de Riesgo y Cuantificación
- **5.3** Medición de Riesgo
- **5.4** VaR
- **5.5** Ciclo Financiero de las Empresas
- **5.6** Gestión de Riesgos

---

## ¿Qué es Riesgo?

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
      src="https://www.mentimeter.com/app/presentation/al6rjjpyedjz3mwws28kngf7x9wbb7ks/embed"
      sandbox="allow-scripts allow-same-origin allow-presentation"
      allowfullscreen
      allowtransparency="true"
      frameborder="0"
      style="position:absolute;top:0;left:0;width:100%;height:100%;"
      loading="lazy">
    </iframe>
  </div>

--

Pérdida Potencial (Esperada e Inesperada)

--

## ¿Cómo Cuantifico el Riesgo?

--

Riesgo=Probabilidad x Severidad

--

## ¿Qué es un rendimiento?

--

Ganancia de Capital + Dividendo

--

$$
R = \left(\frac{P_1 - P_0}{P_0}\right) + \left(\frac{D_1}{P_0}\right)
$$

--

## ¿Cuál es la relación riesgo rendimiento?

<div style="position:relative;padding-bottom:56.25%;height:0;overflow:hidden;">
    <iframe
      src="https://miro.com/app/live-embed/uXjVJ-pN2bw=/?embedMode=view_only_without_ui&moveToViewport=-692,-412,1382,822&embedId=332130586804"
      frameborder="0"
      scrolling="no"
      allow="fullscreen; clipboard-read; clipboard-write"
      allowfullscreen
      style="position:absolute;top:0;left:0;width:100%;height:100%;"
      loading="lazy">
    </iframe>
  </div>

--
<section class="title-slide">
  <div class="midtitle">Riesgo: Definiciones y Enfoque</div>
  <div class="subtitle">Motivación, conceptos clave y marco mental</div>
</section>

--
### ¿Por qué gestionar el riesgo?
- Riesgo como **variabilidad de resultados** con potencial de pérdida.
- Crea valor al **reducir costos de distress**, suavizar inversión y proteger contratos.
- **Objetivo**: decisiones robustas bajo incertidumbre (no eliminar riesgo, _administrarlo_).

--
### Riesgo vs. Incertidumbre
- **Riesgo**: probabilidades estimables (modelo empírico).
- **Incertidumbre**: probabilidades no confiables o desconocidas (regímenes, rupturas).
- Implicación: elegir **métricas y procesos** acordes al _grado_ de conocimiento.

--
### Pérdida esperada y dispersión
- Pérdida esperada: $\mathbb{E}[L]$; riesgo: **dispersión** alrededor de $\mathbb{E}[L]$.
- Varianza: $\mathrm{Var}(R)=\mathbb{E}\!\left[(R-\mu)^2\right]$; desviación: $\sigma=\sqrt{\mathrm{Var}}$.
- **Asimetría** y **colas pesadas** importan para pérdidas extremas.

--
### Exposición y vulnerabilidad
- Exposición: tamaño del libro/posición ($), vencimientos, convexidad.
- Vulnerabilidad: sensibilidad a shocks (_betas_, duraciones, gaps).
- **Idea guía**: Riesgo $=$ **exposición × sensibilidad × volatilidad**.

---
<section class="title-slide">
  <div class="midtitle">Taxonomía de Riesgos</div>
  <div class="subtitle">Tipos, extensiones y mapeo a métricas</div>
</section>

--
### 5.1. Tipos principales
- **Mercado**: precios de activos, tasas, FX, commodities.
- **Crédito**: incumplimiento, migración, concentración.
- **Liquidez**: _market_ (profundidad) y _funding_ (financiamiento)-brechas.
- **Operacional**: procesos, personas, sistemas, eventos externos.

--
### 5.1.1 Extensiones y fronteras
- **Legal/compliance**, **reputacional**, **estratégico**.
- **Riesgo de modelo**: especificación, parámetros, implementación.
- Fronteras: crédito vs. mercado (CVaR (ES) de derivados); liquidez de mercado vs. fondeo.

--
### 5.1.2 Mapeo de riesgos a métricas
- Mercado: $\sigma$, beta, VaR/ES, _greeks_.
- Crédito: PD, LGD, EAD; pérdida esperada: $\mathrm{EL}=\mathrm{PD}\times\mathrm{LGD}\times \mathrm{EAD}$.
- Liquidez: _bid–ask_, profundidad, LCR/NSFR, _time-to-liquidate_.
- Operacional: frecuencia & severidad; colas pesadas (familias _severity_).

--
### 5.1.3 Diversificación y correlaciones
- Correlación **dinámica** (regímenes) — suele **aumentar** en estrés.
- Implicación: límites y colchones deben contemplar **co-movimientos** extremos.

---
<section class="title-slide">
  <div class="midtitle">Medición: Media, Varianza, Correlación</div>
  <div class="subtitle">Momentos, portafolios y volatilidad</div>
</section>

--
### 5.2.1 Retornos y momentos
- Retorno: $R_t=\ln(P_t/P_{t-1})$ (log) o $R_t=(P_t-P_{t-1})/P_{t-1}$.
- $\mu=\mathbb{E}[R]$, $\sigma=\sqrt{\mathbb{E}(R-\mu)^2}$.
- Sesgo y curtosis para **colas y asimetrías**.

--
### 5.2.2 Portafolio: varianza y correlación
- $\mu_p=\sum_i w_i \mu_i$.
- $\sigma_p^2=\mathbf{w}^\top \Sigma \mathbf{w}$, con $\Sigma$ matriz de covarianzas.
- Diversificación: $\sigma_p$ cae si correlaciones $<1$.

--
### 5.2.3. Estimación de volatilidad (intuición)
- Muestras rodantes y **EWMA**: $\sigma_t^2=\lambda\sigma_{t-1}^2+(1-\lambda)r_{t-1}^2$.
- **Clustering** de volatilidad; sensibilidad a ventana y $\lambda$.

--
### 5.2.4. Medición vs. decisión
- Métrica _decision_: interpretable, estable, sensible al riesgo relevante.
- Tensión: rapidez (paramétrico) vs. realismo (histórico/MC).

---
<section class="title-slide">
  <div class="midtitle">Valor en Riesgo (VaR): Conceptos y Métodos</div>
  <div class="subtitle">Definición, enfoques y límites</div>
</section>

--
### 5.3.1. Definición e interpretación
- $\mathrm{VaR}_{\alpha,H}$: pérdida tal que $\mathbb{P}(L \le \mathrm{VaR})=\alpha$ en horizonte $H$.
- **No** es la peor pérdida; no informa la cola más allá de $\alpha$.
- Requiere: posición, horizonte, nivel de confianza, convención de signo (pérdidas $+$).

--
### 5.3.2. VaR paramétrico (normal/t)

<ul>
  <li>Normal:
    \( \mathrm{VaR}_{\alpha} \approx z_{\alpha}\,\sigma_p - \mu_p \) (en pérdidas)
  </li>
  <li>t-Student (\( \nu \) g.l.):
    \( \mathrm{VaR}_{\alpha} \approx t_{\alpha,\nu}\,\sigma_p
       \sqrt{\frac{\nu-2}{\nu}} - \mu_p \)
  </li>
  <li>Pros: rápido, parsimonioso. Contras: colas/asimetrías mal capturadas si no se ajusta.</li>
</ul>

--
### 5.3.3. VaR histórico
- Ordenar P/L empíricos y tomar el percentil $(1-\alpha)$.
- Captura no-normalidad y no linealidades de la cartera.
- Sensible a ventana, ponderaciones y **cambios de régimen**.

--
### 5.3.4. Riesgos y usos del VaR
- Riesgo de modelo (supuestos), de estimación (muestras) y de **implementación**.
- Uso: límites, capital económico, _backtesting_. Compleméntese con ES/CVaR y estrés.

---
<section class="title-slide">
  <div class="midtitle">Ciclo Financiero de las Empresas</div>
</section>

--
### 5.4.1. Ciclo de gestión
- **Identificar → Medir → Monitorear → Controlar**.
- Documentación, _data lineage_, trazabilidad de supuestos.

--
### 5.4.2. Apetito y capacidad de riesgo
- **Capacidad**: límites económicos/regulatorios.
- **Apetito**: variabilidad/pérdida deseada para objetivos.
- Declaraciones claras: métricas, horizontes, umbrales y **tolerancias**.

--
### 5.4.3. Límites, KRIs y escalamiento
- Límites por libro/factor; **triggers** de alerta y acciones.
- KRIs: métricas adelantadas (volatilidad, _liquidity gaps_, concentración).

--
### 5.4.4. Tres líneas de defensa
- 1ª: negocio (toma y primera gestión del riesgo).
- 2ª: riesgos/compliance (política, validación).
- 3ª: auditoría interna (independiente).

---
<section class="title-slide">
  <div class="midtitle">Gestión Corporativa y Creación de Valor</div>
  <div class="subtitle">Cuándo agrega valor y políticas</div>
</section>

--
### 5.5.1. ¿Cuándo agrega valor la gestión de riesgos?
- Reduce costos esperados de quiebra/distress.
- Mitiga subinversión por restricciones financieras.
- Suaviza impuestos (no linealidades) y mejora contratos con _stakeholders_.

--
### 5.5.2. ¿Cuándo _no_ agrega valor?
- Riesgos totalmente **diversificables** por inversionistas.
- Coberturas que destruyen _upside_ sin beneficio en costo de capital.

--
### 5.5.3. Políticas y herramientas
- **Coberturas naturales**: _matching_ de monedas/plazos/índices.
- **Derivados/seguros**: forwards, swaps, opciones; pólizas.
- Diseño: objetivo claro, horizonte, métrica de éxito, gobernanza.

--
### 5.5.4. Métrica riesgo–retorno (intuición)
- Ajuste por riesgo (p. ej., intuición tipo Sharpe/RAROC).
- Evaluar si la política **mejora el perfil** retorno–riesgo y cumple apetito.


---

## Dudas y Preguntas