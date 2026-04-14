# Foundations of Factor Investing

> Extracted from: `Foundations_of_Factor_Investing.pdf` (33 pages)

---
## Page 1

 
 
 
  
 
 
 
 
 
 
 
 
 
 msci.com  
 
Research Insight  
Foundations of  Factor  Investing  
 
Jennifer Bender  
Remy Briand  
Dimitris Melas  
Raman Aylur Subramanian  
 
 
 
December  2013

---
## Page 2

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
2 of 33 Executive Summary  
Factor  investing has become a widely discussed part of today’s investment canon. In this paper , we 
discuss the rationale for factor investing and how indexes  can be constructed to reflect  factor  returns  in 
cost-effective and transparent ways.   
A factor can be th ought of as any characteristic relating a group of securities that is important in 
explaining their return and risk.  A  large body of academic research highlights that long term equity 
portfolio performance can be explained by factors.  This research has b een prevalent for over 40 years; 
Barra  (now an MSCI company)  for instance has undertaken the research of factors since the 1970s.   
Certain  factors have historically earn ed a long -term  risk premium  and represent  exposure to systematic 
sources of risk .  Factor investing is the investment process that aims to harvest these risk premia 
through exposure to factors.  We currently identify six equity risk premia factors: Value, Low Size, Low 
Volatility, High Yield, Quality and Momentum . They are grounded in  academic research and have solid 
explanations as to why they historically have provide d a premium.  
MSCI has created a family of factor indexes  that are designed  to reflect the performance of those six 
equity risk premia factor s.  In turn, i ndexation has p rovided a powerful way for investors to access 
factors in cost -effective and transparent ways.  Factor allocations can be implemented passively using 
factor indexes , which may bring potential cost savings to institutional investors.  Furthermore, factor 
indexes  bring transparency to factor allocations , which helps alleviate the well -known problem of 
manager style drift and has positive implications for risk management.  
We note that f actor indexes  should not be viewed as replacements for market cap indexes .  Market 
capitalization weighted indexes  represent both the opportunity set of investors as well as their 
aggregate holdings.  Market cap weighted indexes  are also the only reference for a truly passive, macro 
consistent, buy and hold investment strategy .  They aim  to capture the long term equity risk premium 
with structurally low turnover, very high trading liquidity and extremely large investment capacity .  In 
contrast, f actor indexes  rebalance away from a neutral market cap starting point. As such, they 
represent the result of an active view  or decision . Investors must form their own belief about what 
explains the historical premium and whether it is likely to persist.  
Factor returns have  also been highly cycli cal. These systematic factors have been  sensi tive to macro -
economic and market forces and have underperform ed the overall market for long periods of time. 
However, they have not all react ed to the same drivers and, hence, any one of them can have low 
correlations  relative to other factors . Diversific ation across factors has historically reduce d the length  of 
these periods of underperformance .  Thus, the MSCI Factor I ndexes provide building blocks  that allow 
investors to assemble multi -factor allocations based on their preferences for performance  and r isk, their 
investment beliefs on individual factors, and their investability  constraints .    

---
## Page 3

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
3 of 33 Introduction  
Factor  investing has become a widely discussed part of today’s investment canon. This paper is the first 
in a three -paper series focusing on factor investing.  In this paper  we lay out the rationale for factor 
investing and how indexation can capture  factors in cost -effective and transparent ways.1  Specifically, 
institutional and individual investors around the world  have asked many of the same quest ions: 
 What are fac tors?  Why have they  provided better risk -adjusted return historically and how 
likely is that to persist in the future?  
 How does one capture factors via allocations to investable indexes ?    
 How should investors think of factor indexes  relative to market cap weighted indexes  and 
active management ? 
This paper focuses on the above questions.  In Section I, we highlight that factors should be grounded in 
the academic literature and should be important in explaining portfolio returns in sta ndard performance 
risk and attribution models.  We also distinguish between generic factors and factors that reflect risk 
premia.  The latter are factors  that earn a persistent risk -adjusted premium over time  and reflect 
exposure to sources of systematic r isk.   
In Section II, we discuss the proposed drivers of factor s’ excess returns.  Understanding the potential 
drivers of factor returns is critical to forming a belief about their likelihood to persist in the future.  
Different theories have been advanced to explain why factors have historically earned a premium.  One 
view is that factor returns are compensation for bearing systematic risk.  A second view is that factor 
returns arise from systematic errors; either investors exhibit behavioral biases or inve stors are subject to 
different constraints (e.g., time horizons, ability to use leverage, etc.) .  
In Section III, we address the question of how factors should be viewed relative to market capitalization 
weighted portfolios.  The latter represent both the opportunity set of investors as well as their 
aggregate holdings.  The market cap weighted benchmark is the only reference for a truly passive, 
macro consistent, buy and hold investment strategy which aims to capture the long term equity risk 
premium with extremely low turnover, very high trading liquidity and infinite investment capacity.  
Factor portfolios on the other hand rebalance away from a neutral market cap starting point. As such, 
they represent an active view.  
In Section IV , we note the significan t cyclicality  of factor returns. There is importantly no free lunch 
attached to factor investing.  All factors have experience d periods of underperformance and some 
factors have been  highly cyclical.  Their cyclicality may in fact be one of the reasons the y have not been 
arbitraged away.   
In Section V, we introduce the concept of capturing factors through indexation .  Until recently, 
capitaliz ing on systematic factors could only reasonably be done by active managers.   Factor indexes  
allow institutional investors to  create passive  factor allocations  in the transparent and cos t efficient 
framework of indexation .  Finally i n Section IV, we illustrate the use of indexation through the MSCI 
Factor Indexes .  
                                                           
1 The next paper in this series covers various aspects of implementation including use cases we have seen.   

---
## Page 4

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
4 of 33 I. What Are Factors?  
Factors Have Their Roots in the A cademic Literature  
The question of what drives stock returns has been a staple of modern finance.  The oldest and most 
well-known model of stock returns is the Capital Asset Pricing Model (CAPM) , which became a 
foundation of modern financial theory in the 1960s ( Lintner, 1965; Mossin, 1966; Sharpe, 1964 and 
Treynor, 1961 ). In the CAPM, securities have  only  two main drivers: systematic risk and idiosyncratic 
risk.  Systematic risk in the CAPM is the risk that arises from exposure to the market and is capture d by 
beta, the sensitivity of a security’s return to the market . Since systematic risk cannot be diversified 
away, investors are compensated with returns for bearing this risk.  In other words, the expected return 
to any stock could be viewed as a function  of its beta to the market.2 
 
Later, Ross (1976) proposed a different theory of what drives stock returns.  “A rbitrage pricing theory ” 
(APT) holds that the expected return of a financial a sset can be modeled as a function of various 
macroeconomic factors or theoretical market indexes3.  We can credit Ross with popularizing the 
original term  “factors ,” as the models he popularized were called “multi -factor models.”   Importantly, 
APT, un like the CAPM, did not explic itly state what these factors should be.  Instead, t he numbe r and 
nature of these factors were  likely to change o ver time and vary across markets . Thus the challenge of 
building factor models became, and continues to be, essentially empirical in nature.  
 
In general, a factor can be thought of as any characteristic relating a group of securities that is important 
in explaining  their returns and risk .   As noted in the early CAPM -related literature, the market can be 
viewed as the first and most important eq uity factor.  Beyond the market  factor , researchers generally 
look for factors that are persistent over time and have strong explanatory power over a broad range of 
stocks.4   Since , unlike stock returns,  factors cannot be directly observed, there of cours e remains a 
vigorous debate about how to define and estimate them .5  There are three main categories of factors 
today: macroeconomic, statistical , and fundamental .6  Macroeconomic factors include measures such as 
surprises in inflation, surprises in GNP, surprises in the yield curve, and other measures of the macro 
economy (see Chen, Ross, and Roll (1986) for one of the first most well -known models).    Statistical 
factor models identify factors using statistical techniques such as principal components anal ysis (PCA) 
where the factors are not pre -specified in advance.7    
Arguably the mostly widely used factors today are fundamental factor s.  Fundamental factors capture 
stock characteristics such as  industry memb ership, country membership, valuation ratios, and technical 
indicators,  to name a few.  The most popular factors today – Value, Growth, Size, Momentum – have 
                                                           
2 The expected return to a stock would just be its beta times the assumed market return. Investors would need no compensation f or the idiosyncratic return which 
would diversify across many stocks.  
3 The model -derived rate of return would then be used to pri ce the stock correctly.  The stock price should equal the expected end of period price discounted at the 
rate implied by the model, and if the price diverged, arbitrage would bring it back into line.  
4 Miller (2006) discusses three key statistical criteria  for factors: persistence over time, “large enough” variability in returns relative to individual stock volatility, and 
application to a “broad enough” subset of stocks within the defined universe.  
5 Factor returns can be constructed by building factor po rtfolios that “mimic” the target factor (as in the Fama -French approach). Factor returns can alternatively be 
estimated through cross -sectional regression (as in the Barra approach).  As far as estimation techniques go, there is a nearly infinite range of techniques that have 
been applied to factor estimation – principal components analysis, panel regressions, Bayesian models, latent factor models, to name a few.  
6 Connor (1995) gives a comprehensive overview of these three types of factor models.  
7 The question of which type of model is the best continues to be hotly debated.  Typically, the appropriateness of a model comes d own to the use case.  And of 
course, within each type of model, there continue to be many debates over the best way to construct a model and specify factors.  

---
## Page 5

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
5 of 33 been studied for decades as part of the academic asset pricing literature and the practitioner risk factor 
modeling research.  Rosenberg and Mar athe (1976) were among the first to  describe the importance of 
these stock traits in explaining stock returns ,8 leading to the creation of the multi -factor Barra risk 
models. Later, one of the best known efforts in this space came from Eugene Fama and Kenn eth French 
in the early 1990s.  Fama and French ( 1992, 1993) put forward a model explaining US equity market 
returns with three factors: the “market” (based on the traditional CAPM model), the size factor (large vs. 
small capitalization stocks) and the value factor (low vs. high book to market). The “Fama -Fren ch” 
model, which today includes Carhart ’s (1997) momentum factor, has become a canon  within the finance 
literature.  In the past few decades, r esearchers have studied a host of other stock traits, from income 
statement and balance sheet measures like earnings revisions and accruals to technical indicators like 
volatility  and relative stre ngth (momentum).  The latest research has even looked at non-traditional 
factors like the number of “Google”  hits a stock receives  or the number of times it is mentioned in  
mainstream media.  
 
Exhibit 1 summarizes six of the most widely studied factors .  More recently, Low Volatility, Yield, and 
Quality factors have become increasingly well -accepted in the academic literature  (see Appendix A).  
Exhibit 1: Well -Known Systemati c Factors from the Academic Research  
Systematic 
Factors   What It is  Commonly Captured by   
Value   Captures excess returns to stocks that have 
low prices relative to their fundamental value   Book to price, earnings to price, book 
value, sales, earnings, cash  earnings, net 
profit, dividends, cash flow  
Low Size (Small Cap)   Captures excess returns of smaller firms (by 
market capitalization) relative to their larger 
counterparts   Market capitalization (full or free float)  
Momentum   Reflects excess returns to stocks with stronger 
past performance   Relative returns (3 -mth, 6 -mth, 12 -mth, 
sometimes with last 1 mth excluded), 
historical alpha  
Low Volatility   Captures excess returns to stocks with lower 
than average volatility, beta, and/or 
idiosyncratic risk   Standard deviation (1 -yr, 2 -yrs, 3 -yrs), 
Downside standard deviation, standard 
deviation of idiosyncratic returns, Beta  
Dividend Yield   Captures excess returns to stocks that have 
higher -than -average dividend yields   Dividend yield  
Quality   Captures exc ess returns to stocks that are 
characterized by low debt, stable earnings 
growth, and other “quality” metrics   ROE, earnings  stability , dividend growth  
stability , strength of b alance sheet, 
financial leverage, accounting policies, 
strength of management, accruals , cash 
flows  
 
                                                           
8 In fact, they argued that the impact of macroeconomic events on individual securities was better captured through these stock characteristics . 

