# factors-and-esg-the-truth-behind-three-myths-MSCI-FaCS-Methodology

> Extracted from: `factors-and-esg-the-truth-behind-three-myths-MSCI-FaCS-Methodology.pdf` (14 pages)

---
## Page 1

 
 
MSCI FACS METHODOLOG Y | JANUARY 2018  
 
MSCI.COM | PAGE 1 OF 14 
© 2016  MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 MSCI F aCS 
METHODOLOGY  
 
George Bonne, Leon Roisenberg, Raman Aylur Subramanian, Dimitris Melas  
January 2018  
  

---
## Page 2

 
 
 
MSCI.COM | PAGE 2 OF 14 
© 2016  MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI FACS METHODOLOG Y | JANUARY 2018  
 
 
Introduction  ................................ ................................ .......................  3 
Construction of a Factor  ................................ ................................ .... 3 
Security and Portfolio Level Factor Exposures  ................................ ... 6 
Construction of MSCI F aCS ................................ ................................ . 7 
Annual Reviews  ................................ ................................ ................  10 
References  ................................ ................................ .......................  11 
Appendix  ................................ ................................ ..........................  12 
Definitions of Factor Statistics  ................................ ................................ ..........  12 
 CONTENTS  

---
## Page 3

 
MSCI.COM | PAGE 3 OF 14 
© 2016  MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
MSCI FACS METHODOLOG Y | JANUARY 2018  
INTRODUCTION 
Factors are important systematic sources of risk and return in equity portfolios . They have 
been document ed extensively in academic research and are used widely in activ e portfolio 
management . Recently, factor indexes hav e also been developed to provide a transparent 
and efficient method to seek exposure to factors. Given the pervasive use of factors in the 
active investment process and the growing popularity of factor investing through indexed  
strategies, a standard approach is needed for defining factors and evaluating t he factor 
characteristics of portfolios.  
We introduce MSCI FaCS, a classificatio n standar d and framewor k for analyzing and 
reporting style factors in equity portfolios. The standard is based on the factor structure in 
the latest global Barra equity factor risk model, the Barra Global Total Market Equi ty Model 
for Long-Term Investors (GEMLT , Morozov, 2016) . The standar d organizes t he 16 style 
factors of GEMLT into eight factor groups – Value, Size , Momentum, Volatility, Quality, Yield, 
Growth and Liquidity. 
MSCI FaCS creates a common languag e and definitions arou nd st yle factors, for us e by asset 
owners , managers, advisors, consultants and in vestors . Managers can use the framework to 
analyze and report factor characteristics, whil e investors and consultants can us e the data to 
compar e funds and monitor exposures over time using common definitions.  
In the following sections, we describe MS CI FaCS from the bottom up – from how we 
construct individual factors and descriptors, to how we combine them into groups . We also 
explain how to interpret the exposures at both the security and portfolio level. 
CONSTRUCTION OF A FACTOR 
All st yle factors in the Barra GEMLT and other Barra fundamental equity factor models are 
constructed in five primary steps: 
1. Calculate descriptor values. Raw values of each descriptor going into the factor are
calculated.
2. Drop extreme outliers and winsorize1 the remaining values to be within three
standard deviations from the mean.
3. Standardize the raw descriptor values, so that each descriptor has a market- cap-
weighted mean of zero and unit standard deviation.
1 Winsorization limits extreme values  in the data to reduce the effect of outliers . 

