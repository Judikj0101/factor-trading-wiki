# USE4 Methodology Notes August 2011

> Extracted from: `USE4_Methodology_Notes_August_2011.pdf` (44 pages)

---
## Page 1

 
 
 
   
 
  
 
    
 msci.com 
 
Model Insight
The Barra US Equity Model (USE4)  
Methodology Notes  
Jose Menchero 
D.J. Orr  
Jun Wang 
 
August 2011

---
## Page 2

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
2o f  4 4Contents 
1. Introduction  ............................................................................ 3  
1.1. Model Highlights  .............................................................................................. 3  
1.2. Modern Portfolio Theory and Barra Risk Models: A Brief History  ..... 3 
1.3 Forecasting Portfolio Risk with Factor Models  ......................................... 6  
2. Factor Exposures  ................................................................. 7  
2.1 General Considerations  .................................................................................. 7  
2.2. Data Quality and Outlier Treatment  ........................................................... 8  
2.3. Style Exposures  ............................................................................................... 9  
2.4. Industry Factors  ............................................................................................... 9  
2.5. Multiple-Industry Exposures  ...................................................................... 10  
3. Factor Returns  .................................................................... 13  
3.1. Country Factor  .............................................................................................. 13  
3.2. Relation to Traditional Approach  ............................................................. 15  
4. Factor Covariance Matrix  ................................................. 17  
4.1 Established Methods  .................................................................................... 17  
4.2 Eigenfactor Risk Adjustment  ...................................................................... 19  
4.3 Volatility Regime Adjustment  ..................................................................... 24  
5. Specific Risk  ........................................................................ 28  
5.1 Established Methods  .................................................................................... 28  
5.2 Bayesian Shrinkage  ..................................................................................... 29  
5.3 Volatility Regime Adjustment  ..................................................................... 31  
6. Conclusion  ........................................................................... 35  
Appendix A: Review of Bias Statistics  ............................... 36  
A1. Single-Window Bias Statistics  ................................................................... 36  
A2. Rolling-Window Bias Statistics  .................................................................. 37  
Appendix B. Eigenfact or Risk Adjustment  ....................... 40  
REFERENCES  ....................................................................... 43  
 
  

---
## Page 3

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
3o f  4 41. Introduction 
1.1. Model Highlights 
This document describes the new methodologies that underpin the USE4 model. Our aim is to produce a 
document that is clear and concise, yet comprehensive as well. MSCI prid es itself not only on setting the 
standard for excellence in factor risk modeling, but also on being the industry leader in model transparency. 
This document is the complement to a companion document: USE4 Empirical Notes . Whereas the 
current document focuses on methodology, the Empirical Notes  contain detailed information about 
USE4 factor structure, extensive analysis on the explanatory power and statistical significance of the 
factors, and a systematic inve stigation into the forecasting accuracy of the model. The Empirical Notes 
also provide a thorough compar ison with the USE3 model. 
The main advances of USE4 are: 
 An innovative Eigenfactor Risk Adjustment that impr oves risk forecasts for optimized portfolios by 
reducing the effects of sampling error on the factor covariance matrix  
 A Volatility Regime Adjustment designed to calibrate factor volatilities and specific risk forecasts to 
current market levels 
 The introduction of a country factor to separate th e pure industry effect from the overall market and 
provide timelier correlation forecasts  
 A new specific risk model based on daily asset-level specific returns 
 A Bayesian adjustment technique to reduce specific risk biases due to sampling error 
 A uniform responsiveness for factor and specific co mponents, providing greater stability in sources of 
portfolio risk 
 A set of multiple industry exposures based on GICS® 
 An independent validation of production code through a double-blind development process to 
assure consistency and fidelity between research code and production code 
 A daily update for all components of the model 
The USE4 model is offered in short-term (USE4S) a nd long-term (USE4L) versions. Both versions have 
identical factor exposures and factor returns, but diff er in their factor covariance matrices and specific 
risk forecasts. The USE4S model is  designed to be more responsive  and provide the most accurate 
forecasts at a monthly prediction horizon. The US E4L model is designed for longer-term investors who 
are willing to trade some degree of accuracy  for greater stability in risk forecasts. 
1.2. Modern Portfolio Theory and Barra Risk Models: A Brief History 
The pioneering work of Markowitz (1952) formally established the in trinsic tradeoff between risk and 
return. This paradigm provided the foundation upon  which the modern theory of finance was built, and 
has proven so resilient that it has survived essentially intact for nearly 60 years. Almost as remarkable is 
the vigor with which the theory has been embraced by academics and practitioners alike.  

---
## Page 4

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
4o f  4 4The specific problem addressed by Markowitz was how to construct an efficient portfolio from a 
collection of risky assets. Markowitz defined an effici ent portfolio as one that had the highest expected 
return for a given level of risk, which he measured as  standard deviation of portfolio returns. Markowitz 
showed that the relevant risk of an asset is not its stand-alone volatility, but rather its contribution to 
portfolio  risk. Thereafter, the concepts of risk and correlation became inseparable. 
A plot of expected return versus volatility for the se t of all efficient portfolios maps out a curve known as 
the efficient frontier. In order to construct the effi cient frontier using the Markowitz prescription, an 
investor must provide expected returns and covarianc es for the universe of all investable assets. The 
Markowitz procedure identifies the optimal portfolio corresponding to the risk tolerance of any given 
investor.  
Tobin (1958) took the Markowitz methodology and exte nded it in a very simple way that nonetheless 
had profound implications for port folio management. By including cash  in the universe of investable 
assets, Tobin showed that there existed a single portfo lio on the efficient frontier that, when combined 
with cash, dominated all other portfolios. For any investor, therefore, the optimal portfolio would 
always consist of a combination of  cash and the “super-efficient” po rtfolio. For instance, risk-averse 
investors may combine the super-efficient portfolio with a large cash position, whereas risk seekers 
would borrow cash to purchase more of the super-effici ent portfolio. As a result, according to Tobin, the 
optimal investment strategy consists of two separate steps. The first is to determine the super-efficient 
portfolio. The second step is to determine the approp riate level of cash that matches the overall risk 
tolerance of the investor. This two- step investment process came to be known as the Tobin separation 
theorem.  
The next major step in the development of Capital Market Theory was due to Sharpe (1964). By making 
certain assumptions (e.g., that all investors follo wed mean-variance preferences and agreed on the 
expected returns and covariances of all assets) Sh arpe was able to show that the super-efficient 
portfolio was the market portfolio itself. Sharpe’s theory, known as the Capital Asset Pricing Model, 
predicts that the expected return of an asset depe nds only on the expected return of the market and 
the beta of the asset relative to the market. In other words, within CAPM, the only “priced” factor is the 
market factor.  
Using the CAPM framework, the return of any asset can be decomposed into a systematic component 
that is perfectly correlated with the market, and a residual component that is uncorrelated with the market. The CAPM predicts that the expected value of the residual return is zero. This does not preclude 
the possibility, however, of correlations  among the residual returns. That is, even under the CAPM, there 
may be multiple sources of equity return co-movemen t, even if there is only  one source of expected 
return.  
Rosenberg (1974) was the first to develop multi-factor  risk models to estimate the asset covariance 
matrix. This work was later extended by Rose nberg and Marathe (1975), who conducted a sweeping 
econometric analysis of multi-factor models. The intu ition behind these models is that there exists a 
relatively parsimonious set of pervasive factors th at drive asset returns. Returns that cannot be 
explained by the factors are deemed “stock specific” and are assumed to be uncorrelated.  
Rosenberg founded Barra, which made widespread use of multi-factor risk models and dedicated itself 
to helping practitioners implement the theoretical insights of Markowitz, Tobin, Sharpe, and others. The first multi-factor risk model for the US market, dubbed the Barra USE1 Mode l, was released in 1975. 
That model was followed by the USE2 Model in 1985,  and USE3 in 1997. Ra pidly changing volatility 
levels during and after the Internet Bubble highlighted the need for more responsive risk models, and in 
2002 the USE3 Model was upgraded to in corporate daily factor returns.  

---
## Page 5

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
5o f  4 4Another key step in developing the theoretical edifice of quantitative investing came with the publishing 
in 1995 of an influential book entitled Active Portfolio Management,  written by Grinold and Kahn while 
at Barra. The widespread success of this book pr ompted a second edition by  Grinold and Kahn (2000), 
and it serves today as an essential guideb ook for many quantitative investment firms. 
For modeling global portfolios, an important mileston e came in 1989 with the development of the first 
Barra Global Equity Risk Model (GEM). This model was estimated via monthly cross-sectional regressions 
using countries, industries, and styles as explanatory factors, as described by Grinold, Rudd, and Stefek 
(1989). 
GEM was followed by a second-generation Global Equi ty Risk Model, GEM2, as described by Menchero, 
Morozov, and Shepard (2008). GEM2 in corporated several advances over the previous model, such as 
improved estimation techniques, higher-frequency observations, and the introduction of the World factor to place countries and industries on an equal footing.  
Barra also pioneered the use of in tegrated models, which combine the breadth of a global model with 
the detail of local single-country models. An innovat ive feature of this approach is that it assures 
consistency between the risk forecasts used by portfo lio managers in the front office and risk managers 
in the middle office. The first-generation Barra In tegrated Model (BIM) was introduced in 2002. The 
second-generation Barra Integrated Model, desc ribed by Shepard (2011), incorporated important 
advances in methodology, such as using the GEM2 model to estimate covariances among local factors 
and employing higher-frequency observations.  
Barra risk models have long played an important ro le in applying the concepts of modern portfolio 
theory to solve practical investment problems. At MSCI, we are dedicated to continuing this proud 
tradition of developing industry-leading risk models . The release of the new Barra US Equity Model, 
USE4, marks only the latest step in this ongoing journey. 
  

---
## Page 6

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
6o f  4 41.3 Forecasting Portfolio Risk with Factor Models 
The asset covariance matrix is critical both for port folio construction and for risk management purposes. 
A key challenge in estimating the asset covariance matrix lies in the sheer  dimensionality of the 
problem. For instance, an active portfolio  containing 2000 stocks requires more than two million  
independent elements. If the asset covariance matrix is computed naively — that is, by brute force — 
then the matrix is likely to be  extremely ill-conditioned. This makes the asset covariance matrix highly 
susceptible to noise and spurious relationships that ar e unlikely to persist out-of-sample. For instance, if 
the number of time observations is less than the number of stocks (as would be typical for large 
portfolios), the matrix is said to be  “rank deficient,” meaning that it is possible to construct apparently 
riskless portfolios. 
Factor risk models were developed to provide a more  robust solution to this problem. Stock returns are 
attributed to a factor component that affects all st ocks, and an idiosyncratic component that is unique 
to the particular stock. More specific ally, the stock return is explained as 
nn k k n
krX f u  ,                                                                      (1.1) 
where nkX is the exposure of stock n to factor k, kf is the return to the factor, and nu is the stock 
specific return.  
Consider a portfolio with weights nw, and return given by 
Pn n
nR wr .                                                                           (1.2) 
The portfolio factor exposures are given by the we ighted average of the asset exposures, i.e.,  
P
kn n k
nX wX .                                                                           (1.3) 
Therefore, the portfolio return can be expressed as 
P
Pk k n n
knR Xf w u .                                                                 (1.4) 
Two key assumptions in factor risk modeling are that (a) the factor returns are uncorrelated with the 
specific returns and (b) the specific returns are un correlated among themselves. This allows the variance 
of the portfolio to be expressed as  
 2var varPP