---
## Page 6

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
6 of 33 Empirical studies show that these factors  have exhibited excess returns above the market .9  For 
instance, the seminal Fama and French (1992) study found that the average small cap portfolio 
(averaged across all sorted book -to-market portfolios) earned monthly returns of 1.47% in contrast to 
the average large cap portfolio’s returns of 0.90% from July 1962 to December 1990 .  Similarly, the 
average high book -to-market portfolio (across all sorted size portfolios) earned 1.63% monthly returns 
compared to 0.64% for the average low book -to-market portfolios.  Fama -French ’s cumulative factor 
returns through August 2013 are shown  in Exhibit 2 (sourced from Kenneth French’s website) .10   The 
factors are long -short portfolios that do not include the market portfolio; the positive cumulative 
returns reflect returns excess of the market.  
Exhibit 2: Well -Known Systematic Factors from the Academic Research (Cumulative Returns)  
  
 
Also shown are factor returns from the Barra US and Global Equity Risk Models (USE4 and GEM2).11  
These f actor portfolios and their accompanying returns are estimated in a different way from Fama -
French, but  they are all long -short portfolios  without features or constraints that would make them 
investable in practice (e.g. limits on position sizes) .12  Decades of research by Barra has also found 
empirical evidence of several important factors beyond the Fama -French factors.  (Note that within the 
                                                           
9 Note that the Barra Volatility factors reflect high  volatility stocks relative to low volatility stocks. The premium to low volatility stocks can be assessed by taking the 
negative of the Volatility factors’ returns.  
10 Note that Fama -French US factor returns are available beginning in July 1926. The chart begins in December 1969 for vis ual clarity.  
11 In some cases, factor returns have been combined or the sign has been reversed so the magnitude s of the premia are visually comparable.   
12 For factor researchers, the difference between the Fama -French and Barra approaches is not trivial. F ama -French factors are found through a process of sorting 
and bucketing stocks to build factor -mimicking portfolios while Barra factors are found through cross -sectional multivariate regression.  Menchero (2010) provides a 
good discussion of the difference s in factor estimation methodologies.  
05001000150020002500300035004000
Dec-69
Dec-71
Dec-73
Dec-75
Dec-77
Dec-79
Dec-81
Dec-83
Dec-85
Dec-87
Dec-89
Dec-91
Dec-93
Dec-95
Dec-97
Dec-99
Dec-01
Dec-03
Dec-05
Dec-07
Dec-09
Dec-11US Fama -French Factors
Low Size (SMB) Value (HML) Momentum (WML)
0100200300400500600
Jun-90
Jun-91
Jun-92
Jun-93
Jun-94
Jun-95
Jun-96
Jun-97
Jun-98
Jun-99
Jun-00
Jun-01
Jun-02
Jun-03
Jun-04
Jun-05
Jun-06
Jun-07
Jun-08
Jun-09
Jun-10
Jun-11
Jun-12
Jun-13Global Fama -French Factors
Low Size (SMB) Value (HML) Momentum (WML)
050100150200250300350Barra US Equity Model (USE4) Factors
Country (Market) Factor Negative SIZE + Sizenonl
Book -to-Price + Earnings Yld Negative Beta + Negative BetaNonl
Yield Factor Momentum Factor
050100150200250Barra Global Equity Model (GEM2) Factors
World factor Momentum factor
Negative Volatility factor Value factor
Negative Size Factor + SizeNonlinearity Factor

---
## Page 7

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
7 of 33 language employed by multi -factor models like Barra, we refer here to style and strategy factors and not 
industry and country factors.)  The charts confirm the historical premiums observed to value, 
momentum, smaller c ap, higher yield, and lower volatility stocks.  
Risk Premia :  Factors Which Earn Persistent Premi um Over Long Periods  
We must stress here that the term “factor” is often used throughout the industry liberally and may refer 
to one of thousands of different s tock characteristics .  The term “factor” is often applied to any stock 
characteristic   that can be shown to be important, either in explaining risk or returns (typically relative 
to the market but not always).  In the Barra Risk Models, for instance,  there  are factors that are 
significant in explaining returns but which do not earn a premium over reasonably long horizons.  For 
instance, as shown in Exhibit 3, factors such as Growth and Liquidity, which capture high growth stocks 
and highly liquid stocks,  have  not outperform ed the market over long periods.   These types of factors 
are not considered good candidates for long -term factor investing.   
Exhibit 3: Differentiating Between Factors Reflecting Risk Premia and Other Factors  (Cumulative Returns 
to Barra  Global Equity Model (GEM2) Factors)  
 
Note: Factors that can earn a premium over long periods  include Value  and Momentum while other factors do not , such as  Growth  and 
Liquidity.  
Thus we distinguish between  generic factors and “risk premia  factors ,” which have earn ed a persistent 
significant premi um over long periods  and reflect exposure to sources of systematic risk . All of the 
Fama -French factors count as risk premia factors since the aim of those original studies was to isolate 
asset pricing driver s.  However, not all of the Barra Risk Model facto rs are candidate factors since the 
purpose of those models focuses on forecast ing risk and explaining fund performance.  
In another vein, there are well -known alpha signals such as earnings revisions or earnings momentum, 
which have been used over the years by active managers to generate excess returns.  These stock 
characteristics are typically called “alpha signals” becaus e they do not explain risk well (i.e., they are not 
volatile) but do earn persistent premia over time.   In our nomenclature, alpha signals could potentially  
050100150200250Cumulative Returns
Value factor Momentum factor Growth factor Liquidity factor

---
## Page 8

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
8 of 33 be candidates for risk premia factors though they must, going back to the previous section, have s trong 
theoretical foundations that support their existence.  
Factors Are Important in Explain ing Manager  Returns  
In addition to historically exhibiting excess returns above the market , an equally important rationale for 
factor  investing is the wealth of evidence that they can account for a significant portion of mutual fund 
returns and institutional active fund returns .  Empirical studies  confirm that it is difficult for active 
managers to earn alpha .  Studies by Malkiel (1995) , Gruber (1996) , Wermers ( 2000, 2003), and Jones 
and Wermers (2011)  found that the median active manager generally does not outperform the cap 
weighted benchmark net of fees and even the small subset of those who do outperform are only able to 
maintain that outperformance for short  periods .   
Studies have also found  that active managers often tilt their portfolios towards  well-known fac tors such 
as Value and Size and that these tilts account for a substantial portion of managers’  returns over market 
capitalization weighted  benchmark s.  For instance, Fama and French (2010 ) found  that mutual funds  in 
aggregate  (CRSP database)  experienced  net returns that underperform ed the Fama -French factor  
benchmarks  by about the costs in expense ratios  from 1984 to 2006 .  Ang, Goetzmann and Schaefer  
(2009)  applied a  similar analysis to the Norwegian Government Pension Fund’s active returns and f ound  
that although added value from active management was still net positive, much of the behavior of the 
Fund’s small active return could  be explained in ter ms of systematic factors.    Recently, Mok, Bender, 
and Hammond (2013) show ed that traditional Fam a-French factors account ed for roughly 50% of 
average alpha using US institutional fund returns.13 
In fact, two of the  systematic factors, Value and Size , form  the basis of what has become a fund 
categorization standard -- “style box investing .”  Style box investing, sometimes referred to as style 
investing, was first popularized by Morningstar in 199214 and is a framework in which institutions 
allocate to manage rs within style segments (large/mid/small and value/growth) .  In fact, style investing 
was originally based on the research of Sharpe (1988, 1992)  who identified the importance of these 
factors in driving fund returns.15  
 
  
                                                           
13 Manager returns were sourced from eVestment from March 2002 to March 2012.  
14 http://news.morningstar.com/pdfs/FactSheet_StyleBox_Final.pd f 
15  Arguably Sharpe’s and other similar empirical studies became the foundation for the“Morningstar Style Box” in 1992.  

---
## Page 9

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
9 of 33 II. How Likely is it that Excess Ret urns to Risk Premi a 
Factors will Persist in the Future?  
A question that comes up repeatedly  from institutional investors is “how likely are the factors ’ excess 
returns  to pers ist in the future?”  There is a vigorous debate about this question across academics and 
practitioners alike, but the short answer is, it depends on what forces have driven a factor historically 
and whether those forces will continue to persist.   
What Drives Factor Returns: Systematic  Risk vs. Systematic Errors  
In general, there are two main camps in the debate over what drives factor returns —one based on the 
view that markets are efficient and that factors reflect  “systematic” sources of risk , and one based on 
the view that investors either exhibit behavioral biases or are subject to different constraints (e.g., time 
horizons, ability to use leverage, etc.) .   
In the first camp, the term “systematic” refers to the fact that risks to these stock traits cannot be 
diversified away (in the  true spirit of Ross’ (1976) APT Model).  This argument is consistent with 
“efficient markets theory” which assumes markets are efficient and investors are rational.  Here, factors 
earn excess returns because there is “systematic risk” attached to them.  For example, some have argued 
that the small cap premium is return earned for exposure to companies that are less liquid  (Liu, 2006) , 
less transparent  (Zhang , 2006) , and more likely to be distressed  (Chan and Chen , 1991 ; Dichev , 1998) . 
Others have argued that factors like Value, Size, and Momentum are linked to important 
macroeconomic factors such as growth and inflation and because of their sensitivity to shocks in the 
economy, must bear a return premium ( Winkelmann et al., 2013 ).  
In the second camp, fac tors are thought to earn excess returns because of investors’ “systematic 
errors.”  One subgroup of this camp, rooted in the “behavioral finance” literature , suggest s that 
investors exhibit b ehavioral biases due to cognitive or emotional weaknesses.  Examp les include  chasing 
winners, over -reacting, overconfiden ce, preferring “familiar” investments such as securities of the 
companies they work for or the country they live in (“home bias”) , and myopic loss aversion .  If enough 
investors exhibit these biases, as long as it is prohibitively costly for rational investors to arbitrage these 
biases away, it can lead to the factor anomalies we observe.  
Within this second camp, another subgroup has tied factor performance to investor constraints  and 
frictions /flows t hat arise from regulatory and industry practice .  In these studies, anomalies can arise 
from investors behaving rationally but subject to constraints.   For instance, consider different investor 
time horizons.  Studies have shown that stocks with low liquidity earn a premium over long horizons (10 
years plus) since most investors have shorter horizons (3 - and 5 -year horizons) and prefer stocks that 
are liquid over the shorter horizons. Investors with longer horizons earn a premium for bearing this 
horizon risk.   Other examples have applied constraint -based arguments for Low Volatility and 
Momentum.  For instance, Baker et al. (2011) cite the use of institutional benchmarks, and the 
subsequent preference for relative returns, as one reason why the low volatility premium exists.  
Dasgupta, Prat and Verardo (2011) argue that  reputation concerns cause managers to herd, and this 
generates  momentum under certain circumstances .16  
In fact, many of the well -known factor s have multiple theorie s supporting them.  Exhibit 5 summarizes 
main theories proposed for factor anomalies.  
                                                           
16 Specifically that the market makers trading with the managers  are either monopolistic or myopic . 