---
## Page 4

 
 
 
MSCI.COM | PAGE 4 OF 14 
© 2016  MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI FACS METHODOLOG Y | JANUARY 2018  
4. Linearly combine descriptors. The standardized s cores of the descriptors are linearly 
combined , with weights that are determined by a combination of intuition and 
statistical metrics from the factor model.  
5. Re-standardize the descriptor combination (the factor) to have a market cap -
weighted mean of zero  and unit standard deviation.  
We first calculate the raw descriptor values . This process can be as simple as taking the ratio 
of two numbers or can be considerably more complicated, such as conducting a regression 
or other processing of a multi -year time s eries of a security. The next step is to remove 
extreme outliers and winsorize the remaining values. This involves calculating a robust mean 
and standard deviation of the raw descriptor distribution, which are determined iteratively. 
We use the robust mean  and standard deviation to winsorize the descriptor values to be 
within three standard deviations of the mean. Outlier removal and winsoriza tion aim to 
prevent extreme values from having an undue influence on the final standardized descriptor 
values.  
Afte r removing outliers and winsorizing , we standardize the descriptor values to have  a 
market -cap-weighted mean of zero and an equal -weighted standard deviation of one. This 
completes the standardization process. The Barra GEMLT model estimation universe, whi ch 
is based on the MSCI ACWI IMI universe, is used to determine the parameters in the 
winsorization and standardization process es, but they are applied to the entire coverage 
universe.  
We use the market -cap-weighted mean to standardize descriptor values , so that a well -
diversified cap -weighted global index, such as MSCI ACWI IMI, has approximately zero 
exposure to all style factors. For the standard deviation, however, we use equal  weight ing to 
prevent large -cap constituents from having an undue influ ence on the overall scale of the 
exposures.  
In GEMLT , descriptors and factors based on price, such as momentum, beta and residual 
volatility , are standardized on the global universe. Descriptors based on fundamental data, 
such as book -to-price, profitabil ity and earnings yield, are standardized with a country -
specific mean but a global standard deviation. We find that using country -specific standard 
deviations can result in undesirable and unintended instability in the descriptor values, 
particularly for c ountries with small numbers of stocks. We standardize fundamental 
descriptors with a country -specific mean because values of some fundamental descriptors 
tend to be systematically low or high in some countries. In the end, each descriptor is 
standardized t o a common scale, which makes combining descriptors into a factor 
straightforward.  

---
## Page 5

 
 
 
MSCI.COM | PAGE 5 OF 14 
© 2016  MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI FACS METHODOLOG Y | JANUARY 2018  
In creating each factor, we seek to incorporate and combine similar descriptors. We 
examined the academic and practitioner literature, and conducted our own research to 
identify descriptors that complement each other and that thoroughly capture a theme . For 
example, the profitability factor in the quality group  contains four descriptors, each of which 
captures slightly different elements of profitability – asset turnover, gross margin, gross 
profit relative to assets and return on assets. Although each of these descriptors has 
significant explanatory power on it s own, naively including them as separate factors in a 
factor model may lead to serious multi -collinearity problems. Combining these descriptors 
into a single style factor overcomes this difficulty, creates a factor that is more 
comprehensive and powerful,  and also leads to a more parsimonious factor structure.  
To calculate a factor, we linearly combine the appropriate standardized descriptors using a 
weighting scheme that is Bayesian in nature and determined by a combination of intuition 
and statistics. Ou r starting point is always equal weighting. However, we will modify the 
weights accordingly if we identify strong reasons why we should deviate from equal 
weighting. Such adjustments could stem from examining factor volatilities, t -stats, 
information ratio s (IRs), marginal added explanatory power, our intuition behind the 
“essence” of a particular style factor and investors’ expectations , or other measures. When 
deviating from equal weighting, we are conservative, and keep the weights to round 
numbers. We u sed the same process for setting the weights in the MSCI FaCS factor groups . 
The final step is to re -standardize the descriptor combination to have a market -cap-
weighted mean of zero and unit standard deviation . This  re-standardized descriptor 
combination is then the factor.  
  