Pk k l l n n
kl nR XF X w u ,                                                       (1.5) 
where klF is the predicted covariance between factors k and l. If, for example, the risk model contains 
60 factors, then the factor covariance matrix contai ns less than two thousand independent elements. It 
is due to this tremendous reduction in the dimensiona lity of the problem that the factor model is able to 
filter out most of the noise and prov ide a robust measure of portfolio risk. 
  

---
## Page 7

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
7o f  4 42. Factor Exposures  
2.1 General Considerations 
Sound factor structure represents a key pillar for pr oducing a high-quality risk model. Factors represent 
broad drivers of asset return co-movement, segmen ting portfolio risk and return into two distinct 
sources. The first source, due to factors, represen ts the systematic compon ent. The second source 
represents the diversifiable component that cannot  be explained by the factors, and is therefore 
deemed idiosyncratic or asset specific.  
A key assumption underlying factor risk models is that  the factors capture all sy stematic drivers of asset 
returns, thus implying that the specific returns are mu tually uncorrelated. Therefor e, it is essential that a 
high-quality factor structure explain as fully as po ssible the cross section of  asset returns. A common 
pitfall in risk model construction is to omit importan t factors. A portfolio with exposures to these factors 
may be adversely impacted by “hidden” risk source s that spuriously appeared to be diversified.  
Another important characteristic of a high-quality factor structure is parsimony, meaning that the 
systematic component of asset returns is explaine d with the fewest possible number of factors. 
Parsimonious factor structures te nd to be more robust in capturing true underlying relationships. 
Indeed, another pitfall in risk model construction is to  indiscriminately add weak or spurious factors, as 
this makes the model more susceptible to noise that  can be detrimental to the portfolio construction 
process. 
When investigating risk model factor structure, care ful attention must also be paid to the statistical 
significance of the factor returns. In particular, th e statistical significance of the factors should be 
persistent across time, and not due to isolated events that are unlikely to recur in the future. Careful and thorough statistical analysis help s ensure that spurious factors do not find their way into the model. 
Stability is another characteristic of a high-quality fa ctor structure. Stability means that typical stock 
exposures do not change drastically over short periods of time, which can be problematic from a risk management perspective. We define a factor stability coefficient  as the cross-sectional correlation of 
factor exposures from one month to the next; this can be expressed as 

 11
2211tt t t t
nn k k n k kn
kt
tt t tt t
nn k k nn k knnvX X X X
vX X vX X



,                                          (2.1) 
where t
nv is the regression weight of stock n at time t. As a rule of thumb, factor stability coefficients 
above 0.90 are considered desirable, whereas th ose below 0.80 are deemed too unstable for model 
inclusion.  
Collinearity, another important consideration when re searching and building a factor structure, occurs 
when a given factor can be approximately replicated by a combination of other factors. If the factor 
structure is excessively collinear, estimation errors  in the regressions can become very large and the 
factor returns difficult to interpret. One measure of factor collinearity is given by the Variance Inflation 
Factor  (VIF). This is computed by regressing a single factor against the other factors in the model: 
nk nk k nk
kkXX b 
 .                                                                   (2.2) 

---
## Page 8

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
8o f  4 4The VIF is defined through the explanatory power of the regression, as measured by R-squared. More 
specifically: 
21
1k
kVIFR.                                                                         (2.3) 
A large value for VIF is indicative  of excessive collinearity. As desc ribed by Menchero (2010), a factor 
rotation procedure known as orthogonalization ca n serve as an effective tool for both reducing 
collinearity and making the factors more intuitive. For instance, the Non-Linear Size factor, after 
orthogonalization, essentially capt ures the return differences between mid-cap stocks and the overall 
market. 
Last, but not least, risk model factors should be intu itive. In other words, they must be transparent, 
easily interpretable, and consistent with investor s’ views about what these factors represent. For 
example, it is reasonable to demand that a broad value or growth index have positive exposure to a 
well-constructed value or growth factor. Further discussion of this issue can be found in the MSCI 
Research Insight, Global Style Factors (2010). 
 
2.2. Data Quality and Outlier Treatment 
The most difficult and time-consuming part of constructing an equity risk model lies in preparation of 
the input data. If the data inputs are of poor quality,  the risk forecasts will likewise be poor, no matter 
how sophisticated the model. Assuring a high degree of  data quality, therefore, is essential for building a 
reliable risk model.  
In order to obtain the highest quality inputs, Barra risk models leverage the same data infrastructure 
used for the construction of MSCI Global Investable Market Indices. Data items such as raw descriptors, 
GICS® codes, country classifications, and clean daily  stock returns are obtained from in-house sources 
that have already undergone extensive quality control.  
No matter how stringent the data quality assuranc e process, we can never exclude the possibility of 
extreme outliers entering the data set. These extr eme outliers may represent legitimate values or 
outright data errors. Either way, such observations  must be carefully handled to prevent a few data 
points from having an undue impact on model estimation. 
In USE4, we employ a multi-step algorithm to iden tify and treat outliers. The algorithm assigns each 
observation into one of three groups. The first group represents values so extr eme that they are treated 
as potential data errors and removed from the esti mation process. The second group represents values 
that are regarded as legitimate, but nonetheless so large that their impact on the model must be limited. We trim  these observations to three standard devi ations from the mean. The third group of 
observations, forming the bulk of the distribution, co nsists of values that are less than three standard 
deviations from the mean; these observations are left unadjusted. 
The thorough data quality assurance process, coupled with the robust outlier algorithm, is designed to 
ensure that the input data are clean and reliable. Th ere is still the issue, however, of dealing with 
missing data. Data could be missing eith er due to lack of availability or  due to removal by the outlier 
algorithm.  

---
## Page 9

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
9o f  4 4If the underlying data required to calculate factor exposures are missing, then the factor exposures are 
generated using a data-replacement algorithm. In th is case, we regress non-missing exposures against a 
subset of factors, with the slope coefficients being used to estimate the factor exposures for the stocks 
with missing data. The intuition is that stocks with similar attributes, such as industry membership or 
market capitalization, are likely to share similar exposures. 
Note also that the data-replacement algorithm is applied at the factor level as opposed to the descriptor 
level. In other words, if a stock has data for some descriptors within a style factor, but not others, then 
the non-missing data will be used to co mpute the factor exposures. Only if all descriptors are absent 
does the replacement algorithm become active. 
2.3. Style Exposures 
Style factors constitute major drivers of equity cro ss-sectional returns. In fact, as shown by Menchero 
and Morozov (2011), there are periods when style factor s explain a greater proportion of cross-sectional 
variation of global equity returns than either country factors or industry factors.  
Style factors are constructed from descriptors, which represent financially intuitive stock attributes and 
serve as effective predictors of e quity return covariance. Since the descriptors within a particular style 
factor are meant to capture the same underlying driver of returns, these descriptors tend to be 
significantly collinear. Combining th ese descriptors into a single style factor overcomes the collinearity 
problem, while also leading to a more  parsimonious factor structure.  
Descriptors are standardized to have a mean of 0 an d a standard deviation of 1. In other words, if Raw
nld  
is the raw value of stock n for descriptor l, then the standardized descriptor value is given by 
Raw
nl l
nl
ldd
 ,                                                                      (2.4) 
where l is the cap-weighted mean of the descriptor (within the estimation universe), and l is the 
equal-weighted standard deviation. We adopt the co nvention of standardizing using the cap-weighted 
mean so that a well-diversified cap-weighted portfo lio has approximately zero exposure to all style 
factors. For the standard deviation, however, we use equal weights to preven t large-cap stocks from 
having an undue influence on the overall scale of the exposures.  
Formally, descriptors are combined  into style factors as follows: 
nk l nl
lkX wd
 ,                                                                        (2.5) 
where lw is the descriptor weight, and the sum takes plac e over all descriptors within a particular style 
factor. Descriptor weights are determined using an optimization algorithm designed to maximize the 
explanatory power of the model. The final step of co nstructing the style factor is to re-standardize the 
exposures so that they have a cap-weighted mean of 0 and an equal-weighted standard deviation of 1. 
2.4. Industry Factors 
Industries represent another major class of risk model fa ctors. When constructing industry factors, it is 
important that the factors reflect the return drivers of the local market. Using a single level of the GICS 
hierarchy, for example, fails to capture the unique ch aracteristics of each financial market. Furthermore, 

---
## Page 10

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
10 of 44this naive approach invariably leaves some system atic risk unaccounted for and suffers from the 
problem of thin industries and low statistical signifi cance. To avert these shortcomings, Barra models 
employ customized factor structure to reflec t the local characteristics of each market. 
Identifying which industry factors to include in the model involves a combination of judgment and 
empirical analysis. Within each sector we drill into  different levels of the GICS hierarchy. The basic 
criteria we use to guide industry factor selection ar e: (a) groupings of industries into factors must be 
economically intuitive, (b) industry factors should ha ve a strong degree of statistical significance, (c) 
incorporating an additional industry factor should significantly increase the explanatory power of the 
model, and (d) thin industries (those with few assets) should be avoided.  
2.5. Multiple-Industry Exposures 
Within the context of an industry classification scheme such as GICS, the industry membership of a given 
stock is determined by analysts who scrutinize fina ncial statements filed by the firm in question. By 
studying such filings, the analysts are able to determine the primary line of business for the firm and make an appropriate industry assignment. However, there are many instances where such analysis will 
reveal complications; for example, when a firm has substantial business activities in multiple  industries. 
It is valuable to model fractional  industry exposures in order to capt ure a more realistic representation 
of the underlying business activities of the stocks in a given portfolio. 
Multiple-industry membership is modeled in USE4 by examining the impact of two key explanatory 
variables — Assets and Sales — on the market value of  a given stock. More specifically, we regress the 
market capitalizations of the estimation universe st ocks against their reported Assets within each 
industry,  
A
nn k k n
kMA    ,                                                                      (2.6) 
where nM is the market capitalization of stock n, nkA is the Assets of the stock within industry k, A
k 
is the industry beta, and nis the residual. Note that A
k can be interpreted as the price-to-assets ratio 
of the industry. The industry exposures, using Assets as the explanatory variable, are given by the 
fraction of market capitalization explained by each industry, 
A
A nk k
nk A
nk k
kAXA
.                                                                         (2.7) 
Note that the industry exposures in Equation 2.7, by construction, will sum to 1.  
We also use Sales as an explanatory variable to estimate industry exposures S
nkX. To produce the net 
USE4 multiple-industry exposures, we combine Assets  exposures and Sales exposures according to the 
following weighting scheme: 
0.75 0.25AS
nk nk nkXXX .                                                                 (2.8) 
The maximum allowable number of multiple-industry exposu res is limited to five. If a firm has more than 
five business segments, the top five are taken and the industry exposures are re-normalized to 1. 

