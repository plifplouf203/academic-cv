title: 'Modeling and Forecasting Volatility: Empirical Evidence from Oracle'

authors:

me

date: '2026-08-22T00:00:00Z'

publishDate: '2026-08-22T00:00:00Z'

abstract: >
An empirical study of volatility modeling and forecasting using daily Oracle
Corporation stock returns from 2000 to 2026. The analysis compares GARCH-type,
CAViaR, and GAS models, examining volatility clustering, leverage effects,
Value-at-Risk, Expected Shortfall, and out-of-sample forecasting performance.

summary: >
An empirical study of Oracle stock volatility using GARCH, CAViaR, and GAS
models, with a focus on volatility clustering, tail risk, and out-of-sample
forecasting.

tags:

Financial Econometrics

Volatility Forecasting

GARCH

Value-at-Risk

Expected Shortfall

CAViaR

Time Series

Oracle

featured: true

Custom links
Add the PDF, code, or data links here if you decide to make them available.

links: []

Featured image
Add featured.jpg or featured.png to this post's folder.

image:
caption: 'Modeling and forecasting volatility in Oracle Corporation stock'
focal_point: ''
preview_only: false

Modeling and Forecasting Volatility

Empirical Evidence from Oracle Corporation

University of Tübingen · August 2026

Overview

This study investigates the modeling and forecasting of financial volatility using daily returns of Oracle Corporation (ORCL). The analysis covers the period from January 1, 2000 to August 9, 2026, with earlier observations excluded because of particularly noisy returns.

The analysis has two main objectives. First, I examine the dynamics of Oracle's stock-return volatility using a range of GARCH-type models and models designed specifically for tail-risk estimation. Second, I conduct a pseudo-out-of-sample forecasting exercise to evaluate how well selected volatility models predict future realized volatility.

The analysis focuses on three broad questions:

How persistent is volatility in Oracle's stock returns?

How do different models behave when confronted with extreme market movements?

How accurately can GARCH-type models forecast volatility outside the estimation sample?

1. Volatility Analysis
Stylized facts

Oracle's daily returns exhibit several characteristics commonly observed in financial markets.

The raw returns show relatively little systematic autocorrelation, making them difficult to predict from their own history. The squared returns, however, display substantial autocorrelation and slowly declining dependence.

This provides evidence of two important characteristics of financial volatility: persistence and volatility clustering.

Periods of high volatility tend to be followed by further periods of high volatility, while relatively calm periods tend to persist as well. These features motivate the use of conditional volatility models such as GARCH.

GARCH-type models

I estimate four specifications:

GARCH-N

GARCH-t

EGARCH

GJR-GARCH-N

Across the models, volatility persistence is consistently high, with the persistence parameters close to one.

The GARCH-t model additionally allows for a Student-t innovation distribution. Its estimated degrees-of-freedom parameter is relatively low, indicating substantial tail thickness compared with a Gaussian distribution.

The asymmetric models also provide evidence of a leverage effect: negative shocks tend to have a larger impact on subsequent volatility than positive shocks of similar magnitude.

Overall, the main volatility dynamics are robust across specifications, although the models diverge more substantially during periods of extreme market movements.

Value-at-Risk and Expected Shortfall

I then extend the analysis to tail-risk measures, focusing on 2.5% Value-at-Risk (VaR) and Expected Shortfall (ES).

The models considered are:

GARCH-N

GJR-GARCH-t

AS-CAViaR

SAV-CAViaR

GAS-1F

Historical Simulation

The different specifications react differently to large negative observations.

Historical Simulation, using a rolling 250-day window, tends to respond slowly to sudden changes in the distribution of returns. CAViaR models, by contrast, directly model the evolution of the conditional quantile and therefore adapt more dynamically to recent observations.

The GJR-GARCH-t model produces relatively conservative estimates during periods of extreme volatility. The CAViaR and GAS specifications provide competitive VaR coverage according to the hit-ratio analysis.

For the 2.5% VaR, the estimated hit ratios are close to the target coverage level for the CAViaR and GAS specifications, while Historical Simulation produces more violations over the sample.

2. Forecasting Volatility

The second part of the analysis focuses on one-step-ahead forecasts of Oracle's conditional volatility.

Three models are considered:

GARCH-N

GARCH-t

GJR-GARCH-N

The forecasts are generated over the final 200 observations of the sample, approximately from October 20, 2025 to August 7, 2026.

Two estimation schemes are compared.

Fixed versus expanding windows

Under the fixed-window approach, the model is estimated once using the initial in-sample observations. The estimated parameters are then kept constant while forecasts are generated recursively.

