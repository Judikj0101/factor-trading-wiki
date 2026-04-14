---
title: "A five-factor asset pricing model"
source: "https://www.sciencedirect.com/science/article/abs/pii/S0304405X14002323"
author:
  - "[[Eugene F. Fama a]]"
  - "[[Kenneth R. French b]]"
published: 2014-05-12
created: 2026-04-14
description: "A five-factor model directed at capturing the size, value, profitability, and investment patterns in average stock returns performs better than the th…"
tags:
  - "clippings"
---
[![Elsevier](https://www.sciencedirect.com/eu-west-1/prod/5897b70532afb1a41b09ce1839f0fc8b7b976c1f/image/elsevier-non-solus.svg)](https://www.sciencedirect.com/journal/journal-of-financial-economics "Go to Journal of Financial Economics on ScienceDirect")

## Journal of Financial Economics

## A five-factor asset pricing model

[https://doi.org/10.1016/j.jfineco.2014.10.010](https://doi.org/10.1016/j.jfineco.2014.10.010 "Persistent link using digital object identifier")

## Introduction

There is much evidence that average stock returns are related to the book-to-market equity ratio, *B* / *M*. There is also evidence that profitability and investment add to the description of average returns provided by *B* / *M*. We can use the dividend discount model to explain why these variables are related to average returns. The model says the market value of a share of stock is the discounted value of expected dividends per share,$m_{t} = \sum_{\tau = 1}^{\infty} E \left(\right. d_{t + \tau} \left.\right) / \left(\left(\right. 1 + r \left.\right)\right)^{\tau} .$

In this equation, *m* <sub><em>t</em></sub> is the share price at time *t*, E(*d* <sub><em>t</em> + <em>τ</em></sub>) is the expected dividend per share for period *t* + *τ*, and *r* is (approximately) the long-term average expected stock return or, more precisely, the internal rate of return on expected dividends.

Eq. (1) says that if at time *t* the stocks of two firms have the same expected dividends but different prices, the stock with a lower price has a higher (long-term average) expected return. If pricing is rational, the future dividends of the stock with the lower price must have higher risk. The predictions drawn from (1), here and below, are, however, the same whether the price is rational or irrational.

With a bit of manipulation, we can extract the implications of Eq. (1) for the relations between expected return and expected profitability, expected investment, and *B* / *M*. Miller and Modigliani (1961) show that the time *t* total market value of the firm׳s stock implied by (1) is,$M_{t} = \sum_{\tau = 1}^{\infty} E \left(\right. Y_{t + \tau} - d B_{t + \tau} \left.\right) / \left(\left(\right. 1 + r \left.\right)\right)^{\tau} .$

In this equation, *Y* <sub><em>t</em> + <em>τ</em></sub>, is total equity earnings for period *t* + *τ* and *dB* <sub><em>t</em> + <em>τ</em></sub> = *B* <sub><em>t</em> + <em>τ</em></sub> *−B* <sub><em>t</em> + <em>τ−</em> 1</sub> is the change in total book equity. Dividing by time *t* book equity gives,$\frac{M_{t}}{B_{t}} = \frac{\Sigma_{\tau = 1}^{\infty} E \left(\right. Y_{t + \tau} - d B_{t + \tau} \left.\right) / \left(\left(\right. 1 + r \left.\right)\right)^{\tau}}{B_{t}} .$

Eq. (3) makes three statements about expected stock returns. First, fix everything in (3) except the current value of the stock, *M* <sub><em>t</em></sub>, and the expected stock return, *r*. Then a lower value of *M* <sub><em>t</em></sub>, or equivalently a higher book-to-market equity ratio, *B* <sub><em>t</em></sub> / *M* <sub><em>t</em></sub>, implies a higher expected return. Next, fix *M* <sub><em>t</em></sub> and the values of everything in (3) except expected future earnings and the expected stock return. The equation then tells us that higher expected earnings imply a higher expected return. Finally, for fixed values of *B* <sub><em>t</em></sub>, *M* <sub><em>t</em></sub>, and expected earnings, higher expected growth in book equity – investment – implies a lower expected return. Stated in perhaps more familiar terms, (3) says that *B* <sub><em>t</em></sub> / *M* <sub><em>t</em></sub> is a noisy proxy for expected return because the market cap *M* <sub><em>t</em></sub> also responds to forecasts of earnings and investment.

The research challenge posed by (3) has been to identify proxies for expected earnings and investments. Novy-Marx (2013) identifies a proxy for expected profitability that is strongly related to average return. Aharoni, Grundy, and Zeng (2013) document a weaker but statistically reliable relation between investment and average return. (See also Haugen and Baker, 1996, Cohen et al., 2002, Fairfield et al., 2003, Titman et al., 2004, Fama and French, 2006, Fama and French, 2008.) Available evidence also suggests that much of the variation in average returns related to profitability and investment is left unexplained by the three-factor model of Fama and French (FF, 1993). This leads us to examine a model that adds profitability and investment factors to the market, size, and *B* / *M* factors of the FF three-factor model.

Many “anomaly” variables are known to cause problems for the three-factor model, so it is reasonable to ask why we choose profitability and investment factors to augment the model. Our answer is that they are the natural choices implied by Eqs. (1), (3). Campbell and Shiller (1988) emphasize that (1) is a tautology that defines the internal rate of return, *r*. Given the stock price and estimates of expected dividends, there is a discount rate *r* that solves Eq. (1). With clean surplus accounting, Eq. (3) follows directly from (1), so it is also a tautology. Most asset pricing research focuses on short-horizon returns – we use a one-month horizon in our tests. If each stock׳s short-horizon expected return is positively related to its internal rate of return in (1) – if, for example, the expected return is the same for all horizons – the valuation equation implies that the cross-section of expected returns is determined by the combination of current prices and expectations of future dividends. The decomposition of cashflows in (3) then implies that each stock׳s relevant expected return is determined by its price-to-book ratio and expectations of its future profitability and investment. If variables not explicitly linked to this decomposition, such as *Size* and momentum, help forecast returns, they must do so by implicitly improving forecasts of profitability and investment or by capturing horizon effects in the term structure of expected returns.

We test the performance of the five-factor model in two steps. Here we apply the model to portfolios formed on size, *B* / *M*, profitability, and investment. As in FF (1993), the portfolio returns to be explained are from finer versions of the sorts that produce the factors. We move to more hostile territory in Fama and French (FF, 2014), where we study whether the five-factor model performs better than the three-factor model when used to explain average returns related to prominent anomalies not targeted by the model. We also examine whether model failures are related to shared characteristics of problem portfolios identified in many of the sorts examined here – in other words, whether the asset pricing problems posed by different anomalies are in part the same phenomenon.

We begin (Section 2) with a discussion of the five-factor model. Section 3 examines the patterns in average returns the model is designed to explain. Definitions and summary statistics for different versions of the factors are in 4 Factor definitions, 5 Summary statistics for factor returns. Section 6 presents summary asset pricing tests. One Section 6 result is that for portfolios formed on size, *B* / *M*, profitability, and investment, the five-factor model provides better descriptions of average returns than the FF three-factor model. Another result is that inferences about the asset pricing models we examine do not seem to be sensitive to the way factors are defined, at least for the definitions considered here. One result in Section 6 is so striking we caution the reader that it may be specific to this sample: When profitability and investment factors are added to the FF three-factor model, the value factor, *HML*, seems to become redundant for describing average returns. Section 7 confirms that the large average *HML* return is absorbed by the exposures of *HML* to the other four factors, especially the profitability and investment factors. Section 8 provides asset pricing details, specifically, intercepts and pertinent regression slopes. An interesting Section 8 result is that the portfolios that cause major problems in different sorts seem to be cast in the same mold, specifically, small stocks whose returns behave like those of firms that invest a lot despite low profitability. Finally, the paper closest to ours is Hou, Xue, and Zhang (2012). We discuss their work in the concluding Section 9, where contrasts with our work are easily described.

## Access through your organization

Check access to the full text by signing in through your organization.

[Access through **your organization**](https://www.sciencedirect.com/user/institution/login?targetUrl=%2Fscience%2Farticle%2Fpii%2FS0304405X14002323)

## Section snippets

## The five-factor model

The FF (1993) three-factor model is designed to capture the relation between average return and *Size* (market capitalization, price times shares outstanding) and the relation between average return and price ratios like *B* / *M*. At the time of our 1993 paper, these were the two well-known patterns in average returns left unexplained by the CAPM of Sharpe (1964) and Lintner (1965).

Tests of the three-factor model center on the time-series regression,$R_{i t} – R_{F t} = a_{i} + b_{i} \left(\right. R_{M t} – R_{F t} \left.\right) + s_{i} S M B_{t} + h_{i} H M L_{t} + e_{i t} .$

In this

## The playing field

Our empirical tests examine whether the five-factor model and models that include subsets of its factors explain average returns on portfolios formed to produce large spreads in *Size*, *B* / *M*, profitability, and investment. The first step is to examine the *Size*, *B* / *M*, profitability, and investment patterns in average returns we seek to explain.

Panel A of Table 1 shows average monthly excess returns (returns in excess of the one-month U.S. Treasury bill rate) for 25 value-weight (VW) portfolios from

## Factor definitions

To examine whether the specifics of factor construction are important in tests of asset pricing models, we use three sets of factors to capture the patterns in average returns in Table 1, Table 2. The three approaches are described formally and in detail in Table 3. Here we provide a brief summary.

The first approach augments the three factors of Fama and French (1993) with profitability and investment factors defined like the value factor of that model. The *Size* and value factors use

## Summary statistics for factor returns

Table 4 shows summary statistics for factor returns. Summary statistics for returns on the portfolios used to construct the factors are in Appendix Table A1.

Average *SMB* returns are 0.29% to 0.30% per month for the three versions of the factors (Panel A of Table 4). The standard deviations of *SMB* are similar, 2.87–3.13%, and the correlations of the different versions of *SMB* are 0.98 and 1.00 (Panel B of Table 4). The high correlations and the similar means and standard deviations are not

## Model performance summary

We turn now to our primary task, testing how well the three sets of factors explain average excess returns on the portfolios of Table 1, Table 2. We consider seven asset pricing models: (i) three three-factor models that combine *R* <sub><em>M</em></sub> − *R* <sub><em>F</em></sub> and *SMB* with *HML*, *RMW*, or *CMA*; (ii) three four-factor models that combine *R* <sub><em>M</em></sub> − *R* <sub><em>F</em></sub>, *SMB*, and pairs of *HML*, *RMW*, and *CMA*; and (iii) the five-factor model.

With seven models, six sets of left-hand-side portfolios, and three sets of right-hand-side (RHS) factors, it

## HML: a redundant factor

The five-factor model never improves the description of average returns from the four-factor model that drops *HML* (Table 5). The explanation is interesting. The average *HML* return is captured by the exposures of *HML* to other factors. Thus, in the five-factor model, *HML* is redundant for describing average returns, at least in U.S. data for 1963–2013.

The evidence is in Table 6, which shows regressions of each of the five factors on the other four. In the *R* <sub><em>M</em></sub> − *R* <sub><em>F</em></sub> regressions, the intercepts (average

## Regression details

For insights into model performance we next examine regression details, specifically, intercepts and pertinent slopes. To simplify the task, we could drop the five-factor model, given that *HML* is redundant for describing average returns. Though captured by exposures to other factors, however, there is a large value premium in average returns that is often targeted by money managers. Thus, in evaluating investment performance, we probably want to know the exposures of LHS portfolios to the *Size*,

## Conclusions

There are patterns in average returns related to *Size*, *B* / *M*, profitability, and investment. The *GRS* test easily rejects a five-factor model directed at capturing these patterns, but we estimate that the model explains between 71% and 94% of the cross-section variance of expected returns for the *Size*, *B* / *M*, *OP*, and *Inv* portfolios we examine.

Judged on regression intercepts, the three sets of factors we use – (i) separate 2×3 sorts on *Size* and *B* / *M*, *OP*, or *Inv*, (ii) separate 2×2 sorts, and (iii)

- *et al.*
	### Stock returns and the Miller Modigliani valuation formula: revisiting the Fama French analysis
	### Journal of Financial Economics
	(2013)
- *et al.*
	### Who underreacts to cashflow news? Evidence from trading between individuals and institutions
	### Journal of Financial Economics
	(2002)
- *et al.*
	### Common risk factors in the returns on stocks and bonds
	### Journal of Financial Economics
	(1993)
- *et al.*
	### Profitability, investment, and average returns
	### Journal of Financial Economics
	(2006)
- *et al.*
	### Size, value, and momentum in international stock returns
	### Journal of Financial Economics
	(2012)
- *et al.*
	### Commonality in the determinants of expected stock returns
	### Journal of Financial Economics
	(1996)
- *et al.*
	### Market underreaction to open market share repurchases
	### Journal of Financial Economics
	(1995)
- ### The other side of value: The gross profitability premium
	### Journal of Financial Economics
	(2013)
- *et al.*
	### The dividend-price ratio and expectations for future dividends and discount factors
	### Review of Financial Studies
	(1988)
- ### On persistence in mutual fund performance
	### Journal of Finance
	(1997)

- *et al.*
	### Accrued earnings and growth: Implications for future profitability and market mispricing
	### The Accounting Review
	(2003)
- ### Multifactor portfolio efficiency and multifactor asset pricing
	### Journal of Financial and Quantitative Analysis
	(1996)
- *et al.*
	### Size and book-to-market factors in earnings and returns
	### Journal of Finance
	(1995)

Fama and French are consultants to, board members of, and shareholders in Dimensional Fund Advisors. Robert Novy-Marx, Tobias Moskowitz, and Ľuboš Pástor provided helpful comments. John Cochrane, Savina Rizova, and the referee, Kent Daniel, get special thanks.

[View full text](https://www.sciencedirect.com/science/article/pii/S0304405X14002323)