---
## Page 6

 
 
 
MSCI.COM | PAGE 6 OF 14 
© 2016  MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI FACS METHODOLOG Y | JANUARY 2018  
SECURITY AND PORTFOLIO LEVEL FACTOR EXPOSURES  
Given that each factor is standardized, the concept of factor exposure for a security is 
straightforward. A security’s exposure represents how far away from the market -cap-
weighted averag e a given security is, and the units are in number of standard deviations. 
Values above zero indicate the security has a value higher than the market -cap-weighted 
average on the given factor, and exposures below zero indicate the security scores below 
that average on the given factor.  For example, an exposure of +2 indicates that the security 
is two standard deviations higher than the average for the particular factor.  
Calculating the exposure (to a descriptor, factor or factor group ) of a portfolio is al so 
straightforward. The exposure of a portfolio is simply the weighted average exposure of all 
the holdings in the portfolio, where the weights are identical to the portfolio weights.  
When considering the magnitude of the exposure and identifying what wou ld constitute a 
“large” or “significant” exposure for a portfolio, and to identify when exposures are likely to 
be intentional and not likely to occur simply from a random selection of securities, one can 
use the statistics of combinations of identically d istributed independent random variables. 
Expressing these concepts mathematically, the portfolio exposure of n stocks is defined as : 
Portfolio exposure = ∑ 𝑤𝑖𝑋𝑖𝑛
𝑖=1    
where the wi  are the individual stock weights and the Xi are the individual stock exposures . 
Assuming stock exposures are independent and have identical distributions, if we take the 
variance of the above equation we get : 
Var(Portfolio e xposure ) = ∑ 𝑤𝑖2𝑉𝑎𝑟 (𝑋𝑖)𝑛
𝑖=1   = ∑ 𝑤𝑖2𝑛
𝑖=1 
since Var( Xi) = 1  
For an equal -weighted portfolio of n stocks (each stock has weight = 1/n), the variance of 
the portfolio exposure is simply : 
∑ (1
𝑛)2𝑛
𝑖=1 = 𝑛(1
𝑛)2
= 1
𝑛 
The standard deviation of an equal -weighted portfolio of n stocks is then   1
√𝑛 
We can also generalize this result to a portfolio with arbitrary security weights using a 
measure of the effective number (EN) of securities in the portfolio based on the Herfindahl -
Hirschman  Index (HHI). The effective number of stocks  is a measure of portfolio 
concentration and ranges between 1  (for a single stock) and the number of stocks in the 
portfolio (for an equal -weighted portfolio) , and is given by the inverse of the sum of squares 
of the weights of the portfolio : 

---
## Page 7

 
 
 
MSCI.COM | PAGE 7 OF 14 
© 2016  MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI FACS METHODOLOG Y | JANUARY 2018  
EN = 1 / ∑ 𝑤𝑖2 𝑛
𝑖=1   
Thus, the variance of a portfolio exposure is simply  1/EN. For a typical portfolio with EN 
~100, this implies a portfolio standard deviation of exposure of 0.1. For such a portfolio, a 
two sigma exposure would be about 0.2, and therefore we adopt the threshold of 0.2 as 
constituting a “significant” portfoli o exposure for a typical portfolio. In a well -diversified 
portfolio, exposures outside of [ -0.2, 0.2] are unlikely to have been produced  by a random 
selection of securities , but can readily  be generated, and are most  likely to have been 
generated , by inten tional positioning and tilts.  
CONSTRUCTION OF  MSCI FaCS 
In constructing MSCI FaCS, we sought to combine factors of a common theme together.  The 
classification standard  structure is displayed in Exhibit 1. In assigning the weights, we used 
the same methodo logy as when assigning weights to the descriptors of a factor – a 
combination of factor statistics and our intuition of the factor group . The factor statistics we 
explored include d the factor returns, volatilities, information ratios ( IRs), t-statistics an d R2 
from cross -sectional regressions . Definitions of these statistics are provided in the Appendix.   
Exhibit 1. Structure of MSCI FaCS  
 
 
The 16 factors of Barra GEMLT are combined into eight factor groups .  
 


---
## Page 8

 
 
 
MSCI.COM | PAGE 8 OF 14 
© 2016  MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI FACS METHODOLOG Y | JANUARY 2018  
When assigning weights to factors in each factor group , we put more emphasis on factor 
returns and IRs for Systematic Equity Strategy (SES )2 factor groups  (quality and value), and 
more emphasis on factor volatilities, t -stats and cross -validated (CV) R2 gain for the non -SES 
factor groups  (i.e., the size and  volatility factor groups ).  
Within the quality group , for example, our multi -variate cross -sectional regression statistics, 
provided in Exhibit 2, also show that the three SES quality factors of earning s quality, 
investment quality and profitability generated significantly higher factor returns and IRs than 
the non -SES quality factors of leverage and earnings variability. Variants of the SES quality 
factors have also been extensively discussed in the aca demic literature – see Sloan (1996) 
for the earnings quality factor , and Fama and French (2015) and Novy -Marx (2013) for the 
profitability and investment quality factors – as providing explanatory power in the cross 
section of stock returns and generating risk premia over long horizons.  
Exhibit 2 shows that the non -SES factors generated t -stats, factor volatilities and CV R2 gains 
comparable to those of the SES quality factors. These results demonstrate that the non -SES 
quality factors added explanatory pow er to the cross section of security returns, even 
though their annualized factor returns were not as large as those of the SES quality factors.  
Therefore, we assigned a 25% weight to each of the three SES quality factors and a -12.5% 
weight to each of the other two quality factors .3 
 
                                                      
2 See Bayraktar (2013) for a detailed description of SES factors.  
3 Leverage and earnings variability received negative weight because low leverage and low earnings variability a re 
associated with high  quality companies.  

