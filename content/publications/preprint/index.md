---
title: "An example preprint / working paper"
math: true
authors:
- me
date: "2019-04-07T00:00:00Z"

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication metadata — structured fields used by citation styles and BibTeX export.
# Preprints typically have no formal venue; omit `publication` until the work is accepted.

peer_reviewed: false
open_access: true
license: CC-BY-4.0

funding:
  - funder: "Wellcome Trust"
    grant: "WT-219123/Z/19/Z"

abstract: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum. Sed ac faucibus dolor, scelerisque sollicitudin nisi. Cras purus urna, suscipit quis sapien eu, pulvinar tempor diam. Quisque risus orci, mollis id ante sit amet, gravida egestas nisl. Sed ac tempus magna. Proin in dui enim. Donec condimentum, sem id dapibus fringilla, tellus enim condimentum arcu, nec volutpat est felis vel metus. Vestibulum sit amet erat at nulla eleifend gravida.

# Summary. An optional shortened abstract.
summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
- Large Language Models

featured: true

hugoblox:
  ids:
    arxiv: 1512.04133v1

links:
- type: preprint
  provider: arxiv
  id: 1512.04133v1
- type: code
  url: https://github.com/HugoBlox/kit
- type: slides
  url: https://www.slideshare.net/
- type: dataset
  url: "#"
- type: poster
  url: "#"
- type: source
  url: "#"
- type: video
  url: https://youtube.com
- type: custom
  label: Custom Link
  url: http://example.org

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/s9CC2SKySJM)'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/projects/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- internal-project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
## Introduction

The calibration of monetary policy is particularly challenging at a time of large shocks to inflation 
and output. In 2022, Hungary faced its biggest headline inflation since the start of the century, 
peaking above 20 %. This disruption was global and hit strongly the whole European continent, 
consequence of a general post-pandemic consumption shock and Russia’s agression war against 
Ukraine among other factors. In this context, the Hungarian economy suffered the highest inflation 
among its neighbours through, notably due to its dependence on imports as a small open economy. 
However, this same country achieved a rapid disinflation the year after relative to historical records,
beating most expectations. At the end of 2023, the Magyar Nemzeti Bank (hungarian for The 
Hungarian National Bank or MNB) had successfully brought inflation back below 5 % by adopting 
a tight monetary policy throughout the year. This decision was motivated by a still unstable 
international environment and fears of second-round inflation expectations. In fact, balancing the 
risks of loosening too quickly and inflation taking longer to sustainably return to target against 
those of loosening too slowly with larger costs to output requires careful calibration. The pace and 
extent of future easing depends on the drivers of recent inflation, the state of the economy, and lags 
in the transmission mechanism. 

But this success was not without its consequences. quarterly GDP growth fell in 2024, going several
times in the negative domain. Such an observation may bring back discussion around the notion of 
sacrifice ratio [Okun, 1978] which measures the tradeoff between inflation stabilization and output 
in the short run. This possibility of a tradeoff is particularly interesting in our case as more recent 
studies [Katayama et al., 2019] specify that the longer the duration of the disinflation process, the 
higher the sacrifice ratio. Our work gets much closer to another notion that also emanates in the 
rational-expectations literature : painless disinflation. Commonly attributed to Sargent [Sargent, 
1982], the latter analysed credible regime changes that brought major inflations to an end with 
relatively limited real costs at the start of the 20th century. We actually draw a lot more inspiration 
from the revival of the concept by Golinelli and Rovelli [Golinelli et al., 2002] who explore how in 
a forward-looking small open economy, a monetary-policy rule can affect inflation through 
expectations, aggregate demand, and the exchange rate simultaneously. If these channels reinforce 
each other, the central bank can achieve a substantial reduction in inflation without requiring an 
equally substantial contraction in output. Coincidentally, the setting they chose is also Hungary, but 
in the 1990s.

On the other end, our framework differs completely. We chose to work on an IMF’s Quarterly 
Projection Model (QPM), a semi-structural New Keynesian model, incorporating nominal rigidities 
and rational expectations. While easing inflation pressures suggest that qualitatively the monetary 
policy stance should be loosened over time, the QPM provides a quantitative indication of the 
appropriate pace and extent. The model offers important features useful for monetary policy and 
scenario analysis. Interest rates are endogenous, reacting to changes in economic conditions. The 
projections for monetary policy and the economy are therefore internally consistent. The model is 
also forward-looking. So what matters is the expected paths for interest rates and inflation, not just 
rates today. This model is a tool of the Forecasting and Policy Analysis System (FPAS) of numerous
central banks around the world, tailored and extended to the specific context of each economy.

