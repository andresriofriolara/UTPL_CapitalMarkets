<section class="title-slide">
Semana 2 | Panorama general de la teoría de los mercados financieros 
<div class="subtitle">Mercados y Riesgos Financieros • <em>Octubre 15, 2025</em></div>
</section>

---

## Agenda
1. Sobre la Semana Anterior
2. Contenido Semana 2
4. Discusión del Caso: "Dilema en Reinicke Ostria"

---

## Sobre la Semana Anterior
- **1.1 Arquitectura del sistema financiero**
  - Monetario · Bancario · Capitales · Divisas · Derivados · Seguros · Mercancías
- **1.2 Ciclo financiero de las empresas**
- **1.3 Eficiencia financiera y generación de valor**

--

## Big Mac Index

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; border:0;">
  <iframe
    src="https://worldpopulationreview.com/country-rankings/big-mac-index-by-country"
    title="Big Mac Index by Country"
    loading="lazy"
    style="position:absolute; top:0; left:0; width:100%; height:100%; border:0;"
    sandbox="allow-scripts allow-same-origin allow-popups allow-forms"
  ></iframe>
</div>

---

## Semana 2
Panorama general de la teoría de los mercados financieros 

---

**Semana 2: Panorama general de la teoría de los mercados financieros**
- 2.1 Teoría del valor presente y tasa de descuento
- 2.2 Modelo de valoración de activos financieros (CAPM)
- 2.3 Teoría moderna de portafolio (Markowitz)
- 2.4 Mercado de capitales eficiente
- 2.5 Instrumentos del mercado de capitales
    - 2.5.1 Clasificación de instrumentos del mercado de capitales.

---

## 2.1 · Teoría del valor presente y tasa de descuento

El tiempo es nuestra variable mas importante. ¡Siempre!



____________________________________________________________________________________________

--

Primero recordemos:

$$V_f = V_p \left(1+i_t \right)^{t}$$

--

$$V_p = \frac{V_f}{\left(1+i_t \right)^{t}}$$

--

**Definición formal**  
Para flujos 
Para flujos $\{CF_t\}_{t=1}^n$ y tasa $r$:

$$
PV = \sum_{t=1}^{n} \frac{CF_t}{(1+r)^t}.
$$

--

- Si hay **múltiples riesgos**, \(r\) debe ser **consistente con el riesgo de los flujos** (no del emisor) y con **moneda** y **horizonte**.  
- **Valor temporal vs prima por riesgo:** \(r=R_f+\mathrm{PR}\), con \(R_f\) libre de riesgo en **misma divisa y plazo**.

--

**Errores comunes**  
- Descontar **flujos nominales** con **tasa real** (o viceversa).  
- Mezclar **horizontes** de tasas.  
- Usar **WACC de la firma** para un **proyecto** con riesgo distinto.

--

**Buenas prácticas (coste de capital)**  
- WACC con **pesos de mercado**, deuda **post-impuestos** y \(K_e\) por **CAPM** (u otro coherente).  
- Ajustar riesgo **específico** en **flujos** o con **hurdle rate** documentado (evitar “sumar puntos” sin sustento).

---

## 2.2 · Modelo de valoración de activos financieros (CAPM)

**Ecuación (SML)**

$$
\mathbb{E}[R_i]=R_f+\beta_i\big(\mathbb{E}[R_M]-R_f\big)
$$

$$
\beta_i=\frac{\mathrm{Cov}(R_i,R_M)}{\mathrm{Var}(R_M)}.
$$

--

**Lectura conceptual**  
- Solo “paga” el riesgo **sistemático**; el **idiosincrático** se **diversifica**.  
- CAPM vincula el coste de capital a la **contribución marginal al riesgo** de la **cartera de mercado**.

--

**Supuestos clave (para discutir límites)**  
1. Inversionistas **media–varianza**.  
2. **Horizonte único**.  
3. Mercados **competitivos/sin fricciones**.  
4. Préstamo/colocación al **\(R_f\)**.  
5. **Expectativas homogéneas**.  
6. **Cartera de mercado invertible**.

--

**Implicaciones empíricas / debate**  
- **SML** con pendiente $(\mathbb{E}[R_M]-R_f)$.  
- Evidencia **mixta**: retorno–beta débil a veces; **anomalías** (tamaño, valor) → **multifactor**.

--

**Pitfalls al estimar CAPM**  
- $(R_f)$ mal elegido (**moneda/plazo**).  
- **Horizonte** de \(\beta\) inconsistente.  
- **Proxy** de mercado estrecho.  
- No **desapalancar/reapalancar** \(\beta\) cuando cambia el **apalancamiento**.

---

## 2.3 · Teoría moderna de portafolio (Markowitz)

**Marco media–varianza** (pesos $ \mathbf{w} $, medias $ \boldsymbol{\mu} $, matriz $ \Sigma $):

$$
\begin{aligned}
\mu_p= \mathbf{w}^\top \boldsymbol{\mu},\\
\sigma_p^2= \mathbf{w}^\top \Sigma\, \mathbf{w},\\
\mathbf{1}^\top \mathbf{w} &= 1.
\end{aligned}
$$

--

**Frontera eficiente**  
- Carteras que **maximizan** retorno para varianza dada (o **minimizan** varianza para retorno objetivo).

--

**Intuición matemática clave**  
- La reducción de riesgo proviene de **covarianzas**; **correlación baja/negativa** desplaza la frontera **a la izquierda**.  
- Con activo sin riesgo surge la **CML**: combinaciones del **risk-free** y la **cartera tangente**.

--

**Errores comunes**  
- \(\Sigma\) con **pocas observaciones** (inestable).  
- Ignorar **costes** y **restricciones** (no short, límites).  
- Históricos sin **estabilización** (shrinkage, Bayes, ventanas).

--

**Notas:**  
- Mostrar **error de optimización** (pequeños cambios en \(\Sigma\) → **pesos extremos**).  
- **Regularización** (ridge/lasso), **restricciones prácticas** y **Ledoit–Wolf** (conceptual).

---

## 2.4 · Mercado de capitales eficiente (EMH: Fama)

**Definición operativa**  
Los precios **reflejan plenamente** la información disponible:
- **Débil**: info **histórica** de precios.  
- **Semifuerte**: toda **información pública**.  
- **Fuerte**: también **información privada**.

--

**Implicaciones**  
- No hay **estrategias sistemáticas** con **alfa neto** de costos/riesgo bajo la forma correspondiente.  
- **Eventos públicos** se incorporan **rápido** en precios.

--

**Notas:**  
- EMH **no** dice que el precio sea “correcto” **siempre**; dice que **no hay reglas replicables** que extraigan rentas con esa info, **ajustada por riesgo y costos**.  
- Puede haber **sobre/infra-reacciones**; lo clave es su **explotabilidad**.

---

## 2.5 · Instrumentos del mercado de capitales

- **Renta variable**: acciones comunes/preferentes; derechos político-económicos; **alto riesgo/volatilidad**.  
- **Renta fija**: bonos corporativos/estatales, convertibles, papel comercial; riesgos de **tasa, crédito, liquidez**; sensibilidad por **duración** \(D\) y **convexidad**.  

--

## 2.5 · Instrumentos del mercado de capitales (Cont.)

- **Derivados**: opciones, futuros, swaps; valor depende del **subyacente**; **cobertura** y **especulación**.  
- **Primario vs secundario**: **emisión** vs **negociación**; **liquidez**, **formación de precios**, señal para **nuevas emisiones**.

---

## Discusión del Caso: "Dilema en Reinicke Ostria"

---

## Dudas y Preguntas