---
## Page 9

 
 
 
MSCI.COM | PAGE 9 OF 14 
© 2016  MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI FACS METHODOLOG Y | JANUARY 2018  
Exhi bit 2. Factor Statistics from Multi-variate Cross-sectional Regressions in GEMLT  
 
Sample period is 1995  to 2016.  
 
For the factor groups composed of more than one factor – value, size, volatility  and quality – 
we re -standardize the factor combination using the same standardization methodology as 
for the individual factors. Each factor group  is standardized to have market -cap-weighted 
mean of zero and unit equal -weighted global standard deviation . The volatility group  is 
standardized using a global mean while the size, value and quality groups are standardized 
using  a country -specific mean and a global standard deviation.  
As an example of the MSCI FaCS calculation, we evaluated Microsoft Co rp.’s exposure to the 
quality factor group . On Sept. 29, 2017, Microsoft’s factor exposures for profitability, 
investment quality, earnings quality, earnings  variability and leverage were 0.169, -0.055, 
0.403, -0.442, and 0.289, respectively. Combining these factor exposures with the quality 
weights listed in Exhibit 2 gives us the raw, pre -standardized quality group  combination:  
0.25*0.169 + 0.25*( -0.055) + 0.25*0.403 - 0.125*( -0.442 ) - 0.125*0.289 = 0.148  
For all U.S. companies in the MSCI ACWI Investable Market Index (IMI), the raw, pre -
standardized quality group  combination had a market -cap- weighted mean of 0.000 and a  
Factor Group FactorMean   
|t-stats|Annual 
Return 
(%)Annual 
Volatility 
(%)IRCV R2 
Gain 
(bp)Weight 
in FaCS 
group
Earnings Yield 2.17 3.64 1.74 2.09 3.21 60%
Book-to-Price 2.03 2.18 1.59 1.38 2.38 30%
LT Reversal 1.96 1.42 1.36 1.05 1.69 10%
Size 4.32 -0.05 2.26 -0.02 19.92 90%
Mid Cap 2.21 0.04 1.48 0.03 3.44 -10%
Leverage 1.70 -0.18 1.01 -0.18 1.11 -12.5%
Earnings Var 1.71 -0.37 1.13 -0.32 0.99 -12.5%
Profitability 1.67 1.17 1.12 1.05 0.49 25%
Earnings Qual 1.47 1.41 0.81 1.73 0.03 25%
Investment Qual 1.48 1.16 0.82 1.42 0.12 25%
Beta 6.99 0.20 5.93 0.03 44.18 60%
Residual Vol 3.94 -2.28 3.05 -0.75 13.18 40%
Momentum Momentum 4.74 4.38 3.54 1.24 22.69 100%
Yield Div Yield 1.85 0.91 1.26 0.72 1.81 100%
Growth Growth 1.72 0.89 1.12 0.80 0.78 100%
Liquidity Liquidity 3.18 -1.13 2.15 -0.53 8.33 100%Value
VolatilitySize
Quality