Thus, this framework allows us to test alternative monetary policy rules in a pseudo-out-of-sample 
forecasting exercise. The objective is to test whether a loosened monetary policy could have 
induced a « softer landing », up to the point if a « painless disinflation » was effectively possible. 
The study of monetary policy in disinflation is quite rare in the literature. In fact, the term 
« disinflation policies » is widely used to describe all decisions taken to recover price stability as 
inflation growing. It is logical as the primary mandate of most central banks is price stability and 
that what matters most is thus, to get back to a stable inflation target as fast as possible, economic 
stability being a non-binding secondary objective. It is also the case of the MNB which has set its 
inflation target to 3% [MNB, 2013]. Our work is rather focused on what the monetary authority 
should do when we are past this spike, in a context where fast disinflation is likely. Although it 
represents an exceptional setting, we consider this work to be an humble contribution to the topic.

Our period of observations ranges from 1999Q1 to 2025Q3. We reject previous periods for lack of 
data availability and quality. Our pseudo-out-of-sample forecasting period starts in 2023Q1 to end 
in 2025Q4. Our baseline conclusions are in line with the literature aforementioned where the 
interest rate and exchange rate channels operate together to push the economy toward fast 
disinflation. The whole process is supported by falling inflation expectations. Our alternative 
model-based forecasts indicates that a lower nominal interest rate could have help inflation fall 
faster, sometimes at a higher output cost. Evaluated through different specifications of a standard 
quadratic loss function, the latter scenario is computed to be preferable. However, the winning 
alternative rules highlight especially that the monetary policy had little effect on disinflation in this 
situation. Moreover, it shows that a standard Taylor rule (as the default one included in the QPM) is 
inefficient to produce an effective monetary policy in this context.

The following content is divided in three sections. Section 1 presents the model, the different block 
of equations, the transmission mechanisms and the calibration. Section 2 gives extented information
about the particular context of Hungary at this period, the expectation about what were to come in 
2023 and further motivation for our design choices. Finally, section 3 compiles our forecasts 
construction and the linked results and evaluation.

## 1. The Model
### 1.1 Canonical Version of the QPM
The basic version of the QPM model (also referred to as the canonical QPM) was proposed by the 
IMF in 2006 [Berg et al., 2006a,b]. It is sometimes considered a New Keynesian model as it blends 
the emphasis on some specific mechanisms. The model is based on the ideas of monopolistic 
competition and features nominal rigidities. Prices are assumed to be sticky, meaning that they don’t
adjust immediately as underlying costs of production change. Output in the short-run is demand
determined. There are indeed some similarities with more sophisticated dynamic stochastic general 
equilibrium (DSGE) models. The equations resemble the log-linearized equations of micro-founded
DSGE models, or in other words, equations that are derived from optimization problems of 
economic agents or firms. Some parts of the model are ad hoc, so they differ from the log-linearized
equations in DSGE models. Such parts are there to help us better approximate the data. Unlike 
DSGE models, equation coefficients in the QPM are not derived from deep structural parameters, 
such as discount factor or risk aversion, but the coefficients are directly calibrated.

The title « canonical » stems from several reasons. The basic QPM assumes an inflation targeting 
central bank, which uses the interest rate as a key policy variable, a flexible exchange rate 
determination and rationnal expectations. The latter means that when agents build their expectations
about macroeconomic variables, like inflation or exchange rate, they would use the model to project
these variables, and use the projections as their best guess or expectations about the inflation and 
exchange rates in the future.

It is a structural model because each key equation has an economic interpretation, but the equations 
are not fully micro-founded. In other words, for every key equation that exists in the model we can 
explain an underlying economic mechanism that this equation approximates. The QPM is a general 
equilibrium model because it describes how the equilibrium is established in the economy as a 
whole, and not only in some particular markets or sectors. The model is stochastic because it allows
for stochastic shocks in its equations.