---
## Page 10

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
10 of 33 Exhibit 5: Theories Behind the Excess Returns to Systematic Fac tors 
Systematic Factors   Systematic Risk -based Theories17 Systematic Errors -based Theories18 
Value   Higher systematic (business cycle) 
risk   Errors -in-expectations  
 Loss aversion  
 Investment -flows -based theory  
Low Size (Small Cap)   Higher systematic (business cycle) 
risk  
 Proxy for other types of 
systematic risk   Errors -in-expectations  
Momentum   Higher systematic (business cycle) 
risk 
 Higher systematic tail risk   Underreaction and overreaction  
 Investment -flows -based theory  
Low Volatility   N/A  Lottery effect  
 Overconfidence effect  
 Leverage aversion  
Dividend Yield   Higher systematic (business cycle) 
risk  Errors -in-expectations  
 
Quality   N/A  Errors -in-expectations19 
 
For example, let’s consider the theories behind the Value factor.  V alue investing has been widely 
discussed since Graham and Dodd first wrote about it 1934 (“ Security Analysis ”).  The Value factor 
captures the positive link between stocks that have low prices relative to their fundamental value and 
returns in excess of the capitalization  weighted benchmark.  There are several explanations for the 
existence of this effect.  In the efficien t ma rkets view, the value premium is compensation for higher real 
or perceived risk.  Cochrane (1991, 1996)  and Zhang (2005) suggest that contrary to their leaner more 
flexible , growth counterparts, value firms have less flexibility to adapt to unfavorab le eco nomic 
environments .  Chen and Zhang (1998) later found that value stocks are riskier due to their high financial 
leverage and large uncertainty in future earnings.  Recently,  Winkelmann et al. (2013) show value and 
small cap portfolios are more immediately sensitive to economic (real GDP) shocks than growth and 
large cap portfolios.  The premium to value can consequently be viewed as compen sation for macro risk. 
From a behavioral perspective, the premium may exist as a result of loss aversion and  mental 
accounting biases .  According to Barberis and Huang (2001), investors become less concerned about 
future losses on stocks with recent good performance because any losses will be cushioned by prior 
gains (“loss aversion” bias).  This bias induces in vestors  to perceive the stock to be less risky than before 
and discounts its future cash flows at a lower rate.   Conversely, if a stock performs poorly in the recent 
                                                           
17 These include all efficient markets -based theories which assume investors are fully rational.  
18 These include behavioral theories that assume investors are not fully rational as well as constraint -based theories that assume investors are rational but oper ate 
under constraints.  
19 Investors  may  mistakenly valu e stocks  based on reported earnings if reported earnings are not reflective of a company’s true fundamentals.  

---
## Page 11

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
11 of 33 past, investors will raise its discount rate.  Th is results in a value premium i n the cross -section  of stocks 
since a stock with a  high price -dividend ratio (a growth stock)20 is often one that has done well in the 
past,  accumulating prior gains for the investor who then views it as less risky and requires  a lower 
average return. A stock wit h a low price -dividend ratio (a value stock) has  often had dismal prior 
performance ; an investor  may now view it as riskier,  and require a higher future  return. Lakonishok, 
Shleifer and Vishny (1994) proposed other behavioral biases that may help explain t he Value premium 
such as investors extrapolating past growth into the future, chasing high -flying glamour stocks, or simply 
overreacting to news.  
More recently, using a n institutional framework /constraint -based argument, Vayanos and Wool ley 
(2011) propose  that value and momentum effects arise because negative sh ocks to assets’ funda mental 
values trigger outflows from funds holding those assets. Outflows cause asset sales, which  amplify the 
shocks’ negative effects. If the outflows are gradual because of in vestor inertia or  institutional 
constraints, then the amplification is also gradual a nd momentum effects arise. More over, because 
flows push prices away from fundamental value, value effects also arise. Both effects  arise  despite 
investors and fund manager s being rational.  
The examples discussed above represent just a small part  of the wealth of research on the value 
premium.    Additional references and d iscussions of other factors can be found in Appendix A.  
Assessing the Likelihood of Future  Performance  
For institutional investors  evaluating factor  allocations , arguably the most critical part of the process for 
adopting the approach is forming a view or belief  about what drives the factor (s) in question .  In 
practice , this first step often focuses on assessing the academic literature and the theories behind what  
drives excess returns to factors.  
For institutional investors who subscribe to the “systematic risk” perspective, a factor can potentially 
persist indefinitely if it is actually  compensation for bearing  undiversifiable  risk.  For those who subscribe 
to the “ behavioral bias ” perspective, a factor can potentially persist as long as there are strong reasons 
why investors will continue to exhibit the behavioral biases in  question and their actions are too costly 
to be arbitraged away by rational investors  (or those who recognize these biases as such) .21  Lastly, for 
those who subscribe to the “constrain t-based” view, a factor can potentially persist only as long as those 
constraints remain in place.  
Regardless of their drivers, Melas, Briand, and Urwin (201 1) point out  that as factor  strategies become 
increasingly popular, institutional investors may over time begin to experience  relatively lower factor 
returns.   The reason  is that, u nlike market capitalization weighted portfolios, factor portfolios lack macro 
consistency. An index or a portfolio is macro  consistent if it can be held by all institutional investors 
without disturbing market prices. If all institutional invest ors tried to hold  the same factor portfolio, the 
factor would experience diminishing active returns relative to the market.  The interplay of investor flows 
and factor premia is complex particularly when viewed over time. While  the idea that increasing 
popu larity could  diminish future returns is widely appreciated,  investors should keep in mind that 
increased capital flows going into a popular strategy  will produce a tailwind to the strategy’s 
performance over the medium term, prior to any possible future reversal.  
                                                           
20 Note that Barberis and Huang (2001) define value/growth using price -to-dividend ratio but the argument would apply to other definitions such as price -to-book 
value and price -to-earnings.  
21 Some have argued that the return to factors observed in the data is roughly equal to the cost of arbitrage ; see Shleifer and Vishny (1997). In practice, inst itutional 
investors may have different costs of arbitrage; thus their ability to exploit certain return anomalies may vary as well. Ins titutions with low costs of arbitrage may be 
able to exploit mispricings which average investors may not. These points sh ould likely be factored into an evaluation of factor investing by large institutions.  

---
## Page 12

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
12 of 33 III. Factor Investing versus Market Cap Investing  
Some researchers have argued that market cap  weighting is  inherently flawed and have advocated 
replacing market cap allocations with factor allocations ; see for example, Arnott, Hsu, and Moore 
(2005).  O ur position is quite the opposite.  First, a market capitalization weighted index reflect s the 
available opportunity set of equity investments as well as the aggregate holdings of all investors.  If an 
investor wants to understand how equities have perform ed, the best gauge is a market  cap weighted 
benchmark .22  Second, market cap investing , the strategy that replicate s a market cap index, is unique in 
being macro -consistent, meaning it is the only portfolio that all investors can hold.   
Factor indexes  do n ot reflect the full equity opportunity set and they are not macro consistent .  Instead, 
they represent strategic tilts away from market capitalization weighted benchmarks.  Exhibit 6 shows 
one way to view factor indexes  relative to the market capitalization weighted index using the MSCI 
World Index as an example.  Some factors (and factor combinations) have higher returns and higher 
volatility while others have higher returns and lower volatility. They represent active d ecisions away 
from the market capitalization weighted index.  One intuitive way to view them is in the rubric of 
traditional active funds (e.g., defensive, balanced, and dynamic strategies).  
Exhibit 6: Factors Represent Strategic Bets Away from the Market Capitalization Weighted Index (Return 
and Risk, June 1988 to June 2013)  
 
Note: The strategies in Exhibit 6 are equally weighted combinations of the MSCI Factor Indexes  shown in parentheses. VW = MSCI World Value 
Weighted Index, EW = MSCI World Equal Weigh ted Index, Qual = MSCI World Quality Index, Mom = MSCI World Momentum Index, MV = MSCI 
World Minimum Volatility Index. All are MSCI Factor Indexes  based on the MSCI World Index.  
In sum, a market capitalization weighted index is the only appropriate candida te for a truly passive, 
macro consistent, buy and hold investment strategy that aims to capture the long term equity risk 
premium with structurally low turnover, very high trading liquidity and extremely large investment 
capacity . In contrast, investing i n factors represents active views  away from the market portfolio and 
investors must form their own belief about what explains the premium and whether it is likely to persist.   
Thus, like traditional active strategies, factor index strategies should be asse ssed in the long run against 
a market capitalization weighted benchmark.   
                                                           
22 Moreover, market capitalization weighted can be viewed as the equilibrium portfolio if investors are rational.   
6.0%7.0%8.0%9.0%10.0%11.0%12.0%
12.0% 13.0% 14.0% 15.0% 16.0%Annualized Return
Annualized RiskMSCI WorldDefensive 
Strategy
(MV, Qual, VW)Dynamic
Strategy
(VW, EW, Mom)Balanced Strategy
(MV, Qual, VW, EW, Mom )

---
## Page 13

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
13 of 33 IV. Is Factor Investing A Free Lunch? The Importance 
of Factor Cyclicality  
A key element  of factor investing is  factor cyclicality.  While factor indexes  have exhibited excess risk -
adju sted returns over long time periods, over short horizons factors exhibit significant cyclicality, 
including periods of underperformance.  Exhibit 7 shows that  each of the factor indexes  has experienced 
at a minimum a consecutive two-to-three year period of  underperformance .  Some factors historically 
have undergone even longer periods; the Small Cap or Low Size factor (captured by the MSCI World 
Equal Weighted Index in the exhibit) went through a six -year period of underperformance in the 1990s.   
Exhibit 7: All Systematic Factors are Cyclical (Cumulative Relative Returns, June 1988 to June  2013)  
 
Thus, there is no free lunch attached to factor investing.  Given strong anecdotal evidence that the 
majority of investors have relatively shorter horizons, their  cyclicality may in fact be one of the reasons 
they have not been arbitraged away.  Investors with shorter horizons would not be able to benefit from 
the full cycle required for factor investing.  Some may argue the premia exist to reward long -horizon 
inve stors for bearing that risk.  
A key part of the decision process for institutional investors implementing factor allocations  is what to 
do about the cyclicality.  Possible approaches include the following : 
 Setting an appropriately long time horizon  
 Establis hing an explicit timing mechanism for the initial investment ; and  
50100150200250300
88 89 90 91 92 93 94 95 96 97 98 99 00 01 02 03 04 05 06 07 08 09 10 11 12 13
Risk Weighted/World Value Weighted/World Min Volatility/World Equal Weighted/World
Quality/World Momentum/World High Div Yield/World