---
## Page 10

 
 
 
MSCI.COM | PAGE 10 OF 14 
© 2016  MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI FACS METHODOLOG Y | JANUARY 2018  
global  equal -weighted standard deviation of 0.513 on th is date. Thus, our final MSCI FaCS 
quality group  exposure for Microsoft on this date was 0.288, calculated as  
(0.148 – 0.000)/0.513  
ANNUAL REVIEWS  
MSCI FaCS is based on an extensive , yet parsimonious, set of factors that explain global long -
term risk  and risk premia. We recognize that other factors do exist, such as those that are 
more regional or narrow in focus and/or short -term in nature.  
Indeed, a number of other factors and categories of factors exist in regional, country, and 
short -term trading  versions of Barra models. For example, trading versions of some Barra 
models contain high -turnover sentiment factors constructed from analyst revisions, news, 
short interest and/or options data. Further , the latest European Barra model includes an ESG 
factor, as today we find it to be an important contributor to explaining risk and return in 
Europe. While it is not currently included in GEMLT or MSCI FaCS, these models are regularly 
updated.  
We expect that just like GICS®,4 MSCI FaCS will evolve slowly ov er time. Factors or factor 
groups may be added, modified or removed. We will conduct annual reviews of the standard 
to ensure it accurately reflects a robust set of factors and factor groups that explain global 
long -term equity risk and retur n at a given point in time.  
  
                                                      
4 GICS is the global industry classification standard jointly developed by MSCI and Standard & Poor’s . 

---
## Page 11

 
 
 
MSCI.COM | PAGE 11 OF 14 
© 2016  MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI FACS METHODOLOG Y | JANUARY 2018  
REFERENCES  
Bayraktar, M., S. Radchenko, K. Winkelmann and P. Zangari . (2013 ). “Employing Systematic 
Equity Strategies: Distinguishing Important Sources of Risk from Common Sources of 
Return .” MSCI Research Insight.  
Fama, E. and K. French . (2015 ). “A Five-factor Asset Pricing Model .” Journal of Financial 
Economics , Vol. 16, pp. 1-22. 
Morozov, A., S. Minovitsky, J. Wang  and D. Barrera . (2016 ). “Barra Global Total Market 
Equity Model for Long Term Investors, Empirical Notes .” MSCI Model Insight.  
Novy -Marx, R.  (2013 ). “The Other Side of Value: The Gross Profitability Premium .”  Journal 
of Financial Economics , Vol. 108, pp. 1-28. 
Rao, A., R. A. Subramanian and D. Melas . (2017 ). “Bridging the Gap: Adding Factors to 
Passive and Active Allocations .” MSCI Research Insight.  
Roisenberg, L., R. A. Subramanian and G. Bonne . (2017 ). “Anatomy of Active Portfolios: How 
Factor Exposures Affect Fund Performance .” MSCI Research Insight.  
Sloan, R. (1996 ). “Do Stock Prices Fully Reflect Inform ation in Accruals and Cash Flows 
about Future Earnings? ” The Accounting Review , Vol. 71, pp. 289-315.  
 
  

---
## Page 12

 
 
 
MSCI.COM | PAGE 12 OF 14 
© 2016  MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI FACS METHODOLOG Y | JANUARY 2018  
APPENDIX  
DEFINITIONS OF FACTOR STATISTICS  
Annual Factor Return . Component of security returns attributed to a factor as determined 
by a multi -variate , cross -sectional regression, accounting for  the market factor,  other style 
factors, indust ries and countries , expressed on an annualized basis.  It can be interpreted as 
the return to a factor given a unit exposure to the factor  and zero exposure to all othe r 
factors . 
Annual Factor Volatility . Standard deviation of factor return, expressed on an annualized 
basis. A high factor volatility indicates that at times stocks make large moves due to the 
factor, indicat ing that  the factor is an important contributor t o explaining the cross section 
of security returns . 
Factor I nformation Ratio (IR) . Annualized factor return divided by annualized factor 
volatility.  
Mean |t -stat| . Average of the absolute value of the t -statistic of the regression coefficient 
to a factor in the multi -variate cross -sectional regressions .  
CV R2 Gain . Gain in R2 in multi -variate, cross -sectional regressions due to adding the factor, 
when all other factors are present in the regression, as determined through hold -one-out 
cross validation (CV) .  
 
 
  

---
## Page 13

 
 
 
MSCI.COM | PAGE 13 OF 14 
© 2016  MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI FACS METHODOLOG Y | JANUARY 2018  
 
AMERICAS  
 