---
## Page 11

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
11 of 44Intuitively, we expect that industry betas (e.g., pr ice-to-assets ratios) may vary from one industry to the 
next. To illustrate this effect, in Figure 2.1  we plot Asset industry betas versus time for Pharmaceuticals 
(with the largest average industry beta over the sample  period), Life Insurance (which had the smallest 
average beta), and three other industries with intermediate betas. Clearly, a dollar of Assets in the 
Pharmaceuticals industry translated into a much higher  market capitalization than a dollar of Assets in 
the Life Insurance industry. 
 
Figure 2.1  
Plot of Asset industry bet as versus time for represen tative industries. A dollar of Assets in Pharmaceuticals 
translated into higher market capitalization than a dollar of Assets in Life Insurance. 
Year1995  1997  1999  2001  2003  2005  2007  2009  2011  Industry Betas (Assets)
0123456Pharmaceuticals
Internet
Oil Gas Exploration
Aluminum Steel
Life Insurance
 
 
It is also important to note that most data sets for segment reporting utilize industry schemes that have 
a far higher level of granularity than GICS. For ex ample, the North American Industry Classification 
System (NAICS) contains nearly ten times the number of segments as represented in GICS. Constructing multiple-industry exposures therefore requires an accurate mapping between NAICS and GICS, along with managing a list of legitimate exceptions. This is  an activity for which MSCI is ideally suited. As a 
partner in the construction of GICS, our firm is able to leverage the same industry analysis experts who 
manage GICS in order to build the NAICS-to-GICS ma pping that is central to the USE4 multiple-industry 
methodology. This produces a multiple-industry scheme that is not only accurate , but consistent  with 
GICS as well. 
As an illustrative example, we consider the multip le-industry exposures for Deere & Company, a leading 
producer of agricultural machinery. In Figure 2.2 , we plot the exposures from 30-Jun-1995 to 31-May-
2011. The largest exposure is consistently on the US E4 Construction and Farm Machinery, which also 
corresponds to the single-industry GICS assignment of the firm. However, Deere & Company also has 

---
## Page 12

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
12 of 44sizeable allocations to Industrial Machinery and Diversified Financials. The jumps in multiple-industry 
exposures are attributable to changes in the financial statement reporting. 
 
Figure 2.2  
Multiple industry exposures for Deere & Company, plotted versus time. 
Year1995  1997  1999  2001  2003  2005  2007  2009  2011  Industry Exposures
0.00.20.40.60.81.0
Construction and Farm Machinery
Industrial Machinery
Diversified Financials
 
 
 
  

---
## Page 13

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
13 of 443. Factor Returns 
3.1. Country Factor 
A significant advance in the USE4 methodology is explicit inclusion of the Country factor. This 
enhancement, which is analogous to the World factor  in GEM2, is beneficial in two ways. First, it 
disentangles the market effect from the pure industr y effect, thus providing greater insight into the 
sources of risk and return. Second, adding the Country factor allows for more accurate risk forecasts and 
more responsive correlations, as  shown in the next section. 
In the USE4 model, local excess returns nr are explained by 
nc n i i n s sn
isrf X f X f u ,                                              (3.1) 
where cf is the return of the Country factor, if is the return of industry factor i, sf is the return of 
style factor s, niX and nsX are the exposures of stock n to industry i and style s, respectively, and 
nu is the specific return. Factor returns in USE4 ar e estimated using weighted least-squares regression, 
assuming that the variance of specific returns is inversely proportional to  the square root of total market 
capitalization. This regression-weighting scheme reflec ts the empirical observation that the idiosyncratic 
risk of a stock decreases as the market capitalization of the firm increases.  
In Equation 3.1, we see that every stock has an ex posure of 1 to the Country factor. Country exposure, 
however, should not be confused with market  exposure. Some stocks are clearly more sensitive to 
market movements than others. This  effect is captured through the Beta factor. Note that the Beta 
factor is highly correlated (temporally, not cross-sect ionally) with the Country factor. This reflects the 
observation that high-beta stocks tend to outp erform low-beta stocks in an up-market, while 
underperforming in down-markets. From a risk perspect ive, therefore, it is important to consider the 
Country factor and the Beta factor jointly. For inst ance, in a fully invested portfolio holding high-beta 
stocks, the portfolio will have positive exposure to  both factors, and the risk contributions will be 
additive. By contrast, in a fully invested portfolio of  low-beta stocks, the risk contributions will partially 
cancel.  
Note that adding the Country factor introduces an exac t collinearity into the mode l. That is, for all stocks
n, the sum of industry factor exposures is given by 
1ni
iX ,                                                                          (3.2) 
which is exactly the USE4 Country factor exposure. A constraint, therefore, must be applied to obtain a 
unique regression solution.  
In USE4 we adopt the constraint that the cap-weighted industry factor returns sum to zero, 
0ii
iwf ,                                                                          (3.3) 
where iw is the capitalization weight of the estimation universe in industry i. The choice of constraint 
does not affect the regression fit or the explanator y power of the model, but does directly affect the 

---
## Page 14

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
14 of 44interpretation of the factors. We select our constraint to provide the most intuitive interpretation of 
factor portfolios, as we now discuss. 
As described by Menchero (2010), factor returns ca n be interpreted as the returns of pure factor 
portfolios. To understand the Country factor portfolio , consider the cap-weighted estimation universe, 
with holdings E
nh. The return of this portfolio ER can be attributed to the USE4 factors, 
EE
Ec i i s s n n
is nR fw fX fh u   ,                                              (3.4) 
where E
sX is exposure of the cap-weighted  estimation universe to style s. Note, however, by Equation 
3.3, the sum over industries must equal zero. Similarl y, since style factors are standardized to be cap-
weighted mean zero (i.e., 0E
sX), the second summation in Equation  3.4 also vanishes. The final sum 
in Equation 3.4 corresponds to the specific return of a broadly diversified portfolio, and is therefore 
approximately  zero (note that it would be exactly  zero had we used regression weights instead of 
capitalization weights). Thus, to an excelle nt approximation, Equation 3.4 reduces to 
E c R f .                                                                                (3.5) 
In other words, the Country factor  essentially represents the cap-weighted estimation universe.  
In Figure 3.1  we plot the cumulative return of the USE4 Country factor, and compare it to the 
cumulative local excess return of the USE4 estima tion universe. The two portfolios track each other 
almost perfectly over the 16-year sample period, wi th a time-series correlation of approximately 99.9 
percent, thus validating the interpretation of the Country factor. 
 

---
## Page 15

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
15 of 44Figure 3.1  
Cumulative returns of the USE4 Country factor and th e USE4 estimation universe (in excess of risk-free rate). 
The two portfolios track each other very closely over the 16-year sample window, with a time-series 
correlation of 99.9 percent. 
Year1995  1997  1999  2001  2003   2005  2007  2009  2011  Cumulative Return (Percent)
050100150200250
USE4 Estimation Universe
USE4 Country Factor
 
 
The industry factors in Equation 3.4 can be interprete d as the returns of dollar-neutral portfolios that go 
100 percent long the particular industry and go 100 perc ent short the Country factor. The industry factor 
portfolios also have zero exposure to all style factors. Therefore, industry factors capture the 
performance of the pure industry relative to the overall market, net of all style effects. 
Similarly, style factors can be in terpreted as the returns of dollar- neutral portfolios that have unit 
exposure to the style in question and zero exposures to all other factors. In particular, pure style factor 
portfolios have net zero weight in every industry. These portfolios allow us to measure the performance 
of a particular style without the confounding effects of other style or industry tilts.  
3.2. Relation to Traditional Approach 
Traditionally, single country models do not include th e Country factor. In this case, stock returns are 
described as follows: 
nn i in s s n
isrX f Xfu  .                                                          (3.6) 
  

---
## Page 16

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
16 of 44There are two differences between Equation 3.1 and Equation 3.6. First, and most obvious, the former 
explicitly includes the Country factor, whereas the latter does not. Second, the industry factor returns are different in the two representations. The industry factor returns in Equation 3.6, however, can be 
easily related to those in Equation 3.1,  
icifff.                                                                         (3.7) 
In other words, the traditional industry factors ar e given by the sum of the Country factor and the 
corresponding dollar-neutral industry factor. This implies that the factor portfolio if is 100 percent net 
long the particular industry and has net zero weight in all other industries. 
Beyond the intuitive benefit of disentangling the market from the pure industries, including the Country 
factor provides advantages for risk-forecasting purpo ses as well. The underlying reason is that the 
covariance matrix, for reasons discu ssed in Section 4, uses different half-life parameters to estimate 
factor volatilities and factor correlations. Typically, th e correlation half-life is significantly longer than the 
volatility half-life. 
Consider the correlation ij between two net-long industry factors, if and jf, as in Equation 3.7. If 
this is estimated in a model without the Country fact or, the responsiveness of the correlation forecast is 
completely determined by the relatively slow correlati on half-life. If, on the other hand, we estimate the 
correlation using a model that contains the Country factor, then the common exposure to the Country 
factor can act as a source return co-movement between if and jf. More specifically, the correlation 
can be expressed as 
2
c c i c ic j c ji j i j
ij
ij  ,                                             (3.8) 
where i is the volatility of if, c is the volatility of cf, i is the volatility of if, and ij, is the 
correlation between if and jf. All estimates in Equation 3.8 are obtained from a model that includes 
the Country factor. Since the volatility of the Country  factor is estimated with the more responsive 
volatility half-life, the correlation forecast ij is likewise more responsive.  
Intuitively, we know that during times of financial crisis, market volatility rises and industries become 
more correlated. In Figure 3.2 , we plot the mean pair-wise correlation ij for all industry pairs in the 
USE4 model. The dashed grey curve is obtained us ing a model without the Country factor, and the dark 
solid line is for a model with the Country factor. The average correlations are si milar in magnitude, but 
the correlations are clearly much more responsi ve in the model with the Country factor.  
 