Finally, this framework does not include all sectors of the economy explicitly (endogenous fiscal 
and financial sectors, export industries…) and specific country features (dollarization, imperfect 
central bank credibility…). This goes beyond the scope of this work. More importantly, it matters to
stress that this model is neither a pure forecasting device (as a VAR would be) nor does it allow 
explicit discussion of optimality (in the absence of microeconomic foundations). It was first and 
foremost created to foster discussions around economic policy through a meaningful and 
transparent model.

The model expresses each variable in terms of its deviation from equilibrium, in other words in 
”gap” terms. This canonical/basic version consists of four blocks, namely: aggregate demand, 
inflation dynamics, exchange rate dynamics, and monetary policy reaction function. Gap terms are 
written with a hat, foreign variables with a star and those measured by their long-run equilibrium a 
bar.
#### Aggregate demand and supply 
The output gap ($\hat{y}_{t}$) is a function of its lag and its expected value, a monetary conditions index ($mci_{t}$), the foreign output gap ($\hat{y}^{*}_{t}$) and aggregate demand shocks ($\epsilon^{y}_{t}$). The mci captures the impact of monetary policy on aggregate demand. It is comprised of a weighted average between the real interest rate gap ($\hat{r}_{t}$) and deviations in the real exchange rate from its trend ($\hat{z}_{t}$). A positive mci indicates tight monetary conditions so $b_{2}$ has a negative sign.

<div>
$$
\begin{centered}
\hat{y}_{t} &= b_{1}\hat{y}_{t-1}-b_{2}mci_{t}+b_{3}\hat{y}^{*}_{t}+\epsilon^{y}_{t} &&(1)\\
mci_{t} &= b_{4}\hat{r}_{t} +(1-b_{4})(-\hat{z}_{t}) &&(2)\\
r_{t} &= i_{t}-E_{t}\left[ \pi_{t+1} \right] &&(3)\\
z_{t} &= s_{t}+p^{*}_{t}-p_{t} &&(4)
\end{centered}
$$
</div>

#### New-keynesian Phillips curve 
Contemporary inflation ($\pi_{t}$) is explained by its value from the previous period, inflation expectations, and real marginal cost ($rmc_{t}$). The latter is determined by the output gap and the real exchange rate gap. In each period, some firms reset their prices to past inflation so $a_{1}$ captures the share of backward-looking firms.
<div>
$$
\begin{}
\pi_{t}=a_{1}\pi_{t-1}+(1-a_{1})E_{t}\left[ \pi_{t+1} \right]+a_{2}rmc_{t}+\epsilon^{\pi}_{t}&&(5)\\
rmc_{t}=a_{3}\hat{y}_{t}+(1-a_{3})\hat{z}_{t}&&(6)
\end{}
$$
</div>

#### Interest rates and the policy rule 

Monetary policy is set according to a standard Taylor rule with a nominal interest rate ($i_{t}$). The monetary authority responds to a deviation of inflation from its target ($\pi^{T}$) and to the deviation of output from its potential level. The central bank is forward-looking and cannot influence today’s inflation because of transmission delay. The smoothing component captures the notion that drastic changes are avoided. The neutral interest rate ($i^{n}_{t}$) is not fixed and represents the level of the interest rate at the economy’s full potential. 
<div>
$$
\begin{aligned}
i_{t}=g_{1}i_{t-1}+(1-g_{1})\left[ i^{n}_{t} + g_{2}\left(E_{t}\left[\pi_{t+4}  \right]-\pi^{T}_{t+4}  \right) + g_{3}\hat{y}_{t} \right]+\epsilon^{i}_{t}&&(7)\\
i^{n}_{t}=\bar{r}_{t}+E_{t}\left[\pi^{4}_{t+N}  \right]&&(8)
\end{aligned}
$$
</div>
#### Uncovered interest rate parity (UIP) and the exchange rate 

The nominal exchange rate ($s_{t}$) is determined by a UIP condition with a backward-looking element to capture stickiness in the adjustment of the exchange rate. A more positive value indicates a depreciation. Growth in the trend real exchange rate ($\bar{z_{t}}$) is a weighted average of its lag and a steady-state value. The exchange rate premium is additional premium investors for holding the currency over and above the returns from the real interest rate differential. The exchange rate is measured at each period (so in quarters) but interest rates are and the premium are expressed in annualized rate so we have to scale them. 
<div>
$$
\begin{aligned}
s_{t}=s^{e}_{t+1} +\frac{i^{*}_{t}-i_{t}+prem_{t}}{4}+\epsilon^{s}_{t}&&(9)\\
where\quad s^{e}_{t+1}=\left( 1-e_{1} \right)E_{t}\left[s_{t+1} \right]+e_{1}\left[s_{t-1}+\frac{2}{4}\left( \pi^{T}_{t}-\bar{\pi}^{*}_{t}+\Delta \bar{z_{t}} \right) \right]&&(10)
\end{aligned}
$$
</div>