---
## Page 14

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
14 of 33  Adopting a multiple factor approach and employing factors that diversify each other  
The first is difficult in practice because the horizon required would typically be far longer than most 
institution’s strategic reviews.   Only institutional investors with extremely long time horizons (15 years 
and up for most of the factors shown in Exhibit 7) would be arguably insensitive to the timing of entry.  
The second option is challenging since facto rs, like markets, have been documented to be extremely 
hard to time.  M ost institutions would rather avoid timing decisions given their inherent difficulty.  
The third is the most straightforward option.  While all factor s have been  historically cyclical, their 
periods of underperformance have not coincided .  For instance, during the peri od between 2001 and 
2007, the MSCI World Momentum , MSCI World Value Weighted, MSCI World Risk Weighted, and MSCI 
World Equal Weighted Indexes  all outperformed  the MSCI World Index, but the MSCI World Quality 
Index underperformed. From 2007 -on, in contrast, the MSCI World Quality Index outperformed  while 
the MSCI World Momentum and MSCI World Value Weighted Indexes  did not fare as well .   Combining 
Quality with Momentum and Value Weighted factor indexes  for instance can yield a “smoother ride” 
and diversify across multi -year cycles.  Or said another way, e mploying multiple factors  is one way to 
address the ir cyclicality.  In the second paper of the series “ Deploying Multi -Factor Index Allocations in 
Institutional Portfolios ”, we discuss in more detail the allocation of equit y portfolios across multiple 
factors. 
V. Capturing Factor s Through Allocations to 
Investable Indexes  
The original studies on factors were intended to identify which stock characteristics explained returns.  
These studies were not concerned with whether th ose factors were actually investable.   Specifically, t he 
factor  portfolios constructed  by the academics in these studies were not designed  for actual 
implementation.   For instance, the Fama -French portfolios include all listed equities (in the US, listed on 
NYSE and AMEX) including many small illiquid names, are pure long/short portfolios with no 
accommodation to the size of short positions, and are rebalanced monthly leading to turnover that is 
considerably higher than institutional benchmarks.  In other words , because these factor studies did not 
assume investors were necessarily investing in these factors, the factors they described did  not, nor 
were they meant to,  take into account features key to implementation: transaction costs, liqu idity, 
investability, and capacity.  
Until recently, the ability to capitalize on factors could only reasonably be done by active managers.  
Value investing and small cap investing have been staples of active management for dec ades .  But over 
the last decade, index providers rec ognized that factors  could be captured in transparent rules -based 
ways.  Investors realized  that factor strategies  could outperform the market similar to their theoretical 
factor counterparts while having strong liquidity and investability characteristics.23 Today , these indexes  
go by a number of names -- alternative beta, smart, b eta, fundamental indexing, etc.  
What has this ability to capture factors through indexation meant for institutional investors?  Factor  
indexes  could , in fact,  revolutionize the inv estment industry by providing a new way  of investing beyond 
traditional market capitalization weighted portfolio and active portfolios.   Factor indexes  could provide:  
                                                           
23 Melas, Briand, and Urwin (2011) first discussed ways to capture factors through transparent rules -based long -only investable portfolios.   

---
## Page 15

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
15 of 33  More relevant benchmarks:  Assigning an active manager a more relevant benchmark means 
investors can more accurately gauge what active managers are adding  
 Potentially more  cost-effective implementation choices:  Funds that passively track these 
indexes  can now potentially deliver re turns previously only available through activ e 
management at potentially lower fees  
 Transparent implementation choices:  Funds that passively track these indexes  can now be used 
in lieu of more  opaque active options with  positive i mplications for risk management  
The benefits to institutional investors  of factor indexes  could be  significant . As illustrated in Exhibit 8, 
factor allocations can be implemented in simple and low cost ways like traditional passive market cap 
weighted allocations.  We note her e that factors do not replace active management (at least fully) 
because many value -added activities such as stock selection cannot be replicated by factor indexes .   
Exhibit 8: Passive Factor Allocations Combine Attractive Elements of Both Traditional Pas sive and Active  
Mandates  
 
 
Beyond cost implications, factor indexes  offer a fully transpa rent way to passively invest in factors.  
Transparency alleviates the well -known problem of manager style drift and also has positive implications 
for risk management. Institutions have full “look -through ” of how exposed the ir portfolios are to the 
factor s. 
The advent of factor indexes  also heralds a change in traditional investing par adigms . As shown in 
Exhibit 9, index -based factor allocations could imply a significant shift in the way institutional investors 
view the asset allocation and active management process.  Instead of focusing on diversif ying across 
active managers in multipl e alpha mandates, institutions would focus first on diversification across 
multiple index mandates .  Risk control  would then  focus principally on managing exposure to these 
factors  while a ctive management would be defined more narrowly as sources of return  that exclude 
factors.  


---
## Page 16

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
16 of 33 Exhibit 9: Potential Redefinition of the Way Institutions Invest  
 Current Framework  Possible New Framework  
Strategy   Diversification across managers in 
multiple alpha mandates  
 Asset owner manages strategy 
through asset allocation and 
manager selection   Diversification across strategies in 
multiple factor index mandates  
 Asset owner manages strategy through 
factor allocation  
Roles and Tools   Alpha is defined broadly: bottom -
up skill, top -down sources and 
timing  
 Risk control is principally through 
asset allocation and manager 
diversification   Alpha is defined more narrowly 
excluding factors  
 Risk control focuses on managing 
exposure to risk factors  
Economics   Active mandates dominate the 
portfolio’s costs  
 Large line -up of external 
managers with small internal 
asset owner staff   Active mandates co -exist with factor  
mandates producing lower costs  
 Larger internal staff managing more 
assets with fewer external managers  
  

---
## Page 17

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
17 of 33 VI. An Illustration with MSCI Factor Indexes  
MSCI’s family of factor indexes , comprising the six key factors —Value, Low Size, Low Volatility, High 
Yield, Quality and Momentum —are shown in Exhibit 1 0.  These indexes  are constructed for flagship 
global indexes  like the MSCI ACWI, MSCI World, MSCI Emerging Markets, and MSCI EAFE Indexes , as well 
as many individual country indexes .   
Exhibit 1 0: MSCI Family of Factor Indexes  
Systematic Factors   MSCI Indexes   
Value   MSCI Value Weighted Indexes :  Capture Value factor by weighting 
according to four fundamental variables (Sales, Earnings, Cash Flow, Book 
Value)  
Low Size (Small Cap)   MSCI Equal Weighted Indexes : Capture low size effect by equally weighting 
all stocks in a given parent index  
Momentum   MSCI Momentum Indexes : Reflect the performance of high momentum 
stocks by weighting based on 6 - and 12 -month momentum scaled by 
volatility  
Low Volatility   MSCI Minimum Volatility Indexes : Reflect empirical portfolio with lowest 
forecast volatility using minimum variance optimi zation   
 MSCI Risk Weighted Indexes :  Capture low volatility stocks by weighting 
based on the inverse of historical variance  
Dividend Yield   MSCI High Dividend Yield Indexes : Select high dividend stocks with screens 
for quality and potential yield traps  
Quality   MSCI Quality Indexes :  Capture high quality stocks by weighting based on 
debt -to-equity, return -on-equity, and earnings variability  
 
Just as “there is more than one way to skin a cat,” there is indeed more than one way to capture 
systematic factors through indexes .  Index methodology comprises  several aspects:  the choice of stock 
universe, weighting scheme, and rebalancing frequency.  All three have important implications for the 
traits investors care about in the resulting index --investability and liquidity, factor exposure, returns, 
risk, and tracking error . For instance, the index could contain all the names in the starting universe and 
merely reweight the names .  Alternatively, the index could contain a narrow subset of names.24  The 
former  would have lower tracking error, higher investability, but lower exposure to the pure factor and 
potentially lower returns.    
More generally, ther e is a tradeoff between the exposure to the factor (and potential returns) and the 
investability  of a factor index.  One can generally only achieve purer factor exposure by sacrificing 
investability and being willing to take on greater amounts of active ri sk.  Detailed discussion about 
                                                           
24   MSCI Factor Indexes span both types.  MSCI Factor Indexes  that contain a broad universe of names (denoted by having the term “Weighted” in the index name) 
usually con tain all the names in a broad “parent index” such as the MSCI ACWI Index and reweight the stocks (differently from market capitalization weighted) 
based on the desired factor characteristic.   These broad indexes  are characterized by very low tracking erro r and high degrees of investability.  

---
## Page 18

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
18 of 33 different index choices is discussed later in the second paper of this series “Depl oying Multi -Factor Index 
Allocations in Institutional Portfolios ”. 
Exhibit 11 shows key characteristics including the performance of some of the MSCI World Factor 
Indexes  for the period June 1988 to June 2013.  
Exhibit 11: MSCI World Factor Indexes  (Main Characteristics, June 1988 to June 2013)  
Index  Factor 
Exposures*  Total 
Return  Total 
Risk  Active 
Return  Active 
Risk  Annual 
Turnover  Pairwise 
Correl - 
ation  
MSCI World  -- 7.1 15.4 0.0 0.0 3.9 NA 
MSCI World 
Equal Weighted  Size 8.3 16.3 1.2 5.2 31.8  0.22 
MSCI World 
Minimum  
Volatility  Volatility  8.5 11.6 1.4 6.7 20.0  0.30 
MSCI World 
Value Weighted  Value  8.6 15.6 1.5 3.6 20.3  0.30 
MSCI World Risk 
Weighted  Size, 
Volatility  9.5 13.7  2.4 5.3 27.2 0.46 
MSCI World 
Quality  Growth, 
Leverage  10.9  14.0 3.8 5.9 27.6  0.13 
MSCI World 
Momentum  Momentum  10.4  15.9 3.3 8.5 127.5 0.03 
MSCI World HDY  -- 10.3  14.6  3.2 6.5 22.0  0.41  
* In the column “Factor Exposures” we show the Barra Global Equity Model (GEM2) factors which are statistically significant o n average (>+/- 
0.20), with the expected sign, since December 1997 . Note that there is no “Yield factor” in the GEM2 Model.   Instead, Yield is a component 
(with a weight of 10%) in the GEM2 Value factor. Turnover reported is the average annual one -way turnover based  on history from June 1988 -
June 2013 . 
Higher capacity indexes  include the MSCI Value Weighted Index.  As illustrated in Exhibit 17 using MSCI 
World variants, it exhibit s the lowest tracking error among the available indexes  since it hold s all the 
constitue nts of the parent index.  The other indexes  (the MSCI Momentum Indexes , MSCI Quality 
Indexes , and MSCI Minimum Volatility Indexes ) are more concentrated indexes , holding only a subset of 
the names in the parent index . These indexes  exhibit higher tracking errors and lower levels of 
investability.  (The MSCI Minimum Volatility Indexes  are turnover -constrained to 20% but other 
measures of investability are more similar to the MSCI Momentum and Quality Indexes .)  The MSCI 
Momentum and MSCI Quality Indexes  historically exhibited the strongest historical returns while the 
MSCI Minimum Volatility Indexes  exhibited sizable risk reduction.    
All the MSCI World Factor Indexes  shown in Exhibit 11 outperform the MSCI World Index over the 
perio d show n, June 1988 to June 2013.  Moreover, they all have turnover levels that are well within 

---
## Page 19

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
19 of 33 reason. For instance, assuming 50 bps in one -way trading costs, the cost of trading for the indexes  
would range between 20.3  basis points annually for the MSCI World Value Weighted Index to 12 7.5 bps 
annually for the MSCI World Momentum Index.  Both estimates are more than offset by their historical 
return premiums over this period – 150 bps and 33 0 bps respectively.   
Conclusion  
Factor investing is based on  the existence of factors that have earned a premium over long periods, 
reflect exposure to systematic risk, and are grounded in the academic literature.  Early financial theory 
established that for stocks, exposure to the market was a significant driver o f returns (e.g., the CAPM).  
Later, researchers like Barr Rosenberg, Eugene Fama and Kenneth  French  extended the CAPM to include 
certain systematic factors that also were important in explaining returns. Tilts towards these factors 
such as Value, Low Size,  and Momentum historically produce d excess long -term returns and there were 
strong theoretical foundations behind these factors.  
Until now, passive investing has focused on capturing market beta through market capitalization 
weighted indexes .  The only way  institutional  investors could get access to factors was through active 
management.   Indexation is opening a new way for f actor investing  today  by allowing investors to access 
factors through passive vehicles that replicate factor indexes .  MSCI Factor Indexes  provide access to six 
solidly grounded factors —Value, Low Size, Low Volatility, High Yield, Quality and Momentum .  These 
indexes  have historically earned excess returns over market capitalization weighted indexes  and 
experienced higher Sharpe Ratios.  
This paper is the first in a three -paper series focusing on factor investing.  In the next paper of this 
series, “Deploying Multi -Factor Index Allocations in Institutional Portfolios ”, we address the topic of 
allocat ing across factors and what role they play in the institutional portfolio.  
 
 
  