Americas  1 888 588 4567 *  
Atlanta   + 1 404 551 3212  
Boston   + 1 617 532 0920  
Chicago   + 1 312 675 0545  
Monterrey  + 52 81 1253 4020  
New York  + 1 212 804 3901  
San Francisco  + 1 415 836  8800  
Sao Paulo  + 55 11 3706 1360  
Toronto   + 1 416 628 1007  
 
 
EUROPE, MIDDLE EAST & AFRICA  
 
Cape Town  + 27 21 673 0100  
Frankfurt  + 49 69 133 859 00  
Geneva   + 41 22 817 9777  
London   + 44 20 7618 2222  
Milan   + 39 02 5849 0415  
Paris   0800 91 59 17 *  
 
 
ASIA PACIFIC  
 
China North  10800 852 1032 *  
China South  10800 152 1032 *  
Hong Kong  + 852 2844 9333  
Mumbai   + 91 22 6784 9160  
Seoul   00798 8521 3392 *  
Singapore  800 852 3749 *  
Sydney   + 61 2 9033 9333  
Taipei   008 0112 7513 *  
Thailand  0018 0015 6207 7181 *  
Tokyo   + 81 3 5290 1555  
 ABOUT MSCI  
 
For more than 40 years, MSCI’s research -
based indexes and analytics have helped 
the world’s leading investors build and 
manage better portfolios.  Clients rely on 
our offerings for deeper insights into the 
drivers of performa nce and risk in their 
portfolios, broad asset class coverage and 
innovative research.  
Our line of products and services includes 
indexes, analytical models, data, real estate 
benchmarks and ESG research.   
MSCI serves 9 9 of the top 100 largest 
money managers, according to the most 
recent P&I ranking.  
For more information, visit us at 
www.msci.com . 
* =  toll free  
 CONTACT US  
 
clientservice@msci.com  

---
## Page 14

 
 
MSCI FACS METHODOLOG Y | JANUARY 2018  
 