### 1.2 Other Specifities
#### Foreign Block 
Unlike in the domestic part of the model, there is no economic structure (or economic 
interpretation) in the foreign block. All variables in the foreign or external block follow simple, autoregressive processes. This is largely based on the assumption that our model simulate a small open economy that cannot influence the world economy. However, the opposite is not true. Foreign variables will affect the domestic economy through all of the above equations. We estimated for each real commodity price, with the gaps relevant for domestic price pressures. The « foreign economy » is assumed to be summarized by variables for the euro area given Hungary’s close trading links with the block. All the foreign equations are reported in the appendix.
#### Transmission Channels
The interest rate and the exchange rate are the two transmission channels. The monetary policy transmission mechanism is summarized by the diagram below : 

![Description of image](trans_channels.png "Figure 1 : Transmission mechanism in the canonical QPM (Source : IMF)")

The transmission starts with the current and expected changes in the policy instrument. In our 
model, this means that the key policy rate affects the current short-term interest rate and its 
expected levels. This, in turn, is transmitted to changes in the longer-term rates, which alters aggregate monetary conditions, aggregate demand and output, and ultimately inflation. This is the interest rate channel. 

Changes in the interest rate also affect the nominal exchange rate, which is assumed to be flexible in the canonical setup. Further, changes in the exchange rate affect inflation directly via the cost of imported factors of production, and indirectly via changes in the relative prices of imported goods vis-à-vis domestic, and the corresponding shifts in aggregate demand between imported and domestic goods. Because of the changes in aggregate demand for domestically produced goods, domestic output and domestic cost pressures change as well, which then affects inflation.

The resolution of the model begins with assigning a value to each structural parameter. When 
parameters are properly calibrated, the model should have a unique stable solution (Blanchard-Kahn condition [Blanchard et al., 1980]). The dedicated software manages the computation of algorithms.
#### Calibration and Parameters Values
As in most QPMs, parameter values are assigned through three approaches: estimation from data 
for available series, calibration from previous studies, and expert judgment. For technical reasons, we relied only on the latter and didn’t perform any estimation ourselves.

Our choice of parameter values follows the initial calibration described by the IMF in their own Hungary QPM [Jackson, 2024]. Although they chose the values corresponding to a period before 2020, their estimated values using Bayesian techniques on their full sample of interest (2006-2024Q1) as a cross-check give very close values. You may refer to this paper for more details. In any case, the model is calibrated to produce plausible impulse responses that also correspond with those from the literature (see section 1.3). 

Steady-state parmeter values are set according to official statements of the MNB, ECB and the IMF or follow the default IMF recommendation. Standard deviations of shocks were calculated using historical averages with respect to the dedicated QPM procedure. More details on the matter are available in the appendix.
#### Data
Data was sourced from various institutional sources. The observation period starts in 1999 on a 
quarterly basis. All data was seasonally adjusted. More information in the appendix.
### 1.3 Impulse Response Functions (IRFs)
The model is calibrated to be broadly similar to previous trusted external estimates of other 
macroeconomic models dedicated to the Hungarian economy [Jackson, 2024 ; Szilágyi et al., 2013].
The series of graphs below describe the response of key variables to a 1.0 percentage point shock.

All IRFs can be found in the Appendix. A 1pp temporary but persistent increase in the policy rate reduces the level of the output gap by almost 0.2 percent and reduces inflation by a peak of close to 0.4pp (Figure 2). This implies a low sacrifice ratio. YoY CPI inflation also falls quite quickly : the peak impact is reached under a year and comes back to normal after two years. Both these features reflect the importance of the exchange rate channel in Hungary, consistent with the findings of the aforementionned papers.
![Description of image](IRF_comparison.png "Figure 2 : IRFs of Szilágyi et al. model (left) VS. our QPM (right) under a monetary policy shock")