---
## Page 17

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
17 of 44Figure 3.2  
Mean pair-wise correlation between net-long pure industry fa ctors. Averages were computed across all 1770 
possible pair-wise correlations for the 60 industry factors in USE4. Results were obtained using the USE4S 
covariance matrix parameters reported in Table 4.1. Common exposures to the Country factor allow industry 
correlations to be more responsive.  
Year                           1995  1997  1999  2001  2003  2005  2007  2009  2011  Mean Pairwise Correlation
0.30.40.50.60.70.80.91.0 No Country Factor
With Country Factor
 
We must also verify that the correlations in the model including the Country factor are more accurate. 
For this purpose, we created long/short industry-pair  portfolios for all possible combinations of USE4 
industries. The returns to these portfolios are given by ijff , and have a large fraction of their risk 
deriving from the correlation term. To evaluate th e accuracy of the risk forecasts, we computed 
standardized returns and Mean Rolling Absolute Deviat ions (MRAD) for these portfolios, as described in 
Appendix A. We found that including the Country factor reduced the MRAD statistic by about 80 bps on 
average during a roughly 16-year sample  period (30-Jun-1995 to 31-May-2011).  
4. Factor Covariance Matrix  
4.1 Established Methods 
The factor covariance matrix predicts the volatilities and correlations of the fact ors and thus represents 
a second key pillar for constructing a high-quality risk  model. The USE4 factor covariance matrix builds 
upon methodologies used in the Barra Global Equity  Model, GEM2, as described by Menchero, Morozov, 
and Shepard (2008). In this section, we provide a br ief overview of these established methodologies. 
Innovations and enhancements to the factor covaria nce matrix methodology ar e described in Section 
4.2 and Section 4.3.  

---
## Page 18

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
18 of 44Estimation of the USE4 factor covariance matrix fo llows a multi-step process. The first step is to 
compute the factor correlation matrix from the set of daily factor returns. We employ exponentially 
weighted averages, characterized by the factor correlation half-life parameter F
. This approach gives 
more weight to recent observations  and is an effective method for de aling with data non-stationarity.  
Special care must be exercised when selecting the correlation half-life. To ensure a well-conditioned 
correlation matrix, the half-life must be sufficiently long so that the effective number of observations T 
is significantly greater than the number of factors K. An ill-conditioned factor covariance matrix may be 
problematic for portfolio optimization purposes, sinc e active portfolios can be constructed that exhibit 
spuriously low factor risk. On the other hand, if the co rrelation half-life is too long, then undue weight is 
placed on distant observations that have little relation to current market conditions. Finding the proper 
balance between these two limits is essential for producing a reliable correlation matrix. 
The prediction horizon of the USE4 model is one mo nth. The factor correlation matrix, however, is 
estimated from daily factor returns. We must therefor e account for the possibility of serial correlation in 
factor returns, as these may affect ri sk forecasts over a longer horizon.  
In USE4, we employ the Newey-West methodology (1987)  to account for serial-correlation effects. A key 
parameter in this approach  is the number of lags FL over which the serial correlation is deemed 
important. For instance, 2FL implies that the return of any factor may be correlated with the return 
of any other factor with in a two-day time span. 
Another complication in estimating the factor correlati on matrix arises from the case of missing factor 
returns. In a global model, country holidays are one possible reason for missing factor returns. In single 
country models, missing factor returns may arise fr om using time series of differing lengths. For 
instance, the Internet factor may appear in the mode l only after the start date of the cross-sectional 
regressions.  
We use the EM algorithm of Dempster  (1977) to estimate the correlatio n matrix for the case of missing 
factor returns. This method employs an iterative pr ocedure to estimate the correlation matrix. The EM 
algorithm also refines the correlation forecasts as new information flows into the model, while ensuring 
that the correlation matrix is positive semi-definite. 
With the correlation matrix thus computed, the next step is to compute the factor volatilities. We use 
exponentially weighted averages, with half-life parameter F
. In estimating factor volatilities, we also 
employ the Newey-West approach allowing factor retu rns to be auto-correlated over a number of lags 
FL. Next, we construct the initial co variance matrix by scaling in the factor volatilities. That is, the 
covariance between factors i and j is given by 
0
ij ij i jF  ,                                                                        (4.1) 
where i and j are the factor volatilities and ij is their respective correlation.  
Selecting the proper factor volatility half-life is an  important modeling decision that involves analyzing 
the trade-off between accuracy and responsiveness on  the one hand, and stability on the other. If the 
half-life is too long, the model gives undue weight to  distant observations that  have little to do with 
current market conditions. This leads to stable risk forecasts, but at the cost of reduced accuracy. By 
contrast, a short half-life makes the model more resp onsive, generally improving the risk forecasts, but 
at the cost of increased variability.  

---
## Page 19

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
19 of 44In general, the volatility half-life ca n be made considerably shorter than the correlation half-life. This is 
because sampling error for the diagonal elements has very little impact on the conditioning of the covariance matrix, whereas the effect is much larg er for the off-diagonal elements. Of course, the 
volatility half-life cannot be made arbitrarily small; if  it is too short, then sa mpling error can become so 
dominant that the risk forecasts are not only less stable, but also less accurate.  
The parameters that are used to compute th e USE4S and USE4L models are presented in Table 4.1 . Note 
that the VRA (Volatility Regime Adjustment) half-life re ported in Table 4.1 is described in Section 4.3. 
 
Table 4.1  
Factor covariance matrix parameters for the USE4 model. All values are reported in trading days. 
Factor Newey-West Factor Newey-West Factor
Volatility Volatility Correlation Correlation VRA
Model Half-Life Lags Half-Life Lags Half-Life
USE4S 84 5 504 2 42
USE4L 252 5 504 2 168 
 
4.2 Eigenfactor Risk Adjustment 
In 1952, Markowitz (1952) established the mean- variance framework for constructing efficient 
portfolios. The required inputs include a set of expe cted asset returns and the asset covariance matrix, 
with the output being an optimal portfolio that has maximum expected return for a given level of risk. 
This framework forms the basis of modern portfolio theory and has led to a rich body of academic 
literature, as well as widespread adoption within the quantitative investment community. 
Given the level of attention that the mean-variance framework has attracted, it is perhaps surprising 
that more than 40 years passed before it was empi rically demonstrat ed (see Muller, 1993) that risk 
models have a systematic tendency to underpredict the risk of optimized portfolios. More recently, 
Shepard (2009) derived an analyt ic result for the magnitude of the bias. Under assumptions of 
normality, stationarity, and ma ny assets (i.e., the large N limit), he found 
1/pred
trueKT,                                                                      (4.2) 
where true  is the true volatility of the optimized portfolio, pred  is the predicted volatility from the risk 
model, K is the number of factors, and T is the effective number of obse rvations used to compute the 
covariance matrix. The basic cause of the bias is estima tion error; in essence, stocks that appear to be 
good hedges in-sample tend to be less effective at hedging risk out-of-sample.  
An important innovation in the USE4 model is to id entify portfolios that reliably capture these biases, 
and to build corrections directly into the factor co variance matrix. This section provides a high-level 
overview of the methodology, with additional de tails given in Appendix B. Further analysis and 
discussion are provided by Menchero, Wang, and Orr (2011). 

---
## Page 20

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
20 of 44The underestimation of risk for optimized port folios is closely linked with the concept of eigenfactors . 
Mathematically, eigenfactors are given by the eigenv ectors of the factor covariance matrix; financially, 
they represent uncorrelated portfolios of pure factors.  
In Figure 4.1  we report eigenfactor bias statistics computed  using the factor covariance matrix given by 
Equation 4.1. As described in Appendix A, the bias st atistic essentially represents the ratio of realized 
risk to predicted risk. The factor returns were take n from the USE4 model and the parameters used to 
construct 0
ijF were the same as for the USE4S model, as reported in Table 4.1. We standardize the 
eigenfactors to be unit norm and so rt the eigenfactors from low volat ility to high volatility. Figure 4.1 
demonstrates a strong and direct relationship betw een the bias statistic of the eigenfactor and the 
eigenfactor number. More specifically, the lowest vola tility eigenfactors have realized volatilities about 
40 percent higher than their predicted volatilities and fall well outside the 95 percent confidence 
interval (indicated by the dashed horizontal lines). The larger eigenfactors, by contrast, fall mostly within the confidence interval.  
Figure 4.1  
Bias statistics of eigenfactors using the unadjusted covariance matrix of Equation 4.1. Results were 
computed using the USE4S covariance matrix parameters reported in Table 4.1. The sample period 
comprised 191 months, from July 1995 through May 2011. The 95-percent confidence interval is indicated by 
the two dashed horizontal lines. While the large eigenfactors lie mostly within the confidence interval, the 
small eigenfactors fall well outside it. 
Eigenfactor Number0 1 02 03 04 05 06 07 0Bias Statistic
0.70.80.91.01.11.21.31.41.51.61.7
 
 
While these results are intriguing, quantitative port folio managers are more interested in optimized 
portfolios. To study thes e, we generated 100 random alpha signals at the factor level, drawn from a 
standard normal distribution. Each alpha signal was ke pt constant across time, but centered at the start 
of each month so that the cap-weighted alpha of th e estimation universe was zero. We then constructed 
the minimum risk factor portfolio subject to the constraint that 1. In Figure 4.2 , we plot the bias 

---
## Page 21

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
21 of 44statistics for the optimized factor portfolios. We ob serve the classic example of underprediction of risk 
of optimized portfolios, with all 100 bias statisti cs falling outside of the confidence interval. 
Figure 4.2  
Bias statistics of 100 optimized factor portfolios usin g the unadjusted covariance matrix of Equation 4.1. 
Factor alphas were randomly drawn from a standard normal distribution, and held constant across time for 
each portfolio. Optimized factor portfolios were cons tructed at the start of each month by minimizing 
predicted factor risk subject to the 1 constraint. Results were computed using the USE4S covariance 
matrix parameters re ported in Table 4.1. The sample period co mprised 191 months, from July 1995 through 
May 2011. The 95-percent confidence interval is indicated by the two dashed horizontal lines. All 100 
observations fall outside the confidence interval, indicating underprediction of risk. 
Optimized Portfolio Number0 1 02 03 04 05 06 07 08 09 0 1 0 0Bias Statistic
0.70.80.91.01.11.21.31.41.51.61.7
 
 
As described in Appendix B, we can estimate the magnitude of the empirical eigenfactor biases via 
Monte Carlo simulation. Although we cannot directly observe the true factor covariance matrix, we suppose for a moment that the sample factor covar iance matrix represents the “truth.” We then 
simulate histories of factor returns (using, for instance, the Cholesky decomposition) whose true 
distribution is drawn from the multivariate normal given by the sample factor covariance matrix. For each history, we compute a simulated factor covaria nce matrix. By comparing the predicted volatilities 
of the simulated eigenfactors with their “true” vola tilities (i.e., using the sample factor covariance 
matrix), we determine the size of the simulated volatility bias.  
In Figure 4.3 , we plot the average simulated volatility bias over the entire sample period. Qualitatively, 
Figure 4.3 is very similar to Figure 4.1, indicating that the simulations are effective in capturing the 
biases. Quantitatively, however, we see that the re alized biases are larger in magnitude than those 
observed in the simulations. Note that the simulati ons assume normality and stationarity, both of which 
are violated in practice. As described in Appendix B, slightly larger adjustments are required to fully 
remove the biases of the eigenfac tors. We refer to this as the scaled adjustment, defined by Equation B8 

