---
title: "An example preprint / working paper"
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
The output gap (ŷt) is a function of its lag and its expected value, a monetary conditions index 
(𝑚𝑐𝑖t), the foreign output gap (ŷt∗) and aggregate demand shocks (𝜖ty). The mci captures the impact 
of monetary policy on aggregate demand. It is comprised of a weighted average between the real 
interest rate gap (𝑟̂t) and deviations in the real exchange rate from its trend (𝑧̂t). A positive mci 
indicates tight monetary conditions so b2 has a negative sign.

> [!NOTE]
> Create your slides in Markdown - click the *Slides* button to check out the example.

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/).