The response to a cost-push shock explains further the functioning of our model (Figure 3). The 
increase in inflation triggers an immediate response from the central bank, causing the real interest rate to become substantially more restrictive. At the same time, the exchange rate depreciates and continues to tighten the monetary conditions. The resulting contraction in aggregate demand generates a temporary negative output gap of -0.015pp. The output cost is relatively small in this case. It does not conform to a textbook « painless » reaction to an inflationary scenario but it remains low-cost and doesn’t go completely against it either. 

![Description of image](IRF_square.png "Figure 3 : IRFs of our QPM under a cost-push shock")

## 2. Context
### 2.1 The Post-Covid Inflation
The context regarding Hungary’s recent disinflation episode was not simply the mechanical reversal of the 2022 inflation shock, but rather the gradual unwinding of several mutually reinforcing sources of inflationary pressure. One side of the post-Covid dynamics can be explained by foreign shocks have played an important role in disrupting price stability, encompassing both demand shocks, such as deferred post-pandemic global consumption, and supply shocks, including disruptions to global value chains and the impact of Russia’s war of aggression against Ukraine. 
This side of the story is not only acknowledged in the literature for Hungary [Botos, 2023 ; Sipiczki et al., 2024] but also for all Central Europpean countries [Šestořád et al., 2024]. On the other side, the domestic inflationary drivers for 2022 can be summarized as traditional energy price increases, wage increases, retailer responses to the price cap regime, credit expansion consumption, and the effects of a drought year. The agricultural situation is specifically to be noted as food price inflation was the highest in Hungary compared to the rest of Europe while the the country’s food industry experienced a sharp decline in the performance. This decline is the consequence of the dependence of the sector on imports whom also got more expensive through an extended period of of the currency. According to Cohn-Bech et al. [2023], during 2022, the forint depreciated against the US dollar by more than most emerging markets currencies globally. Moreover, frequent disputes with the European Union and withholding of more than 10 billion euros added to risk perceptions and intensified pressure on the exchange rate[^1]. [^1]: As of the time of writing this work (May 2026), the latter issue is yet to be resolved.

The MNB responded with a strong demonstration of the role of monetary policy as a stabilizing 
force. Among the first in Europe to act, the MNB signaled heightened inflationary risks in early 2021 and promptly began raising interest rates. To restore price stability, the MNB undertook the largest cumulative rate hikes among EU countries, further underscoring the central role of monetary policy in counteracting inflation. Although the intervention was strong, it is to be noted that some observers view it as late, as the ECB took action in 2022Q2 whereas the MNB did so only in September of the same year. Nevertheless, this decisive policy led to inflation peaking in early 2023, followed by a period of rapid disinflation.  

The Kalman filter decomposition of qoq inflation in our QPM broadly supports this narrative 
(Figure 4). The exceptionally large inflation episode in 2022 is initially dominated by shock and real-exchange-rate components, consistent with the above statements.

![Description of image](kalman.png "Figure 4 : QPM’s Kalman filter decomposition of quarter-on-quarter inflation")

### 2.2 A Situation of Disinflation
Our period of study begins at the peak of the inflation episode. A few months into 2023, the general sentiment was in favor of an overturn of past-year’s dynamics. First, it is to be seen that the forint gradually strengthened against the euro since late 2022, showing a solid 3.5% appreciation between the two quarters. It is also partly owing to positive developments regarding the EU funding as negociations were announced to start over again. External shocks have faltered with a slowdown of global economic activity and decreasing in energy prices and global food base material prices. Internally, the situation is much stable too. The tight monetary policy is proving to influence the monetary conditions allowing them to exert their disinflationary impact in a widening range. At the same time, the decline in domestic demand narrows enterprises’ room for manoeuvre in pricing. The MNB’s quarterly inflation reports are particularly insightful on the matter. From March 2023, the central bank announces that « the consumer price index in Hungary is expected to decline moderately in the coming months, followed by an acceleration in the disinflationary process in the second half of the year » and that « the consumer price index is expected to return to the central bank tolerance band in 2024 » [MNB, 2023]. The projection from the Q1 report displays a corresponding sharp fall in inflation (Figure 5). Despite not finding access to the exaxt figures, it is strikingly close to our own model’s forecast, reinforcing the relevance of our design choices and calibration.

![Description of image](forecast_vs.png "Figure 5 : Year-on-year inflation forecast of the MNB (left) VS. our QPM (right)")