---
## Page 22

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
22 of 44of Appendix B. By contrast, Figure 4.3 was obtain ed using Equation B7; we refer to this as the simulated 
adjustment. 
 
Figure 4.3  
Mean simulated volatility bias, computed per Equation  B7. Averages were comput ed from 30-Jun-1995 to 31-
May-2011. Results were obtained using the USE4S parameters reported in Table 4.1. 
Eigenfactor Number0 1 02 03 04 05 06 07 0Simulated Volatility Bias
0.91.01.11.21.3
 
 
Since the sample factor covariance matrix and si mulated factor covariance matrix share the same 
estimator, we assume that they also suffer from the same biases. We then adjust the eigenvariances of 
the sample factor covariance matrix. The final step, as described in Appendix B, is to rotate back to the 
original pure factor basis. 
In Figure 4.4  we show the bias statistics of the eigenfac tors using the eigen-adjusted covariance matrix. 
The results were computed using the scaled adjustment  of Equation B8. We see that most observations 
now fall squarely within the confidence interval, in dicating unbiased risk forecasts. Furthermore, the 
relationship between the bias statistic and the eige nfactor number is now essentially flat, in sharp 
contrast to Figure 4.1.  
  

---
## Page 23

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
23 of 44Figure 4.4  
Bias statistics of eigenfactors using the eigen-adjusted  covariance matrix of Equation B10. Results were 
computed using the USE4S covariance matrix parameters reported in Table 4.1. The sample period 
comprised 191 months, from July 1995 through May 2011. Most observations fall within the 95-percent 
confidence interval. 
Eigenfactor Number0 1 02 03 04 05 06 07 0Bias Statistic
0.70.80.91.01.11.21.31.41.51.61.7
 
 
Again, while this result is encouraging, the prim ary interest of quantitative managers is not in 
eigenfactors, but rather in optimized portfolios. In Figure 4.5  we report the bias statistics of the 
portfolios optimized using the same alpha signals as in  Figure 4.2. The results were computed using the 
scaled adjustment of Equation B8. This demonstrat es that the eigen-adjusted covariance matrix has 
essentially removed the biases of the optimized factor portfolios as well.  
As discussed by Menchero, Wang, and Orr (2011), the Eigenfactor Risk  Adjustment may induce small 
biases for the pure factors. In particular, the factors wi th the smallest volatilities (i.e., the style factors) 
tend to have their volatilities adjusted slightly upward. To mitigate this effect, in the USE4 Model we employ the milder simulated adjustment defined by Equation B7. We find that this approach significantly reduces forecasting biases for optimi zed portfolios, while also ensuring that the bias 
statistics for the style factors fall mostly within the 95-percent confidence interval as expected. 
  

---
## Page 24

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
24 of 44 
Figure 4.5  
Bias statistics of 100 optimized factor portfolios using th e eigen-adjusted covariance matrix of Equation B10. 
Factor alphas were randomly drawn from a standard normal distribution, and held constant across time for 
each portfolio. Optimized factor portfolios were cons tructed at the start of each month by minimizing 
predicted factor risk subject to the 1 constraint. Results were computed using the USE4S covariance 
matrix parameters re ported in Table 4.1. The sample period co mprised 191 months, from July 1995 through 
May 2011. Most observations fall within the 95-percent confidence interval. 
Optimized Portfolio Number0 1 02 03 04 05 06 07 08 09 0 1 0 0Bias Statistic
0.70.80.91.01.11.21.31.41.51.61.7
 
 
4.3 Volatility Regime Adjustment 
In the traditional approach to estimating factor volatilitie s, each factor is consider ed in isolation. That is, 
volatility estimates for a particular factor are based exclusively on the time series of returns to the 
individual factor.  
Another significant innovation in the USE4 model is  to use cross-sectional observations to produce 
timelier and more accurate forecasts of factor volat ility. The basic intuition behind this method is that 
the returns and risk forecasts of the other factors provide additional information for refining the volatility estimates. In particular, if cross-sectiona l observations show that the model is consistently 
overforecasting or underforecasting risk over a recent  period, then the volatilities of all factors can be 
collectively adjusted to remove this bias.  
More specifically, let 
ktf be the return to factor k on day t, and let kt be the one-day volatility 
forecast for the factor at the start of the day. The st andardized return of the factor is given by the ratio 
kt ktf , and should have standard deviation close to 1 if the risk forecasts are accurate. Normally, as 

---
## Page 25

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
25 of 44described in Appendix A, we compute the time-series  standard deviation to investigate whether an 
individual factor is unbiased across time.  
Alternatively, we can compute the cross-sectional  standard deviation to investigate whether the factor 
volatility forecasts are collectively unbiased at a give n point in time. We define the factor cross-sectional 
bias statistic F
tB on day t as 
21F kt
t
k ktfBK
 ,                                                                   (4.3) 
where K is the total number of factors. This quantity represents an instantaneous measure of factor 
risk bias. For instance, if the risk forecast s were too small on a particular day, then 1F
tB. By observing 
the cross-sectional bias statistics over time, we ca n determine the extent to which volatility forecasts 
should be adjusted to remove these biases. 
We define the factor volatility multiplier F as an exponentially weighted average 
2F
Ft t tBw  ,                                                                  (4.4) 
where tw is an exponential weight with Volatility Regime Adjustment half-life F
VRA . This parameter 
serves as the primary determinant of model resp onsiveness for factor risk. The Volatility Regime 
Adjustment forecasts are given by  
kF k .                                                                           (4.5) 
This is equivalent to multiplying the entire  factor covariance matrix by a single number, 2
F. As a result, 
the Volatility Regime Adjustment has no effect on factor correlations.  
We define the factor cross-sectional volatility (CSV) on day t as 
2 1F
tk t
kCSV fK .                                                                   (4.6) 
In Figure 4.6  we plot factor CSV, together wi th the factor volatility multiplier,F. Results were computed 
using the USE4S model parameters, shown in Table 4.1. 
   

---
## Page 26

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
26 of 44Figure 4.6  
Factor cross-sectional volatility (CSV) and factor volatilit y multiplier. Factor CSV le vels are reported in daily 
percentage and smoothed using a 42-day half-life. 
Year1995  1997  1999  2001  2003  2005  2 007  2009  2011  Factor Volatility Multiplier
0.20.40.60.81.01.21.41.61.8
Factor CSV (percent daily)
0.20.40.60.81.01.21.41.61.8Factor
VolatilityMultiplier
Factor
CSV
 
 
It is instructive to analyze the interplay between fa ctor CSV levels and the factor volatility multiplier. 
From 1995-1998, we see that factor CSV gradually ro se from about 60 bps to roughly 80 bps per day. 
During this same time, the volatility multiplier F was only slightly greater than 1, indicating that the 
traditional time-series approach did quite well predic ting factor volatility, needing only a slight upward 
adjustment.  
The Russian Default, in the summer of 1998, marks th e first major crisis of the sample period. Over a 
very short window, we see that factor CSV spiked  from about 70 bps to above 100 bps per day. The 
Volatility Regime Adjustment quickly detected the increased volatility levels, with F rapidly adjusting to 
a value of nearly 1.4. Over the subsequent year, fa ctor CSV stabilized in the range of 100-110 bps daily. 
During this period, the traditional time-series appr oach adjusted to the new volatility levels and F 
decayed back to 1 by the fall of 1999.  
Another interesting period to consider is 2005-2007, during which the factor CSV was quite stable at 
about 70 bps per day. During stable periods, the trad itional approach works well, and again we see that 
the volatility multiplier was very close to 1. Howeve r, as the financial crisis unfolded, from August 2007 
until the end of 2008, factor  CSV increased dramatically to nearly  180 bps per day. During the entire 
financial crisis, the volatility multiplier was significantly  greater than 1, reaching a peak of about 1.45 in 
late 2008. During 2009, as the financial crisis subsided , factor CSV plummeted back  to pre-crisis levels. 
Again, the Volatility Regime Adjustment detected this sudden drop in volatility and F fell to 0.7 by the 
end of 2009, thereby reducing the volatility forecast by  30 percent relative to the traditional approach. 
We have seen that the factor volatility multiplier re sponds quickly and intuitiv ely to market shocks in 
volatility. To evaluate the performance gain of th e Volatility Regime Adjustment, we compute the mean 

---
## Page 27

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
27 of 44of the rolling 12-month bias statistics for the factors over the sample period. Th e results are plotted in 
Figure 4.7 , together with the corresponding results comput ed without the Volatility Regime Adjustment. 
Over the vast majority of the sample period, the Volatility Regime Adjustment produced mean bias 
statistics that were closer to 1. During times of  extreme market stress, th e outperformance was even 
greater. For instance, during the most severe part of  the financial crisis in 2008, the Volatility Regime 
Adjustment provided mean bias st atistics very close to 1. By co ntrast, without th e methodology we 
significantly underpredicted risk. Similarly, in the wake of the financial crisis, the Volatility Regime 
Adjustment again produced bias statistics much closer to 1, whereas without the methodology we 
significantly overforecasted risk fo r an extended period of time.  
 
Figure 4.7  
Mean rolling 12-month bias statistics for USE4 factors, with and without the Volatility Regime Adjustment. 
Results were computed using the USE4S covariance matrix  parameters reported in Table 4.1. The Volatility 
Regime Adjustment led to mean bias statistics closer to 1 over most of the sample period. 
Year1996  1998  2000  2002  200 4  2006  2008  2010  2012  Mean Bias Statistic
0.60.70.80.91.01.11.21.31.4
With Volatility 
Regime
AdjustmentUnadjusted
 
 
In summary, without the Volatility Regime Adju stment we observed the classic signature of 
underprediction of risk entering a crisis, followed by overprediction afterwards. The Volatility Regime 
Adjustment greatly reduced these non-stationarity biases.  
  

---
## Page 28

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
28 of 445. Specific Risk  
5.1 Established Methods 
 