---
## Page 20

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
20 of 33 References  
 
Ang, A., W. N. Goetzmann and S. M. Schaefer (2009), “Evaluation of Active Management of the 
Norwegian Government Pension Fund – Global,” www.regjeringen.no . 
Arnott, Robert D., Jason C. Hsu, and Philip Moore (2005),  “Fundamental Indexation”, Financial Analysts 
Journal, Vol.61, No. 2 (March/April): 83 –99. 
Baker, Malcolm, Brendan Bradley, and Jeffrey Wurgler (2011), “Benchmarks as Limits to Arbitrage: 
Understanding the Low -Volatility Anomaly”, Financial Analyst Journal , Vol. 67, No. 1, pp. 40 –54. 
Barberis, N. and M. Huang (2001), “Mental Accounting, Loss Aversion and Individual Stock  Returns,” 
Journal of Finance 56, 1247 -1292.  
Carhart, M. (1997), “On Persistence in Mutual Fund Performance,” the Journal of Finance 52(1),  57-82. 
Chan, K. C., and Chen, Nai -fu (1991), “Structural and return characteristics of small and large firms,” 
Journal of Finance 46: 1467 –84. 
Chen, Nai -fu, Richard Roll, and Stephen Ross (1986), “Economic forces and the stock market”. Journal of 
Business  59: 383 –403.  
Chen, Nai -fu, and Feng Zhang  (1998), “ Risk and Return of Value Stocks ,” Journal of Business,  Vol. 71, No. 
4. 
Cochrane, John H.  (1991 ), "Volatility tests and efficient markets : A review essay," Journal of Monetary 
Economics, Elsevier, 27(3) : 463-485. 
Cochrane, John H. (1996), “ A Cross -Sectional Test of an Investment -Based Asset Pricing Model ,” Journal 
of Political Economy, 104.  
Connor, Gregory (1995), “The Three Types of Factor Models: A Comparison of Their Explanatory Power,” 
Financial Analys ts Journal, May/June 1995, Vol. 51, No. 3: 42 -46. 
Dasgupta, Amil , Andrea Prat, and Michela Verardo  (2011) , “The price impact of institutional herding ,” 
Review of Financial Studies, 24 (3) : 892-925. 
Dichev, I.D. (1998), “Is the Risk of Bankruptcy a Systematic Risk?”, Journal of Finance, 53: 1131 -1147.   
Fama, Eugene F. and Kenneth R. French (1992), “The Cross -Section of Expected Stock Returns,” Journal 
of Finance  47, 427 -465.  
Fama, Eugene F., and Kenneth R. French (1993), “Common Risk Factors in the R eturns on Stock and 
Bonds,” Journal of Financial Economics  33, 3 -56. 
Fama, Eugene F., and Kenneth R. French  (2010) , “Luck versus Skill in the Cross -section of Mutual Fund 
Returns”, Journal of Finance Vol. 65, No. 5.  
Graham, B., and Dodd, D. 1934. Security Analysis . New York: McGraw Hill.  
Gruber , M. (1996), “Another Puzzle: The Growth in Actively Managed Mutual F unds, ” Journal of  Finance 
52, 783 -810.  
Jones, R.C. and R. Wermers (2011), “Active Management in Mostly Efficient Markets,” Financial Analysts 
Journa l 67(6), 29 -45.  
Lintner, J. (1965), “ Portfolios and Capital Budgets ,” The Review of Economics and Statistics , 47(1), 13-37. 

---
## Page 21

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
21 of 33 Lakonishok, Josef, Andrei Shleifer, and Robert Vishny (1994), “Contrarian investment, extrapolation, and 
risk,” Journal of Finance 49: 1541 –78. 
Liu, W. (2006), “A liquidity -augmented capital asset pricing model,” Journal of Financial Economics 82(3), 
631-671.  
 
Malkiel (1995), “Returns from Investing in Equity Mutual F unds 1971 to 1991, ” Journal of Finance 50, 
549-572.  
Menchero, Jose (2010), “ Characteristics of Factor Portfolios ,” MSCI Barra Research Insights.  
Melas, D., Briand, R., R.Urwin  (2011 ), “Harvesting Risk Premia with Strategy Indices  – From Today’s 
Alpha to Tomorrow’s Beta ,”  MSCI Research Insight . 
Miller, Guy (2006), “ Needles, Haystacks, and Hidden Factors ,” Journal of Portfolio Management, Vol. 32, 
No. 2: pp. 25 -32. 
Mok, William, Jennifer Bender, and P. Brett Hammond (2013), “Can Alpha be Captured by Risk Premia?” 
forthcoming, Journal of Portfolio Management.  
Mossin, J . (1966), “ Equilibrium in a Capital Asset Market", Econometrica , 34, 768–783. 
Rosenberg, Barr, and Vinay Marathe (1976), “Common Factors in Security Returns: Microeconomic 
Determinants and Macroeconomic Correlates,” University of California Institute of Bu siness and 
Economic Research, Research Program in Finance, Working paper No. 44.  
Ross, Stephen (1976),  "The arbitrage theory of capital asset pricing ,” Journal of Economic Theory 13(3) , 
341–360.  
Sharpe, W illiam (1964), “ Capital Asset Prices: A Theory of M arket Equilibrium under Conditions of Risk ,”  
Journal of Finance 19 , 425 -442.  
Sharpe, William  (1988) , "Determining a Fund's Effective Asset Mix," Investment Management Review,  
September/October 1988, pp. 16 -29. 
Sharpe, William  (1992) , "Asset allocation: Management style and performance measurement," The 
Journal  of Portfolio Management, Volume 18, Number 2, Winter 1992, pp. 7 -19.  
Treynor, J. L. (1961), “Market Value, Time, and Risk.” Unpublished manuscript. Rough draft dated 
8/8/61, #95 -209.  
Vayanos, Dimi tri and Paul Woolley  (2011 ), “An institutional theory of momentum and reversal ,”  London 
School of Economics (LSE), Working paper.  
Vishny, Robert W. & Shleifer, A. (1997), “The Limits of Arbitrage,” Journal of Finance 52(1), 35 –55.  
Wermers, Russ (2000), “ Mutual Fund Performance: An Empirical Decomposition into Stock -Picking 
Talent, Style, Transactions Costs, and Expenses,” Journal of Finance, 55: 1655 -1695.  
Wermers, R.  (2003), “ Is Money Really ‘Smart’? New Evidence on the  Relation between Mutual Fund 
Flow s, Manager Behavior, and  Performance Persistence.” Unpublished paper, University of  Maryland 
(May). ” 
Winkelmann, Kurt , Raghu Suryanarayanan, Ludger Hentschel, and Katalin Varga (2013), 
“Macro‐Sensitive Portfolio Strategies: Macroeconomic Risk and Asset Cash‐Flows”, MSCI Market Insight, 
March 2013.  

---
## Page 22

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
22 of 33 Zhang, Lu  (2005 ), “The value premium ”, Journal of Finance 60, 67 –103.  
 
Zhang, X.F. (2006), “Information uncertainty and stock returns,” Journal of Finance 61(1), 15 -136.  
 
  

---
## Page 23

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
23 of 33 Appendix  
Appendix A: Additional Information about the Academic Literature  
There is a vast literature on systematic factors.  Subgenres which fall under the umbrella of systematic 
factors include asset pricing anomalies, stock market anomalies, multi -factor models, risk factor models, 
alpha signals, etc.  To start,  it is useful to begin with several good general references on  these issues : 
 “Dissecting Anomalies ”  by Eugene Fama and Ken French (2008)  
 “Explaining Stock Returns: A Literature Review ” by James L. Davis (2001)  
 “Market Efficien cy, Long -Term Returns, and Behavioral Finance ” by Eugene Fama (1997)  
 “The Efficient Market Hypothesis and It's Critics ” by Burton Malkiel (2003)  
  “The New Palgrave Dictionary of Economics” (2008) by Steven Durlauf and Lawrence Blume, 2nd 
ed. 
 “Anomalies a nd Market Efficiency” by G. William Schwert25 (Ch. 15 in Handbook of the 
Economics of Finance , by Constantinides, Harris, and Stulz, 2003)  
 “Investor Psychology and Asset Pricing,” by David Hirshleifer  (2001)26 
 
While the construction of factor models occupies a somewhat segregated landscape from the market 
anomalies literature, this research provides guidance on how alpha signals and risk factors are iden tified 
and estimated by quantitative manage rs.  Some g ood starting references include : 
 The Barra Equity Risk Model Handbook  
 Active Portfolio Management: A Quantitative Approach for Producing Superior Returns and 
Controlling Risk  by Richard Grinold and Ronald Kahn  
 Modern Investment Management: An Equilibrium Approach  by Bob Litterman  
 Quantitative Equit y Portfolio Management: Modern Techniques and Applications  by Edward 
Qian, Ronald Hua, and Eric Sorensen  
Additional references are provided below for the main systematic factors discussed in this paper: Value, 
Low Size, Momentum, Low Volatility, Quality, a nd Yield.  
Value  
The Value factor captures the positive link between stocks that have low prices relative to their 
fundamental value and returns in excess of the capitalization -weighted benchmark. A  value strategy 
consists of buying stocks that have low  prices normalized by  some indicator of company fundamentals 
(such as book value, sales, earnings, or dividends, etc.) and selling stocks that have  high prices ( also 
normalized). Value  investing has been widely discussed since Graham and Dodd first wrote about  it 1934 
(“Security  Analysis ”).  It was later formalized by Basu (1977), who was the first to test the notion that 
value -related variables might explain violations of the  CAPM. He found a significant positive relation 
between E/P ratios and average returns for US stocks that  could not be explained by the CAPM. Later 
studies documented a significant positive relation between Book -to-Price ratio s and average returns as 
well; see Rosenberg,  Reid and Lanstein (1985) and  DeBondt and Thaler (1987)  for example.  Other 
measures of value have also been found to have positive excess returns including value ratios that use 
cash flow.  The V alue effect in its many forms has been  reproduc ed by numerous researchers for many 
different sample periods and for most major securities markets  around the world (see Hawaw ini and 
                                                           
25 http://schwert.ssb.rochester.edu/hbfech15.pdf  
26 “Investor Psychology and Asset Pricing,” David Hirshleifer, Journal of Finance, 56 (4), August, (2001):1533 -1597.  

---
## Page 24

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
24 of 33 Keim (2000) ).  We note that critics of the value premium have argued that empirical evidence is based 
on data mining and p oint out the sample -dependency of empirical studies; see for instance Black (1993).  
A discussion of theories behind the Value premium appears in Section II.  
Low Size 
The S ize factor captures the excess returns of smaller firms  (by market capitalization) relative to their 
larger counterparts  even after adjusting for betas  and other factors like Value . This result was first 
discovered by Banz (1981), and triggered a vast literature on the topic. Banz (1981) showed smaller 
companies listed on the NYSE on avera ge delivered higher risk -adjusted returns than larger companies 
using data from 1936 -1975.  This “size effect” was later generalized by the Fama -French Three Factor 
Model in the early 1990’s.  
The small cap  premium  has been found to exist even after influen ces are controlled for: market beta, 
the value effect, the momentum effect, liquidity effects, leverage, and so forth.  Moreover, the 
phenomenon has been identified across the world in both developed and emerging markets; see Rizova 
(2006)  for a synopsis of  work applying the Fama -French framework to individual countries such as 
Australia, Canada, France, Germany, and the UK .  
There are several th eories explaining this phenomenon, and the debate continues today . In the efficient 
market view, Fama and French ( 1992, 1993) originally hypothesized that small caps have higher 
systematic risk which earns them a higher return premium. Subsequent researchers suggested that size 
may proxy for other unobservable and underlying risk factors associated with smaller firms such as 
liquidity (Amihud, 2002), information uncertainty (Zhang, 2006), financial distress (Chan and Chen, 1991) 
and default risk (Vassalou and Xing, 2004). Chan, Chen and Hsieh (1985) in particular argue the most 
powerful factor in explaining the size ef fect is the spread between low and high quality corporate bonds, 
which is essentially an indication of the macro environment and default risk.  
From the behavioral perspective, similar behavioral arguments for the value premium are also made for 
the size ef fect, i.e. incorrectly extrapolating past into the future, chasing high -flying glamour stocks, or 
overreacting to news ; see (Lakonishok, Shleifer, and Vishny, 1994 ). The explanations of the size effect 
remain highly debated.  
Skeptics of the size premium po int to the survivorship bias in the relevant research, which typically does 
not include busted companies. This seems a legitimate claim given small companies often have 
sustainability issues. Others argue the size premium is difficult – if not impossible – to capture in the real 
world given the low trading volume of small cap stocks.  
 
 
  