Under the expanding-window approach, the model is re-estimated as each new observation becomes available.

The resulting forecasts are remarkably similar under the two approaches. The expanding-window scheme produces slightly different loss values, but the overall differences are relatively small.

A particularly volatile period

The out-of-sample period contains a particularly large episode of volatility during June 2026.

The highest volatility forecasts are concentrated between June 3 and June 16, around Oracle's FY2026 fourth-quarter earnings announcement.

The models correctly identify the clustering of volatility around this period, but they substantially underestimate some of the largest realized movements.

This illustrates an important limitation of traditional GARCH models: they are highly dependent on information contained in past returns and therefore have difficulty anticipating exceptionally large news-driven shocks.

3. Comparing Forecast Accuracy

To evaluate forecast performance more formally, I use two loss functions:

Mean Squared Error (MSE)

QLIKE

MSE gives a conventional measure of forecast error, while QLIKE is specifically designed for volatility forecasting and places greater emphasis on certain forms of underestimation.

The results are very similar across the two estimation schemes.

For MSE, GARCH-N produces the lowest loss in the evaluated sample. For QLIKE, GARCH-t produces the lowest loss.

This illustrates an important point: the apparent performance of a volatility model can depend on how forecast accuracy is measured.

Diebold-Mariano tests

To investigate whether the differences are statistically meaningful, I perform pairwise Diebold-Mariano tests.

The results are consistent across both fixed-window and expanding-window estimation.

The null hypothesis of equal predictive accuracy is rejected when comparing GARCH-t with GARCH-N and GJR-GARCH-N under both MSE and QLIKE. In contrast, the difference between GARCH-N and GJR-GARCH-N is not statistically significant.

Thus, although the loss functions produce different rankings of the models, the statistical tests provide evidence that the forecasting performance of GARCH-t differs from that of the other two specifications over this particular evaluation period.

4. One-Step versus 21-Step Forecasts

Finally, I compare one-step-ahead forecasts with 21-step-ahead forecasts using GARCH-N.

A 21-step horizon corresponds approximately to one trading month.

As expected, the multi-step forecasts are smoother than the one-step forecasts. One-step forecasts react more directly to recent shocks, while forecasts further into the future tend toward the model's long-run variance.

Interestingly, the 21-step forecasts achieve lower MSE and QLIKE losses over the evaluation period.

This result is somewhat counterintuitive because one might expect forecasts using more recent information to perform better.

There are several possible explanations.

First, the particular evaluation period is unusually volatile, meaning that recent shocks may not provide a reliable guide to future volatility. Second, the multi-step forecasts are smoother and therefore may benefit from the way forecast errors are measured. Finally, realized squared returns are themselves a noisy proxy for the latent conditional variance.

The result should therefore not be interpreted as evidence that long-horizon forecasts are generally superior. Repeating the experiment over several different evaluation periods would be necessary to establish whether the finding generalizes.

Conclusion

This study examined the modeling and forecasting of Oracle Corporation's stock volatility using several classes of financial econometric models.

The empirical analysis confirms several well-known characteristics of financial returns. Raw returns display relatively little autocorrelation, while squared returns exhibit strong persistence and volatility clustering. The estimated GARCH-type models also indicate high volatility persistence, while asymmetric specifications provide evidence of a leverage effect. The Student-t specification points toward fat-tailed innovations.

The tail-risk analysis shows that different models behave differently during extreme market movements. CAViaR and GAS models provide dynamic estimates of VaR and Expected Shortfall, while the GJR-GARCH-t specification tends to produce more conservative estimates during periods of high volatility.

The out-of-sample forecasting exercise shows that GARCH-type models can capture volatility clustering but have difficulty predicting exceptionally large, news-driven movements. Forecast performance also depends on the choice of loss function: GARCH-N performs best according to MSE in the evaluated sample, whereas GARCH-t produces the lowest QLIKE loss.

Finally, the 21-step-ahead forecasts achieve lower losses than the corresponding one-step-ahead forecasts over the selected evaluation period. This result is statistically significant according to the Diebold-Mariano tests, but should be interpreted cautiously given the relatively short and unusually volatile sample and the noisy nature of squared returns as a volatility proxy.

Overall, the results illustrate both the usefulness and the limitations of GARCH-type models for financial volatility analysis. They provide a useful framework for describing persistent volatility dynamics, but their backward-looking nature makes forecasting sudden, extreme market movements particularly challenging.

Reference
Patton, A. (2011). Volatility Forecast Comparison Using Imperfect Volatility Proxies. Journal of Econometrics, 160, 246–256.the _Slides_ button to check out the example.

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/).
