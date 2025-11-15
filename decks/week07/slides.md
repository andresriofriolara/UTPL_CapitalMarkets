<section class="title-slide">
Semana 7 | Planeación financiera a largo plazo
<div class="subtitle">Mercados y Riesgos Financieros • <em>Noviembre 19, 2025</em></div>
</section>

---

## Agenda
1. Sobre la Semana Anterior
2. Contenido Semana 7

---

## Sobre la Semana Anterior
Planificación de la estrategia de inversión

- **6.1** Estrategias de Momentum
- **6.2** Estrategias de valor
- **6.3** Opciones reales
- **6.4** Estructura Óptima de Capital
- **6.5** Fusiones y Adquisiciones Estratégicas

---

## Contenido Semana 7
Planeación financiera a largo plazo

- **7.1** Volatilidad financiera y su medición 
- **7.2** Simulación de Monte Carlo
- **7.3** Taller Simulador

---

## Semana 7: Planeación financiera a largo plazo

--

## Planeación financiera a largo plazo

- La planeación financiera a largo plazo busca:
  - Alinear los **objetivos estratégicos de crecimiento** con:
    - La **capacidad interna de financiamiento** (utilidades retenidas).
    - La política de **endeudamiento** y de **dividendos**.

--

- Requerimientos:
  - **Estados financieros pro forma**:
    - Estado de resultados proyectado.
    - Balance general proyectado.
    - Estado de flujos de efectivo proyectado.

--

- Preguntas clave:
  - ¿Las metas de crecimiento son **consistentes** con la estructura financiera actual?
  - ¿Se requerirá **financiamiento externo** (nueva deuda o nuevo capital)?

--

## Método del porcentaje de ventas: Proyección

- Algunas partidas del estado de resultados y del balance general se modelan como proporcionales a las ventas.
- Supongamos:
  - Ventas actuales: $\text{Ventas}_0$.
  - Tasa de crecimiento de ventas: $g_{\text{ventas}}$.

--

- Ventas proyectadas:
  $$\text{Ventas}_1 = \text{Ventas}_0 \cdot (1 + g_{\text{ventas}}).$$
- Partida ligada a ventas (por ejemplo inventarios):
  $$\text{Inventarios}_1 = \text{Inventarios}_0 \cdot \frac{\text{Ventas}_1}{\text{Ventas}_0}.$$
- Uso:
  - Construir estados pro forma.
  - Estimar **necesidades adicionales de financiamiento**.

--

## Rendimiento sobre el capital (ROE)

- Definición:
  - El **rendimiento sobre el capital** (ROE) mide la rentabilidad
    para los accionistas:
  $$ROE = \frac{\text{Utilidad Neta}}{\text{Capital Contable}}.$$

--

## Modelo DuPont del $ROE$