The large tolerance bands characterise nonetheless great uncertainty regarding the outlook. In our projection, the tolerance is represented by 30 %, 60 % and 90 % probability bands. However, it is far from enough to offset the base disinflation scenario. In conclusion, most indicators pointed to a clear return to normal metrics in a fast manner, the actual development proved this manner to be historically short. In Europe, the sentiment was shared with more moderation. In a speech from March 2023, the president of the ECB Christine Lagarde starts the speech by announcing that « headline inflation is likely to decline steeply this year » while also acknowledging « underlying inflation dynamics remain strong » [ECB, 2023].
## 3. Forecast
We run our model through a pseudo-oos forecast exercise. The objective is to test the sensitivity of our model-dictated monetary policy by modifying the parameters value of the interest-rate rule equation (namely $g_{1-3}$). We evaluate our forecasts with a standard quadratic loss function.
### 3.1 In-sample Simulations
In order to assess the ability of our QPM to capture the salient properties of available data, we perform an in-sample simulation exercise. More precisely, we run recursive one- to eight-quarter ahead forecasts for the period 1999Q1-2023Q1, conditioning on the full sample estimates for the trajectories of foreign variables, output trend, real exchange rate trend, inflation target. As compared to an actual real-time forecasting exercise, we don’t consider any near-term forecasts or expert judgments. The results for a subset of observed variables are presented in the figure below (Figure 6). The recursive in-sample model simulations are represented with various colors, while actual data is displayed in black lines. See the appendix for the full set. 

![Description of image](in_sample.png "Figure 6 : In-sample forecasts and actual data (black)")

For most variables, the model matches actual data reasonably well. Despite occasional visible 
forecast errors for all variables, to a large extent, the QPM manages to capture the relevant turning points in most indicators. Some of the measurements suffer for under- and/or overshooting in periods of high volatility. It is expected as the standard QPM is noted to not be particularly performant in case of an exceptional crisis. For example, the output gap in-sample simulations shows a strong under-evaluation of the pandemic crisis and the model consistently  undershoot the 2022 inflation spike. It also made it so that tuning some of the parameters and/or steady-state values did not substantially improve the model’s accuracy while straying us further away from previous experts judgments and calibration. Hence, we decided to keep our initial calibration untouched.
### 3.2 The Policy Loss Function
To evaluate alternative monetary policy rules, we use a quadratic loss function that captures the central bank’s trade-offs between inflation stabilization, output stabilization, and interest-rate smoothing. The specification is inspired by the conclusions of a report by the IMF Research Department [Debortoli et al., 2019] that motivates the addition of economic activity’s measurements when designing loss functions for central banks. Such factors are driven by the will to better approximate social welfare, especially in our case where the strong disinflation led to a sharp detrioration in GDP growth. The period loss is given by
</div>
$$
\begin{aligned}
L_{t}= \omega_{\pi}\left( \frac{\pi_{t}-\pi^{*}_{t}}{\sigma_{\pi}} \right)^{2}+\omega_{y}\left( \frac{y^{gap}_{t}}{\sigma_{y}} \right)^{2}+\omega_{\Delta i}\left(\frac{\Delta i_{t}}{\sigma_{\Delta i}}  \right)^{2}&&(11)
\end{aligned}
$$
</div>
where inflation deviations, the output gap, and changes in the policy rate are normalized by their respective historical standard deviations σ. This normalization puts the three components on comparable scales, while the weights determine their relative importance in the policymaker’s objective. Future losses are discounted using a quarterly discount factor β. Considering the horizon length, we fix β = 0.95. Thus, the total loss over the policy horizon is :
</div>
$$
\begin{aligned}
L = \sum_{t=0}^{T-1}\beta^{t}L_{t}&&(12)
\end{aligned}
$$
</div>

We run our model on two sets of weights level (Table 1). The first set puts more emphasis on 
inflation, while the second one allows for an equal influence of both price stability and economic activity. A third set giving more importance to the output gap was not selected as the MNB Founding Act still explicitly mentions that its primary objective shall be to achieve and maintain price stability. This third set would have been highly likely to be unfeasible. On the other side, putting an stronger weight on price stability is contrary to our topic, and so, not relevant.


> [!NOTE]
> Create your slides in Markdown - click the *Slides* button to check out the example.

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/).