MSCI.COM | PAGE 14 OF 14 
© 2016  MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 This document and all of the information contained in it, including without limitation all text, data, graphs, charts (collect ively, the “Information”) is 
the property of MSCI Inc. or its subsidiaries (collectively, “MSCI”), or MSCI’s licensors, direct or i ndirect suppliers or any third party involved in making 
or compiling any Information (collectively, with MSCI, the “Information Providers”) and is provided for informational purpose s only.  The Information 
may not be modified, reverse -engineered, reproduce d or redisseminated in whole or in part without prior written permission from MSCI.  
The Information may not be used to create derivative works or to verify or correct other data or information.   For example ( but without limitation), 
the Information may n ot be used to create indexes, databases, risk models, analytics, software, or in connection with the issuing, offering, 
sponsoring, managing or marketing of any securities, portfolios, financial products or other investment vehicles utilizing or  based on, linked to, 
tracking or otherwise derived from the Information or any other MSCI data, information, products or services.   
The user of the Information assumes the entire risk of any use it may make or permit to be made of the Information.  NONE OF THE INFO RMATION 
PROVIDERS MAKES ANY EXPRESS OR IMPLIED WARRANTIES OR REPRESENTATIONS WITH RESPECT TO THE INFORMATION (OR THE RESULTS TO BE 
OBTAINED BY THE USE THEREOF), AND TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, EACH INFORMATION PROVIDER EXPRESSLY 
DISC LAIMS ALL IMPLIED WARRANTIES (INCLUDING, WITHOUT LIMITATION, ANY IMPLIED WARRANTIES OF ORIGINALITY, ACCURACY, TIMELINESS, 
NON -INFRINGEMENT, COMPLETENESS, MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE) WITH RESPECT TO ANY OF THE 
INFORMATION.  
Without limiting any of the foregoing and to the maximum extent permitted by applicable law, in no event shall any Information Provid er have any 
liability regarding any of the Information for any direct, indirect, special, punitive, consequential (including lost p rofits) or any other damages even if 
notified of the possibility of such damages. The foregoing shall not exclude or limit any liability that may not by applicabl e law be excluded or limited, 
including without limitation (as applicable), any liability for death or personal injury to the extent that such injury results from the negligence or 
willful default of itself, its servants, agents or sub -contractors.   
Information containing any historical information, data or analysis should not be taken as an indic ation or guarantee of any future performance, 
analysis, forecast or prediction.  Past performance does not guarantee future results.   
The Information should not be relied on and is not a substitute for the skill, judgment and experience of the user, its m anagement, employees, 
advisors and/or clients when making investment and other business decisions.  All Information is impersonal and not tailored to the needs of any 
person, entity or group of persons.  
None of the Information constitutes an offer to sell (or a solicitation of an offer to buy), any security, financial product or other investment vehicle or 
any trading strategy.  
It is not possible to invest directly in an index.  Exposure to an asset class or trading strategy or other category represen ted b y an index is only 
available through third party investable instruments (if any) based on that index.   MSCI does not issue, sponsor, endorse, m arket, offer, review or 
otherwise express any opinion regarding any fund, ETF, derivative or other security, inv estment, financial product or trading strategy that is based on, 
linked to or seeks to provide an investment return related to the performance of any MSCI index (collectively, “Index Linked Investments”). MSCI 
makes no assurance that any Index Linked Inves tments will accurately track index performance or provide positive investment returns.  MSCI Inc. is 
not an investment adviser or fiduciary and MSCI makes no representation regarding the advisability of investing in any Index Linked Investments.  
Index retu rns do not represent the results of actual trading of investible assets/securities. MSCI maintains and calculates indexes, bu t does not 
manage actual assets. Index returns do not reflect payment of any sales charges or fees an investor may pay to purchase the securities underlying the 
index or Index Linked Investments. The imposition of these fees and charges would cause the performance of an Index Linked In vestment to be 
different than the MSCI index performance.  
The Information may contain back tested dat a.  Back -tested performance is not actual performance, but is hypothetical.  There are frequently 
material differences between back tested performance results and actual results subsequently achieved by any investment strat egy.   
Constituents of MSCI equit y indexes are listed companies, which are included in or excluded from the indexes according to the application of the 
relevant index methodologies. Accordingly, constituents in MSCI equity indexes may include MSCI Inc., clients of MSCI or supp liers to MSC I.  Inclusion 
of a security within an MSCI index is not a recommendation by MSCI to buy, sell, or hold such security, nor is it considered to be investment advice.  
Data and information produced by various affiliates of MSCI Inc., including MSCI ESG Researc h LLC and Barra LLC, may be used in calculating certain 
MSCI indexes.  More information can be found in the relevant index methodologies on www.msci.com.  
MSCI receives compensation in connection with licensing its indexes to third parties.  MSCI Inc.’s re venue includes fees based on assets in Index 
Linked Investments. Information can be found in MSCI Inc.’s company filings on the Investor Relations section of www.msci.com . 
MSCI ESG Research LLC is a Registered Investment Adviser under the Investment Advise rs Act of 1940 and a subsidiary of MSCI Inc.  Except with 
respect to any applicable products or services from MSCI ESG Research, neither MSCI nor any of its products or services recom mends, endorses, 
approves or otherwise expresses any opinion regarding an y issuer, securities, financial products or instruments or trading strategies and MSCI’s 
products or services are not intended to constitute investment advice or a recommendation to make (or refrain from making) an y kind of investment 
decision and may not be relied on as such. Issuers mentioned or included in any MSCI ESG Research materials may include MSCI Inc., clients of MSCI  
or suppliers to MSCI, and may also purchase research or other products or services from MSCI ESG Research.  MSCI ESG Research  mate rials, including 
materials utilized in any MSCI ESG Indexes or other products, have not been submitted to, nor received approval from, the Uni ted States Securities 
and Exchange Commission or any other regulatory body.  
Any use of or access to products, serv ices or information of MSCI requires a license from MSCI.  MSCI, Barra, RiskMetrics, IPD, FEA, InvestorForce, and 
other MSCI brands and product names are the trademarks, service marks, or registered trademarks of MSCI or its subsidiaries i n the United Stat es 
and other jurisdictions.  The Global Industry Classification Standard (GICS) was developed by and is the exclusive property o f MSCI and Standard & 
Poor’s.  “Global Industry Classification Standard (GICS)” is a service mark of MSCI and Standard & Poor’s.  NOTICE AND 
DISCLAIMER  