Accurate prediction of specific vo latility constitutes the third essentia l pillar for producing a high-quality 
risk model. The USE4 specific risk model builds upon methodological advances introduced with the European Equity Model (EUE3), as described by Brin er, Smith, and Ward (2009). The EUE3 model utilizes 
daily observations to provide timely estimates of specif ic risk directly from the time series of specific 
returns. A significant benefit of this approach is that specific risk is estimated individually for every stock, 
thus reflecting the idiosyncratic nature of this risk source.  
The specific returns are obtained from  daily cross-sectional regressions, 
nt nk kt nt
krX f u   ,                                                           (5.1) 
where ntr is the return of stock n on day t, nkX is the stock exposure to factor k, ktf is factor return, 
and ntu is the specific return of the stock. It is u nderstood that although the factor exposure matrix 
varies slowly with time, the t subscript is suppressed for notational simplicity.  
Asset-level specific risk is computed directly  from the time series of specific returns, 
2 TS NW
nn t n t n tCw u u       ,                                                  (5.2) 
where tw is an exponential weight characterized by  the specific volatility half-life parameter S
, and 
NW
nC  is the Newey-West serial correlation adjustment for stock n. To estimate NW
nC , we use an auto-
correlation half-life parameter S
 and allow specific returns to be correlated over a number of lags SL.  
While the time-series approach offers the advantage  of estimating specific volatility directly, one 
challenge is that not all stocks are well-suited to su ch an estimation methodolog y. For instance, recently 
issued IPOs lack sufficient history to reliably estimate  their specific risk. Similarly, thinly traded stocks 
often exhibit poor return characteristics such as consecutive days of zero returns followed by large 
returns on days when the stock eventually trades. Earnings announcements can also lead to extreme 
jumps in specific returns that make the ti me-series specific-risk forecasts unreliable. 
For such stocks, the USE4 model follows the EUE3 trea tment and blends the asset-level forecast with the 
fit value from a structural model. More specifically, we define a blending parameter n that equals 1 if 
the stock has sufficiently few missing returns and the specific returns are not excessively fat tailed. For 
stocks that strongly violate either of these conditions, n is set to zero. In general, n varies from 0 to 1, 
although most stocks in USE4 have 1n.  
  

---
## Page 29

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
29 of 44To estimate the structural model, we take all stocks with 1n and regress the logarithm of specific 
volatility forecasts against the factors in the model, 
 lnTS
nn k k n
kXb     ,                                                         (5.3) 
where kb is the regression coefficient and n is the residual. We perform th is cross-sectional regression 
daily. The structural specific ri sk forecasts are then given by 
0expSTR
nn k k
kEX b  ,                                                        (5.4) 
where 0E is a number slightly greater than 1 that is required to remove the small bias arising from 
exponentiation of the residuals. The intuition behind the structural model is th at stocks with similar 
characteristics are also likely to h ave similar specific volatilities.  
The blended specific risk forecast is given by 
 ˆ 1TS STR
nn n n n     .                                                           (5.5) 
As most stocks in USE4 have 1n, they receive the full weight fr om the time-series component.  
5.2 Bayesian Shrinkage 
One potential problem with using a pure time-series a pproach is that specific volatilities may not fully 
persist out-of-sample. In particular, stocks with eith er extremely low or extremely high specific volatility 
forecasts tend to revert to the mean. To illustrate  this effect, every month we segment stocks into 
deciles based on their specific ri sk forecasts as given by Equation 5.5. We then compute the bias 
statistics, as described in Appendix A, for each decile over the entire sample period. The results are plotted in Figure 5.1 , and show that the bias statistics depe nd strongly on the volatility decile. More 
specifically, Equation 5.5 tends to underpredict the lo w-volatility stocks and overpredict those with high 
volatility. These biases can be problematic for portfo lio construction purposes, since stocks that appear 
to have low specific volatility in-sample may exhibit higher volatility out-of-sample. 
  

---
## Page 30

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
30 of 44 
Figure 5.1  
Bias statistics of specific returns groupe d by specific risk deciles (sorted from low to high), without Bayesian 
shrinkage adjustments. Specific risk was computed per Equation 5.5. Both cap-weighted and equal-weighted 
results are reported. The sample period comprised 191 months, from July 1995 through May 2011. Without 
Bayesian shrinkage, not e the tendency to overpredic t high-volatility stocks and underpredict low-volatility 
stocks.  
Specific Volatility Decile123456789 1 0Bias Statistic
0.900.920.940.960.981.001.021.041.061.081.101.12
Cap Weighted
Equal WeightedNo Shrinkage
 
 
To remove this bias, we shrink our estimates toward  the cap-weighted mean specific volatility for the 
size decile ns to which the stock belongs. More precisely, the shrunk estimate SH
n  is given by 
ˆ () 1SH
nn n n nvs v   ,                                                   (5.6) 
where ˆn is the blended forecast (given by Equation 5.5) and nv is the shrinkage intensity that 
determines the weight given to the Bayesian prior, also known as the shrinkage target,  
ˆ ()
nnn n
nssw 
  ,                                                                (5.7) 
where nw is the capitalization weight of stock n with respect to the size de cile. The shrinkage intensity 
is given by 
ˆ ()
ˆ () ()nn
n
nn nqsvs qs
 ,                                                       (5.8) 
where q is an empirically determined shrinkage parameter and  

---
## Page 31

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
31 of 442 1ˆ () ()()nnn n
nsnssNs 
                                                         (5.9) 
is the standard deviation of specif ic risk forecasts within the size decile. The intuition behind this 
approach is straightforward: the more ˆn deviates from the mean, the greater the weight we assign to 
the Bayesian prior ()ns . 
In Figure 5.2  we show the bias statistics for the same sp ecific risk deciles, now after applying the 
Bayesian shrinkage technique. We see that the bias statistics are closer to the ideal value of 1. 
Furthermore, the relationship is essentially flat, so that we do not observe significant biases associated 
with specific volatility levels. 
 
Figure 5.2  
Bias statistics of specific returns grouped by specific risk deciles (sorted from low to high), with Bayesian 
shrinkage adjustments. Specific risk was computed using Equation 5.6. Both cap-weighted and equal-
weighted results are reported. Th e sample period comprised 191 months, from July 1995 through May 2011. 
The Bayesian shrinkage technique largely removes the biases associated with either extreme. 
Specific Volatility Decile123456789 1 0Bias Statistic
0.900.920.940.960.981.001.021.041.061.081.101.12
Cap Weighted
Equal WeightedWith Shrinkage
 
 
5.3 Volatility Regime Adjustment 
The specific risk model follows a similar approach as for the factor covariance matrix and adjusts the 
volatility forecasts based on cross-sectional observations. Let ntu be the specific return to stock n on 
day t, and let nt be the one-day volatility forecast at the st art of the day, obtained from Equation 5.6 

---
## Page 32

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
32 of 44after removing adjustments for serial correlation. We de fine the specific cross-se ctional bias statistic on 
day t as the cap-weighted average 
2
S nt
tn t
n ntuBw
 .                                                       (5.10) 
This quantity represents an instantaneous measure of specific risk bias. For instance, if the model 
underpredicts specific risk on day t, then 1S
tB.  
We define the specific volatility multiplier  by  
2S
St t
tBw  ,                                                                 (5.11) 
where tw is an exponential weight with a Volat ility Regime Adjustment half-life parameter S
VRA . In 
order to ensure that the specific risk model has cons istent responsiveness with th e factor risk model, we 
select SF
VRA VRA . The Volatility Regime Adjustment forecasts are then given by  
SH
nS n ,                                                                  (5.12) 
where SH
n  is the specific risk forecast after Ba yesian shrinkage (i.e., Equation 5.6).  
We define the specific cross-sectional volatility (CSV) as 
2 S
tn t n t
nCSV w u .                                                                  (5.13) 
In Figure 5.3  we plot the specific CSV, together with the specific volatility multiplier S. Results were 
computed using the USE4S model parameters, reported in Table 5.1 . 
  

---
## Page 33

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
33 of 44 
Figure 5.3  
Specific cross-sectional volatility (CSV) and specific vola tility multiplier. Specific C SV levels are reported in 
daily percentage and smoothed using a 42-day half-life. 
Year1995  1997  1999  2001  2003  2005  2007  2009  2011  Specific Volatility Multiplier
0.60.81.01.21.41.6
Specific CSV (percent daily)
0.51.01.52.02.53.0Specific
Volatility
MultiplierSpecific
CSV
 
 
 
Table 5.1  
Specific risk parameters for the USE4 model. Except for the dimensionless shrinkage parameter q, all values 
are reported in trading days.  
Specific Newey-West Newey-West Bayesian Specific
Volatility Auto-Corr. Auto-Corr. Shrinkage VRA
Model Half-Life Lags Half-Life Parameter q Half-Life
USE4S 84 5 252 0.1 42
USE4L 252 5 252 0.1 168 
 
It is interesting to compare Figure 5.3 for specific risk with the corresponding result for factor risk, 
shown in Figure 4.6. Qualitatively, the plots are rema rkably similar. For instance, specific CSV and factor 
CSV each exhibited major peaks during the Internet Bubble period of 2000 and the financial crisis of 
2008. The differences, rather, are primarily in the details. For instance, factor CSV reached a maximum 
in 2008 whereas specific CSV reache d an absolute peak in 2000.  
The volatility multipliers also behave similarly. For example, during the stable period 2005-2007 
immediately prior to the financial crisis, the specific volatility multiplier S was very close to 1. At the 

---
## Page 34

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
34 of 44height of the financial crisis, S reached a peak of about 1.45 in la te 2008, and hit a minimum near 0.75 
at the end of 2009.  
The specific volatility multiplier responds intuitivel y to market shocks. To demonstrate the performance 
gain of the Volatility Regime Adjustment, we compute the mean of the rolling 12-month bias statistics of 
the specific returns. Th e results are plotted in Figure 5.4 , together with the corresponding results 
computed without the Volatility Regime Adjustment.   
Figure 5.4  
Mean rolling 12-month bias statistics for specific returns, with and without the Volatility Regime Adjustment. 
Results were equal weighted across the USE4 estimat ion universe and computed using the USE4S specific 
risk parameters reported in Table 5.1. The Volatility Regi me Adjustment led to mean bias statistics closer to 1 
over most of the sample period. 
Year                           1996  1998  2000  2002  200 4  2006  2008  2010  2012  Mean Bias Statistic
0.60.70.80.91.01.11.21.31.4
UnadjustedWith Volatility
Regime Adjustment
 
 
Similar to Figure 4.7, over most of the sample period  we see a significant benefi t in the accuracy of the 
risk forecasts, with the performance gain becoming  even greater during times of financial stress. For 
instance, during the financial crisis, the Volatility Regi me Adjustment produced bias statistics very close 
to 1, whereas without the methodology we observed the classic signature of underprediction during the 
crisis, followed by an extended period of overprediction after the crisis.   