---
## Page 25

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
25 of 33 Momentum  
The M omentum factor reflects future excess returns to stocks with stronger past performance.  In other 
words, stock prices tend to exhibit trend over certain horiz ons; winner s continue to win and losers 
continue to lose . Jegadeesh and Titman (1993) led one of the first seminal studies on momentum in the 
US stock market, which shows buying past winners and selling past losers produced significant 
“abnormal” returns i n 1965 -1989. In a study of mutual fund performance, Ca rhart (1997) expanded the 
Fama -French Three Factor Model to a Four -Factor Model to include momentum as an additional 
explanatory variable.  Rowenhorst (1998) found an internationally diversified portfol io of past winners 
outperformed a portfolio of past losers by about 1% per month, using a sample of 2,000 European 
stocks from 1978 to 1995. Fama  and French (2012) found strong momentum returns in North America, 
Europe, and Asia Pacific but not Japan in th e sample period of 1989 -2011. They also confirmed the 
robustness of the Four Factor Model, i.e. momentum is a persistent factor not captured by either value 
or size.  Empirically the Four Factor Model seems to work best with global stocks excluding micro c aps.  
Asness (1995, 1997)  not only confirmed earlier findings on the momentum effect at the country level, 
but also showed that winners and losers tend to revert over the long -term, i.e. winners 
underperforming and losers outperforming in 3 -5 years out. In  fact, empirical research suggests the 
momentum effect is most prominent in the following 3 -12 months, after which it will likely disappear. 
This implies the momentum strategy requires relatively high turnover in order to work. Geczy and 
Samonv (2013) cond ucted a 212 -year backtest of the momentum strategy in the US market, which 
shows the momentum effect is statistically significant and not a product of data -mining.  
The theory underlying this premium is still matter of extensive discussion. Unlike value and  size, there is 
no satisfactory efficient markets -based theory to explain the momentum factor. The most widely cited 
theories are all behavioral. Investors either over -react (Barberis, Sheleifer and Vishny 1998, and Daniel , 
Hirshleifer and Subrahmanyam 199 8) or under -react to news (Hong, Lim and Stein 2000), both of which 
may lead to the momentum effect under varying assumptions. Without diving deep into behavioral 
finance, these “irrational” reactions are driven by overconfidence, self -attribution, conserv atism bias, 
aversion to realize losses, representative heuristic (tendency to identify an uncertain event by the 
degree to which it’s similar to the parent population), or simply lack of analyst coverage. Or as another 
example, Dasgupta, Prat and Verardo (2011) argue that  reputation concerns cause managers to herd, 
and this generates  momentum under certain assumptions.27 More recently, Vayanos and Woolley 
(2011) propose a framework based on the dynamics of institutional investing rather than individual 
biases.  In their framework, momentum and  value effects jointly arise because of flows between 
investment funds. Negative shocks to assets’ fundamental values trigger outflows from funds holding 
those assets  while o utflows cause asset sales, which  amplify the shocks’ negative effects. If the outflows 
are gradual because of  institutional constraints  or inertia , then momentum effects arise. More over, 
because flows push prices away from fundamental value, value effects also arise.  
Common criticisms of the momentu m strategy include data mining, high turnover, crowded trading, and 
the risk of a sudden reversal – which is difficult to predict and manage. History shows the probability of 
a short -term reversal is positively correlated with volatility, and forecasting v olatility is anything but 
easy. In addition, like other factor  strategies, momentum could go through an extended period of 
negative performance. This suggests it’s perhaps better to combine momentum with other factor 
strategies than using it alone. Asness,  Moskowitz and Pedersen ( 2010 ) supported this argument with a 
study on the interaction between value and momentum. They found potential diversification benefits 
                                                           
27 Specifically that the market makers trading with the m anagers  are either monopolistic or myopic . 

---
## Page 26

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
26 of 33 from combining the two strategies as value and momentum can be negatively correlated within and  
across asset classes.  
Low Volatility  
The Low Volatility factor captures excess returns to stocks with lower than average volatility, beta, 
and/or idiosyncratic risk.  The empirical evidence for this factor is a puzzle since it is clearly at odds with 
one of the most basic principles in finance, that higher volatility is associated with higher returns (Blitz 
and Vliet, 2007) . While the CAPM model asserts that riskier assets should earn higher returns, research 
around the Low Volatility factor shows that the  opposite is true --less risky stocks outperform the 
market.  
Haugen and Baker’s (1991) critique of capitalization -weighted benchmarks was the first to document 
the effect. They showed that for the 1972 to 1989 period, low volatility stocks in the US performed 
better than the capitalization -weighted alternative.   Later, Chan, Karceski and Lakonishok (1999), 
Schwartz (2000), Jagannat han and Ma (2003) and Clarke, de Silva and Thorley (2006) confirmed these 
results for the US market  using a range of volat ility measures .  Geiger and Plagge (2007), Nielsen and 
Subramanian (2008) and Poullaouec (2008) all find qualitatively similar results for glob al markets. Ang et 
al (2006, 2009) found  that the low volatility  effect persists both in the US and globally, bas ed on 
extensive periods of time (for US  stocks,  1963 to 2003 , and for international stocks, 1980 to 2003).  
Metrics used for identifying low volatility  stocks range along a broad spectrum, with realized volatility on 
one end and forecast volatility and corr elations on the other. Some operationalize low volatility  as low 
beta.  The metrics for identifying low volatility stocks also vary, with realized (historical) volatility on one 
end, and forecasted (implied) volatility and correlations on the other end. However, the research 
findings appear robust despite such differences.  
The low volatility anomaly clearly contradicts the EMT and assumptions of the CAPM. The explanations 
here are mostly behavioral.  The most common explanation is the “lottery effect”, i.e. people tend to 
take bets with a small expected loss but a large expect ed win, even though the probability of a loss is 
much higher than the win, and the weighted average of the outcome may be negative. This is similar to 
buying a lottery whereby the customer pays a small sum for potentially winning a large amount of 
money al beit at a very low probability. Some argue that buying a low price, volatile stock is similar to 
buying a lottery with similar risk -return payoffs, and thus it can be an attractive bet for investors. 
Therefore investors often overpay for high volatility st ocks and underpay for low volatility stocks due to 
the “irrational” preference for volatile stocks.  
Other behavioral explanations include:  
 Representativeness – The success of a few, well publicized high volatility stocks make all volatile 
stocks seem good  investments, and the speculative nature of such stocks is often ignored by 
investors.  
 Overconfidence – Investors are overconfident in their ability to forecast the future, and the 
extent of their differences in opinions are higher for stocks with more unc ertain outcomes (high 
volatility stocks). In the real world, it is easier and more practical to express a positive view (buy) 
than a negative view (short sell). This means the pessimists cannot effectively express their view 
of a volatile stock, leaving on ly the optimists to keep driving up its price. The result is overpricing 
and lower returns for high volatility stocks.  
 Agency issue – There appears to be a natural tendency to avoid low volatility stocks in asset 
management because there is often less atte ntion and support (in the form of research and 
trading) for low volatility stocks.  

---
## Page 27

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
27 of 33  Asymmetric behaviors in bull vs. bear markets – Investors behave differently in bull markets vs. 
bear markets. When the market is going down, there is often a huge dispersi on of beta between 
low volatility and high volatility portfolios (i.e. the low volatility portfolio will have much lower 
beta). Therefore, the low volatility portfolio experiences much less drawdown than the high 
volatility portfolio. When the market is go ing up, this dispersion is not so great, and thus the low 
volatility portfolio u nderperforms only slightly. Net, the low volatility portfolio still does better 
over the long term (Sefton  et al. , 2011 )28 
Finally, Baker, Bradley, and Wurgler (2011) propose a theory that is not based on behavioral bias but 
instead based on the use of  equity benchmarks. Low volatility stocks often have lower betas, and 
overweighting them leads to higher tracking errors for institutional investors. S uch tracking errors need 
to be  justified by sufficient excess returns (alpha).  In other words, institutional investors cannot buy low 
volatility stocks indiscriminately. To a certain extent, the benchmark issue prohibits institutional 
investors from fully exploiting the low volatility  anomaly.  
Critics of the volatility factor argue that buying a basket of low volatility stocks may lead to unintended 
bets on valuation and sectors, because such stocks tend be expensive and concentrated in just a few 
sectors (such as financials). There is  also a philosophical argument that low volatility investing is 
successful at reducing risk but lacks an investment thesis on returns.  Therefore technically speaking it is 
a risk management as opposed to an investment tool.  
Quality  
The Quality factor aims  to capture the excess return of “high quality” companies vs. the market. This has 
been a widely adopted concept in fundamental analysis (stock selection) but a relatively new 
phenomenon in quantitative investments. The main challenge is how to define the “quality” factor 
consistently and objectively using quantitative indicators.    The quality of companies is a highly 
subjective matter. Though there is no standard definition, it is commonly associated with a company’s 
competitiveness, efficiency, transpare ncy, growth, financial and operating leverage, profit sustainability, 
and return -on-equity (ROE).   
Sloan (1996) was one of the first to validate the excess returns to high earnings quality stocks, where 
accruals proxy for earnings quality.  (Low accruals reflect higher earnings quality).  Besides accruals, 
other measures of earnings quality include, earnings persistence, smoothness, and loss avoidance, and 
they are reviewed by Dechow, Ge, and Schrand (2010)29. These other measures have been related to 
stock  returns by Perotti and Wagenhofer (2011), although the general finding is that accruals have been 
the strongest quality -based predictor of stock returns.  In recent years, Bender and Nielsen (2013) and 
Kozlov and Petajisto ( 2013 ) have reconfirmed the accr uals effect for the 2000s.   Also, Asness, Frazzini, 
and Pedersen (2013) recently show that quality as measured by profitability, stable growth, and high 
payout ratio, has significantly higher risk -adjusted returns.  
More recently, some have argu ed that the original Dodd & Graham  and Buffett investing  styles include 
an important quality component .   “[T]he secret to Buffett’s success is his preference for cheap, safe, 
high -quality stocks combined with his consistent use of leverage to magnify return s while surviving the 
inevitable large absolute and relative drawdowns this ent ails” according to Frazzini, Kabiller and 
                                                           
28 This “minimal drawdown” advantage can be easily demonstrated as follows: A high volatility portfolio may go down 50% in value  in a bear market, and will need 
to go up 100% (double) in order to recover to its ori ginal value. However, a low volatility portfolio may go down only 30% in value, and need to go up only 43% to 
recover to its pre -crisis level. This puts the low volatility portfolio well ahead of the high volatility portfolio during the initial stage of a recovery.  
29 Chen, Novy -Marx and Zhang (2011) made an ambitious attempt to include ROE in an alternative three -factor model for explaining the cross -sectional stock 
returns.  

