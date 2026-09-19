---
title: 'An example conference paper'
math: true
# Authors
# If you created a profile for a user (e.g. the default `me` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - me
  - Robert Ford

# Author notes (optional)
author_notes:
  - 'Equal contribution'
  - 'Equal contribution'

date: '2013-07-01T00:00:00Z'

# Schedule page publish date (NOT publication's date).
publishDate: '2017-01-01T00:00:00Z'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['paper-conference']

# Publication metadata — structured fields used by citation styles and BibTeX export.
publication:
  name: "Proceedings of the HugoBlox Kit Conference"
  short_name: "ICW"

peer_reviewed: true
open_access: true
license: CC-BY-4.0

# Awards, honors, and recognitions. Surfaced as badges on the page and in listings.
awards:
  - name: "Best Paper Award"
    level: winner
    note: "Top 5 of 8000 submissions"
  - name: "Oral Presentation"
    level: selected

# Funders and grants. Required by many funders for compliance reporting.
funding:
  - funder: "National Science Foundation"
    grant: "NSF-2401234"
  - funder: "European Research Council"
    grant: "ERC-StG-101234"

abstract: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum. Sed ac faucibus dolor, scelerisque sollicitudin nisi. Cras purus urna, suscipit quis sapien eu, pulvinar tempor diam. Quisque risus orci, mollis id ante sit amet, gravida egestas nisl. Sed ac tempus magna. Proin in dui enim. Donec condimentum, sem id dapibus fringilla, tellus enim condimentum arcu, nec volutpat est felis vel metus. Vestibulum sit amet erat at nulla eleifend gravida.

# Summary. An optional shortened abstract.
summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis posuere tellus ac convallis placerat. Proin tincidunt magna sed ex sollicitudin condimentum.

tags:
  - Large Language Models

# Display this page in the Featured widget?
featured: true

# Standard identifiers for auto-linking
hugoblox:
  ids:
    doi: 10.5555/123456

# Custom links
links:
  - type: pdf
    url: ""
  - type: code
    url: https://github.com/HugoBlox/kit
  - type: dataset
    url: https://github.com/HugoBlox/kit
  - type: slides
    url: https://www.slideshare.net/
  - type: source
    url: https://github.com/HugoBlox/kit
  - type: video
    url: https://youtube.com

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/projects/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
  - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
## Introduction
The following work analyses the performance of some predictive volatility models built to exploit high frequency data. This is carried out through the development of mainly GARCH-type models but we will sometimes extend the class of models to some other specifications such as CAViaR models. Our object of research is the Oracle Corporation stock. Oracle is an American software company founded in 1977 by Larry Ellison. Starting with a database management product with notable clients among which the CIA, it has now expanded in various branches in the tech industry among which supply chain-, capital-, sales-, human resources-management through its cloud-based software services. The company’s focus on cloud and license business infrastructure technologies put it at the heart of the recent AI-boom in the US. As such, its market capitalization today is evaluated around 420 billion dollars which is comparable to the likes of Palantir, another major American AI company. Oracle stock price is frequently subject to large volatility movements, mostly in relation to major news regarding the company or the US tech sector.

This work is divided in two sections. Firstly, we perform a volatility analysis of the stock returns estimating a wide array of models on the data. The latter is then evaluated through different metrics to observe their sensibility to extreme risks. Secondly, we perform a forecasting exercise in the form of a pseudo-out-of-sample experiment on the last few months of observations. We focus there on a more restricted set of models for the sake of explanatory power and comparability. Again, the models are evaluated by their accuracy, their actual predictive ability and how they behaved in comparison to the realized series. Our period of analysis spans from January 1, 2000 to August 9, 2026. Previous observations were also available but excluded due to extremely noisy returns in 
those early years.
## 1 Volatility Analysis
The Oracle daily stock prices follow the classic story of the tech companies that are still today successful. Historically, the company suffered for its financial mismanagement at the end of the 1990s, aggravated by the Internet Bubble at the start of the century. But Oracle survived and solidified its positions in the tech sector by acquiring key companies such as Hyperion Solutions in 2007, Sun Microsystems (Java, MySQL, LibreOffice…) in 2010 or even Taleo in 2012. From 2021, the steady growth exploded exponentially in relation to bigger acquisitions (ex: Cerner…), exceptional financial results and the implication of the different activities in the AI ecosystem. The all-time high is reached in September 2025 when Oracle announced being part of Project Stargate, which is a 500 billion dollar investment plan in AI infrastructure copiloted with OpenAI and Softbank with the support of the Trump administration. However, concerns and missed expectations surrounding the project subsequently contributed to a sharp decline in the stock price within less 
than a year.
![image](orcl_fig_1.png "Figure 1 : ORCL Daily Prices")