- El **modelo DuPont** descompone el $ROE$ en tres factores:
  $$ROE
  = \frac{\text{Utilidad Neta}{\text{Ventas}}
    \times \frac{\text{Ventas}}{\text{Activos Totales}}
    \times \frac{\text{Activos Totales}}{\text{Capital Contable}}.$$

--

- Términos:
  - $\dfrac{\text{Utilidad Neta}{\text{Ventas}}$:
    - **Margen neto** (rentabilidad de las ventas).
  - $\dfrac{\text{Ventas}}{\text{Activos Totales}}$:
    - **Rotación de activos** (eficiencia en el uso de activos).
  - $\dfrac{\text{Activos Totales}}{\text{Capital Contable}}$:
    - **Multiplicador de capital** (apalancamiento financiero).

--

## Crecimiento sostenible: definición

- La empresa elige una política de:
  - Dividendos.
  - Endeudamiento.
  - Rentabilidad operativa.

--

- **Tasa de reinversión** ($RR$, por sus siglas en inglés *Retention Ratio*):
  - Sea $\text{payout}$ la proporción de la **utilidad neta** pagada como dividendos.
  - Entonces:
    $$RR = 1 - \text{payout}.$$

--

  - El crecimiento sostenible es la tasa a la cual:
    - La empresa puede crecer **sin emitir nuevo capital**.
    - Mantiene constante su razón de endeudamiento.
    - Mantiene su política de dividendos.

--

## Crecimiento sostenible: fórmula

- El **crecimiento sostenible** $g^\*$ viene dado por:
  $$g^\* = \frac{ROE \cdot RR}{1 - ROE \cdot RR}.$$
- Interpretación:
  - $ROE \cdot RR$ representa la proporción del **capital contable** que se incrementa
    cada periodo gracias a las **utilidades retenidas**.
  - El denominador ajusta por el hecho de que el capital crece con el tiempo.

--

- Consistencia financiera:
  - Si la empresa fija un crecimiento de ventas $g_{\text{ventas}}$:
    - Si $g_{\text{ventas}} \le g^\*$ ⇒ puede financiarse principalmente con utilidades retenidas.
    - Si $g_{\text{ventas}} > g^\*$ ⇒ necesitará financiamiento externo.

--

## Crecimiento sostenible: ejemplo numérico

- Suponiendo:
  - $ROE = 0.15$ (15 %).
  - Proporción de dividendos $\text{payout} = 0.40$ (40 %).
- Tasa de reinversión:
  $$RR = 1 - 0.40 = 0.60.$$

--

- Producto $ROE \cdot RR$:
  $$ROE \cdot RR = 0.15 \cdot 0.60 = 0.09.$$
- Crecimiento sostenible:
  $$g^\* = \frac{0.09}{1 - 0.09}
        = \frac{0.09}{0.91}
        \approx 0.0989
        \quad (\text{9.89\,\%}).$$


--

## Análisis de sensibilidad y escenarios

- La planeación de largo plazo no se hace con un solo escenario:
  - **Escenario base**:
    - Supuestos considerados más probables.
  - **Escenario pesimista**:
    - Menores ventas, mayores costos, menor margen, menor $ROE$.
  - **Escenario optimista**:
    - Mayores ventas, mejores márgenes, mayor $ROE$.

--

- Para cada escenario se recalculan:
  - Utilidad neta proyectada.
  - Rendimiento sobre el capital ($ROE$).
  - Crecimiento sostenible $g^\*$.

---

## 7.1 Volatilidad financiera y su medición

- La **volatilidad** es una medida de:
  - La **dispersión** de los rendimientos de un activo en torno a su media.
  - El **riesgo de variaciones extremas** (tanto al alza como a la baja).
  
--

  - Base para:
    - Medir riesgo de mercado.
    - Calcular Valor en Riesgo (VaR, por sus siglas en inglés *Value at Risk*).
    - Diseñar coberturas con derivados.
    - Asignar activos en portafolios.

--

- Tipos:
  - Volatilidad histórica.
  - Volatilidad implícita.

--

## Rendimientos financieros

- Precio de un activo:
  - $P_t$: precio en el día $t$.
  - $P_{t-1}$: precio en el día anterior.

--

- **Rendimiento simple diario**:
  $$R_t = \frac{P_t - P_{t-1}}{P_{t-1}} = \frac{P_t}{P_{t-1}} - 1.$$
- Serie de rendimientos:
  - $R_1, R_2, \dots, R_n$.

--

- **Media muestral** de rendimientos:
  $$\bar R = \frac{1}{n} \sum_{i=1}^n R_i.$$
- Pregunta:
  - ¿Qué tan dispersos están los $R_i$ alrededor de $\bar R$?

--

## Volatilidad histórica: fórmula

- La **volatilidad histórica** se mide como la **desviación estándar muestral** de
  los rendimientos:
  $$\sigma = \sqrt{\frac{\sum_{i=1}^n (R_i - \bar R)^2}{n - 1}}.$$
- Donde:
  - $R_i$: rendimiento en el periodo $i$.
  - $\bar R$: media de los rendimientos.
  - $n$: número de observaciones.
  - $\sigma$: volatilidad histórica en la frecuencia utilizada (por ejemplo, diaria).

--

## Volatilidad histórica: interpretación práctica

- A nivel operativo:
  - Se calcula a partir de una ventana de datos (por ejemplo, 60 días, 1 año, etc.).
  - Se actualiza continuamente (ventanas móviles).

--

- Uso:
  - Para evaluar la **estabilidad** de un activo.
  - Para comparar el riesgo relativo entre activos:
    - Misma media de rendimiento pero distinta volatilidad.

--

  - Como insumo en:
    - Modelos de valoración.
    - Modelos de riesgo (Valor en Riesgo, simulación de Monte Carlo).

--

## Volatilidad anualizada

- Si los rendimientos diarios son aproximadamente independientes y con distribución similar,
  se puede aproximar la **volatilidad anual** como:
  $$\sigma_{\text{anual}} \approx \sigma_{\text{diaria}} \cdot \sqrt{N},$$
  donde:
  - $\sigma_{\text{diaria}}$: volatilidad medida con rendimientos diarios.
  - $N$: número de días de mercado en el año (frecuentemente $N = 252$).

--

- Ejemplo:
  - Si $\sigma_{\text{diaria}} = 0.012$ (1.2\,\%):
    $$\sigma_{\text{anual}} \approx 0.012 \cdot \sqrt{252}.$$
- Interpretación:
  - La volatilidad anual refleja la dispersión esperada de los **rendimientos anuales**.

--

## Volatilidad histórica vs volatilidad implícita

- **Volatilidad histórica**:
  - Se calcula a partir de datos pasados de precios.
  - Describe el comportamiento **observado** del activo.

--

- **Volatilidad implícita**:
  - Se deriva de los **precios de opciones** sobre el activo.
  - Se obtiene al “invertir” un modelo de valoración (por ejemplo, Black–Scholes).
  - Refleja la **expectativa del mercado** sobre la volatilidad futura.

--

- Uso combinado:
  - La comparación entre volatilidad histórica e implícita:
    - Ayuda a evaluar si el mercado espera cambios en el riesgo.
    - Es clave en la valoración y en la gestión de coberturas.


---

## 7.2 Simulación de Monte Carlo: idea general

- La **simulación de Monte Carlo** es una técnica que:
  - Usa **números aleatorios** y **distribuciones de probabilidad**.
  - Genera muchas trayectorias posibles para las variables de interés.

--

- Ventaja:
  - En lugar de un solo resultado puntual, produce una **distribución de resultados**.

--

- En finanzas se usa para:
  - Valorar portafolios con componentes no lineales (por ejemplo, opciones).
  - Evaluar proyectos de inversión con incertidumbre en precios, volúmenes y costos.
  - Calcular Valor en Riesgo y otras medidas de riesgo extremo.
  - Realizar pruebas de estrés (stress testing).

--

## Pasos de una simulación de Monte Carlo

- Paso 1: Modelo determinístico base.
  - Ejemplo: valor del portafolio al final del día:
    $$V_1 = V_0 \cdot (1 + R),$$
    donde $R$ es el rendimiento diario.

--

- Paso 2: Identificar variables aleatorias clave.
  - Rendimiento del activo.
  - Tipo de cambio.
  - Tasa de interés.
  - Volumen de ventas, etc.

--

- Paso 3: Asignar distribuciones de probabilidad.
  - Por ejemplo, rendimiento diario $R$ con:
    $$R \sim \mathcal{N}(\mu, \sigma^2).$$

--

- Paso 4: Generar números aleatorios.
  - Se generan valores $Z$ de una distribución normal estándar:
    $$Z \sim \mathcal{N}(0, 1).$$
  - Se transforman en rendimientos:
    $$R = \mu + \sigma \cdot Z.$$

--

- Paso 5: Ejecutar muchas iteraciones.
  - Para cada simulación $i$:
    $$R_i = \mu + \sigma \cdot Z_i,$$
    $$V_{1,i} = V_0 \cdot (1 + R_i).$$
  - Repetir para $i = 1, 2, \dots, N$ (por ejemplo, $N = 1000$).

--

- Paso 6: Analizar la distribución simulada.
  - Valores $\{V_{1,1}, \dots, V_{1,N}\}$.
  - Pérdidas $\{L_1, \dots, L_N\}$ con:
    $$L_i = V_0 - V_{1,i}.$$
  - Calcular media, volatilidad, percentiles y Valor en Riesgo.

--

## Ejemplo Monte Carlo: portafolio de un activo (1 día)

- Supuestos:
  - Valor inicial del portafolio: $V_0 = 100{,}000$.
  - Media de rendimiento diario: $\mu = 0.0005$ (0.05\,\%).
  - Volatilidad diaria: $\sigma = 0.015$ (1.5\,\%).

--

- Para cada simulación $i$:
  - Generar $Z_i \sim \mathcal{N}(0, 1)$.
  - Calcular:
    $$R_i = \mu + \sigma \cdot Z_i.$$
    $$V_{1,i} = V_0 \cdot (1 + R_i).$$
    $$L_i = V_0 - V_{1,i}.$$

--

- Repetir para $i = 1, \dots, N$ (por ejemplo, $N = 1000$).
- Resultado:
  - Distribución simulada de $V_1$ y de $L$ (pérdidas).

--

## VaR a partir de la simulación

- Con las pérdidas simuladas $\{L_1, \dots, L_N\}$:
  - Se ordenan de menor a mayor.
  - Se obtiene el **percentil 95** de la distribución de pérdidas.

--

- Valor en Riesgo al 95\,\% estimado por Monte Carlo:
  $$\text{VaR}_{95\%}^{\text{MC}} \approx Q_{0.95}(L_1, L_2, \dots, L_N),$$
  donde $Q_{0.95}$ denota el percentil 95.

--

- Interpretación:
  - Con 95\,\% de confianza, la pérdida en un día no superará $\text{VaR}_{95\%}^{\text{MC}}$.
  - Hay un 5\,\% de probabilidad de incurrir en una pérdida mayor.

--

## Extensión a múltiples días

- Queremos simular el valor del portafolio en un horizonte de $T$ días.
- Para cada día $t = 1, \dots, T$ y escenario $i$:
  - Se genera:
    $$Z_{t,i} \sim \mathcal{N}(0, 1),$$
    $$R_{t,i} = \mu + \sigma \cdot Z_{t,i}.$$

--

- El valor del portafolio al final del día $T$ en el escenario $i$ es:
  $$V_{T,i} = V_0 \cdot \prod_{t=1}^{T} (1 + R_{t,i}).$$
- Se define la pérdida:
  $$L_i = V_0 - V_{T,i}, \quad i = 1, \dots, N.$$

--

- Con $\{L_i\}$ se calculan:
  - Valor esperado de $V_T$.
  - Volatilidad de $V_T$.
  - Valor en Riesgo en el horizonte $T$.

--

## Monte Carlo y crecimiento sostenible

- La empresa fija metas de crecimiento basadas en:
  - Rendimiento sobre el capital ($ROE$).
  - Tasa de reinversión ($RR$).
  - Crecimiento sostenible $g^\*$.

--

- La realidad incorpora:
  - Volatilidad de ventas, márgenes y rendimientos.
  - Incertidumbre sobre los resultados futuros.

--

- La simulación de Monte Carlo permite:
  - Generar trayectorias simuladas de rendimiento y valor.
  - Evaluar en cuántos escenarios:
    - Se alcanza el crecimiento objetivo.
    - Se viola alguna restricción de apalancamiento.
    - Se erosionan significativamente las utilidades o el capital.

---

## 7.3 Taller Simulador

---

## Dudas y Preguntas