---
## Page 28

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
28 of 33 Pedersen  (2012).   In other words, the original “value” -based style of investing pioneered by Dodd & 
Graham is really one that favors stocks that appear to be safe and have high quality, but are priced as 
bargains.   Frazzini, Kabiller and Pedersen  (2012)  show that Berkshire Hathaway’s alpha becomes 
insignificant when controlling for “Betting -Against -Beta” and quality factors.  
There is very  little literature on why the Quality factor works. It’s also difficult to provide a unified 
theory since the definition of quality varies. According to the Fam a-French model, all systematic risks are 
ultimately economic risks. In light of this argument, i t is not difficult to see the connection between 
stock returns and quality measures such as financial leverage and earnings growth. Cam pbell, Polk and 
Vuolteenaho (2010 ) offered a form of this “fundamental” explanation, arguing the primary source of 
system atic risks of both growth and value stocks is the cash flow fundamentals as opposed to market 
sentiments. From a corporate finance angle, it is easy to see how firm quality impacts stock prices. For 
example, a well -run company often manages its capital car efully and reduces the risk of over -leveraging 
or over -capitalization. The steady growth in earnings will further reduce its need for capital market 
financing, which will support its stock price. This will trigger a positive feedback loop making the 
compan y more competitive in the eyes of its customers and investors.  
Critics of the Quality factor argue it is highly subjective and contain s behavior biases. Active managers 
are often strong proponents of the Quality factor but argue it can only be captured th rough 
fundamental analysis and stock picking.  
Yield  
The Yield factor aims to capture the outperformance of high dividend yield stocks.   Dividend yield is 
commonly used as a valuation tool and closely related to price -to-book and price -to-earnings ratios. 
Therefore, assuming the payout ratio is uniformly distributed. The compounding of dividend 
reinvestments also contribute s to the excess return of high dividend yield stocks. In addition, changes in 
the dividend tax regulations may also account for the divi dend factor.  
Blume (1980 ) found a positive relationship between the risk -adjusted returns and the expected dividend 
yield of dividend -paying stocks. Litzenberger and Ramaswamy (1979)  later confirmed there is a positive 
but non -linear relationship between stock returns and expected dividend yields, assuming investors 
have no knowledge of the future ex -dividend month. Fama and Fre nch (1988) found the dividend yield 
has more explanatory power for longer term returns over 2 -4 years. Tweedy, Browne Company LLC  
(2007) offered a summary of the empirical evidence of the dividend factor in both US and UK markets 
for over 40 years. Various attempts have been made to integrate the dividend yield into a model to 
forecast stock returns using creative statistical techniques (Hodrick , 1992).  Dividend yield has also been 
shown to have cross -sectional return  predictability. Although similar in construction to the value ratios, 
the explanatory power of d ividend yields is  most often attributed to the differential taxation of capital 
gains and ordinary income as described in the  after -tax asset pricing models developed by Brennan 
(1970) and Litzenberger and Ramaswamy (1979).  
The Yield factor can be controve rsial. Black and Scholes (1974) concluded there is no significant 
relationship between dividend yield and stock returns after adjusting for risks. Ang and Bekaert (200 7) 
found the excess return predictability by the dividend yield is not statistically sign ificant or robust, which 
is contrary to Fama  and French’s findings above. The difference is mainly due to the statistical 
techniques used by the two research groups. Ang and Bekaert (200 7) further noted the dividend is an 
unreliable indicator since it is “ smoothed and manipulated” by the company.  
  

---
## Page 29

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
29 of 33 Appendix B: References for Appendix  A 
 
Amihud, Y. (2002), “Illiquidity and stock returns: cross -section and time -series effects,” Journal of 
Financial Markets 5 (1), 31 -56. 
Ang, Andrew, and Geert Bekaert (2007): “Stock return predictability: Is it there?,” Review of Financial 
Studies 20, 3: 651 -707.  
Asness, C. (1995), “The Power of Past Stock Returns to Explain Future Stock Returns.” Working paper, 
Goldman Sachs Asset Management.   
Asness, C.  (1997), “The Interact ion of Value and Momentum Strategies,” Financial Analysts Journal, 
March/April 1997.  
Asness, C., A. Frazzini, and L. Pedersen (2013), “Quality Minus Junk,” Working paper, New York 
University (NYU) , AQR Capital Management, LLC . October 9, 2013.  
Asness, C.,  T.J. Moskowitz, and L. Pedersen (2010), "Value and Momentum Everywhere", University of 
Chicago and AQR Capital Management working paper.  
Baker, Malcolm, Brendan Bradley, and Jeffrey Wurgler (2011), “Benchmarks as Limits to Arbitrage: 
Understanding the Low-Volatility Anomaly”, Financial Analyst Journal, Vol. 67, No. 1, pp. 40 –54. 
Banz, R. W. (1981), “The relationship between return and market value of common stocks,” Journal of 
Financial Economics 9(1), 3 -18. 
Barberis, Nicholas & Shleifer, Andrei & Vishn y, Robert  (1998 ), "A model of investor sentiment," Journal 
of Financial Economics, V ol. 49(3) : 307 -343.  
Basu, Sanjay. 1977. “Investment Performance of Common Stocks in Relation to Their Price -Earnings 
Ratios: A Test of the Efficient Market Hypothesis.” Jo urnal of Finance. 12:3,  129-56. 
Bender, J. and F. Nielsen (2013), “Earnings Quality Revisited,” Journal of Portfolio Management, Vol. 39, 
No. 4: 69 -79. 
Black, Fischer (1993), “Beta and Return,” Journal of Portfolio Management, Vol. 20, No. 1: 8 -18. 
Black, Fischer and Myron Scholes (1974), “Effects of Dividend Yield on Stock Prices,” Journal of Financial 
Economics 1 (May 1974).  
Blitz, D. and P. van Vliet (2007), “The Volatility Effect: Lower Risk without Lower Return ,” Journal of 
Portfolio Management , Fall 2 007, Vol. 34, No. 1: pp. 102 -113. 
Blume,  Marshall E. (1980), “Stock Returns and Dividend Yields: Some More Evidence,” The Review of 
Economics and Statistics, Vol. 62, No. 4 (Nov., 1980), pp. 567 -577.  
Brennan , M. J.  (1970) , “Taxes, Market Valuation, and Fin ancial Policy,” National Tax Journal 3(3), 417 -
429.  
Campbell , J.Y., C. Polk , and T. Vuolteenaho  (2010), “ Growth or Glamour? Fundamentals and Systematic 
Risk in Stock Returns ,” Review of Financial Studies, 23(1):305 -344.  
Carhart, M. (1997), “On Persistence in Mutual Fund Performance,” the Journal of Finance 52(1), 57 -82. 
Chan, K. C., and Chen, Nai -fu (1991), “Structural and return characteristics of small and large firms,” 
Journal of Finance 46: 1467 –84. 

---
## Page 30

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
30 of 33 Chan, K. C., Nai -fu Chen, and David Hsieh (1985), “An exploratory investigation of the firm size effect,” 
Journal of Financial Economics 14:451 –71. 
Chan, Louis K.C., Jason Karceski , and Josef Lakonishok (1999) , “On Portfolio Optimization: Forecasting 
Covariances and Choosing the Risk Model,” The Review of Fin ancial Studies, Vol. 12, No. 5: 937 -974.  
Clarke, Roger, Harindra de Silva , and Steven Thorley (2006) , “Minimum -Variance Portfolios in the US 
Equity Market,” Journal of Portfolio Management 33 (Fall 2006), pp. 10 -24. 
Dasgupta, Amil , Andrea Prat, and Michel a Verardo  (2011) , “The price impact of institutional herding ,” 
Review of Financial Studies, 24 (3) : 892-925. 
Davis, James L. (2001), “Explaining Stock Returns: A Literature Review,” White Paper, Dimensional Fund 
Advisors.   Retrieved from  http://www.dfaus.com/2009/05/explaining -stock -returns -a-literature -
survey.html . 
Durlauf, Steven N. and Lawrence E. Blume (2008), Eds., The New Palgrave Dictionary of Economics . 
Second Edition. Palgrave Macmillan, 2008.  
DeBondt, Wern er F. M. and Richard H. Thaler ( 1987 ), “Further Evidence on Investor  Overreaction and 
Stock Market Seasonality.” Journal of Finance. 42:3, pp. 557 -81. 
Dechow, Patricia, Weili Ge, and Catherine Schrand (2010), “Understanding earnings quality: A review of 
the proxies, their determinants and their consequences,” Journal of Accounting and Economics. Vol. 50, 
Issue 2 -3, pp. 344 -401.  
Fama, Eugene F. (1997), “Market Efficiency, Long -Term Returns, and Behaviora l Finance,” Journa l of 
Financial Economics, 49(3), pp. 283 -306.  
Fama , Eugene F. and Kenneth R.  French  (1988), “ Dividend yields and expected stock returns ,” Journal of 
Financial Economics , 22: 3 -25. 
Fama, Eugene F. and Kenneth R. French (1992), “The Cross -Section of Expected Stock Returns,” Journal 
of Finance  47, 427 -465.  
Fama, Eugene F., and Kenneth R. French (1993), “Common Risk Factors in the Returns on Stock and 
Bonds,” Journal of Financial Economics  33, 3 -56. 
Fama, Eugene F., and Kenneth R. French ( 2008 ), “Dissecting Anomalies ,” Journal of Finance 63:  1653 -
1678.  
Frazzini, Andrea, David Kabiller , and Lasse Heje Pedersen  (2012) , “Buffett’s Alpha,” Working Paper, AQR 
Capital Management, New York University.  
Geczy, Christopher and Mikhail Samonv (2013), “ 212 Years of Price Momentum (The World's Longest 
Backtest: 1801 -2012) ,” Working Paper, University of Pennsylvania (The Wharton School), 
OctoQuant.com.  
Geiger, H., & Plagge, J. (2007), “Minimum variance indexes ,” Frankfurt: Deutsche Börse AG. Retrieved 
from 
http:/ /deutscheboerse.com/dbag/dispatch/de/binary/gdb_content_pool/imported_files/public_files/10
_downloads/50_informations_services/30_ indexes _Index_Licensing/21_guidelines/20_strategy_ indexe
s/presentation_DAXplus_Minimum_Variance.pdf  
Grinold, Richard C., R. Ka hn (1999), Active Portfolio Management: A Quantitative Approach for 
Producing Superior Returns and Controlling Risk, 2nd ed. McGraw -Hill, 1999.  