The log-returns displays that very volatile tendency at the start and end of our period of analysis. Nonetheless, we observe the traditional mean-reverting property of the returns (figure 2a) as well assome signs of leverage effect as the squared returns as high-volatility is dominated by the period where Oracle found itself in the most difficult positions (figure 2b).

![image](orcl_fig_2ab.png "Figure 2a : ORCL Daily Log-returns      Figure 2b : ORCL Daily Squared Log-returns")

Our observation of stylized facts is not yet finished. Raw returns show no clear pattern of autocorrelation as shown by the ACF (figure 3a) consistently with the idea that they are difficult to predict from their own past values. On the other hand, the ACF of squared returns (figure 3b) displays a strong memory. Not only does this imply the volatility is persistent as the autocorrelation slowly decays but it also clusters as it remains high above our 95 % confidence dotted box.

![image](orcl_fig_3ab.png.pdf " Figure 3a : ORCL ACF of Daily Returns
           Figure 3b : ORCL ACF of Daily Squared-returns")

This motivates empirically the estimation by GARCH-type models. Below is a summary table of the results (table 1) :

| |$\mu$ | $\omega$    | $\alpha$ |$\beta$ |$\nu$|$\gamma$|
| -------------- | ---------|------ | -----|--------|---|---|
| GARCH-N        | 0.00051  | ~0  | 0.101 | 0.884 | | |
| GARCH-t        | 0.00078 | ~0   |0.077 | 0.922 | 4.1 | |
| EGARCH         | 0.00012 | -0.1417  |-0.037 | 0.980 | |0.015|
| GJR-GARCH-N    | 0.00034 | ~0  | 0.033 | 0.0912 | |0.08|
Table 1 : Parameter estimates of GARCH models for daily ORCL returns

All of the estimated models highlight a strong volatility persistence in ORCL returns ($\alpha + \beta$ very close to 1 each time) and thus confirms volatility clustering. Our GARCH-t specification allows us to evaluate the shape of the innovation distribution outside of the standard normal distribution. Here, our $\nu$ is relatively low (4.1) which is a significant sign of excess kurtosis and fat tails. Finally the $\gamma$ estimates are both positive and important. GJR-GARCH and EGARCH allow for an asymmetric innovation distribution (skewness) which shows here to underline a leverage effect : negative shocks affect more volatility than positive ones of the same magnitude. Overall, the main volatility dynamics are robust across model specifications, while differences between the models become more apparent during periods of extreme market movements at the start and end of our period of analysis (figure 4).


![image](orcl_fig_4.png "Figure 4 : Conditional Volatility of the four models")

In contrast, the GJR-GARCH model displays somewhat larger responses to several individual shocks, consistent with its ability to capture asymmetric responses in comparison to GARCH-N and-t. 

Next, we must manage the possibility of extreme risks through the computation of the 2.5 % VaR and its Expected Shortfall. We estimate and evaluate again multiple models, using the whole sample
(table 2).

| | $\omega$ | $\alpha$ |$\beta_{1}$ |$\beta_{2}$ |$\beta_{3}$ |$\beta_{4}$ |$\nu$|$\gamma_{1}$|$\gamma_{2}$|$\gamma_{3}$|a|b|
| -------------- | ---|--|----|---|--- | --|---|--|---|---|---|---|
| GARCH-N        | 0.114| 0.102  | 0.883 | | | | | | | | | |
| GJR-GARCH-t    | 0.039 | 0.039  |0.921 | | | | | | | | | |
| CARE-AS        | | |-0.171 | -0.287 |-0.290 |0.854| |1.098 |0.132|0.857| | | 
| SAV-CARE       | | | -0.165 | -0.267 |0.863 | | |1.176|0.112|-0.527| | |
| GAS-1F         | | | 0.989 |  | | | |0.006 | | | -4.140|-5.701 |
| HistSim (250d) |(No Parameters) |
Table 2 : Parameter estimates of different models to model VaR and ES

The estimated parameters generally exhibit the expected signs and admissible ranges. The GARCH and GJR-GARCH estimates imply positive volatility responses and high persistence, while the positive GJR-GARCH asymmetry parameter indicates a leverage effect. These results remain consistent with the previous estimation. The CARE and GAS specifications also produce persistent VaR/ES dynamics with negative tail-risk levels. For CARE-AS the positive value of $\beta_{4}$ indicates substantial persistence in the VaR process and the negative values for $\beta_{2}$ mean larger returns push the VaR in the negative tail for CARE-AS and SAV-CARE. For the GAS-1F, the very high $\beta$ makes it so that it remembers its previous risk/volatility state for a long time. Thus, the estimated VaR and ES don't change abruptly from one day to the next unless there is sufficiently strong new information in the returns. 

Plotting against the realized returns help us gain substantial insights about how each model behaves against extreme risks (figure 5a and 5b). Historical Simulation is a non-parametric method that relies only on past observations (here 250-days rolling window). It underestimates consistently VaR (and subsequently ES) at any large negative spikes and takes a long time to recover. Aside from thisspecial case, all models react pretty similarly in calmer times. They also react accordingly against more hefty movements but it is on the scale of the reactions where divergence shows to be the strongest. CAViaR-type models (AS-CAViaR and SAV-CAViaR) tend to respond dynamically to recent observations as they directly model our two targets. This adaptation scheme helps them improving over time as although they were underestimating risks at the start of the period, they anticipated correctly the numerous spikes from 2020 onward. Also, they remain very accurate in calmer times in both ES and VaR. Surprisingly, on VaR estimates, the GAS1F specification takes a longer time (as anticipated) to recover from negative shocks. It is as unfortunate as the ES computations were very consistent. GARCH-N displays relevant performance though underestimates regularly most of the risks on the more hefty periods of analysis. GJR-GARCH-t tends to give relatively conservative estimates during extreme market conditions. This is especially visible in the ES plot, where it occasionally produces substantially more negative ES forecasts. Hence, it would be the more appropriate model to follow in volatile times in reason of its exaggerated cautiousness. In calmer times, one of the CAViaR specifications is suitable enough. 

![image](orcl_fig_5a.png "Figure 5a : VaR estimates of multiple models against realized return")
![image](orcl_fig_5b.png "Figure 5b : ES estimates of multiple models against realized return")

It is to be noted though that visual appreciation is not sufficient to deliver a proper evaluation of which model perfoms actually better. One way to address this situation is to compute how many times our VaR forecast was violated (e.g. the Hit ratio). For a good model, it should only happen as much as the level we defined our VaR on. Hence, we retrieved the computations of the Hit ratios for each model (table 3).

|GARCH-N|GJR-GARCH-t |HistSim | SAV-CAViaR |AS-CAViaR|GAS1F|
| -------------- | ---------|------ | -----|--------|---|
| .02572  | .02647  | .02901  | .02422 | .02437 |.02422 | 
Table 3 : Hit ratio for VaR 2.5%

The closest the ratio is to the defined model (here 2.5%), the better it is. SAV-CAViaR and GAS-1F arrive first ex-aequo closely followed by AS-CAViaR. Unsurprisingly, the over-pessimistic GJR-GARCH-t arrives second-to-last and HistSim dead last.

## 2 Forecasting exercise
The following part handles a one-step-ahead forecasting exercise of the conditional volatility of ORCL.

The first four models that we estimated are all valid candidate models for this task because they are specifically designed to model time-varying volatility and volatility clustering, which are important characteristics of financial returns. As we’ve previously tested their behaviour on our stock, we will 
focus our efforts on those specifically. One thing to note is that EGARCH is a bit more difficult because of its non-linear structure (EGARCH models the logarithm of the conditional variance to 
circumvent the sign restrictions of the parameters). It can make the optimization procedure more tedious and the interpretation of the parameters less direct. Thus, before diving in the results, let’s observe how we obtain one-step forecast for the GARCH-N, GARCH-t and GJR-GARCH-t (we exclude EGARCH). The standard equation for a GARCH(1,1) is :











> [!NOTE]
> Click the _Cite_ button above to demo the feature to enable visitors to import publication metadata into their reference management software.

> [!NOTE]
> Create your slides in Markdown - click the _Slides_ button to check out the example.

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/).