---
## Page 35

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
35 of 446. Conclusion 
MSCI has a long and proud tradition in developing rigorous, innovative, and pioneering solutions for the 
investment management community. As the industry  leader for portfolio construction and equity 
analytics, we are committed to the continual improv ement of the models, tools, and products that we 
provide to our clients. We believe in the value of high-quality research and it remains a cornerstone of 
our approach to investment problem solving.  
The new Barra US Equity Model, USE4, is the result  of these research efforts in combination with 
extensive client consultations. The USE4 Model inco rporates many methodological innovations designed 
to address long-standing problems in risk modeling. For instance, the Eigenfactor Risk Adjustment 
addresses the issue of underestimation of risk of op timized portfolios, and leads to better conditioning 
of the covariance matrix. The Volatility Regime Adjust ment calibrates volatility levels to current market 
levels and represents an important determinant of ri sk, especially during times of market turmoil. The 
introduction of a country factor leads to greater in sight into the sources of portfolio risk, as well as 
providing timelier forecasts of industry correlations.  Another enhancement is the use of a Bayesian 
adjustment technique to reduce biases in specific risk forecasts.  
During consultations, our clients stre ssed the importance of factor structure. In particular, they strongly 
endorsed the value of our unique multiple industry exposure methodology. In response to strong client demand, the USE4 Model continues to provide mult iple industry exposures. Furthermore, extensive 
research was performed to customize the industry st ructure to the local mark et. The USE4 Model also 
offers an enhanced set of style factors that have  undergone comprehensive empirical and statistical 
testing. These rigorous procedures assure a robust fa ctor structure with a high degree of explanatory 
power. 
Building high-quality risk models is a challenging an d fascinating endeavor. While the USE4 model marks 
a significant milestone in our research and developmen t efforts, we remain committed to continuing our 
search for new and better ways to model risk. 
  

---
## Page 36

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
36 of 44Appendix A: Review of Bias Statistics  
A1. Single-Window Bias Statistics 
A commonly used measure to assess a risk model’s accu racy is the bias statisti c. Conceptually, the bias 
statistic represents the ratio of re alized risk to forecast risk.   
Let ntR be the return to portfolio n over period t, and let nt be the beginning-of-period volatility 
forecast. Assuming pe rfect forecasts, the standardized return, 
nt
nt
ntRb ,                                                                                    (A1) 
has an expected standard deviation of  1. The bias statistic for portfolio n is the realized standard 
deviation of standardized returns, 
2
11
1T
nn t n
tB bbT  ,                                                                 (A2) 
where T is the number of periods in the observation window. 
Assuming normally distributed returns and perf ect risk forecasts, for sufficiently large T the bias 
statistic nB is approximately normally distributed about 1, and roughly 95 percent of the observations 
fall within the confidence interval, 
12 / , 12 /nB TT    .                                                          (A3) 
If nB falls outside this interval, we reject the null hy pothesis that the risk forecast was accurate.  
If returns are not normally distributed, however, then  fewer than 95 percent of the observations will fall 
within the confidence interval, even  for perfect risk forecasts. In Fi gure A1, we show simulated results 
for the percentage of observations actually falling within this interval, plotted versus observation 
window length T, for several values of kurtosis k.  
For the normal case (kurtosis 3k), except for the smallest values of T, the confidence interval indeed 
captures about 95 percent of the observations. As the kurtosis increases, however, the percentage 
falling within the interval drops significantly. For instance , at a kurtosis level of 5, only 86 percent of bias 
statistics fall inside the confidence inter val for an observation window of 120 periods. 
 
  

---
## Page 37

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
37 of 44A2. Rolling-Window Bias Statistics 
The purpose of bias-statistic testing is to assess th e accuracy of risk forecasts, typically over a long 
sample period. Let T be the length of the observation window,  which corresponds to the number of 
months in the sample period. One possibility is to se lect the entire sample period as a single window, 
and to compute the bias statistic as in Equation A2. Th is would be a good approach if financial data were 
stationary, as sampling error is reduced by increasi ng the length of the window. In reality, however, 
financial data are not stationary. It is possible to significantly overpredict ri sk for some years, and 
underpredict it for others, while ending up with a bias statistic close to 1.  
Often, a more relevant question is to study the accuracy  of risk forecasts over 12-month periods. For this 
purpose, we define the rolling 12-mo nth bias statistic for portfolio n, 
11
2 1()11nn t n
tB bb


 ,                                                                (A4) 
Where  denotes the first month of the 12-month window. The 12-month windows are rolled forward 
one month at a time until reaching the end of the observation window. If T is the number of periods in 
the observation window, then each portfolio will have 11T  (overlapping) 12-month windows.  
It is useful to consider, for a collection of N portfolios, the mean of the rolling 12-month bias statistics, 
1
n
nB BN  .                                                                  (A5) 
We also define (5%)B and (95%)B to be the 5-percentile and 95-percentile values for the rolling 12-
month bias statistics at a given po int in time. Assuming normal distributions and perfect risk forecasts, 
these values should be centered about 0.66 and 1.34, respectively. Plotting these quantities versus time 
for different classes of portfolios is a visually powerf ul way of understanding the predictive accuracy of 
the risk model.  
Another useful measure to consider is the 12-month mean rolling absolute deviation (MRAD), defined as 
1MRAD 1n
nBN  .                                                              (A6) 
This penalizes every deviation away from the ideal bias  statistic of 1. Smaller MRAD numbers, of course, 
are preferable to larger ones. A lo wer limit for this statistic can be obtained by assuming the ideal case 
of normally distributed returns and perfect risk forecasts, which leads to an expected value of 0.17 for 
the 12-month MRAD.  
It is interesting to consider how MRAD depends on kurtosis levels. In Figure A2 we report simulated 
results for 12-month MRAD assumi ng perfect risk forecasts. For no rmally distributed returns, as 
discussed, the expected MRAD value is 0.17. At highe r kurtosis levels, however, the expected MRAD for 
perfect forecasts increases significant ly. For instance, even at moderate kurtosis levels in the range of 
3.5 to 4.0, the 12-month MRAD  for perfect risk forecasts rises to approximately 0.19. 
 

---
## Page 38

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
38 of 44Figure A1  
Percent of observations falling wi thin the confidence interval 12 T , where T is the number of 
periods in the observation window. Results were simulated using a normal distribution (3 )k , and 
using a t-distribution with kurtosis values 5k and 10k . The standard deviations were equal to 1 in 
all cases.  
For the normal distribution, the percentage of observations inside the confidence interval quickly 
approaches 95 percent. As kurtosis is increased, ho wever, the proportion within the confidence interval 
declines considerably. 
Number of Periods, T0 20 40 60 80 100 120 140Percent in Confidence Interval7580859095100
k=10k=5k=3 (Normal)
 
 

---
## Page 39

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
39 of 44Figure A2  
Plot of 12-month MRAD versus kurtosis levels for pe rfect risk forecasts. Resu lts were simulated using a t-
distribution. 
Kurtosis3456789 1 012-Month MRAD
0.160.170.180.190.200.210.220.230.24
 
 

---
## Page 40

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
40 of 44Appendix B. Eigenfactor Risk Adjustment  
Let 0F denote the xKK  sample factor covariance matrix (FCM),  
0cov ,Ff f  ,                                                                            (B1) 
where f is the xKT  matrix of realized factor returns, K is the number of factors and T is the number 
of periods. The covariance matrix esti mator is described in Section 4.1.  
The sample FCM can be expressed in diagonal form as 
00 0 0DU F U  ,                                                                         (B2) 
where 0U is the xKK  rotation matrix whose columns are given by the eigenvectors of 0F. The thj 
element of the thk column of 0U gives the weight of pure factor j in eigenfactor k. The predicted 
variances of the eigenfactors are given by the diagonal elements of 0D. The fact that 0D is diagonal 
indicates that the eigenfactors are mutually uncorrelated.  
Although the true FCM is unobservable, we suppose for simulation purposes that the sample FCM 0F 
governs the “true” return-generati ng process. We generate a set of factor returns for simulation m as 
0 mmfU b  ,                                                                           (B3) 
where mb is a xKT  matrix of simulated eigenfacto r returns. The elements of row k of mb are drawn 
from a random normal distribution with mean zero and variance given by the diagonal element 0()Dk 
of matrix 0D. It can be easily verified that the simulated returns in Equation B3 have a true FCM given 
by 0F. Due to sampling error, however, the estimated  FCM  
 cov ,mm mFf f  ,                                                                        (B4) 
will differ from the true FCM 0F. Nevertheless, mF is unbiased in the sense that 0 []mEFF . We 
diagonalize the simulated FCM 
mm m mDU F U  ,                                                                         (B5) 
where mU denotes the simulated eigenfactors with estimated variances given by the diagonal elements 
of mD, i.e., ()mDk.  
Since we know the true distribution that governs the simulated factor returns, we can compute the true 
FCM of the simulated eigenfactors, 
0 mm mDU F U  .                                                                       (B6) 

---
## Page 41

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
41 of 44Note that since mU is not composed of the “true” eigenfactors, the matrix mD is not diagonal. 
Nevertheless, our current focus is on the diagonal elements of the matrix. 
As shown in Figure 4.1, the predicted volatilities of  the empirical eigenfactors are biased. We compute 
the simulated  volatility biases according to 
1( )()()m
m mDkvkM Dk
 ,                                                                (B7) 
where M is the total number of simulations. The simula ted volatility bias is computed daily, and the 
average over the entire sample period is plotted in Figure 4.3. As shown by Menchero, Wang, and Orr (2011), the simulated volatility bias  is very stable over time. 
Qualitatively, Figure 4.3 is in good agreement with Fi gure 4.1. Closer inspecti on, however, reveals that 
the simulations do not capture the full extent of the forecasting bias. Our simulations assume both 
normality and stationarity. Real financial data, of cour se, violate both of these assumptions. In practice, 
therefore, additional scaling is required to fully remove the biases of the eigenfactors.  
To obtain the scaled version of 
()vk , and hence fully remove the eige nfactor biases, two additional 
steps are required. First, we fit the simulated volatility bias ()vk  every day using a parabola. When 
estimating the fit, we assign zero weight to the fi rst 15 eigenfactors, which has the effect of removing 
the sawtooth structure on the left side of Figure 4. 3. The second step is to scale the fit values in 
proportion to their deviation from 1, 
 () () 1 1SPvk a vk  ,                                                          (B8) 