---
## Page 31

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
31 of 33 Hawawini, G., and D.B. Keim  (2000 ), “The Cross -Section of Common Stock Returns: A Review  of the 
Evidence and Som e New Findings,” in D.B. Keim, and W.T Ziemba (eds.),  Security Market Imperfections 
in World -Wide Equity Markets, Cambridge University  Press.  
Haugen, R, and N. Baker (1991), “The Efficient Market Inefficiency of Capitalization -Weighted Stock 
Portfolios”, J ournal of Portfolio Management.  
Hirshleifer , David  (2001), “ Investor Psychology and Asset Pricing," Journal of Finance, 56(4) : 1533 -1597.  
Hodrick, R. (1992), “Dividend Yields and Expected Stock Returns: Alternative Procedures for Inference 
and Measurement, ” Review of Financial Studies, 5, 357 –386.  
Hong , Harrison , Terence Lim , and Jeremy C. Stein  (2000), “Bad News Travels Slowly: Size, Analyst 
Coverage, and the Profitability of Momentum Strategies, ” Journal of Finance, 55(1 ): 265-295. 
Jagannathan, R., and T.  Ma (2003), “Risk Reduction in Large Portfolios: Why Imposing the Wrong 
Constraints Helps”, Journal of Finance, 58(4): 1651 -1684.  
Jegadeesh, N. and S. Titman (1993), “Returns to Buying Winners and Selling Losers: Implications for 
Market Efficiency,” Journa l of Finance 48(1), 65 -91. 
Daniel, Kent, David Hirshleifer, and Avanidhar Subrahmanyam (1998), “Investor Psychology and Security 
Market Under - and Overreactions,” Journal of Finance, Vol. 53, No. 6, pp. 1839 -1885.  
Kozlov, Max, and Antti Petajisto ( 2013 ), “Global Return Premiums on Earnings Quality, Value, and Size,” 
Working paper, Blackrock, New York University, Yale School of Management. January 7, 2013.  
Lakonishok, Josef, Andrei Shleifer, and Robert Vishny (1994), “Contrarian investment, extrapolation, an d 
risk,” Journal of Finance 49: 1541 –78. 
Litterman, Bob (2003). Modern Investment Management: An Equilibrium Approach . Hoboken, NJ: John 
Wiley & Sons Inc.  
Litzenberger, R., and K. Ramaswamy (1979) , “The Effects of Personal Taxes and Dividends on Capital 
Asset Prices: Theory and Empirical Evidence,” Journal of Financial Economics 7(2), 163 -195.  
Malkiel, Burton (2003), “The Efficient Market Hypothesis and Its Critics,” Journal of Economic 
Perspectives, Vol. 17, No. 1 (Winter 2003), pp. 59 -82. 
Nielsen , Frank  and Raman Aylur Subramanian (2008) , “Far From the Madding Crowd – Volatility Efficient 
indexes ,” MSCI Barra Research Insights, April 2008.  
O'Higgins , Michael B. , and John Downes (1991). Beating the Dow . Harper Collins Publishers.  
Perotti, P., and A. Wagen hofer (2011), “Earnings quality measures and excess returns,” Working paper, 
University of Graz.  
Poullaouec, T. (2008), “Things to consider when investing in minimum variance strategies,” State Street 
Global Advisors. Retrieved from 
http://www.ssga.com/library/resh/Things_to_Consider_when_Inv_in_MV_Strategies_Thomas_Poullaou
c_10.16.08rev3CCRI1225381984.pdf  
Qian,  Edwar d, Ronald Hua, and Eric Sorensen  (2007). Quantitative Equity Portfolio Management: 
Modern Techniques and Applications . London: Chapman and Hall.  
Rizova, S. (2006), “International Evidence on the Size Effect,” Dimensional Fund Advisors, White paper.  
Rosenberg,  Barr, Kenneth Reid, and Ronald Lanstein (1985), “Persuasive evidence of market 
inefficiency,” Journal of Portfolio Management, Vol. 11, No. 3, pp. 9 -16. 

---
## Page 32

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
32 of 33 Rouwenhorst, K. Geert (1998), “International Momentum Strategies,” The Journal of Finance 53 (1), 267 -
284.  
Schwartz , Tal (2000) , “How to Beat the S&P500 with Portfolio Optimization, ” Unpublished Manuscript , 
Retrieved from 
http://www.departments.bucknell.edu/management/apfa/Dundee%20Papers/27Schwartz.pdf  
Schwert, G. William (2003), “Anomalies and Market Efficiency” in Ch. 15 in Handbook of the Economics 
of Finance , by Constantinides, Harris, and Stulz.  
Sefton, James, David J essop, Giuliano De Rossi, Claire Jon es, and Heran Zhang (2011), “ Low-risk 
investing, ” UBS Investment Research.  
Sloan, R. (1996), “Do stock prices fully reflect information in accruals and cash flows about future 
earnings?” The Accounting Review 71: 289 -315. 
Tweedy, Browne Company LLC (2007), “The High Dividend Yield Return Advantage: An Examination of 
Empirical Data Associating Investment in High Dividend Yield Securities with Attractive Returns Over 
Long Measurement Periods ,” Paper, Retrieved from 
http://www.tweedy.com/resources/whdyf/TheHighDivAdvantageStudyFUNDwebcopy.pdf  
Vassalou, M. and Y. Xing (2004), “Default Risk in Equity Returns,” Journal of Finance 59, 83 1-868.  
Vayanos, Dimitri and Paul Woolley  (2011 ), “An institutional theory of momentum and reversal ,”  London 
School of Economics (LSE), Working paper.   
Zhang, X.F. (2006), “Information uncertainty and stock returns,” Journal of Finance 61(1), 15 -136.  
   

---
## Page 33

    
 
MSCI Index Research  msci.com  
© 2013  MSCI  Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document   Research Insight  
Foundations of  Factor Investing  
December  2013  
 
33 of 33 Client Service Information is Available 24 Hours a Day  
clientservice@msci.com  
Notice and Disclaimer  
 This document and all of the information contained in it, including without limitation all text, data, graphs, charts (collec tively, the “Information”) is the property of MSCI Inc. or its 
subsidiaries (collectively, “MSCI”), or MSCI’s licensors, direct or indirect suppliers or any third party involved in making or compiling any Information (collectively, with MSCI, the 
“Information Providers”) and is provided for informational purposes only.  The Information may not be reproduced or redissemi nated in whole or in part without prior written 
permission from MSCI.  
 The Information may not be used to create derivative works or to verify or correct other data or information.   For example ( but without limitation), the Information may not be used to 
create indices , databases, risk models, analytics, software, or in connection with the issuing, offering, sponsoring, managing or marketing o f any securities, portfolios, financial products 
or other investment vehicles utilizing or based on, linked to, tracking or otherw ise derived from the Information or any other MSCI data, information, products or services.   
 The user of the Information assumes the entire risk of any use it may make or permit to be made of the Information.  NONE OF THE INFORMATION PROVIDERS MAKES ANY E XPRESS OR 
IMPLIED WARRANTIES OR REPRESENTATIONS WITH RESPECT TO THE INFORMATION (OR THE RESULTS TO BE OBTAINED BY THE USE THEREOF), AND  TO THE MAXIMUM EXTENT 
PERMITTED BY APPLICABLE LAW, EACH INFORMATION PROVIDER EXPRESSLY DISCLAIMS ALL IMPLIED WARRANTIES (INCLUDING, WITHOUT LIMITATION, ANY IMPLIED WARRANTIES OF 
ORIGINALITY, ACCURACY, TIMELINESS, NON -INFRINGEMENT, COMPLETENESS, MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE) WITH RESPECT TO ANY OF THE 
INFORMATION.  
 Without limiting any of the foregoing  and to the maximum extent permitted by applicable law, in no event shall any Information Provider have any liability regardin g any of the 
Information for any direct, indirect, special, punitive, consequential (including lost profits) or any other damages even if notified of the possibility of such damages. The foregoing shall 
not exclude or limit any liability that may not by applicable law be excluded or limited, including without limitation (as ap plicable), any liability for death or personal injury to t he extent 
that such injury results from the negligence or willful default of itself, its servants, agents or sub -contractors.   
 Information containing any historical information, data or analysis should not be taken as an indication or guarantee of any future performance, analysis, forecast or prediction.  Past 
performance does not guarantee future results.  
 None of the Information constitutes an offer to sell (or a solicitation of an offer to buy), any security, financial product or other investment vehicle  or any trading strategy.  
 You cannot invest in an index.  MSCI does not issue, sponsor, endorse, market, offer, review or otherwise express any opinion  regarding any investment or financial product that may be 
based on or linked to the performance of any MSCI index.  
 MSCI’s indirect wholly -owned subsidiary Institutional Shareholder Services, Inc. (“ISS”) is a Registered Investment Adviser under the Investment Adv isers Act of 1940.  Except with 
respect to any applicable products or services from ISS (including applicable products or services from MSCI ESG Research, which are provided by ISS), neither MSCI nor any of its 
products or services recommends, endorses, approves or otherwise expresses any opinion regarding any issuer, securities, fina ncial pr oducts or instruments or trading strategies and 
neither MSCI nor any of its products or services is intended to constitute investment advice or a recommendation to make (or refrain from making) any kind of investment decision and 
may not be relied on as su ch. 
 The MSCI ESG Indices  use ratings and other data, analysis and information from MSCI ESG Research.  MSCI ESG Research is produced by ISS or its sub sidiaries.  Issuers mentioned or 
included in any MSCI ESG Research materials may be a client of MSCI, ISS,  or another MSCI subsidiary, or the parent of, or affiliated with, a client of MSCI, ISS, or another MSCI 
subsidiary, including ISS Corporate Services, Inc., which provides tools and services to issuers.  MSCI ESG Research material s, including materials ut ilized in any MSCI ESG Indices  or other 
products, have not been submitted to, nor received approval from, the United States Securities and Exchange Commission or any  other regulatory body.  
 Any use of or access to products, services or information of MSCI r equires a license from MSCI.  MSCI, Barra, RiskMetrics, IPD, ISS, FEA, InvestorForce, and other MSCI brands and 
product names are the trademarks, service marks, or registered trademarks of MSCI or its subsidiaries in the United States an d other jurisdictio ns.  The Global Industry Classification 
Standard (GICS) was developed by and is the exclusive property of MSCI and Standard & Poor’s.  “Global Industry Classificatio n Standard (GICS)” is a service mark of MSCI and Standard 
& Poor’s.  
About MSCI  
MSCI Inc. i s a leading provider of investment decision support tools to investors globally, including asset managers, banks, hedge funds  and pension funds. MSCI 
products and services include indices , portfolio risk and performance analytics, and governance tools.  
The company’s flagship product offerings are: the MSCI indices with approximately USD 7.5 trillion estimated to be benchmarked to them on a worldwide basis1; 
Barra multi -asset class factor models, portfolio risk and performance analytics; RiskMetrics multi -asset class market and credit risk analytics; IPD real estate 
information, indices and analytics; MSCI ESG (environmental, social and governance) Research screening, analysis and ratings;  ISS corporate governance research, 
data and outsourced proxy voting a nd reporting services; and FEA valuation models and risk management software for the energy and commodities markets. MSCI is 
headquartered in New York, with research and commercial offices around the world.  
1 As of March 31, 2013, as reported on July 31, 2013 by eVestment, Lipper and Bloomberg        Oct 2013  Americas   Europe, Middle East & Africa  Asia Pacific   
Americas  
Atlanta  
Boston  
Chicago  
Monterrey  
New York  
San Francisco  
Sao Paulo  
Toronto  1.888.588.4567 (toll free)   
+ 1.404.551.3212  
+ 1.617.532.0920  
+ 1.312.675.0545  
+ 52.81.1253.4020  
+ 1.212.804.3901  
+ 1.415.836.8800  
+ 55.11.3706.1360  
+ 1.416.628.1007  Cape Town  
Frankfurt  
Geneva  
London  
Milan  
Paris  
 + 27.21.673.0100  
+ 49.69.133.859.00  
+ 41.22.817.9777  
+ 44.20.7618.2222  
+ 39.02.5849.0415  
0800.91.59.17 (toll free)  
 China North  
China South  
Hong Kong  
Seoul  
Singapore  
Sydney  
Taiwan  
Tokyo  10800.852.1032 (toll free)   
10800.152.1032 (toll free)  
+ 852.2844.9333  
00798.8521.3392 (toll free)  
800.8 52.3749 (toll free)  
+ 61.2.9033.9333  
008.0112.7513 (toll free)  
+ 81.3.5226.8222  

