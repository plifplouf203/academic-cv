---
title: 'An example conference paper'

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
The following work analyses the performance of some predictive volatility models built to exploit 
high frequency data. This is carried out through the development of mainly GARCH-type models 
but we will sometimes extend the class of models to some other specifications such as CAViaR 
models. Our object of research is the Oracle Corporation stock. Oracle is an American software 
company founded in 1977 by Larry Ellison. Starting with a database management product with 
notable clients among which the CIA, it has now expanded in various branches in the tech industry 
among which supply chain-, capital-, sales-, human resources-management through its cloud-based 
software services. The company’s focus on cloud and license business infrastructure technologies 
put it at the heart of the recent AI-boom in the US. As such, its market capitalization today is 
evaluated around 420 billion dollars which is comparable to the likes of Palantir, another major 
American AI company. Oracle stock price is frequently subject to large volatility movements, 
mostly in relation to major news regarding the company or the US tech sector.

This work is divided in two sections. Firstly, we perform a volatility analysis of the stock returns 
estimating a wide array of models on the data. The latter is then evaluated through different metrics 
to observe their sensibility to extreme risks. Secondly, we perform a forecasting exercise in the form
of a pseudo-out-of-sample experiment on the last few months of observations. We focus there on a 
more restricted set of models for the sake of explanatory power and comparability. Again, the 
models are evaluated by their accuracy, their actual predictive ability and how they behaved in 
comparison to the realized series. Our period of analysis spans from January 1, 2000 to August 9, 
2026. Previous observations were also available but excluded due to extremely noisy returns in 
those early years.
## 1 Volatility Analysis
The Oracle daily stock prices follow the classic story of the tech companies that are still today 
successful. Historically, the company suffered for its financial mismanagement at the end of the 
1990s, aggravated by the Internet Bubble at the start of the century. But Oracle survived and 
solidified its positions in the tech sector by acquiring key companies such as Hyperion Solutions in 
2007, Sun Microsystems (Java, MySQL, LibreOffice…) in 2010 or even Taleo in 2012. From 2021,
the steady growth exploded exponentially in relation to bigger acquisitions (ex: Cerner…), 
exceptional financial results and the implication of the different activities in the AI ecosystem. The 
all-time high is reached in September 2025 when Oracle announced being part of Project Stargate, 
which is a 500 billion dollar investment plan in AI infrastructure copiloted with OpenAI and 
Softbank with the support of the Trump administration. However, concerns and missed expectations
surrounding the project subsequently contributed to a sharp decline in the stock price within less 
than a year.
[!image](ORCL_Prices_Daily.pdf "Figure 1 : ORCL Daily Prices")

The log-returns displays that very volatile tendency at the start and end of our period of analysis. 
Nonetheless, we observe the traditional mean-reverting property of the returns (figure 2a) as well as
some signs of leverage effect as the squared returns as high-volatility is dominated by the period 
where Oracle found itself in the most difficult positions (figure 2b).

[!image](ORCL_Log_Returns_Daily.pdf "Figure 2a : ORCL Daily Log-returns")
[!image](ORCL_Squared_Log_Returns_Daily.pdf "Figure 2b : ORCL Daily Squared Log-returns")

Our observation of stylized facts is not yet finished. Raw returns show no clear pattern of 
autocorrelation as shown by the ACF (figure 3a) consistently with the idea that they are difficult to 
predict from their own past values. On the other hand, the ACF of squared returns (figure 3b) 
displays a strong memory. Not only does this imply the volatility is persistent as the autocorrelation 
slowly decays but it also clusters as it remains high above our 95 % confidence dotted box.

[!image](ORCL_Log_Returns_Daily.pdf "Figure 2a : ORCL Daily Log-returns")
[!image](ORCL_Squared_Log_Returns_Daily.pdf "Figure 2b : ORCL Daily Squared Log-returns")






> [!NOTE]
> Click the _Cite_ button above to demo the feature to enable visitors to import publication metadata into their reference management software.

> [!NOTE]
> Create your slides in Markdown - click the _Slides_ button to check out the example.

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/).