where ()Svk  is the scaled value, ()Pvk  is obtained from the parabolic fit, and 1.4a  is an empirically 
determined constant. Empirically, we find that this procedure is effective at removing the eigenfactor 
biases, as indicated in Figure 4.4. Furthermore, we co nfirmed that this procedure is robust over different 
sub-periods. 
As discussed by Menchero, Wang, and Orr (2011), this procedure may induce small biases at the 
individual pure factor level. To mitigate this effect , in the USE4 Model we adopt the milder simulated 
adjustment given by Equation B7. We find that this approach significantly reduces the forecasting biases 
for optimized portfolios, while also ensuring that the bias statistics of the individual factors fall mostly 
within the 95-percent confid ence interval as expected. 
We now assume that the sample FCM 0F, which uses the same covariance estimator as the simulated 
FCM mF, also suffers from the same biases. Let 0D denote the diagonal FCM whose eigenvariances have 
been adjusted  
2
00Dv D  ,                                                                            (B9) 
  

---
## Page 42

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
42 of 44where 2v is a diagonal matrix wh ose elements are given by 2()vk . The FCM in Equation B9 is now 
rotated from the diagonal basis to the pure factor basis using the sample eigenfactors. That is, 
00 0 0FU D U  ,                                                                           (B10) 
where 0F denotes the eigen-adjusted factor covariance matrix.  

---
## Page 43

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
43 of 44REFERENCES 
Briner, Beat, Rachael Smith, and Paul Ward. 2009.  “The Barra European Equity Model (EUE3).” Research 
Notes . 
Dempster, A.P., N.M. Laird, and D. B. Rubin. 1977. “Maximum  Likelihood from Incomplete Data via the 
EM Algorithm.” Journal of the Royal Statistical Society , Vol. 39, No. 1: 1-38. 
Grinold, R., and R. Kahn. 2000. Active Portfolio Management . New York: McGraw-Hill.  
Grinold, R., A. Rudd, and D. Stefek, Fall 1989. “Global Factors: Fact or Fiction.” Journal of Portfolio 
Management , vol. 16, no. 1: 79-88. 
MSCI, Inc. 2010. “Global Style Factors.” MSCI Research Insight . 
Markowitz, Harry. 1952. “Portfolio Selection.” Journal of Finance , vol. 7: 77-91. 
Menchero, Jose. 2010. “The Characte ristics of Factor Portfolios.” Journal of Performance Measurement , 
vol. 15, no. 1 (Fall): 52-62. 
Menchero, Jose, Andrei Morozov, and Peter Shepard.  2008. “The Barra Global Equity Model (GEM2).” 
Research Notes . 
Menchero, Jose, and Andrei Morozov. 2011. “Decomp osing Global Equity Cross-Sectional Volatility.” 
Financial Analysts Journal , vol. 67, no. 5 (Septemb er/October): to appear. 
Menchero, Jose, Jun Wang, and D.J. Orr. 2011. “Eigen-Adjusted Covariance Matrices.” MSCI Research 
Insight . 
Muller, Peter. 1993. “Financial Optimization.”  Cambridge University Press (Zenios): 80-98. 
Newey, W., and K. West. 1987. “A Simple, Posi tive Semi-Definite, Heteroskedasticity and 
Autocorrelation Consiste nt Covariance Matrix.” Econometrica , Vol. 55, No. 3: 703-708. 
Rosenberg, B. March 1974. “Extra-Market Componen ts of Covariance among Security Prices,” Journal of 
Financial and Quantitative Analysis , vol. 9: 263-274. 
Rosenberg, B., and V. Marathe, May 1975. “Tes ts of Capital Asset Pricing Hypotheses,” Research 
Program in Finance , Working Paper no. 32. 
Sharpe, W.F. September 1964. “Capital Asset Prices: A Theory of Market Equilibrium Under Conditions 
of Risk,” Journal of Finance , vol. 19, no. 3: 425-442. 
Shepard, Peter. 2009. “Second Order Risk.” Wo rking paper, http://arx iv.org/abs/0908.2455v1.  
Shepard, Peter. 2011. “Barra Integrated Model.” Research Notes .  
Tobin, J. February 1958. “Liquidity Pref erence as a Behavior Toward Risk,” Review of Economic Studies , 
vol. 67: 65-86.  
 
  

---
## Page 44

    
 
MSCI Research  msci.com  
© 2011 MSCI Inc. All rights reserved.  
Please refer to the disclaimer at the end of this document RV May 2011 Model Insight
USE4 Methodology
August 2011 
44 of 44Client Service Information is Available 24 Hours a Day 
clientservice@msci.com  
Notice and Disclaimer 
 This document and all of the information contained in it, including without limitation all text, data, graphs, charts (collecti vely, the “Information”) is the property of MSCl Inc. or its 
subsidiaries (collectively, “MSCI”), or MSCI’s licensors, direct or indirect suppliers or any third party involved in making or  compiling any Information (collectively, with MSCI, the 
“Information Providers”) and is provided for informational purposes only.  The Information may not be reproduced or redissemina ted in whole or in part without prior written permission 
from MSCI.  
 The Information may not be used to create derivative works or to verify or correct other data or information.   For example (bu t without limitation), the Info rmation many not be used to 
create indices, databases, risk models, analytics, software, or  in connection with the issuing, offering, sponsoring, managing or marketing of any securities, portfolios, financial products or 
other investment vehicles utilizing or based on, linked to, tracki ng or otherwise derived from the Information or any other MSC I data, information, products or services.   
 The user of the Information assume s the entire risk of any use it may make or permit to be made of the Information.  NONE OF TH E INFORMATION PROVIDERS MAKES ANY EXPRESS OR 
IMPLIED WARRANTIES OR REPRESENTA TIONS WITH RESPECT TO THE INFORM ATION (OR THE RESULTS TO BE OBTA INED BY THE USE THEREOF), AND T O THE MAXIMUM EXTENT 
PERMITTED BY APPLICABLE LAW, EACH INFORMATION PROVIDER EXPRE SSLY DISCLAIMS ALL IMPLIED WARRANTIES (INCLUDING, WITHOUT LIMITATIO N, ANY IMPLIED WARRANTIES OF 
ORIGINALITY, ACCURACY, TIMELINESS, NON-INFRINGEMENT, COMPLETENESS, MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE) WITH R ESPECT TO ANY OF THE 
INFORMATION. 
 Without limiting any of the foregoing and to the maximum extent permitted by applicable law, in no event shall any Information Provider have any liability regarding any of the 
Information for any direct, indirect, special, punitive, consequential (including lost profits) or any other damages even if no tified of the possibility of such damages. The foregoing shall not 
exclude or limit any liability that may not by applicable law be excluded or limited, including without limitation (as applicab le), any liability for death or personal injury to the extent that 
such injury results from the negligence or wilful default of itself, its servants, agents or sub-contractors.   
 Information containing any historical information, data or analysis should not be taken as an indication or guarantee of any fu ture performance, analysis, forecast or prediction.  Past 
performance does not guarantee future results. 
 None of the Information constitutes an offer to sell (or a solicitation of an offer to buy), any security, financial product or  other investment vehicle or any trading strategy.   
 MSCI’s indirect wholly-owned subsidiary Institutional Shareholder Services, Inc. (“ISS”) is a Registered Investment Adviser und er the Investment Advisers Act of 1940.  Except with respect 
to any applicable products or services from ISS (including applicable products or services from MSCI ESG Research Information, which are provided by ISS), none of MSCI’s products or 
services recommends, endorses, approves or otherwise expresses any opinion regarding any issuer, securities, financial products  or instruments or trading strategies and none of MSCI’s 
products or services is intended to constitute investment advice or a recommendation to make (or refrain from making) any kind of investment decision and may not be relied on as such. 
 The MSCI ESG Indices use ratings and other data, analysis and information from MSCI ESG Research.  MSCI ESG Research is produce d ISS or its subsidiaries.  Issuers mentioned or included 
in any MSCI ESG Research materials may be a client of MSCI, ISS, or another MSCI subsidiary, or the parent of, or affiliated wi th, a client of MSCI, ISS, or another MSCI subsidiary, including 
ISS Corporate Services, Inc., which provides tools and services to issuers.  MSCI ESG Research materials, including materials u tilized in any MSCI ESG Indice s or other products, have not 
been submitted to, nor received approval from, the United States Securities and Exchange Commission or any other regulatory bod y. 
 Any use of or access to products, services or information of MSCI requires a license from MSCI.  MSCI, Barra, RiskMetrics, ISS,  CFRA, FEA, and other MSCI brands and product names are 
the trademarks, service marks, or registered  trademarks of MSCI or its subsidiaries in the United States and other jurisdiction s.  The Global Industry Classification Standard (GICS) was 
developed by and is the exclusive property of MSCI and Standard  & Poor’s.  “Global Industry Classification Standard (GICS)” is a service mark of MSCI and Standard & Poor’s. 
About MSCI  
MSCI Inc. is a leading provider of invest ment decision support tools to investors globally, includi ng asset managers, banks, he dge funds and pension funds. MSCI 
products and services include indice s, portfolio risk and performance an alytics, and governance tools.  
The company’s flagship product offerings ar e: the MSCI indices which include over 148 ,000 daily indices covering more than 70 c ountries; Barra portfolio risk and 
performance analytics covering gl obal equity and fixed income ma rkets; RiskMetrics market and cr edit risk analytics; ISS govern ance research and outsourced proxy 
voting and reporting services; FEA valuation models and risk management software for the energy and commodities markets; and CF RA forensic accounting risk 
research, legal/regulatory risk assessment, and due-diligence. MSCI is headquartered in  New York, with research and commercial offices around the world. Americas  Europe, Middle East & Africa Asia Pacific  
Americas 
Atlanta 
Boston Chicago Montreal 
Monterrey 
New York San Francisco Sao Paulo Stamford 
Toronto 1.888.588.4567 
(toll free)   
+ 1.404.551.3212 
+ 1.617.532.0920 + 1.312.675.0545 + 1.514.847.7506 
+ 52.81.1253.4020 
+ 1.212.804.3901 + 1.415.836.8800 + 55.11.3706.1360 +1.203.325.5630 
+ 1.416.628.1007 Cape Town
Frankfurt 
Geneva London Milan 
Paris 
 + 27.21.673.0100
+ 49.69.133.859.00 
+ 41.22.817.9777 + 44.20.7618.2222 + 39.02.5849.0415 
0800.91.59.17 
(toll free)  
 China North
China South 
Hong Kong Seoul Singapore 
Sydney 
Tokyo 10800.852.1032 
(toll free)
10800.152.1032 (toll free)  
+ 852.2844.9333 798.8521.3392 
(toll free) 
800.852.3749 (toll free)  
+ 61.2.9033.9333 
+ 81.3.5226.8222 

