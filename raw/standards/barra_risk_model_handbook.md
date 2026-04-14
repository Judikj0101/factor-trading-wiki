# barra risk model handbook

> Extracted from: `barra_risk_model_handbook.pdf` (202 pages)

---
## Page 1

Handbook
Barra Risk ModelBarra Risk Model

---
## Page 2

• This document and all of the information contai ned in it, including without limitation all text, 
data, graphs, charts (collectively, the “Information”) is  the property of MSCl Inc. (“MSCI”), Barra, Inc. 
(“Barra”), or their affiliates (including without limit ation Financial Engineering Associates, Inc.) (alone 
or with one or more of them, “MSCI Barra”), or their direct or indirect suppliers or any third party involved in the making or compiling of the Informati on (collectively, the “MSCI Barra Parties”), as 
applicable, and is provided for info rmational purposes only.  The Information may not be reproduced 
or redisseminated in whole or in part without prio r written permission from MSCI or Barra, as 
applicable.  
• The Information may not be used to verify or correct other data, to create indices, risk 
models or analytics, or in connection with issuing,  offering, sponsoring, managing or marketing any 
securities, portfolios, financial products or other in vestment vehicles based on, linked to, tracking or 
otherwise derived from any MSCI or Barra product or data.   
• Historical data and analysis should not be taken as an indication or guarantee of any 
future performance, analysis, forecast or prediction. 
• None of the Information constitutes an offer to sell (or a solicitation of an offer to 
buy), or a promotion or recommendation of, any security, financial product or other 
investment vehicle or any trading strategy, and none of the MSCI Barra Parties endorses, approves or otherwise expresses any opinion regarding any issuer, securities, financial 
products or instruments or trading strategies.  None of the Information, MSCI Barra indices, 
models or other products or services is intended to constitute investment advice or a recommendation to make (or refrain from making) any kind of investment decision and may 
not be relied on as such.   
• The user of the Information assumes the entire risk of any use it may make or permit to be 
made of the Information.   
• In particular, historical data and analysis should not be taken as an indication or guarantee 
of any future performance, analysis or prediction.   
• NONE OF THE MSCI BARRA PARTIES MAKES ANY EXPRESS OR IMPLIED 
WARRANTIES OR REPRESENTATIONS WITH RESPECT TO THE INFORMATION (OR THE 
RESULTS TO BE OBTAINED BY THE USE THEREOF), AND TO THE MAXIMUM EXTENT PERMITTED BY LAW, MSCI AND BARRA, EACH ON THEIR BEHALF AND ON THE BEHALF OF 
EACH MSCI BARRA PARTY, HEREBY EXPRESSLY DISCLAIMS ALL IMPLIED WARRANTIES 
(INCLUDING, WITHOUT LIMITATION, ANY IMPLIED WARRANTIES OF ORIGINALITY, ACCURACY, TIMELINESS, NON-INFRINGEMENT, COMPLETENESS, MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE) WITH R ESPECT TO ANY OF THE INFORMATION.   
• Without limiting any of the foregoing and to the maximum extent permitted by law, in no 
event shall any of the MSCI Barra Parties have any liability regarding any of the Information for any 
direct, indirect, special, punitive , consequential (including lost profit s) or any other damages even if 
notified of the possibility of such damages.  The foregoing shall not exclude or limit any liability that 
may not by applicable law be excluded or limited. 
• Any use of or access to products, services or information of MSCI or Barra or their 
subsidiaries requires a license from MSCI or Barra, or their subsidiari es, as applicable.  MSCI, Barra, 
MSCI Barra, EAFE, Aegis, Cosmos, BarraOne, and all other MSCI and Barra product names are the 
trademarks, registered trademarks, or service marks of MSCI, Barra or their affiliates, in the United 
States and other jurisdictions.  The Global Indus try Classification Standard (GICS) was developed by 
and is the exclusive property of MSCI and Standard & Poor’s.  “Global Industry Classification 
Standard (GICS)” is a service mark of MSCI and Standard & Poor’s. 
 
• The governing law applicable to t hese provisions is the substant ive law of the State of New 
York without regard to its conflic t or choice of law principles. 
 
© 2007 MSCI Barra.   All rights reserved. 
 
        R V  1 0 - 2 0 0 7  
 

---
## Page 3

Contents
ContentsiAbout Barra . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . v
A Pioneer in Risk Management . . . . . . . . . . . . . . . . . . . . . . . . . . . v
Contacting Barra . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .vi
Other Barra Resources  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . .vi
Introduction . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . vii
1. Forecasting Risk with Multiple-Fac tor Models  . . . . . . . . . . . .1
What Are Multiple-Factor Models? . . . . . . . . . . . . . . . . . . . . . . . . 1
How Do Multiple-Factor Models Work? . . . . . . . . . . . . . . . . . . . . 2
Advantages of Multiple-Factor Models. . . . . . . . . . . . . . . . . . . . . . 2
An Illustration of Multiple-Factor Models . . . . . . . . . . . . . . . . . . . 3
Model Mathematics  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 5
Single-Factor Model . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 6Multiple-Factor Model . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 6
Multiple-Asset Portfolio . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 8
Risk Prediction with MFMs  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 8
The Covariance Matrix . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 10
Deriving the Variance-Covariance Matrix of Asset Returns. . . 10
Final Risk Calculation  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 11
Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 12
2. Forecasting Equity Risk . . . . . . . . . . . . . . . . . . . . . . . . . . . .15
A Historical Perspective  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 15
Barra’s Equity Multiple-Factor Model  . . . . . . . . . . . . . . . . . . . . . 19
Common Factors  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 20
Risk Indices . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 20Industries . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 20
Specific Risk. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 20

---
## Page 4

Barra Risk Model
Handbookii3. Barra Equity Risk Modeling  . . . . . . . . . . . . . . . . . . . . . . . . 21
Model Estimation Overview . . . . . . . . . . . . . . . . . . . . . . . . . . . . 21
Data Acquisition  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 24
Descriptor Selection and Testing . . . . . . . . . . . . . . . . . . . . . . . . . 24
Descriptor Standardization . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 25
Risk Index Formulation  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 25
Industry Allocation. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 26
Factor Return Estimation . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 27Covariance Matrix Calculation . . . . . . . . . . . . . . . . . . . . . . . . . . 27
Exponential Weighting . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 28
Covariance Matrix Scaling: Computing Market Volatility  . . . 29
Specific Risk Modeling . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 33
Methodology . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 33
Updating the Model . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 35
4. Forecasting Fixed-Income  Risk . . . . . . . . . . . . . . . . . . . . . . 39
A Historical Perspective  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 39
Barra’s Multiple-Factor Model. . . . . . . . . . . . . . . . . . . . . . . . . . . 40
Common Factors . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 41
Interest Rate Risk . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 43Spread Risk  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 46
Specific Risk  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 49
Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 49
5. Interest Rate Risk Modeling . . . . . . . . . . . . . . . . . . . . . . . . 51
Estimation Process Overview  . . . . . . . . . . . . . . . . . . . . . . . . . . . 51
Term Structure Specification. . . . . . . . . . . . . . . . . . . . . . . . . . . . 55
Interpolation  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 55
Estimation Algorithm Implementation . . . . . . . . . . . . . . . . . 58
Factor Shape Determination . . . . . . . . . . . . . . . . . . . . . . . . . . . . 63Factor Exposure Calculation . . . . . . . . . . . . . . . . . . . . . . . . . . . . 64
Factor Return Estimation . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 65
Term Structure Covariance Matrix Construction . . . . . . . . . . . . . 66Covariance Matrix Correlation . . . . . . . . . . . . . . . . . . . . . . . . . . 66
Updating the Model . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 67

---
## Page 5

Contentsiii6. Spread Risk Modeling . . . . . . . . . . . . . . . . . . . . . . . . . . . . .69
Swap Spread Risk Model. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 70
Data Acquisition and Factor Return Estimation. . . . . . . . . . . 70
Factor Exposure Calculation . . . . . . . . . . . . . . . . . . . . . . . . . 70
Detailed Credit Spread Risk Model . . . . . . . . . . . . . . . . . . . . . . . 71
Currency Dependence  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 72
Model Structure . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 74
Data Acquisition  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 77Factor Return Estimation . . . . . . . . . . . . . . . . . . . . . . . . . . . 77
Covariance Matrix Estimation. . . . . . . . . . . . . . . . . . . . . . . . 77
Factor Exposure Calculation . . . . . . . . . . . . . . . . . . . . . . . . . 78
Emerging-Market Risk Modeling  . . . . . . . . . . . . . . . . . . . . . . . . 78
Model Structure . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 79
Data Acquisition and Factor Return Estimation. . . . . . . . . . . 80Covariance Matrix Estimation. . . . . . . . . . . . . . . . . . . . . . . . 80
Factor Exposure Calculation . . . . . . . . . . . . . . . . . . . . . . . . . 81
Updating the Model . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 81
7. Specific Risk Modeling. . . . . . . . . . . . . . . . . . . . . . . . . . . . .83
Heuristic Models  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 83
Data Acquisition  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 83
Sovereign, U.S. Agency, and MBS Specific Risk Estimation . . 84
Corporate Bond Specific Risk Estimati on  . . . . . . . . . . . . . . . 85
T ransition-Matrix-Based Model. . . . . . . . . . . . . . . . . . . . . . . . . . 86
Data Acquisition  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 87
T ransition Matrix Generation . . . . . . . . . . . . . . . . . . . . . . . . 87Rating Spread Level Calculation . . . . . . . . . . . . . . . . . . . . . . 88
Credit Migration Forecasting  . . . . . . . . . . . . . . . . . . . . . . . . 91
Updating the Model . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 94
8. Currency Risk Modeling . . . . . . . . . . . . . . . . . . . . . . . . . . . .97
Model Structure . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 97
Data Acquisition and Return Calculation  . . . . . . . . . . . . . . . . . . 98Estimation of the Covariance Matrix . . . . . . . . . . . . . . . . . . . . . . 98
Currency Correlation Model . . . . . . . . . . . . . . . . . . . . . . . . . 99
Currency Volatility Model. . . . . . . . . . . . . . . . . . . . . . . . . . 100

---
## Page 6

Barra Risk Model
HandbookivVolatility Across Markets  . . . . . . . . . . . . . . . . . . . . . . . . . . 102
Time-Scaling Currency Risk Forecasts. . . . . . . . . . . . . . . . . . . . 105
Updating the Model . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 106
9. Integrated Risk Modeling . . . . . . . . . . . . . . . . . . . . . . . . . 109
Model Integration Overview  . . . . . . . . . . . . . . . . . . . . . . . . . . 109
Building Global Asset Class Models  . . . . . . . . . . . . . . . . . . . . . 110
The Structure of Local Models . . . . . . . . . . . . . . . . . . . . . . 111Aggregating Local Models. . . . . . . . . . . . . . . . . . . . . . . . . . 111
Implementing Global Factor Models . . . . . . . . . . . . . . . . . . 113
Consistency Between Local Models and Global Model  . . . . 114
Global Equities. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 114
Global Equity Factors . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 115
Exposures of Local Equity Factors to Global Equity Factors . 115
Estimating Returns to Global Equity Factors. . . . . . . . . . . . 115
Computing Covariances of Global Equity Factors . . . . . . . . 117
Scaling to Local Markets. . . . . . . . . . . . . . . . . . . . . . . . . . . 117
Global Bonds . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 118
Global Bond Factors. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 119Exposures of Local Bond Factors to Global Bond Factors. . . 122
Computing Covariances Of Global Bond Factors  . . . . . . . . 122
The Currency Model  . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 123Putting It All Together—A Multi-Asset Class Risk Model  . . . . . 125
Summary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 128
Glossary . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 131
Contributors . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 181Index. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 183

---
## Page 7

About BarravAbout Barra
In recent years the investment management industry has adjusted 
to continuing changes—theoretic al advances, technological devel-
opments, and volatility. To address these, investment managers 
and financial institutio ns require the most advanced and powerful 
analytical tools available.
A Pioneer in Risk Management
As the leading provider of global  investment decision support 
tools and innovative risk ma nagement technology, Barra has 
responded to these industry cha nges by providing quantitative 
products and services  that are both flexible and efficient. 
Barra products are a combination of advanced technology and 
superior analytics, research, mode ls, and data that provide clients 
around the world with comprehen sive risk management solutions. 
Barra uses the best da ta available to develop econometric financial 
models. In turn, these models are the basis of software products 
designed to enhance portfolio performance through returns fore-casting, risk analysis, portfolio co nstruction, transaction cost anal-
ysis, and historical pe rformance attribution.
With more than 80 researchers in offices around the world and 
products that cover most of th e world’s traded securities, Barra 
maintains one of the strongest risk management research practices 
in the world today. 

---
## Page 8

Barra Risk Model
HandbookviContacting Barra 
Client Services is available 24 hours a day, Monday through Fri-
day. You can reach the Client Services as follows:
For local access numbers, visi t the Client Support web site, 
http://support.barra.com.
Client Services is your first point of contact concerning your 
Barra product or service. Support desk analysts are available to 
assist you with general, technical, data, product usage, and model 
questions. 
Other Barra Resources
You can visit the Library at http://support.barra.com  for more 
information on the topics discussed in this handbook. 
In addition to handbooks and reference guides, Barra offers 
numerous workshops and seminars  throughout the year. For more 
information, visit the Events Calendar at http://www.barra.com .Web: http://www.barra.com/support/service_request/
new_request.asp
Phone: North America: 888.588.4567
Europe: +44 (0)20.7618.2222
Asia: +813 5424 5470 (Japanese)

---
## Page 9

IntroductionviiIntroduction
Barra risk models are products of a thorough and exacting model 
estimation process. This handbook  discusses the methods Barra 
uses to model portfolio risk.
Section I. The Theory of Risk
Chapter 1. Forecasting Risk with Multiple Factor Models dis-
cusses the application  of multiple-factor modeling to the risk 
analysis problem.
Section II. Eq uity Risk 
Chapter 2. Forecasting Equity Risk  takes a historical perspective 
on equity risk modeli ng and provides an overview of Barra equity 
risk models and their factors. 
Chapter 3. Barra Equity Risk Modeling  details the process of cre-
ating and maintaining a Barra equity risk model. 
Section III. Fixed-Income Risk 
Chapter 4. Forecasting Fixed-Income Risk  takes a historical per-
spective on fixed-income risk modeling and provides an overview of Barra fixed-income risk models and their factors. Product Sections of Particular Interest
Aegis I, II
BarraOne allBIMe text files I, II, IV, VCosmos I, III, IV, VEquity text files I, IITotalRisk all

---
## Page 10

Barra Risk Model
HandbookviiiChapter 5. Interest Rate Risk Modeling  describes the process of 
determining the term structure of  interest rates for nominal and 
inflation-protected bonds. 
Chapter 6. Spread Risk Modeling explains how the different 
models describe the spread risk in various markets and discusses 
the process of estimating three spread risk models. 
Chapter 7. Specific Risk Modeling  describes the process of creat-
ing heuristic specific risk models  and detailed transition-matrix 
based models to account for is sue- and issuer-specific risk. 
Section IV. Currency Risk 
Chapter 8. Curren cy Risk Modeling describes the process of creat-
ing and maintaining Barra currency risk models.  
Section V. Integrated Risk 
Chapter 9. Integrated Risk Modeling discusses the Barra Inte-
grated Model (BIM)—which is a mult i-asset class model for fore-
casting asset- and portfolio-level risk of global equities, bonds, 
and currencies—and the innovative  methods behind the global 
model. 
Finally, the Glossary  and Index  are useful resources for clarifying 
terminology and finding specific topics.
Further references
Barra has a comprehensive collectio n of articles and other materi-
als describing the models and their applications. To learn more about the topics contained in this handbook, consult the follow-
ing references or our extensive Publ ications Bibliography, which is 
available from Barra offices and from our Web site at http://www.barra.com .

---
## Page 11

IntroductionixBooks
Andrew Rudd and Henry K. Clasing, Modern Portfolio Theory: 
The Principles of Investment Management , Orinda, CA, Andrew 
Rudd, 1988.
Richard C. Grinold and Ronald N. Kahn, Active Portfolio Man-
agement: A Quantitative Approach  for Producing Superior Returns 
and Controlling Risk , Second Edition, McGraw-Hill Professional 
Publishing, Columbus, OH, 1999.

---
## Page 12

Barra Risk Model
Handbookx

---
## Page 13

Section OneThe Theory of Risk
This section explains the underlying 
concepts behind risk forecasting. It 
includes: 
Chapter 1: Forecasting Risk with 
Multiple-Factor Models

---
## Page 15

Chapter 1
Forecasting Risk with Multiple-Factor Models11. Forecasting Risk with Multiple-
Factor Models
The analysis of risk—which is the total dispersi on or volatility of 
returns for a security or portfo lio—is a critical element of supe-
rior investment performance. The goal of risk analysis is not to 
minimize risk but to properly  weigh risk against return. 
Through the years, theoretical ap proaches to risk analysis have 
become increasingly sophisticate d. With more advanced concepts 
of risk and return, investment portfolio models have changed to 
reflect this growing complex ity. The multiple-factor model 
(MFM) has evolved as a helpful to ol for analyzing portfolio risk.
What Are Multiple-Factor Models?
Multiple-factor models are formal statements about the relation-
ships among asset returns in a po rtfolio. The basic premise of 
MFMs is that similar assets disp lay similar returns. Assets can be 
similar in terms of quantifiable attributes, such as market infor-
mation (such as price changes  and volume), fundamental com-
pany data (such as industry and capitalization), or exposure to 
other factors (such as interest rate changes and liquidity).
MFMs identify common factors , which are categories defined by 
common characteristics of differe nt securities, and determine the 
return sensitivity to these factors. 
Multiple-factor models of security  market returns can be divided 
into three types: macroeconomic, fundamental, and statistical fac-
tor models. Macroeconomic factor models  use observable eco-
nomic variables, such as changes in inflation and interest rates, as 
measures of the pervasive sh ocks to security returns. Fundamental 
factor models  use the returns to portfolios associated with 
observed security attributes such as dividend yield, book-to-mar-
ket ratio, and industry membership. Statistical factor models  
derive their factors from factor analysis of the co variance matrix 
of security returns. “Since the factors can represent 
the components of return as seen 
by the financial analyst, the multi-
ple-factor model is a natural repre-
sentation of the real environment.”
Barr Rosenberg, 1974
Multiple Factor Models

---
## Page 16

Barra Risk Model
Handbook2Barra equity models are fundamen tal factor models, which outper-
form the macroeconomic and stat istical models in terms of 
explanatory power.1 Barra fixed-income models are combinations 
of fundamental and macroeconomic  factor models. Returns of 
high-quality debt are largely expl ained by macroeconomic factors 
such as changes in the de fault-free or other lo w-risk yields (that is, 
in terms of government bond re turns or movements of the swap 
curve). Returns of other forms of debt are accounted for by fun-
damental factors based on industry and credit  quality, in addition 
to macroeconomic factors.
How Do Multiple-Factor Models Work?
Barra derives MFMs from asset patt erns observed over time. The 
difficult steps are pinpointing thes e patterns and then identifying 
them with asset factors that investors can understand. 
The asset exposures to these fact ors are specified or calculated. 
Then, a cross-sectional regression is performed to determine the 
returns to each factor over the relevant time period. A history of 
the factor returns is taken to crea te the common factor risk model 
with its variance-covariance matrix and the specific risk model. 
The resulting models forecast  portfolio or asset risk. 
Investors rely on risk forecasts to  select assets and construct port-
folios. They base their decision s on information gleaned from 
MFM analyses as well as their risk preferences and other informa-
tion they possess.
Advantages of Multiple-Factor Models
Using multiple-factor models for security and portfolio analysis 
has many advantages, including: 
■MFMs offer a more thorough breakdown of risk and, there-
fore, a more complete analysis of risk exposure than other 
methods, such as single-factor approaches.
1.  Gregory Connor, “The Three Types of  Factor Models: A Comparison of Their 
Explanatory Power,” Financial Analysts Journal , May/June 1995.

---
## Page 17

Chapter 1
Forecasting Risk with Multiple-Factor Models3■Because economic logic is used  in their development, MFMs 
are not limited by purely historical analysis.
■MFMs can be built using method s that can withstand outliers 
in asset data.
■As the economy and characteris tics of individual issuers 
change, MFMs adapt to reflect changing asset characteristics.
■MFMs isolate the impact of in dividual factors, providing seg-
mented analysis for better i nformed investment decisions.
■Lastly, MFMs are realistic, trac table, and understandable to 
investors.
Of course, MFMs have their limitations. They predict much, but 
not all, of portfolio risk. In additi on, they predict risk, not return; 
investors must choose the invest ment strategies themselves.
An Illustration of Multiple-Factor Models
Accurate characterization of portfo lio risk requires an accurate 
estimate of the covariance  matrix of security returns. A relatively 
simple way to estimate this covariance matrix is to use the history 
of security returns to compute each variance and covariance. This 
approach, however, suffers from two major drawbacks:
■Estimating a covariance matrix for, say, 3,000 assets requires 
data for at least 3 ,000 periods. With mont hly or weekly esti-
mation horizons, such a long hi story may simply not exist. 
■It is subject to estimation error:  in any period, two assets such 
as Weyerhaeuser and Ford may show very high correlation— 
higher than, say, GM and Ford . Our intuition suggests that 
the correlation between GM and Ford should be higher because they are in the same line of business. The simple 
method of estimating the cova riance matrix does not capture 
our intuition.
This intuition, however, points to an alternative method for esti-
mating the covariance matrix. Our feeling that GM and Ford 
should be more highly correlated than Weyerhaeuser and Ford 

---
## Page 18

Barra Risk Model
Handbook4comes from Ford and GM being in the same industry. Taking this 
further, we can argue that firms with similar chara cteristics, such 
as their line of business, should have returns that behave similarly. 
For example, Weyerhaeuser, Ford, and GM will all have a com-mon component in their return s because they would all be 
affected by news that affects the market as a whole. The effects of 
such news may be captured by a stock market component in each 
stock’s return
1 or a yield curve movement component in each 
bond’s return. The degree to which each of the three securities responds to this market componen t depends on the sensitivity of 
each security to the stock market or yield curve component. 
Additionally, we would expect GM and Ford to respond to news 
affecting the automobile industry, whereas we would expect 
Weyerhaeuser to respond to news  affecting the forest and paper 
products industry. The effects of  such news may be captured by 
the average returns of securities in the auto industry and the forest 
and paper products industry. There  are, however, events that 
affect one security without affe cting the others. For example, a 
defect in the brake system of GM cars, which forces a recall and 
replacement of the system, will l ikely have a negative impact on 
GM’s stock and bond prices. This ev ent, however, will most likely 
leave Weyerhaeuser and Ford security prices unaltered. 
In other words, the overall variat ion in GM’s asset returns is the 
joint result of several sources of  variation. The volatility of GM 
stock returns can be attributed to stock ma rket return, variation 
in auto industry returns, and any variations that are specific to 
GM. Similarly, the volat ility of bonds issued by GM can be attrib-
uted to the movement in the yi eld curve generally, variation in 
auto sector and bond ratings, and any variations that are specific 
to GM. The same can be said abou t Ford’s asset returns, and since 
the market and industry  variations are identical for the two com-
panies, we expect GM and Ford returns to move together to a large degree. Weyerhaeuser and GM, or Weyerhaeuser and Ford, 
on the other hand, are likely to move together to a lesser degree 
because the only common component in their returns is the mar-ket return. Some additional correlation may arise, however, 
because the auto industry and pa per products in dustry returns 
may exhibit some correlation.
1.  This common component may be the weighted average return to all U.S. 
stocks.

---
## Page 19

Chapter 1
Forecasting Risk with Multiple-Factor Models5This approach of analyzing total va riation or risk into its compo-
nent factors provides insight into many types of assets. 
By beginning with our intuition about the sources of co-
movement in security returns, we  have made subs tantial progress 
in estimating the covariance matri x of security returns. What we 
need now is the covari ance matrix of common sources in security 
returns, the variances of security-s pecific returns, and estimates of 
the sensitivity of secu rity returns to the co mmon sources of varia-
tion in their returns.  Because the common sources of risk are 
likely to be much fewer than the n umber of securities, we need to 
estimate a much smaller covariance matrix and hence a smaller 
history of returns is required. Moreover, because similar assets are 
going to have larger sensitivitie s to similar common sources of 
risk, similar assets will be more highly correlated than dissimilar 
assets: our estimated correlation for GM and Ford will be larger 
than that for Ford and Weyerhaeuser.
The decomposition of security returns into common and specific 
sources of return is, in fact, a multiple-factor model of security 
returns. 
Model Mathematics
Portfolio risk and return can be decomposed along two dimen-
sions: that which is due to factors which are prevalent throughout 
the market and that which is due to the idiosyncratic nature of 
the securities in the portfolio. A multiple-factor model is a power-
ful tool to shed light on these so urces of risk and return within a 
portfolio. 

---
## Page 20

Barra Risk Model
Handbook6Single-Factor Model
For single-factor models, the equa tion that describes the excess 
rate of return is:
The rate of factor return ( f) and the specific return ( u) are 
assumed to be uncorrelated, and the u’s are uncorrelated across 
different assets.
Multiple-Factor Model
MFMs build on single-fa ctor models by including and describing 
the interrelationships among factor s. We can expand the model to 
include many factors, as sh own in the equation below:
The asset’s return is broken out into the return due to individual 
factors and a portion unique to the asset and not due to the com-
mon factors. In addition, each factor ’s contribution is a product of 
the asset’s exposure or weight in the factor and the return of that 
factor. The total excess return equation for a multiple-factor 
model can be summarized with:(EQ 1-1)
where
ri = total excess return over the risk-free rate of 
security i
xi = sensitivity of security i to the factor
f = rate of return on the factor
ui = non-factor or specific return of security i
(EQ 1-2)
common factor return specific return

---
## Page 21

Chapter 1
Forecasting Risk with Multiple-Factor Models7Note that when K=1, the MFM equation reduces to the earlier 
single-factor version.1
Exposures ( xik) 
By observing patterns over time, common factors can be identi-fied and exposures to these fact ors can be determined. These fac-
tors are based on market or fundamental data. 
The model’s profile of a security responds immediately to any 
change in the company’s structure or the market’s behavior. Barra 
updates the security exposures of most fixed-income models on a 
daily basis and the security exposures of most equity models on a monthly basis, using the last tr ading day’s information to com-
pute exposures for the coming month. 
Factor Returns ( fk) 
Factor returns  are pure measures of the factor’s actual perfor-
mance net of any other effects. Si nce factor returns are not readily 
observable, we must estimate them . Recall that asset exposures are 
computed at the end of each month. Using our multiple-factor 
model framework and the observed asset returns over the next month, we can estimate factor returns over the month. This is 
done with a cross-sectional regres sion of asset returns over the 
month on the exposures of th e assets to the factors. (EQ 1-3)
where
xik = risk exposure of security i to factor k
fk = rate of return to factor k
ui = non-factor or specific return of security i
1.  For example, a single-factor model in which the market return is the only rel-
evant factor.


---
## Page 22

Barra Risk Model
Handbook8Multiple-Asset Portfolio
When a portfolio consists of only one security, Equation 1-3 
describes its excess return. But most portfolios comprise many securities, each represen ting a proportion, or weight , of the total 
portfolio. When weights h
P1, hP2,...,hPN reflect the weights of N 
securities in portfolio P, we express the excess return in the follow-
ing equation:
This equation includes the return  from all sources and lays the 
groundwork for further MFM analysis. 
Risk Prediction with MFMs
A central part of the model is its  factor covariance matrix. This 
matrix contains the variances an d covariances of the common fac-
tors. To estimate a portfolio’s ri sk, we must consider not only the 
security or portfolio’s exposures to the factors, but also each fac-
tor’s risk and the covariance or interaction between factors.
Without the framework of a multipl e-factor model, estimating the 
covariance of each asset with every other asset would likely result 
in finding spurious relationships. For example, an estimation uni-(EQ 1-4)
where
rP = total excess return of portfolio
xPk =
fk = return of factor k
hPi = weight of security i
ui = non-factor or specific return of security i


---
## Page 23

Chapter 1
Forecasting Risk with Multiple-Factor Models9verse of 1,400 assets entails 980,700 covariances and variances to 
calculate. 
A multiple-factor model simplifies these calculations dramatically. 
This results from replacing indivi dual asset profiles with catego-
ries defined by common characteris tics (factors). For example, in 
the Multiple-Horizon U.S. Equity  Model, 68 factors capture the 
risk characteristics of  equities. This reduces the number of covari-
ance and variance calculations to 2,346. Moreover, determining fewer parameters results in a sm aller chance of finding spurious 
relationships. (EQ 1-5)
where
V(i,j) = asset covariance matrix
i,j = individual assets
(EQ 1-6)
where
F(k,m) = factor covariance matrix
k,m = common factors
Figure 1-1
Asset Covariance Matrix
For N=1,400 assets, there are 
980,700 covariances and vari-
ances to estimate. 


---
## Page 24

Barra Risk Model
Handbook10The Covariance Matrix
Barra’s risk models use historical returns to create a framework for 
predicting the future re turn volatility of an asset or a portfolio. 
Each month, the estimation universe , which is the set of represen-
tative assets in each lo cal market, is used to attribute asset returns 
to common factors and to a sp ecific, or residual, return. 
The monthly returns for the estima tion universe are formulated as 
a single matrix equation of n assets and k factors. Each row repre-
sents one of the assets in  a portfolio or universe. 
The return of each asset at the end of a month, along with its fac-
tor exposures at the beginning of  the month, is known. The factor 
returns, which are the values that best explain the asset returns, 
are estimated via regression. The time series of factor returns are 
then used to generate factor vari ances and covariances in the cova-
riance matrix.   
Deriving the Variance-Covaria nce Matrix of Asset Returns
We can easily derive the matrix algebra calculations that support 
and link the above diagrams by us ing an MFM. We can start with 
the MFM equation, r = Xf + u.
Figure 1-2
Equity Factor Covariance Matrix
For K=68 factors, there are 
2,346 covariances and vari-
ances to estimate. Quadrant I 
includes the covariances of risk indices with each other; quad-
rants II and III are mirror 
images of each other, showing the covariances of risk indices 
with industries; and quadrant IV 
includes covariances of indus-tries with each other. 
Figure 1-3
Factor Return CalculationUsing an MFM greatly simplifies 
the estimation process. The 
matrix depicts the multiple fac-tor model. 

---
## Page 25

Chapter 1
Forecasting Risk with Multiple-Factor Models11Substituting this relation in th e basic equation, we find that:
Risk = Var(r)  (EQ 1-7)
Risk = Var(Xf + u) (EQ 1-8)
Risk = Var(Xf) + Var(u)  (EQ 1-9)
Using the matrix algebra formula for variance, the risk equation 
becomes:
Final Risk Calculation
The covariance matrix is used in conjunction with a portfolio’s 
weight in each asset and the factor  exposures of those assets to Risk = XFXT+Δ (EQ 1-10)
where
X = matrix of factor exposures of n assets to k 
factors: 
F = factor return variance -covariance matrix for 
m factors:
XTtransposition of X matrix
Δ diagonal matrix of sp ecific risk variances


---
## Page 26

Barra Risk Model
Handbook12calculate portfolio risk. The foll owing formula is the underlying 
form of Barra risk calculations: 
Summary
Robust risk analysis can provide in sight to all investors. The goal 
of risk analysis is no t to minimize risk but to properly weigh risk 
against return. In this book, we discuss the methods Barra uses to model portfolio risk. The foundations of risk modeling are rele-
vant for analyzing a wide variety of asset types, including stocks, 
bonds and other fixed-income sec urities, currenci es, and deriva-
tives.(EQ 1-11)
where
σp = volatility of portfolio returns
hp = vector of portfolio
weights for N assets: .


---
## Page 27

Section TwoEquity Risk
Section Two provides an overview of 
equity risk models and discusses the 
extensive, detailed process of creating 
Barra equity models.
Chapter 2: Forecasting Equity Risk
Chapter 3: Barra Equity Risk Modeling

---
## Page 29

Chapter 2
Forecasting Equity Risk152. Forecasting Equity Risk
Many methods exist for forecastin g a stock’s future volatility. One 
method is to examine its histor ical behavior and conclude that it 
will behave similarly in the futu re. An obvious problem with this 
technique is that results depend on  the length and type of history 
used. The security might have chang ed over time due to mergers, 
acquisitions, divestitures, or ot her corporate actions. The past 
contains information that may be  no longer relevant to the 
present. Yet this is the approa ch most commonly used for measur-
ing beta (see section on Barra Predicted Beta  on page 18).
A more informative approach uses insights into the characteristics 
and behavior of the stock and mark et as a whole, as well as the 
interactions between them. We co uld determine the future behav-
ior of a stock or portfolio by ex amining its charact eristics with 
respect to the overall market. 
A Historical Perspective
Before the 1950s, there was no concept of systematic,  or market-
related, return. Return was a rise in the value of an asset and risk 
was a drop in the value of an asse t. The investor’s primary invest-
ment tools were intuition and insi ghtful financial analysis. Portfo-
lio selection was simply an act of  assembling a group of “good” 
assets.
Financial theorists became more sc ientific and statistical in the 
early 1950s. Harry Markowitz was the first to quantify risk (as 
standard deviation) and diversific ation. He showed precisely how 
the risk of the portfolio was less than the risk of its components. In the late 1950s, Leo Breiman and John L. Kelly Jr. derived 
mathematically the peril of igno ring risk. They showed that a 
strategy that explicitly accounte d for risk outperformed all other 
strategies in the long run.
1
1.  See, for example, Leo Breiman, “Investment Polici es for Expanding Business-
es Optimal in a Long-Run Sense,” Naval Research Logistics Quarterly  Volume 
7, No. 4, (December 1960): 647–651.

---
## Page 30

Barra Risk Model
Handbook16We now know how diversification reduces portfolio risk. It aver-
ages factor-related risk (such as industry exposures for equities and 
credit exposure for bonds) and significantly reduces asset-specific 
risk. However, diversification does  not eliminate all risk because 
assets tend to move up and down together with the market. 
Therefore, while non-market-related risk, or residual risk , can be 
minimized, market or systematic risk  cannot be eliminated by 
diversification. 
Figure 2-1 shows the balance between residual risk and market 
risk changing as the number of diffe rent assets in a portfolio rises. 
At a certain portfolio size, all residual risk is effectively removed, 
leaving only market risk. 
As investment managers became more knowledgeable, there was a 
push to identify the conceptual basis underlying the concepts of 
risk, diversification, and returns. The Capital Asset Pricing Model 
(CAPM) was one approach that de scribed the equilibrium rela-
tionship between retu rn and market risk.1 
1.  William Sharpe earned the Nobel Pr ize in Economics for his development of 
CAPM.“Diversification is good.”
Harry Markowitz, 1952Figure 2-1Diversification and Risk
As a portfolio manager 
increases the number of assets 
in a portfolio, residual—or non-
market related—risk is diversi-fied or concentrated. Risk is 
diversified if any position added 
to the portfolio is less than per-fectly correlated with others 
already in the portfolio and has 
lower volatility. Market risk is undiversifiable. One benefit of 
using a multiple-factor model is 
better understanding of the results of adding and eliminat-
ing positions.Total RiskResidual Risk
Number of Stocks in PortfolioSystematic (Market) RiskRisk of Portfolio
(Standard Deviation of Return)
Number of Assets in Portfolio

---
## Page 31

Chapter 2
Forecasting Equity Risk17 
The central premise of CAPM  is that, on average, investors are 
not compensated for taking on residual risk. CAPM asserts that 
the expected residual return is zero while the expected systematic 
return is greater than zero and is linearly related to an asset’s beta 
with relation to the market portfolio.
The measure of portfolio exposure to  systematic risk is called beta 
(β). Beta is the relative volatility or sensitivity of a security or 
portfolio to market moves. Returns, and hence risk premia, for 
any asset or portfolio will be rela ted to beta, the exposure to undi-
versifiable systematic ri sk. Equation 2-1 states this linear relation-
ship.
(EQ 2-1)
where:
 = return on asset i
rF = risk-free rate of return
βi =
= return on market portfolioMarket
Return
Risk-Free
RateRate of Return
01 2Market Portfolio
BetaExpected rate of return
Market 
return
Risk-free 
rateMarket portfolioFigure 2-2
Capital Asset Pricing Model 
(CAPM)
Capital Asset Pricing Model 
asserts that the expected excess return on securities is proportional 
to their systematic risk coefficient, 
or beta. The market portfolio is 
characterized by a beta of unity.


---
## Page 32

Barra Risk Model
Handbook18CAPM is a model of return. Unde rlying it are eq uilibrium argu-
ments and the view that the market  is efficient because it is the 
portfolio that every investor on average owns. CAPM does not 
require that residual returns be  uncorrelated. But it did inspire 
Sharpe to suggest a one-factor ris k model that does assume uncor-
related residual returns. This model has the advantage of simplic-
ity. It is quite useful for ba ck-of-envelope calculations; but it 
ignores the risk that arises from  common factor sources, such as 
industries, capitalization, and yield. 
By the 1970s, the investment community recognized that assets 
with similar characteristics tend to behave in similar ways. This Learn more about
Barra Predicted Beta
Beta is a gauge of the expect ed response of a stock, bond, or portfolio to the overall 
market. For example, a stock with a beta of  1.5 has an expected excess return of 1.5 
times the market excess return. If the market is  up 10% over the risk -free rate, then—other 
things held equal—the portfolio is expected  to be up 15%. Beta is one of the most 
significant means of measuring portfolio risk. 
Historical Beta vs. Predicted BetaHistorical beta  is calculated after the fact by running a regression (often over 60 months) 
on a stock's excess returns against the market's excess returns. There are two important problems with this simp le historical approach: 
■It does not recognize fundamental chang es in the company's operations. For 
example, when RJR Nabisco spun off it s tobacco holdings in 1999, the com-
pany's risk characteristics changed sign ificantly. Historical beta would recog-
nize this change only slowly, over time. 
■It is influenced by events specific to the company that are unlikely to be repeated. For example, the December 1984 Union Carbide accident in Bho-
pal, India, took place in a bull market , causing the company's historical beta 
to be artificially low. 
Predicted beta , the beta Barra derives from its risk model, is a forecast of a stock's 
sensitivity to the market. It is  also known as fundamental beta, because it is derived from 
fundamental risk factors. In the Barra model, these risk factors include attributes—such as size, yield, and volatility— plus industry exposure. Becaus e we re-estimate these risk 
factors monthly, the predicted beta reflects changes in the company's underlying risk structure in a timely manner. Ba rra applications use predicted beta rather than historical 
beta because it is a better forecast of ma rket sensitivity of an  asset in a portfolio.
“Only undiversifiable risk should 
earn a premium.“
William F. Sharpe, 1964
Capital Asset Pricing Model

---
## Page 33

Chapter 2
Forecasting Equity Risk19notion is captured in the Arbitrage Pricing Theory (APT). APT  
asserts that security and portfolio expected returns are linearly 
related to the expected returns of an unknown number of system-
atic factors.
The focus of APT is on forecast ing returns. Inst ead of equilib-
rium arguments, Stephen Ross and others used arbitrage argu-
ments to assert that expected specific returns are zero, but expected common factor returns (including the market and other 
factors) need not be zero. Just  like the CAPM, APT inspired a 
class of risk models: the multiple-factor model (MFM). 
In the mid-1970s, Barr Rosenberg pioneered a new class of risk 
models based on the idea that a ssets with similar characteristics 
should display similar returns. Mu ltiple-factor models assert that 
many influences act on the volatility  of an asset, and these influ-
ences are often common across many assets. A properly con-
structed MFM is able to produce risk analyses with more accuracy 
and intuition than a simple covaria nce matrix of security returns 
or the CAPM. 
Barra’s Equity Multiple-Factor Model
Barra’s equity risk models deco mpose asset returns into compo-
nents due to common factors and a specific, or idiosyncratic, fac-
tor. The models capture the va rious components of risk and 
provide a multifaceted, quantitat ive measure of risk exposure. 
Together with specific risk, mark et membership, industries, and 
risk indices provide a compreh ensive partition of risk.  
Total Risk
Common Factor Specific Risk
Industries Risk IndicesFigure 2-3
Equity Risk Decomposition“The arbitrage model was pro-
posed as an alternative to the mean variance capital asset 
pricing model.”
Stephen A. Ross, 1976
Arbitrage Pricing Theory

---
## Page 34

Barra Risk Model
Handbook20Common Factors
Stocks with similar characteristics exhibit similar return behavior. 
These shared characteristics, or common factors , are excellent pre-
dictors of future risk. 
Many of the influences that affect the volatility of a stock or port-
folio are common factors which are prevalent across the entire 
market. These common factors— industry membership (and 
trends in that industry) and risk  indices—not only help explain 
performance, but also anticipate future volatility. 
Risk Indices
Barra combines fundamental and market data to create risk indi-
ces that measure risk asso ciated with common features of an asset. 
Common dimensions of style such as growth/value and smallcap/
largecap can be described using risk indices. Each Barra equity 
risk model has a predefined set of risk indices.
Industries
An industry  is a homogeneous collection of business endeavors. 
Each Barra equity risk model has a predefined set of industries 
and sectors appropriate to its envi ronment. Each security is classi-
fied into an appropriate industry  as defined by its operations, 
although a number of models su pport multiple-industry classifica-
tion for large conglomerates.
Specific Risk
Specific risk forecasting is a thr ee-part process. We first estimate 
the average specific risk of all assets covered in a model, then the 
specific risk of each asset relative to  the universe of assets. Finally, 
we combine the average and rela tive components and scale the 
product to adjust for average bias. The result is a specific risk 
forecast for each asset that  is generally unbiased. 

---
## Page 35

Chapter 3
Barra Equity Risk Modeling213. Barra Equity Risk Modeling
The creation of a comprehensive equity risk model is an exten-
sive, detailed process of  determining the factor s that describe asset 
returns. Model estimation involves a series of intricate steps that 
is summarized in Figure 3-1.
Model Estimation Overview
The first step in model estimation  is acquiring and cleaning data. 
Both market information (such as  price, trading volume, dividend 
yield, or capitalizati on) and fundamental data (such as earnings, 
sales, industry information, or to tal assets) are used. Special atten-
tion is paid to capital restructuri ngs and other atypical events to 
provide for consistent cr oss-period comparisons.
Descriptor selection follows. This involves choosing and standard-
izing variables which best capture the risk characteristics of the 
assets. To determine which descript ors partition risk in the most 
effective and efficient way, the desc riptors are tested  for statistical 
significance. Useful descriptors often significantl y explain cross-
sectional returns. 
Risk index formulation and assignme nt to securities is the fourth 
step. This process involves collecti ng descriptors into their most 
meaningful combinations. A variety of techniques are used to 
evaluate different possibilities. Fo r example, cluster analysis is one 
statistical tool that mi ght be used to assign  descriptors to risk 
indices.
Along with risk index exposures, industry allocations are deter-
mined for each security. In most Barra models, a single industry 
exposure is assigned, but multipl e exposures for conglomerates are 
calculated in a few models, including the U.S. and Japan models. 
Next, through cross-sectional regressions, we calculate factor 
returns to estimate covariances be tween factors, generating the 
covariance matrix used to forecast  risk. The factor covariances are 
computed for most models by expo nentially weighting historical 
observations. This method places mo re weight on recent observa-Model Estimation Process
1. Data acquisition 
2. Descriptor selection and 
testing
3. Descriptor standardization
4. Risk index formulation5. Industry allocation
6. Factor return estimation
a. Covariance matrix 
calculation
b. Exponential weightingc. Covariance matrix 
scaling: DEWIV and GARCH 
7. Specific risk forecasting
a. Average specific risk 
estimation
b. Relative specific risk 
estimation
c. Average and relative 
forecasting
8. Model updating

---
## Page 36

Barra Risk Model
Handbook22tions and allows the model to cap ture changes in ri sk in a timely 
fashion. We may further modify th e matrix with eith er generalized 
auto-regressive conditional he teroskedasticity (GARCH) tech-
niques or daily exponentially we ighted index volatility (DEWIV) 
methods to make it more responsive to changing market condi-
tions. 
Specific returns are separated out at  this stage of return estimation 
and specific risk  is forecast. This is the por tion of total risk that is 
related solely to a particular st ock and cannot be accounted for by 
common factors. The greater an asse t’s specific risk, the larger the 
proportion of return variation attrib utable to idiosyncratic, rather 
than common, factors.   
Lastly, the model undergoes final testing and updating. Risk fore-
casts are tested against alte rnative models. Tests compare ex ante  
forecasts with ex post  realizations of beta, specific risk, and active 
risk. New information from company fundamental reports and 
market data is incorporated, and th e covariance matrix is recalcu-
lated.
Figure 3-1 summariz es these steps.

---
## Page 37

Chapter 3
Barra Equity Risk Modeling23Figure 3-1
Data Flow for Model EstimationPhase I: Factor Exposures
Phase III: AnalysisPhase II: Factor Return EstimationFundamental
and
Market Data
 Industry
AllocationsDescriptor
Formulas
DescriptorsRisk Index
Formulas
Risk Indices
Estimation
Universe
Factor LoadingsMonthly
Cross-Sectional
Weighted
RegressionsAsset Returns
Factor
Returns
Covariance
MatrixSpecific
 Risk
ForecastSpecific
Returns

---
## Page 38

Barra Risk Model
Handbook24Data Acquisition 
The first step in model estimati on is acquiring and standardizing 
data. Market data and fundamen tal data for each equity risk 
model are gleaned, verified, and compiled from more than 100 
data feeds supplied by 56 data vendors. 
Market information is collected daily. Fundamental company data 
is derived from quarterly and annual financial statements. 
After data is collected, it is scruti nized for inconsistencies, such as 
jumps in market cap italization, missing dividends, and unex-
plained discrepancies between the day’s data and the previous 
day’s data. Special attention is paid to capital restructurings and 
other atypical events to provid e for consistent cross-period com-
parisons. Information then is compared across different data 
sources to verify accuracy. 
Our robust system of checks and our data collection infrastruc-
ture, which has been continuously refined for more than 25 years, ensure that Barra’s risk models  utilize the best available data. 
Descriptor Selection and Testing
Descriptor candidates are drawn from several sources. For some 
descriptors, market and fundamenta l information is combined. An 
example is the earnings to price ratio, which measures the rela-
tionship between the market’s valu ation of a firm and the firm’s 
earnings.
Descriptor selection is a largely qualitative proces s that is sub-
jected to rigorous quant itative testing. First,  we identify prelimi-
nary descriptors. Good descripto r candidates are individually 
meaningful; that is, they are base d on generally accepted and well-
understood asset attributes. Furt hermore, they divide the market 
into well-defined categories, provid ing full characterization of the 
portfolio’s important risk fea tures. Barra has more than two 
decades of experience identifying important descriptors in equity 
markets worldwide. This experience  informs every new model we 
build.

---
## Page 39

Chapter 3
Barra Equity Risk Modeling25Selected descriptors must have a so und theoretical justification for 
inclusion in the model. They must be useful in predicting risk 
and based on timely, accurate, and available data. In other words, 
each descriptor must ad d value to the model. If the testing pro-
cess shows that they do not add predictive power, they are 
rejected.
Descriptor Standardization
The risk indices are composed of descriptors designed to capture 
all the relevant risk characteristic s of a company. The descriptors 
are first normalized , that is, they are standardized with respect to 
the estimation universe. The norm alization process involves set-
ting random variables to a uniform scale. A constant (usually the 
mean) is subtracted from each nu mber to shift all numbers uni-
formly. Then each number is divided  by another cons tant (usually 
the standard deviation) to shift the variance.
The normalization proc ess is summarized by  the following rela-
tion:
The descriptors are then combined into meaningful risk factors, 
known as risk indices.  
Risk Index Formulation
Asset returns are regressed agains t industries and descriptors, one 
descriptor at a time, after the no rmalization step. Each descriptor 
is tested for statistical significa nce. Based on the results of these 
calculations and tests, descriptors for the model are selected and 
assigned to risk indices. 
Risk index formulation is an iterative process. After the most sig-
nificant descriptors are added to the model, remaining descriptors 
are subjected to stricter testing.  At each stage of model estima-
tion, a new descriptor is added only  if it adds explanatory power 


---
## Page 40

Barra Risk Model
Handbook26to the model beyond that of indu stry factors and already assigned 
descriptors.
Industry Allocation
Industry allocation is defined a ccording to what is appropriate to 
the local environment. Each security is classified into an industry 
by its operations. Barra either us es a data vendor’s allocation 
scheme or creates one that better categorizes the assets in the esti-
mation universe. 
For most equity models, companie s are allocated to single indus-
tries. For the United States, Mexico, and Japan, however, suffi-
cient data exists to alloca te to multiple industries. 
Learn more about
Multiple Industry Allocation—U.S. and Japan
For the United States and Ja pan, industry exposures ar e allocated using industry 
segment data. For Japan, it’s sales; for the U. S. it’s operating earn ings, total assets, and 
sales. For any given multi-industry alloca tion, the weights will add up to 100%. Walt 
Disney Co., for instance , is allocated to 65% media and 35% entertainment.
Multiple industry allocation pr ovides more accurate risk prediction and better describes 
market conditions and company activity. Barra’s multiple-indus try model captures 
changes in a company’s risk profile as soon as new business activity is reported to shareholders. Alternative approaches can require 60 months or more of data to recognize changes that result from market prices.

---
## Page 41

Chapter 3
Barra Equity Risk Modeling27Factor Return Estimation
The previous steps have defined the exposures of each asset to the 
factors at the beginning of every period in the estimation window. 
The factor excess returns over th e period are then obtained via a 
cross-sectional regression of asset excess returns on their associated 
factor exposures:
(EQ 3-1)
where
The resulting factor returns ar e robust estimates which can be 
used to calculate a factor covaria nce matrix to be used in the 
remaining model estimation steps.
Covariance Matrix Calculation
The simplest way to estimate the factor covariance matrix is to 
compute the sample covariances am ong the entire set of estimated 
factor returns. Implicit in this process is the assumption that we 
are modeling a stable process and, therefore, each point in time 
contains equally relevant information. 
A stable process implies a stable variance for a well-diversified 
portfolio with relatively stable ex posures to the factors. However, 
considerable evidence shows th at correlations among factor 
returns change. In some markets, the volatility of  market index 
portfolios changes. For example, pe riods of high volatility are 
often followed by persistent period s of high volatility; in other 
words, periods of high volatility cl uster. The high level of volatil-
ity eventually stabilizes  to a lower level of volatility. The changing 
correlations among factor return s and the changing volatility of ri = excess returns to each asset
Xi = exposure matrix of assets to factors
fi = factor returns to be estimated
ui = specific returns


---
## Page 42

Barra Risk Model
Handbook28market portfolios belie the stabil ity assumption un derlying a sim-
ple covariance matrix. 
For certain models, we relax the assumption of stability in two 
ways. First, in computing the cova riance among the factor returns, 
we assign more weight to recent observations relative to observa-
tions in the distant past. Second , we estimate a model for the vol-
atility of a market index portfo lio—for example, the S&P 500 in 
the United States and the TSE1 in Japan—and scale the factor 
covariance matrix so that it produ ces the same volatility forecast 
for the market portfolio as th e model of market volatility.
Exponential Weighting 
Suppose that we think that observ ations that occurred 60 months 
ago should receive half the weight of the current observation. Denote by T the current period, and by t any period in the past, 
t = 1,2,3,…,T–1,T , and let 
λ =.51/60. If we assign a weight of 
λT–t to observation t, then an observation that occurred 60 
months ago would get half the weight of the current observation, 
and one that occurred 120 months  ago would get one-quarter the 
weight of the current observatio n. Thus, our weighting scheme 
would give exponentially declining weights  to observations as they 
recede in the past.
Our choice of sixty months was ar bitrary in the above example. 
More generally, we give an observation that is HALF-LIFE  
months ago one-half the weight of the current observation. Then 
we let: 
(EQ 3-2)
and assign a weight of:
.( E Q  3 - 3 )
The length of the half-life contro ls how quickly the factor covari-
ance matrix responds to recent cha nges in the market relationships 
between factors. Equal weighting of all observations corresponds to HALF-LIFE  =
∞. Too short a half-life effectively throws away 
data at the beginning of the series . If the process is perfectly sta-
ble, this decreases the precision of the estimates. Our tests show 
that the best choice of half-life varies from country to country. 


---
## Page 43

Chapter 3
Barra Equity Risk Modeling29Hence, we use different values of half-life for different single- 
country models.
Covariance Matrix Scaling: Computing Market Volatility 
In some markets, market volatil ity changes in a predictable man-
ner. As stated before, we find th at returns that are large in abso-
lute value cluster in time, or th at volatility persists. Moreover, 
periods of above normal returns are, on average, followed by 
lower volatility, relative to periods of below-normal returns. 
Finally, we find that actual asse t return distributions exhibit a 
higher likelihood of extreme outc omes than is predicted by a nor-
mal distribution with a constant volatility. 
Variants of daily exponentiall y weighted index volatility 
(DEWIV) and generalized autoregr essive conditional heteroske-
dasticity (GARCH) models capture these empirical re gularities by 
allowing volatility to increase fo llowing periods of high realized 
volatility, or below-normal return s, and allowing volatility to 
decrease following periods of low realized volatility, or above-nor-
mal returns.
Variants of these system atic scalings are app lied as appropriate to 
Barra local models over time.1See the Barra Equity Risk Model 
Reference Guide  for specific information on what scaling—if suit-
able for the market—is applied to the equity model.
Before we implement DEWIV or GARCH scaling on any model, 
we first test and validate its application for that model. If we can satisfactorily fit DEWIV or GARCH to the vola tility of a market 
proxy portfolio, we use the model to scale the factor covariance 
matrix so that the matrix gives th e same risk forecast for the mar-
ket portfolio as the DEWIV or GARCH model. Only the system-
atic part of the factor co variance matrix is scaled.
DEWIV Model
DEWIV is applied as appropriate to local models over time. The 
model is expressed as: 
1.  Some markets, such as the emerging  markets, are not scaled. Neither GARCH 
nor DEWIV is appropriate for th e 26 emerging market models.

---
## Page 44

Barra Risk Model
Handbook30(EQ 3-4)
where
The DEWIV model has only one parameter: the weighting coeffi-
cient; that is, the half-life. Befo re scaling the covariance matrix, 
the monthly DEWIV variances are fi rst calculated by multiplying 
the daily variance forecast by th e approximate number of trading 
days in a month (21 days). The monthly DEWIV variances can 
be calculated only if daily marke t index data is available for the 
relevant country model. 
GARCH Model and Its Variants
Variants of GARCH1 are applied as appropriate to some Barra 
single-country models over time. Denote by rt the market return 
at time  t, and decompose it into its expected component, E(rt), 
and a surprise, εt, thus:
(EQ 3-5)
The observed persistence in realiz ed volatility indicates that the 
variance of the market return at t can be modeled as:
(EQ 3-6)= variance of market return at time t
21 = approximate number of trading days in a 
month
=
rt–s = return of the index port folio over the period t–
s–1 and t–s
= mean of the return of the index portfolio
1.  The form of the variance foreca sting function dist inguishes the GARCH 
models from one another.
λ


---
## Page 45

Chapter 3
Barra Equity Risk Modeling31where
This equation, which is referred to as a GARCH(1,1) model, says 
that current market volatility depend s on recent realized volatility 
via , and on recent fore casts of volatility via .
If α and β are positive, then this period ’s volatility increases with 
recent realized and forecast vo latility. GARCH(1,1) models fit 
many financial time series. Neverthe less, they fail to capture rela-
tively higher volatility  following periods of below-normal returns. 
We can readily extend the GARCH(1,1) model to remedy this 
shortcoming by modeling market volatility as:
 (EQ 3-7)
where θ is sensitivity to surprise return. If θ is negative, then 
returns that are larger than expe cted are followed by periods of 
lower volatility, whereas returns th at are smaller than expected are 
followed by higher volatility. 
Scaling
Scaling the covariance matrix involv es taking volati lity forecasts 
for a market index and scaling the less dynamic factor covariance 
matrix with the volatility  forecasts. Barra starts  with a pre-existing 
positive definite factor  covariance matrix and a diagonal matrix of 
specific risks. 
The forecast for the variance of the market from the unscaled 
model is: 
(EQ 3-8)= variance of market return at time t
ω = forecasted mean volatility of the market
α = sensitivity to recent  realized volatility
= recent realized volatility at time t–1
β = sensitivity to previous forecast of volatility


---
## Page 46

Barra Risk Model
Handbook32The monthly specific risk of the monthly market index is defined 
as:
(EQ 3-9)
where
The factor covariance matrix is th en scaled using a forecast for a 
market index variance. The number of assets is n and the number 
of factors is k. Given a monthly scaled variance forecast for the 
market index portfolio, σs2, we construct a new (k × k) factor 
covariance matrix, Fs , thus: 
(EQ 3-10)
wherehm = market index portfolio holdings ( n ×1)
Δ = specific variance diagonal matrix (n × n)
Fs = factor covariance matrix with scaling
F = original factor covariance matrix (k × k)
= monthly scaled variance forecast for the 
market index, which is based on either 
DEWIV σd2 or GARCH σg2 models
= monthly total variance of the market index, 
calculated from the pre-existing factor 
model
= monthly specific risk of the market index
hm = market index portfolio holdings ( n × 1)
X = risk factor exposure matrix (n × k)


---
## Page 47

Chapter 3
Barra Equity Risk Modeling33Specific Risk Modeling 
Referring to the basic factor model:
(EQ 3-11)
The specific risk of asset i is the standard deviation of its specific 
return, ui. The simplest way to estimate  the specific risk matrix is 
to compute the historical variance s of the specific returns. This, 
however, assumes that the specific return variance is stable over time. Rather than use historical estimates, we build a forecasting 
model for specific risk to capture fluctuations in the general level 
of specific risk and the relationsh ip between specific risk and asset 
fundamental characteristics.
Conceptually, an asset’s forecast sp ecific risk may be viewed as the 
product of two factors: the forecast average  level of specific risk 
across assets during a given mont h and the riskiness of each asset 
relative  to the average level of specific risk. Our research has 
shown that the average level of spec ific risk can be forecast using 
historical average levels and, occasionally, lagged market return. 
Additionally, our resear ch has shown that the re lative specific risk 
of an asset is related to the asse t’s fundamentals. Thus, developing 
an accurate specific risk model involves a model of the average 
level of specific risk across as sets and a model that relates each 
asset’s relative specific risk to the asset’s fundam ental characteris-
tics.
Methodology
For robustness reasons,  we first construct a model to forecast an 
asset’s expected absolute specific return. This forecast is generated 
as the product of forecasts for the average level of absolute specific 
return and the asset’s relative leve l of absolute specific return. We 
then calculate the forecast specific risk (that is, the standard devi-
ation of specific return) as the product of the forecast for the 
expected absolute return and a scalin g factor. Thus, specific risk is 
a combination of three components—the average level of absolute 
specific return, the relative level of absolute specific return, and 
the scaling factor. These produce th e final asset-specific risk fore-
cast:


---
## Page 48

Barra Risk Model
Handbook34 (EQ 3-12)
where
 is estimated via time-series analysis, in which the average level 
of realized absolute specific return  is related to its lagged values 
and, in some models, to lagged market returns. The general form 
is:
(EQ 3-13)
where
The Multiple-Horizon U.S. Equity Model and the Mexico Equity 
Model (MXE1) have an addition al lagged market return term.1
To model the relative level of ab solute specific return, we first 
identify factors that may account for the cross-sectional variation 
in specific risk among assets. Havi ng identified these factors, we 
forecast an asset’s real level of absolute specific return using the 
following model:= specific risk of asset i at time t
κ = scaling factor that converts absolute return 
forecasts into standard deviation units
= forecast relative level of absolute specific 
return of asset i at time t
= forecast average level of absolute specific 
return across all assets at time t 
= forecast average absolu te return at time t
α, β = estimated parameters
St = is the realized average of absolute specific 
return of estimation universe assets in month t
1.  For specific model details, see the Equity Risk Model Reference Guide  or the 
relevant model data sheet on http://support.barra.com.


---
## Page 49

Chapter 3
Barra Equity Risk Modeling35(EQ 3-14)
where
Updating the Model
Model updating is a process whereby  the most recent fundamental 
and market data is used to calcula te individual stock exposures to 
the factors, to estimate the latest  month’s factor returns, and to 
recompute the covariance matrix.
The latest data is collected and cl eaned. Descriptor values for each 
company in the database are co mputed, along with risk index 
exposures and industry allocations . Next, a cross-sectional regres-
sion is run on the asset returns for the previous month. This gen-erates factor returns, which are used to update the covariance 
matrix, and the specific return, which are used to calculate the 
relative absolute specific return and the average absolute specific return. The relative absolute specif ic return and the average abso-
lute specific return are combined with a scaling factor to forecast 
specific risk. Finally, this updat ed information is distributed to 
users of Barra’s software.= forecast relative absolute specific return for 
asset i at time t
Zikt = the exposure of asset i to characteristic k at 
time t
γk = characteristic k’s contribution to relative 
specific risk 


---
## Page 50

Barra Risk Model
Handbook36

---
## Page 51

Section ThreeFixed-Income Risk
Section Three provides an overview of 
fixed-income risk models and discusses 
the extensive, detailed process of 
creating Barra fixed-income risk models.
Chapter 4: Forecasting Fixed-Income Risk
Chapter 5: Interest Rate Risk ModelingChapter 6: Spread Risk ModelingChapter 7: Specific Risk Modeling

---
## Page 53

Chapter 4
Forecasting Fixed-Income Risk394. Forecasting Fixed-Income Risk 
Through the years, theoretical ap proaches to fixed-income invest-
ment analysis have become increasingly sophisticated. With more 
advanced concepts of risk and return, investment portfolio mod-
els have changed to reflect this growing complexity. 
A Historical Perspective
Until the last few decades, inve stors perceived high-grade bonds 
largely as a safe haven. But as inte rest rates spiked upwards in the 
1970s and early 1980s, investors lear ned quickly that even T rea-
sury bonds are not immu ne from risk. T raditio nally, a bond’s risk-
iness was measured by its duration —the sensitivity of a bond’s 
price to changes in yield. Assuming  all bond yields were perfectly 
correlated and equally volatile, th e riskiness of a high-grade bond 
portfolio could be measured in terms of the aggregate duration. 
Given the absence of awareness and availability of suitable analyti-
cal models, bond durations (and durations of other traditional 
fixed-income securities, such as mortgage-backed securities) were 
computed on the assumption that they would provide determinis-tic cash flows.
It is now generally recognized that neither assumption is ade-
quate. Interest rate risk includes ri sk due to changes in yield curve 
slope and curvature, not just over all shifts. Portfolios with bonds 
from multiple markets are exposed to multiple interest rate fac-
tors. And most fixed-income secur ities are not really fixed: they 
may be callable or putable, subj ect to prepayment, or have vari-
able interest rates. Thus, fixed -cashflow duration is not a valid 
measure of risk exposure for such securities.
In addition to interest rate risk , most bonds are also subject to 
credit risk. The holder of a corpo rate bond is exposed to the risk 
of a general change in credit spreads—as what happened dramati-
cally in the second half of 1998
1—and to issuer-specific credit 
events, which might lead to default.
1.  On August 17, 1998, the Russian government defaulted on domestic debt, 
declared a 90-day moratorium on paymen t to foreign creditors, and devalued 
the ruble. 

---
## Page 54

Barra Risk Model
Handbook40The key to building a successful risk model is to provide both an 
accurate decomposition of the ma rket risk factors driving bond 
returns and accurate forecasts of their covariances. Fundamental 
models of risk for fixed-income securities decompose bond returns 
into contributions arising from cha nges in interest rates, credit 
spreads and, to a lesser degree, liquidity premia, volatility uncer-
tainty, and prepayment expectations . Returns to portfolios of high 
credit quality securiti es are typically affect ed primarily  by varia-
tion in interest rates, while returns on lower quality portfolios may be determined mostly by credit factors. 
Barra’s Multiple-Factor Model
Barra’s fixed-income risk models decompose asset returns into components due to common fact ors and a specific, or idiosyn-
cratic, factor. 
For a given security, a valuation algorithm enables the calculation 
of the predictable return component  attributable to the passage of 
time.
1 The remaining “excess” return is due to a combination of 
changes in default-free interest rates (the benchmark yield curve), 
changes in market spread levels, cha nges in market volatility and 
prepayment expectations, and the specific return. Barra’s fixed-
income risk model incorporates many of these factors together 
with models of specific risk. 
1.  This might include short-term intere st rates and time value decay of embed-
ded options.Total Risk
Common Factor Specific Risk
Credit Spread Interest RateFigure 4-1
Fixed-Income Risk Decomposition

---
## Page 55

Chapter 4
Forecasting Fixed-Income Risk41Common Factors
Each bond is assigned to a single  market. The common factor risk 
of a bond is determined by the vo latilities of the term structure of 
interest rates and spread risk factors in that market, the correla-
tions between factors, and the bond  exposures to the risk factors.
Except for the euro block, each ma rket has three nominal interest 
rate risk factors. The se are the first three principal components of 
a key rate covariance matrix: shif t, twist, and butterfly (STB)—so 
called because of their shapes. The euro market has three term 
structure factors for each country and three that describe average 
changes in rates across the euro zone. In addition, the euro, ster-ling, U.S. dollar, and Canadian do llar blocks include one or more 
real yield factors applicable to  inflation-protected bonds. The 
U.S. dollar block also includes interest rate factors for municipal 
bonds. 
Every market
1 has a swap spread factor . The only instruments not 
exposed to swap spread are sovereig n issues. The U.S. dollar, ster-
ling, yen, and euro markets have detailed credit spreads, which are 
measured to the swap spread, in  addition to the swap spread fac-
tor.
1.  A market is defined by its currency . For example U.S. corporate and U.S. sov-
ereign bonds belong  to one market. 

---
## Page 56

Barra Risk Model
Handbook42 
Risk Factor Type Exposure of Asset to Risk Factor
Term structure Always. The local market is determined by the 
currency of the bond’s denomination.1
1. Euro-denominated sovereign bonds from European Monetary Union 
(EMU) member countries are expose d to the term structure factors 
of the country; all other euro-den ominated bonds are exposed to the 
EMU local market term structure factors.Swap spread Always, unless the asset is issued by a sover-
eign issuer.
Credit spread  When the asset is denominated in U.S. dollar, 
sterling, yen or euro, AND
 The asset’s sector and rating match an 
existing local market credit spread sector and 
rating, AND
 The asset is not a sovereign issue, AND
 The asset is not exposed to an emerging 
market factor.
Emerging market  When the issuer is an emerging market 
country or a corporation domiciled in an emerging market country, AND
 The asset is denominated in a currency other 
than that of the bond issuer’s country of 
incorporation (or domicile).
Currency When the asset is denominated in a currency 
other than the numeraire.Table 4-1
Risk Factor ExposureThe table below summarizes the 
rules for exposing assets to risk 
factors.

---
## Page 57

Chapter 4
Forecasting Fixed-Income Risk43Interest Rate Risk
The largest source of within-market risk1 for typical investment- 
grade portfolios is interest rate va riation. Barra models this risk in 
terms of the shift, twist, and b utterfly factor movements of the 
benchmark interest rate curve in each market.2 Together, these 
three principal components ca pture between 90% and 98% of 
interest rate variation (as measured by an 8-factor key rate model) 
in most developed markets.3  
The factors reflect the way term structures actually move, and 
their characteristics persist across  markets and time periods. Re-
1.  Within-market risks excludes currency risk.
2.  Interest rate movements are expres sed in terms of chan ges in zero-coupon 
bond yields inferred from a combinat ion of money-market rates and coupon 
bond yields. The zero-coupon yield curve is also referred to as the “term struc-
ture of interest rates,” or some times just the “term structure.”
3.  Approximately 98% of the monthly variation in U.S. government bond in-
terest rates from 1 to 30 years can be ex pressed in terms of these three factors.-1.50-1.00-0.500.000.501.001.502.002.50
0 1 02 03 04 0
Maturity in YearsWeightShiftTwist
ButterflyFigure 4-2
Shift, Twist, and Butterfly in the 
Germany Market
Like most markets, the shift factor 
in the Germany market tends to be slightly humped at the short 
end because short rates tend to 
be more volatile than long rates.

---
## Page 58

Barra Risk Model
Handbook44estimation of factors is required only when the market structure 
changes.
Because of its parsimony, the sh ift-twist-butterfly (STB) model is 
Barra’s preferred approach for interest rate forecasts.-1.50-1.00-0.500.000.501.001.502.002.503.00
0 1 02 03 04 0
Maturity in YearsWeight
x = old factor = new factorShiftTwist
ButterflyFigure 4-3
Re-estimation is Required Only 
When Market Structure Changes 
The introduction of long bonds in 
the Spain market in February 
1998 changed the length of the 
market from 15 to 30 years. The new factors, especially twist and 
butterfly, look quite different from 
the old. 

---
## Page 59

Chapter 4
Forecasting Fixed-Income Risk45Learn more about
Shift, Twist, and Butterfly Movements
Shift  describes approximately parallel yield curv e movements; that is, all key rates are 
moving by approximately the same amount. Twist  describes yield curve movements with 
short and long ends moving in opposite directions. Butterfly  describes a flexing motion 
of the yield curve.
An example
Suppose the Federal Reserve System attemp ts to stimulate the U.S. economy by 
decreasing short-term interest rates. The change in the U.S.  term structure can be seen 
in a comparison of the spot rate curve before and after the decrease. The actions of the Federal Reserve System are seen in the downwa rd movement of most of the spot rates. 
Each spot rate decreased, but with different magnitude.
 
The movement of the curve can clearly be de composed into a shift movement (the level 
of interest rates went down) and a twist movement (the slope of the curve went up). -1.50-1.00-0.500.000.501.001.502.002.50
0 1 02 03 04 0Maturity in YearsWeightButterfly
ShiftTwist
0.0%1.0%2.0%3.0%4.0%5.0%6.0%7.0%
0 5 10 15 20 25 30 35Maturity in YearsRatesBefore Decrease

---
## Page 60

Barra Risk Model
Handbook46Spread Risk
In addition to the STB interest rate factors, the risk model 
includes spread factors to acco mmodate credit-sensitive bonds. 
Barra takes a layered approach to modeling spread risk. In each 
local market, a single factor acco unts for changes in the difference 
between the swap and sovereign cu rves. Spreads on high-quality 
issuers are highly correlated with the swap spread, so this has been 
a reasonable and parsimonious approach to accounting for credit 
exposure. 
In markets with detailed credit mo dels (such as the United States, 
United Kingdom, Japan, and euro  zone), additional factors cap-
ture the risks due to changes in credit spreads over the swap Figure 4-4
Swap Spread Model 
33.544.555.566.5
0 5 10 15 20 25 30
Maturity in YearsRatessovereign curveswap curve

---
## Page 61

Chapter 4
Forecasting Fixed-Income Risk47curve. In these markets, spread risk is decomposed into swap 
spread risk and risk due to credit  spreads over the swap curve.  
In emergent markets, spread risk is decomposed into swap spread 
risk and risk due to emerging market spreads over the sovereign 
curve of the market where the bonds are issued. 2.53.54.55.56.57.5
0 5 10 15 20 25 30
Maturity in YearsRatescredit spread
swap curve
sovereign curveFigure 4-5
Credit Spread Model 
Figure 4-6
Emerging Market Model 
2345678
0 5 10 15 20 25 30
Maturity in YearsRatesemerging-market spread
swap curve
sovereign term structure

---
## Page 62

Barra Risk Model
Handbook48Learn more about
Alternative Risk Model: Key Rates
The multiple-factor key rate model  first described in the 1990s uses changes in rates at 
key maturities as the factors. Each interest rate scenario predicted a probable set of cash flows, from which the present value of a bond is calculated.
At the core of the model is the covariance matr ix that represents the price sensitivity of a 
security to key rate changes. Using a sufficiently large set of key rates, the maturity dependence of interest rate variation can be described with as much detail as desired. Since the full maturity dependence is represen ted, this model completely describes term 
structure variation.
However, the key rate model uses more factors than necessary. There is a high degree of 
dependency among factors. Neighboring key rates are typically 90% correlated, while even the longest and shortest maturity rates are nearly 60% correlated. 
Barra uses a succinct multiple -factor model that has far fewer factors than a key rate 
model yet has virtually the same explanatory power. 1 
Year2 
Years3 
Years4 
Years5 
Years7 
Years10 
Years20 
Years
1 
Year1.00 0.91 0.86 0.83 0.81 0.72 0.63 0.56
2 
Years1.00 0.97 0.95 0.93 0.84 0.75 0.69
3 
Years1.00 0.99 0.98 0.92 0.84 0.77
4 
Years1.00 0.99 0.94 0.88 0.81
5 
Years1.00 0.97 0.91 0.84
7 
Years1.00 0.97 0.89
10 
Years1.00 0.87
20 
Years1.00

---
## Page 63

Chapter 4
Forecasting Fixed-Income Risk49Specific Risk 
The specific risk model comes in  two versions. A simpler version, 
applicable to markets where credit  risk is modeled using the swap 
spread factor alone, forecasts issu e-specific spread  volatility as a 
linear function of a bond’s spre ad. A more detailed version, appli-
cable to U.S. dollar, euro, and st erling credit markets, forecasts 
specific risk based on  a transition matrix. 
We individually calibrated specific risk to each market and com-
bined it with the market common factor risk to determine total 
risk.
Summary
The search for yield has increasi ngly led portfolio managers to 
take larger positions in credit-risk y assets. The risk profile of these 
portfolios can no longer be adequa tely understood purely in terms 
of interest rate movements. Nor are “slice-and-dice” representa-tions of sub-portfolio exposures to different sector and rating 
groups adequate, as these pictures fail to reflect the impact of par-
tial diversification between sub-por tfolios, and fail to capture the 
potentially large effects of spre ad volatility and credit migration 
events. Barra’s global fixed-inco me risk model provides an effec-
tive solution for analyzing fixed-i ncome portfolios in a world of 
many risks.
Consisting of interest rate risk models for nominal and real mar-
kets, detailed and independently constructed models for four 
major markets, simpler swap-ba sed models for the remaining 
developed markets, and emerging market models, Barra’s global 
fixed-income risk model covers a large fraction of public credit 
markets. The model provides asse t managers with valuable fore-
casts of portfolio risk due to cha nges in market-wide and issuer-
specific credit spreads.

---
## Page 64

Barra Risk Model
Handbook50

---
## Page 65

Chapter 5
Interest Rate Risk Modeling515. Interest Rate Risk Modeling
Accurate interest rate risk mode ling depends on a term structure 
of interest rates. The term structure  is a curve that describes the 
rate of interest that an issuer  must pay today to borrow for each 
term.
In developed markets, yields of high-grade or low default-risk 
bonds are closely linked to thos e of similar government bonds. 
Changes in the term structure of government interest rates there-
fore imply changes in th e pricing of such bonds. 
Term structures can change in any number of ways: yields of 
bonds of all maturities may rise or fall, or yields of bonds of one 
end of the maturity pole may rise or fall while the other end 
remains unchanged. These movement s are a major contributor to 
portfolio risk for high-grade bonds.
Estimation Process Overview
Barra’s asset valuation models i ncorporate a model of interest 
rates, which are inferred from obse rved prices of bonds and other 
financial instruments. The basic objective of the term structure 
estimation algorithm is to find rates that minimize the difference 
between model and market prices. 
We use constraints to smooth the term structure and the LIBOR-
driven specifications for short rates.1 We do this to eliminate 
kinks that are idiosyncratic to the estimation period.
Next, we apply principa l components analysis to a key-rate covari-
ance matrix estimated from a hist ory of term structure changes. 
The three principal components, or eigenvectors with the largest 
variance, are the shift, twist, and butterfly factors. 
1.  LIBOR rates are used in markets that  do not have short-term government se-
curities such as treasury  bills. The London Interban k Offered Rate is the in-
terest rate offered to banks in the Lo ndon interbank market and is well known 
as a reference for short-term rates.

---
## Page 66

Barra Risk Model
Handbook52We calculate factor re turns from a cross-sectional regression of 
bond excess returns onto factor exposures. 
The principal components analysis amounts to a “rotation” of the 
factors and covariance matrix to  a representation in which the 
covariance matrix is diagonal. By keeping only the leading three 
factors, we retain the dominant sources of risk while reducing the 
potential for spurious correlations . The shift, twist, and butterfly 
factors underlying the rotated matrix are orthogonal, weighted 
combinations of changes in intere st rates. The diagonal elements 
of the covariance matrix are the in-sample variances of the factors.
We generate the 3x3-interest rate risk block of the model with the 
time series of monthly shift, twis t, and butterfly returns. The fac-
tor volatilities (expressed as on e standard deviation) and correla-
tions determine the in terest rate block. 
Data Acquisition
We obtain daily price data on lo cal government bonds issued in 
29 markets, inflation-protected bo nds (IPBs) issued in four mar-
kets,1 AAA-rated tax-exempt munici pal bonds issued in the 
United States, and LIBOR/swap curves in 23 markets.
1.  Barra collects daily price data on IPBs issued by the governments of the 
United States, Great Britain, Canada, and France.Model Estimation Process
1. Data acquisition
2. Term structure specification: 
a. Interpolationb. Estimation algorithm 
implementation
3. Factor shape determination: 
key rate covariance matrix
4. Factor exposure calculation
5. Factor return estimation 
6. Covariance matrix 
estimation 
7. Covariance matrix 
correlation
8. Model updating

---
## Page 67

Chapter 5
Interest Rate Risk Modeling53Learn more about
Inflation-Protected Bonds
An inflation-protected bond  (IPB) is a fixed-income security whose principal is 
periodically adjusted to provid e a fixed return over inflation. The adjustment lags a pre-
specified measure of inflation by an amount of time determined by the issuer.1 The 
coupon is a fixed rate applie d to the adjust ed principal. 
In the case of U.S. Treasury inflation-protected bonds, the Treasury pays a fixed rate of 
return over inflation (as measured by the non-seasonally adjusted U.S. City Average All Items Consumer Price Index for All Urban Cons umers or CPI). The adju stment lags the CPI 
release by two months to remove the ambiguity of the nominal amount of the next coupon. 
To the extent that IPBs comprise a signific ant portion of a portfo lio, a risk model that 
accurately and reliably distinguishes the mo vements of the real yield curve (on which 
these securities are directly dependent) fr om those of the nomi nal curve is needed. 
Barra Risk ForecastingTo forecast the risk of the nominal return of an IPB on a monthly horizon, its payoffs are 
expressed in real, or inflation-adjusted currency. The IPB can then be treated as a garden-
variety fixed-principal bond. 
IPB prices, which are quoted in real terms in  every market but the United Kingdom, are 
used to estimate the real yield curve. The real  risk factors and real return risk forecasts 
are then determined by applying standard principal components analysis, which is the 
same methodology used in no minal markets. Finally, the re al returns are approximately 
related to nominal returns through 
rN = rR + rI , where rN is the nominal return of an 
IPB, rR is the real return, and rI is the return due to the in flation adjustment factor. Due 
to the lag between the inflation index and the inflation adjustment of the bond, the rI is 
known with certainty more than a month in advance. So, for the corresponding risk forecasts, 
σN = σR, where σN is the nominal return risk and σR is the real return risk.
1.  For details on IPBs, see Barra white pa per, “Barra’s Real Yield Model.” It is 
available on http://www.barra.com. 

---
## Page 68

Barra Risk Model
Handbook54Learn more about
U.S. Municipal Bonds
Municipal bonds  are debt obligations issued by stat es, counties, cities, and other local 
governmental entities to support general governmental needs or special projects for the public good.
The municipal bond market is affected by financial factors somewhat distinct from the 
primary drivers of the taxable bond market . Aside from the obvious difference in tax 
treatment, municipal bonds, or munis , include:
■A very large number (about two million)  of relatively small, illiquid issues
■Additional option features, such as pre-refunding.
Barra’s U.S. municipal bond model1 is based on histories of four yield curves for national 
general obligation (GO) bonds rated AAA (uninsured), AA, A, and BBB. Histories of these yields, which go back to 1994, are the basic in formation used in constructing the model. 
The risk model structure is si milar to the taxable U.S. model. Like the investment-grade 
portion of the taxable model, the dominant contribution to ri sk arises from market-wide 
interest rate levels. These are captured in the municipal bond model by eight key rate 
factors: 1, 2, 3, 5, 7, 10, 20, and 30 years.  Rather than following the usual practice of 
calculating spot rates from yields by “bootstrapping, ”
2 we calculate the current levels for 
the key rates by means of a modified vers ion of our standard spot-rate estimation 
mechanism, which minimizes ro ot-mean-squared pricing error of a universe of bonds. 
This is done because market yields for maturi ties beyond 10 years are quoted in yields 
of callable bonds. The root-mean-squared minimization method allows us to properly handle the callabilit y of the longer maturity yields. Were  we to do standa rd bootst rapping 
and then use the resulting spot rate curve to  value callable bonds, we would not be able 
to reproduce the market yields we started from.
In addition to the non-taxable interest rate factors, the model includes three credit spread 
factors—one each for AA-rated,  A-rated, and BBB-rated bonds.  These are calculated as 
average spreads of the corresponding spot ra te curves over the general-obligation AAA 
curve. In total, then, the municipal bond ri sk model contains 11 common factors: eight 
key rates and three rating spreads. In addition to common factor risk, the municipal bond model incorporates a modified version of the taxable issuer credit-risk model. The issuer 
credit-risk model uses historical information about credit migration rates together with 
current spread levels to forecast risk du e to upgrades or downgrades and default.
1.  For details on municipa l bonds, see Barra white pa per, “The U.S. Municipal 
Bond Risk Model.” It is avai lable on http://www.barra.com. 
2.  Bootstrapping is a procedure for rec ursively calculating su ccessively longer 
spot rates based on market yields.

---
## Page 69

Chapter 5
Interest Rate Risk Modeling55Term Structure Specification
Since interest rates are neither boug ht nor sold, a term structure is 
a derived quantity. Term structures  differ across borrowers and 
can change dramatically in the cour se of a day. We estimate term 
structures for valuation and exposure calculation on a daily basis.
Interpolation
We determine the term structure by a numerical procedure that 
sets spot rates at predefined ve rtices to minimize the differences 
between observed and theoretical bond prices. The term structure 
is specified by spot rates at a set of vertices.1 A higher density of 
vertices is used at the short end to reflect the greater amount of 
short-end information available.
Interpolation is used to compute  rates of maturities that are 
between the vertices. The interpolation rule assumes that forward rates are constant between vertices . We constrain optimization to 
keep these forward rates positi ve. We then continuously com-
pound the rates. 
The forward rate between t
i–1 and ti is first obtained with:
(EQ 5-1)
where
Then spot rates between vertices are determined by interpolating 
with the following formula:
1.  For each market, a subset of standard  maturities (1, 3, and 6 months, and 1, 
2, 3, 4, 5, 6, 7, 10, 15, 20, and 30 year s) is selected. The number of vertices 
used to estimate the term structure depe nds on the availabili ty of price data 
on the maturities of bonds. fi–1, i = forward rate of period ti–1 to ti
si = spot rate of maturity i 
ti = length of time before maturity i


---
## Page 70

Barra Risk Model
Handbook56(EQ 5-2)
where
Suppose the ten-year spot rate, s10, is 3%, and the 20-year spot 
rate, s20, is 5%. Then the 10-to-20 forward rate is:
(EQ 5-3)
The 15-year spot rate is then:
(EQ 5-4)si = spot rate of vertex i
fi = forward rate of period ti–1 to t
t = length of time before maturity


---
## Page 71

Chapter 5
Interest Rate Risk Modeling57Learn more about
The Benchmark Yield Curve
Interest rates are modeled glob ally based on sovereign issuer s' domestic bonds. For the 
euro zone, in addition to estimating interest rate factors for each “legacy” sovereign issuer, we also estimate a euro sovereign term structure of interest rates and factor series 
from the aggregate of all euro government bonds weighted by GDP .
Because interest-rate risk is the dominant source of day-to-day variation in value for 
investment-grade securities, security prices ha ve traditionally been quoted relative to a 
market-wide benchmark yi eld curve. Until recently, in most  markets, this curve has been 
based on the yields of government bonds—gene rally the highest credit  quality issuer in 
the domestic currency.
This situation has changed, for several reasons. First, in the euro zone, there is no natural 
government bond yield curve. French and Ge rman bonds generally trade at the lowest 
yields, with other issuers at comparable or hi gher levels. This lack of an obvious standard 
has led to the emergence of the LIBOR/swap curve
1 as the valuation benchmark. 
Second, the U.S. and other government bond markets have experienced a number of 
technical, supply-related distortions, particularly since 1998. These are the results of a global flight to quality at the time of the Russian default and LTCM collapse, the debt buybacks of 2000 and early 2001, and the chan ging issuance patterns, such as the 
termination of 30-year bond issuance. These market distortions have led to a decoupling 
of the U.S. Treasury bond market from th e mortgage-backed securities (MBS), asset-
backed securities (ABS), and bond markets. To varying degrees, traders have shifted to 
the swap curve as a benchmark in the United States as well.
2 
Finally, the growing liquidity and transparency of swap curves have led to increased 
acceptance of these financial rates as a reference for the broader debt markets. 
This acceptance is, however, not universal. The U.K. and Japan markets, for example, 
continue to trade primarily relative to government benchmarks. Barra therefore devised a hybrid scheme that admits alternative views to create a factor structure for interest rate 
risk. 
1.  The LIBOR/swap curve, hereafter a bbreviated to “swap curve,” is derived 
from deposit rates out to on e year and par fixed/floating swap rates at longer 
maturities. Liquid swap rates are now ro utinely available up to maturities of 
30 years in most developed markets.
2.  There was brief speculation that U. S. agency debt would replace T reasury 
debt as a trading benchmark—speculation that was encouraged by the agen-cies’ large “global benchmark” bond is sues. However, it was quickly realized 
that the agencies are subject not only to  liquidity risk but also political un-
certainty, and their use as benchmarks has largely fizzled. 

---
## Page 72

Barra Risk Model
Handbook58Estimation Algorithm Implementation
We estimate the term structure wi th an objective function com-
posed of three pieces. The objective function is expressed as:
(EQ 5-5)
The first term minimizes the di fferences between market and fit-
ted prices in the term structure; the second term subjects the term 
structure to a smoothing constr aint; the third term uses LIBOR-
driven specification to determine short-end vertices of term struc-
tures of markets where there are no short sovereign issues. The terms in the objective function i ncorporate weights that serve to 
control the relative impact of di fferent effects. For example, plac-
ing large weights on the second term ( E
2) would force the result-
ing term structure to be very smooth. 
Term structures for real, or infl ation-adjusted, markets are esti-
mated with only the first term of the objective function. The 
smoothing term ( E2) and the short-end correction ( E3) are both 
zero.
Barra Research Methods
Diagnostics on Term Structure Estimation
The estimation algorithm identifies bonds with  large pricing errors and eliminates them. 
This is done by an iterative process. First,  a term structure which includes all bonds is 
estimated; bonds with pricing errors above a threshold are discarded. Then the estimation runs again. This procedure is repeated until there are no more bonds with large pricing errors.
We use a set of automated diagnostics to identify potential problems with the term 
structure estimation. The simplest of thes e measures flags the deviation between the 
newly estimated term structure and the previo us day’s estimated term structure. Large 
daily or monthly changes are investigated. 
The root mean square pricing error is also computed. All ot her things being equal, this 
statistical quantity tends to increase with the number of bonds in the universe. In the U.S. Treasury term structure estimation, for ex ample, there are appr oximately 110 bonds and 
the root mean square error ranges between 30 to 50 basis points. Although the number itself has no definitive interpretation, abrupt  changes in its value are useful for flagging 
problems in the estimation.

---
## Page 73

Chapter 5
Interest Rate Risk Modeling59Sum of Squared Relative Pricing Errors ( E1)
The first and dominant term in the objective function is the sum 
of squared relative pr icing errors of bonds in the estimation uni-
verse. It minimizes the differences between market and fitted prices in the term structure.
The pricing error term E
1 is given by:
(EQ 5-6)
where
The relative pricing error, εi  is given by:
(EQ 5-7)
where
The weighting scheme ( ωi) can, for example, be used to down-
weight callable bonds. Since the model price Qi depends on the 
term structure, changes in term st ructure give rise to changes in 
E1. The fitting routine works by moving rates until the minimum 
difference between fitted price and market price is found. 
Smoothing Function ( E2)
Because term structures  produced with only E1 in the objective 
function may have idiosyncrasies due to noise in the data or a 
mismatch between the data and the location of vertices, a second term, E
2, is included. ωi= weights
εi = relative pricing error
Pi = market price of bond i
Qi= fitted price of bond i


---
## Page 74

Barra Risk Model
Handbook60This term is based on a three-parameter family of equations that 
acts as a smoothing function. The fa mily of functions is expressed 
as:
The parameters θ, r0, and κ are jointly estimated with the spot 
rates.
A discrete version of the smooth ing function generates the second 
term of the objective function, which is expressed as:
(EQ 5-9)
where(EQ 5-8)
where
θ = long rate
r0 = short rate
κ = decay constant
T =t e r m
αj = weight of smoothing term
Figure 5-1
Typical Smoothing Curve 
The three parameters (which are 
r0 = 2%, θ = 6%, κ = .09), along 
with the rates at the vertices, are 
outputs of the fitting routine. Typi-
cally, all the parameters are posi-tive and 
θ > r0. 
01234567
0 1 02 03 04 0
Maturity in YearsRates


---
## Page 75

Chapter 5
Interest Rate Risk Modeling61In the equation above, the αj’s are weights that control the rela-
tive importance of th e smoothing terms at different maturities. αj 
is smaller for shorter maturities,  so the smoothing function has 
less influence on the 1-year ve rtex than on the 30-year vertex.
Short-End Shape Correction ( E3)
The universe of bonds used to  determine the term structure 
excludes bonds with remaining time to maturity under one year. 
These bonds tend to be relatively illiquid, hence their prices do 
not reflect current rates. As a result, there is generally not enough information in the objective fu nction to reliably determine key 
rates under one year. 
This problem can be handled in so me markets by adding treasury 
bills or equivalent asse ts to the estimation.
1 However, many 
important markets do not include short domestic government 
issues. Therefore, the shape of the LIBOR term structure is used 
as an indicator of the shape of the short end of the government term structure.
2 
Since LIBOR rates are not default free, they are not directly 
included in the government te rm structure estimation. Instead, 
we impose the assumption that th e ratio between the government 
and one-year LIBOR rates is roughly constant for the short end 
of the term structure. This assum ption is imposed with the addi-
tion of a third term to the objective function, which is:
(EQ 5-10)ψ = smoothing curve
Tj = maturity of vertex j
s(T) = spot rate curve
1.  For example, Japan and the Unit ed States have treasury bills.
2.  The 1-, 3-, and 6-month, and 1-year LIBOR rates are used to determine the 
short end of the term structure in  the fixed-income risk models.


---
## Page 76

Barra Risk Model
Handbook62where
The constant μ is typically between 0.7 and 1.05. Along with the 
spot rates and smoothing parameters, μ is found by the estimation 
routine. The weights, τi, can be individually calibrated to each 
market. The weights on E1 are larger than the weights on E3, so if 
short bonds are available, they will  be used to determine the short 
end of the term structure. For ex ample, if treasu ry bill informa-
tion is available, the resulting low E1 weights would de-emphasize 
the E3 term in the estimation.
 τi = weight of ith short-end constraint term
μ = constant ratio between LIBOR and sovereign 
rates
44.555.566.57
0 5 10 15 20 25
MaturityPercent
From Australian LIBOR ratesRates
Maturity in YearsFigure 5-2
Estimated Australian Treasury 
Term Structure
In these estimated interest rates, 
the shape of the short end is 
given by the LIBOR curve.

---
## Page 77

Chapter 5
Interest Rate Risk Modeling63 
Factor Shape Determination 
The spot rate covariance matrix can now be generated from the 
historical term structure. A time series of month-over-month dif-
ferences in spot rates is first created for each of the standard verti-ces. From these time series, we obtain the key rate covariance 
matrix. The eigenvectors of this matrix, or princi pal components, 
correspond to uncorrelated movements of the term structure. The three largest contributors—called shift, twist, and butterfly 
(STB)—typically accoun t for about 95% of th e empirical volatil-
ity. 
In markets with a large number of bonds representing a broad 
spectrum of maturities (such as the nominal U.S. market), these 
three factors are significant. In IP B markets, fewer factors are rele-
vant. Generally speaking, IPB markets consist of a small set of bonds with long maturity. For simplic ity, we treat the shift factor 
in these real market as  a uniform, parallel shift of the term struc-
ture. The twist factor—if present— is then the leading source of 
risk residual to the parallel shift.
1
1.  Only the U.S. and U.K.  IPB markets have a twist fa ctor in addition to the 
shift factor. 01234567
0 5 10 15 20 25 30 35MaturityPercent
U.S. Treasury bill rate
Maturity in YearsRatesFigure 5-3
Estimated U.S. Treasury Term 
Structure
Because treasury bill information 
is available for the U.S. market, 
the weight in the third term (E3) of 
the objective function is small. 

---
## Page 78

Barra Risk Model
Handbook64Factor Exposure Calculation
Term structure factor exposures are computed by numerical differ-
entiation. The exposure of a bond or portfolio to a risk factor is 
the sensitivity of its value to changes  in the factor level. For exam-
ple, effective duration  is the sensitivity of va lue to a parallel shift 
of interest rates. The term structure is shocked, or shifted up and 
down, by a small scalar  multiple of the STB factor, and the bond 
is revalued. In other words, we calculate how the price of a bond 
changes for a given change in th e yield curve. The difference Barra Research Methods
Normalizing Term Structure Factors
Principal components analysis  of the key rate covariance matrix, which generates the 
shift, twist, and butterfly fact ors, determines the relative weights of the factors at the key 
maturities. The absolute sizes of the factors are not determined. 
If a factor is scaled by a constant c, the exposure of a portfolio to this factor is scaled by 
c as well. The returns to the factor are scaled by 1/c so that the scale factor cancels out 
of the risk calculation. 
The shift factor is roughly a parallel change in interest rates. For non-callable bonds, 
therefore, the exposure to shift should be a number comparable to effective duration. The 
magnitude of the shift exposure  can be controlled by changing the size of the shift factor. 
By convention, the factors are normalized so that their mean-squared value is the number 
of vertices (a true parallel shift is normalized at a constant 1) and so that they are positive at long maturities. The base shift is normaliz ed so that the shift ex posure is comparable 
to effective duration. The base twist and butt erfly factors are normaliz ed to have the same 
magnitude as the shift.
1
This normalization is not preserved in the transformation of the STB factors.2 However, 
since the magnitude of the transformation is re latively small, the re vised shift exposures 
is still comparable to  effective duration.
1.  For more details see, for example, Richard A. Johnson and Dean W. Wich-
ern, Applied Multivariate Statistical T echniques, 4t h ed., (Upper Saddle Riv-
er, NJ: Prentice Hall, 1998) 458-497. 
2.  T ransformation of STB fact ors is discussed in detail in Covariance Matrix 
Correlation on page 66 .

---
## Page 79

Chapter 5
Interest Rate Risk Modeling65between “up” and “down” values is divided by twice the size of the 
shift. The mathematical formula is given as:
(EQ 5-11)
where
Factor Return Estimation
First, we identify the factors that  explain the asset return and cal-
culate the exposures to these fact ors; then, we es timate the factor 
returns by regressing the compute d exposures against the realized 
bond return. 
(EQ 5-12)
where
The regression universe includes the set of bonds that are in an 
established market index at the start and end of the month. x = factor exposure
P+ , P– = bond present values obta ined by shocking the 
term structure
Pdirty = dirty price (price and accrued interests) of the 
bond
δ = size of the shock (typically 25 bps)
rj = vector of excess return
xi = matrix of factor exposures
f = vector of factor returns
ui = vector of specific returns 


---
## Page 80

Barra Risk Model
Handbook66Term Structure Covariance Matrix Construction
We use the time series  of STB factor returns  to generate the cova-
riance matrix.
Covariance Matrix Correlation
In principle, factor returns can be  estimated from a regression of 
changes in term structures onto the factors. This simple method-
ology results in a diagonal co variance matrix in sample.1 But it 
does not take into account the un even distribution of bonds along 
the maturity spectrum. Therefore , we rejected this method.
Regression based on bond returns , on the other hand, not only 
accounts for uneven distributio n, but also changes dynamically 
with the distribution. With this regression, the portion of risk 
that is accounted for by bond-s pecific factors declines by 20%, 
while the portion that can be accounted for by common factors 
increases correspondingly.Term Structure 
FactorsAnnual Volatility 
Shift 67.6
Twist 35.7Butterfly 18.0
Shift Twist Butterfly
Shift
67.6 0.33 –0.23
Twist 35.7 0.43
Butterfly 18.0
1.  Nonzero correlations of small magnitude would result from a difference be-
tween the risk analysis date and the date at which the factors are fixed.Table 5-1
Shift, Twist, and Butterfly Return 
Volatility in the United Kingdom (November 30, 2000)
Volatilities are reported in basis 
points per year. The annualized numbers are obtained from the 
monthly time series by multiplying 
the monthly estimate by . In a developed market, the typical 
shift volatility is 65–100 basis 
points per year (roughly 20–30 basis points per month).12
Table 5-2
U.K. Shift, Twist, and Butterfly 
Covariance Matrix (November 30, 
2000)
The diagonal shows the volatili-
ties, the standard deviation of 
annual returns.The off-diagonals 
show the correlations between 
the factors.

---
## Page 81

Chapter 5
Interest Rate Risk Modeling67However, regression based on bo nd returns results in nontrivial 
factor correlations th at can be as high as 0.5. The bond-return
regression used to esti mate the factor returns,1 the initial smooth-
ing process applied to the factor s, and the out-of-sample factor 
returns contribute to the correlations. 
These correlations carry informa tion important to risk forecast-
ing. As long as the correlations  are not perfect, the explanatory 
power of the model is not compromised. 
For the U.S. municipal bond market, we use a key-rate-based 
term-structure factor model, derived from a yield curve for 
national AAA-rated gener al obligation bonds. 
Updating the Model
The most recent fundamental and ma rket data is used to calculate 
bond exposures to the factors and to estimate the latest month’s 
factor returns.
The term structure is estimated on a daily basis, but the covari-
ance of the risk factor s is estimated on a mo nthly basis. We run a 
cross-sectional regression on the asset returns for the previous 
month. This generates factor re turns we use to update the covari-
ance matrix. 
The precise base forms of the shif t, twist, and butterfly factors 
depend on the estimation period, smoothing technique, exponen-
tial weight, and other details. Since the key rate matrices evolve 
slowly, factor re-estimation requires occasional, rather than fre-quent, review and re-estimation.
1.  Bond-return regression is the main co ntributor to the non-trivial correlations 
between the factors.Shift Twist Butterfly
Shift 1.00 0.33 –0.23
Twist 1.00 0.43
Butterfly 1.00Table 5-3
Correlations Between U.K. Shift, 
Twist, and Butterfly Returns as of 
November 30, 2000
The correlation comes from the 
bond-return regressions used to 
estimate the factor returns, the 
initial smoothing process applied to the factors, and the out-of-sam-
ple factor returns.

---
## Page 82

Barra Risk Model
Handbook68

---
## Page 83

Chapter 6
Spread Risk Modeling696. Spread Risk Modeling
In the past, international bond mangers focused largely on gov-
ernment bond issues, which were  the constituents of the domi-
nant global fixed-income indexes. Recently, managers have 
increased the exposure of their global fixed-income portfolios to corporate and agency bonds, foreign sovereigns, supranationals, 
and credit derivatives. These bo nds are subject to spread risk.
1
Spread risk in bond portfolios ar ises for two reasons: market-wide 
spread risks and credit event risk s. Market-wide spread risk arises 
from changes in the general spread level of a market segment. For 
example, the spreads of BBB-rat ed telecom bonds might widen. 
Credit event risk arises when an in dividual issuer suffers an event 
that affects it alone. It is the ri sk associated with changes in com-
pany fundamentals. For example, Ford Motor Company’s car sales 
might fall relative to other automa kers due to a product recall and 
bad publicity, or sale s might grow through th e roof because Ford’s 
engineers invent a car that runs on tap water. 
In each market, a single swap-spread factor accounts for changes 
in the difference between the swap and sovereign curves. For mar-kets with detailed credit mode ls (such as the United States, 
United Kingdom, Japan, and euro  zone), we decompose credit 
spread risk into two separately modeled components: the swap spread component and the sector-by-rating credit spread compo-
nent. For emerging markets, we expose the bond to the swap 
spread factor and the appropriate emerging market spread factor.
1.  The market perceives varying levels of creditworthiness among EMU sover-
eigns, giving rise to spreads between EM U sovereign issuers, so we estimate a 
term structure for each EMU sovereign.

---
## Page 84

Barra Risk Model
Handbook70Swap Spread Risk Model
In markets where a detailed cred it spread model or an emerging 
market model is not estimated, credit spread risk is accounted for 
by exposing bonds to the swap spread. 
Data Acquisition and Fa ctor Return Estimation
Barra obtains daily swap rate dat a for 26 markets from data ven-
dors. In each market, swap spread ris k is based on a single factor: 
the monthly change in the average spread between the swap and 
treasury curve. 
Factor Exposure Calculation
For bonds that are exposed to a credit factor or an emerging-market factor in addition to the swap-spread factor, the swap-
spread exposure is equal to the se nsitivity of a bond’s return to 
change in the swap spread level. The  exposure is equal to effective 
duration. 
For bonds that do not have additi onal factors to explain their 
credit risk, the swap-spread factor is  used to forecast  risk for debts 
of widely varying credit quality. Since bonds of lower credit qual-
ity tend to be more volatile, we scale their exposures to the swap 
spread by their (higher) option-a djusted spread (OAS), as shown 
in the formula:-30-20-10010203040
Sep-91
Jan-93
Jun-94
Oct-95
Mar-97
Jul-98
Dec-99
Apr-01
Sep-02Basis Point s Basis PointsFigure 6-1
Monthly Changes in BBB Credit 
Spreads for Bonds Denominated 
in U.S. Dollars
Volatility spiked  during the cur-
rency crisis in autumn of 1998 
and was followed by a period of 
persistently high volatility. Risk of 
this type is modeled with spread 
factors.
Swap Spread Model Estima-
tion Process (All Markets):
1. Data acquisition
2. Factor return estimation 

---
## Page 85

Chapter 6
Spread Risk Modeling71(EQ 6-1)
where 
For fixed rate bonds, this reduces to xswap=αDeff, because for these 
bonds, Deff = Dspr. The bond sensitivity to a change in the swap 
spread level (typically spread durati on) is scaled by the ratio of the 
bond’s OAS to the swap-spread level raised to the power γ, which 
is typically 0.6. Hence, bonds with  higher OAS will have corre-
spondingly higher volatility fore casts. The exponent takes into 
account the nonlinearity in the relationship between OAS and volatility. The exponent 
γ is fitted in each market with maximum 
likelihood estimation.  
Detailed Credit Spread Risk Model
In four of the most active market s, additional factors capture the 
risks due to changes in credit sp reads over the swap curve. The 
spread risk in the U.S. dollar, st erling, yen, and euro markets is 
decomposed into swap spread risk an d risk due to credit spreads 
over the swap curve.xswap = swap spread exposure
α =
Dspr = spread duration of the bond
-60-50-40-30-20-1001020304050
May-90
Sep-91
Jan-93
Jun-94
Oct-95
Mar-97
Jul-98
Dec-99
Apr-01
Sep-02Basis Point s Basis PointsFigure 6-2
Monthly Changes in Average 
Swap Spread for Bonds Denomi-nated in Australian Dollars
This series and others of the 
same type are incorporated into the covariance matrix estimation.

---
## Page 86

Barra Risk Model
Handbook72The euro zone presents a more complicated picture due to the 
presence of more than one sovereign issuer. A single set of inter-
est-rate factors is not sufficien t to capture the disparate credit 
qualities of the EMU sovereigns . Consequently, we provide inter-
est rate factors for each sovereign issuer as well as factors for 
changes in average euro zone rates.1 Thus, euro-denominated sov-
ereign bonds from EMU member countries will be exposed to the 
term-structure factors of the co untry’s local market. All other 
euro-denominated bonds will be exposed to the general EMU term-structure factors.
Currency Dependence
Bond credit spreads are not mark et independent. To date, high-
grade bonds issued in different ma rkets by a single issuer often 
have no significant correlation be tween spread changes in the dif-
ferent markets. If T oyota were to  issue U.S. doll ar-, sterling-, and 
euro-denominated bonds, the credit spread levels and returns of 
the bonds will not be equal. The differences will persist even if 
the bonds were to have an appare nt hedge overlay that allows the 
conversion of a credit exposure in one currency to an equivalent 
one in another currency.2
Factors based on investment-grade bonds with a common cur-
rency and a common sector or ratin g show a very high degree of 
correlation; factors based on bond s with a common sector and rat-
ing but denominated in different cu rrencies show very little corre-
lation. For example, Canadian government bonds in the three 
1.  These are based on monthly changes in  a yield curve estimated from the pool 
of actively traded EMU sovereign issues. Bonds are weighted by the GDP of 
the issuer. See Lisa Goldberg and Anto n Honikman, “The Euro Yield Curve: 
Projecting the Future,” Euro (December 1998).
2.  For example, a series of currency forward rate agreements (FRA) could be 
used, in principle, to convert a ster ling-denominated bond into a euro-
denominated bond with the same spread over the LIBOR/swap curve.

---
## Page 87

Chapter 6
Spread Risk Modeling73markets had essentiall y zero correlation in their spread changes 
over the two-year period June 1999–May 2001.  
 020406080100
FactorAnnualized volatility (bps
Euro Sterling US dollarSwap spread
Agency AAA
Financial AAA
Financial AA
Financial A
Industrial AA
Industrial A
Industrial BBB
Supranational AAASovereign shift(bps) Annualized Volatility (bps)Figure 6-3
Cross-Market Volatility Compari-
son 
A comparison of term structure 
shift, swap, and several credit spread volatilities for the U.S. dol-
lar, sterling, and euro markets 
shows that U.S. dollar volatilities are higher than eu ro volatilities, 
sometimes by a factor of three. 
The volatility of the sterling sec-tors consistently lies between the 
two extremes. Estimates are 
based on monthly data weighted exponentially with a 24-month 
half-life.
Euro
Sterling
U.S. DollarFigure 6-4
Map of Spread Return Correla-
tions for the U.S. Dollar, Sterling, 
and Euro Markets
The “heat map” shows correla-
tions among credit factors. High 
correlations (0.7–1.0) are consis-tently observed within a single 
market, whereas global market 
correlations remain mostly between –0.3 and 0.3.

---
## Page 88

Barra Risk Model
Handbook74Because empirical evidence indica tes that credit spreads are cur-
rency dependent, we base our mode ls on currency-specific credit 
risk factors.1
Model Structure
Spreads of different rating categories in different sectors are not 
perfectly correlated.
For U.S. dollar-, sterling-, and eu ro-denominated securities, the 
detailed common-factor spread mo dels are based on a sector and 
rating breakdown. Non-government se curities are exposed to some 
combination of sector and ratin g spread risk factors—generally 
one spread factor for each sector /rating combination (the Japan 
model works somewhat differentl y). In addition, each non-gov-
ernment security is exposed to th e swap spread for its currency.
The U.S. dollar, sterli ng, and euro blocks have one factor for each 
combination of sector and rating. The U.S. dollar block, however, 
has some exceptions. It has a se ctor-independent CCC rating fac-
tor, as well as an agency and fi ve mortgage-backed security (MBS) 
factors. 
For the yen block, rating dependence is restricted to the Samurai 
(foreign) and Corporate sectors.  In addition, yen bonds are 
exposed to a premium/discount spread factor, where the exposure is equal to the market pr emium (positive  or negative)
2 of the 
bond. The exposure to the factor is equal to the difference 
between the market pric e and par (market price  – par). So a bond 
that has a par at 100 but is trad ing at 103 has an exposure of 3. 
The farther from par the bond is trading at, the greater the expo-
sure to this factor.
In the U.S. dollar, sterling, and eu ro blocks, factors with sparse or 
absent data are proxied by a generic rating-based spread factor. 
For example, if there is no information on BBB-rated suprana-
tional securitie s, we use generic BBB spread data instead. This 
1.  Further discussion of this point can be found in A. Kercheval, L. Goldberg, 
and L. Breger, “Currency Dependence in  Global Credit Markets: The Need 
for More Detailed Risk Models,” Barr a, 2001, in the Client Support Library 
http://www.barra.com. 
2.  The spread indicates how much of a premium or discount the bond is trading 
at.

---
## Page 89

Chapter 6
Spread Risk Modeling75improves model coverage. If a user wants coverage outside the 
estimation universe or if new bond s appear in a previously empty 
sector/rating bucket,1 the model provides a reasonable forecast.
1.  This was recently the case with A-rated supranational bonds.Barra Research Methods
Sector-by-Rating Framework
Why does Barra use what looks like a tremendo us excess of factors within each market, 
breaking up the market structure into individual sector-by-rating factors, rather than having each bond exposed both to a sector factor and a rating factor (with far fewer total factors)? Using a sector + rating factor structure, rather than a sector-by-rating structure would provide a more parsimonious framework, and, consequently, one might expect, more reliable volatility forecasts.
The explanation is fairly straightforward. Trying to represent bond spread changes as the 
sum of a sector spread change and a rating spread change fails in many cases. Spreads of different rating categories in different sectors behave independently. 
Consider what happens to bond spreads after a positive shock to energy prices. One 
expects energy company bond spreads to be unaffected, or perhaps even tighten and transport company bonds to widen. The degree of this widening is likely to be strongly dependent on rating (BBB-rated transport b onds will widen much mo re than AAA-rated 
ones). In the sector + rating framework, the difference between transport bonds and energy bonds has to be explained entirely by  generic transport and energy spreads. There 
is no place in the model to allow for BBB and AAA energy spreads to stay more or less 
the same, while the difference between BBB and AAA transport spreads widens 
significantly. This sort of phenomenon happens often enough for us to reject the sector + rating model as a viable structure. Statistical tests of the added explanatory power of the sector-by-rating model over the sector + rating  scheme demonstrate that, in more volatile 
historical periods, the more detailed model captures genuine effects not seen by the 
more restrictive model.
After the attacks on New York City and Wa shington, D.C. on September 11, 2001, the 
transport company spreads—particularly for lower rated bonds—widened dramatically. The changes for energy and finance bonds, while historically large, were not nearly so significant. In order to accommodate both the sector effect and the rating effect, the restricted sector + rating model actually entails a tightening of both the energy and finance spreads to compensate for the very large BB–A spread widening needed to fit the transports. The result is that the more restrictive model gives a poor fit for the higher rated sectors. Although the magnitude of Sept ember 11 is extraordinary, less dramatic 
instances of the same phenomenon occur frequently.

---
## Page 90

Barra Risk Model
Handbook76 
Euro U.S. Dollar Yen
Sector by Rating:  9 x 4 
factors estimated for the nine sectors listed below 
and four rating catego-
ries, AAA to BBB:
 Agency Energy
 Financial 
 Industrial Pfandbrief
 Sovereign
 Supranational Utility
 Telecommunications
High Yield : one BB, one 
B, and one CCC factorAgency:  One factor for all 
agency bonds
Sector by Rating:  Up to 9 
x 6 factors estimated for 
the nine sectors listed below and six rating cat-
egories, AAA to B:
 Canadian-issued bond 
(any sector)
 Energy (industrial 
sector–oil and gas 
subsector)
 Financial
 Industrial (all 
industrial subsectors
 
other than  aerospace 
and airlines, oil and 
gas, railway, or 
shipping)
 Supranational 
(supranational issuers only)
 Telecommunications 
(utility sector–
telephone subsector)
 Transportation 
(industrial sector–
aerospace and airlines, railways, and 
shipping subsectors)
 Utility (utility 
subsectors other than 
telephone)
 Yankee (non-U.S., non-
Canada, non-supranational issuer)
CCC Rating:  One factor 
estimated across all sec-
tors
MBS: Five spreads, one 
each for conventional 15 year, 30 year, and bal-
loons, and GNMA 15 
year and 30 year
Muni:  one AA, one A, and 
one BBB factorSector and Rating: 33 factors
 Government Benchmark Bank of Tokyo Norinchukin Bank Shokochukin Bank Corporate AAA Corporate AA Corporate A Corporate BBB Corporate BB Corporate B and CCC Current Yield (government) Current Yield (non-
government)
 Government Guaranteed Highway International Bank of Japan Finance Long-Term Credit Bank Government Mid-Term Big 5 Municipal (Osaka, 
Kobe, etc)
 Other Muni Tokyo Muni Nippon Credit BankN T T Non-Government 
Guaranteed (NHK, TRT)
 Other Electric Sinking Fund Bond Government Six-Year Samurai AAA Samurai AA Samurai A Samurai BBB Tokyo Electric Zenshiren Bank Railway (guaranteed) Fiscal Investment and Loan 
Program
Sterling
Sector by Rating:  7x 4 
factors estimated for the 
seven sectors listed below and four rating cat-
egories, AAA to BBB:
 Agency
 Financial  Industrial
 Sovereign
 Supranational Telecommunication
 Utility
High Yield : one BB, one 
B, and one CCC factorTable 6-1
Credit Risk Factors in Each 
Market
In the United States, United King-
dom, and the European Union, most factors are determined by 
combinations of sector and rating. 
The U.S. block has some excep-
tions, specifically, the CCC rating 
factor, which does not take account of the sector, and the 
mortgage spreads, which do not 
depend on rating. In Japan, the model structure is somewhat 
unique as it is based on local Jap-
anese market conventions. Many factors are issuer-specific, and 
many more are based only on sec-
tors, rather than on a combination of sectors and ratings.
These factors are subject to 
change. Updates are available on the Fixed Income Local Market 
Factors list at
http://www.barra.com/support/models/fixed_income/
local_markets.asp.

---
## Page 91

Chapter 6
Spread Risk Modeling77Data Acquisition 
We obtain daily bond price, term , rating, and sector data for cor-
porate bonds issued in the U.S.  dollar, yen, sterling, and euro 
markets.
Factor Return Estimation
We calculate monthly credit spread factor return series as 
weighted average changes in spreads  for bonds present in a partic-
ular sector-by-rating category at both the start and end of each 
period.1 When fewer than a minimum number of bonds are avail-
able in a category, we proxy the return for that sector-by-rating 
bucket with the aggregate spread return for all bonds with the same rating, independent of sector.
Covariance Matrix Estimation
The covariances of risk factors are based on the historical factor- 
return series. The credit factor covariance forecasts are con-
structed market by market. We separately estimate local covari-
ance matrices for the U.S. dollar, sterling, euro, and yen credit factors. We obtain the correlatio ns between factors in different 
local markets with Barra’s global integration method.
2
Exponential Weighting
Since local market factor  volatilities change ov er time, we use an 
exponential weighting scheme that attaches greater importance to 
recent events than to older ones. Older returns are weighted by a coefficient, λ
n, where n is the age of the return in months. The 
value of n is such that λn= ½ is the half-life of the weighting 
scheme. The mathematical relationship between λ and n is given 
as:
(EQ 6-2)
1.  The average is duration weighted. 
2.  For more information on the integr ation method, see Chapter , “Integrated 
Risk Modeling,” starting on page 109.Detailed Credit Spread
Model Estimation Process: 
U.S., U.K., Japan, and EMU
1. Data acquisition
2. Factor return estimation
3. Covariance matrix 
estimation
4. Model updating


---
## Page 92

Barra Risk Model
Handbook78The local market factor return s are weighted with a 24-month 
half-life.1 This value was chosen on the basis of the results of out-
of-sample testing.
Factor Exposure Calculation
A bond is exposed to one of the sector-by-rating credit spreads if 
all of the following conditions are satisfied:
■The bond is denominated in U.S. dollar, U.K. sterling, Euro-
pean euro, or Japanese yen.
■The bond’s sector and credit ra ting match a spread sector and 
rating within the applicable local-market factor block.
■The bond is not exposed to  an emerging-market spread.
The exposure of a cred it instrument to the fa ctor with matching 
currency, sector, and rating is spread duration. Mathematically, 
spread duration is given by the following formula:
(EQ 6-3)
where
Emerging-Market Risk Modeling
Much of the debt issued by emer ging-market sovereigns and com-
panies is denominated in currenci es of developed markets such as 
the U.S. dollar, sterling, yen, and euro. The dominant source of 
risk for these bonds tends to come  from the creditworthiness of 
the issuer and not from the local market interest rate factors indi-
cated by the currency of the bond.
1.  This corresponds to a weight multiplier λ=0.51/24 or 0.9715.Pdirty = dirty price of bond
Sspr = parallel spread shift


---
## Page 93

Chapter 6
Spread Risk Modeling79For each emerging market, there is  a single, global emerging-mar-
ket spread factor. This means that there are not, for example, sep-
arate factors for Nigerian bonds issued in U.S. dollars and 
Nigerian bonds issued in British st erling. The effect of the credit 
quality of the issuer dominates any distinction one might make 
between the developed-market currencies in which the bonds 
could be denominated.
Consider for example an Argentine corporate bond issued in ster-
ling. It will be exposed to the lo cal U.K. interest rate factors, the 
U.K. swap spread fact or, the currency factor, and the Argentine 
emerging-market spread factor. 
Model Structure
The emerging-market factor block forecasts risk for bonds issued 
in an external currency (primarily , U.S. dollar and euro) by an 
emerging-market sovereign or corp oration. As with the detailed 
credit spreads, emerging-market sp reads are measured relative to 
the swap curve. 
As of June 2003, the block is composed of 26 factors, one for 
each emerging market. We estima te the emerging-market block 
separately from other factors an d rely on high-frequency data. 0500100015002000
ARG BUL CHN COL ECU HUN LBN MEX NGA PER POL THA VENAnnualized Volatility (bps
7/31/2000 7/31/2001Annualized Volatility (bps)Figure 6-5
Volatility Levels in Emerging 
Markets 
The spread of emerging-market 
bonds has both hi gher volatility 
and greater variability of volatility 
than investment-grade corporate 
and developed-market sovereign bonds. 
For example, during the period of 
July 31, 2000, to July 31, 2001, the Ecuadorian sucre (ECU) was 
dollarized and macroeconomic 
conditions improved. The resulting large decrease in volatility is obvi-
ous. In contrast, the volatility in 
Argentina (ARG) increased after continuing political and social 
pressures.

---
## Page 94

Barra Risk Model
Handbook80Data Acquisition and Fa ctor Return Estimation
The changes in the weekly stripped spread1 levels (which are ven-
dor-supplied2 basic market data) provide the weekly return history 
of the risk factors. 
Covariance Matrix Estimation
Stripped-spread factor s for emerging-market bonds, like the cur-
rency factors, can be quite volati le and tend to exhibit variable 
volatility over time.
The factor return variance and covariance estimates, which are 
based on weekly data, are weight ed exponentially with an eight-
week half-life.3 Next, the exponentially weighted variance and 
covariances are time-scaled to a one-month horizon. They are multiplied by a weekly-to-mo nthly conversion constant
4 (52/12). 
The block is subsequently integrated into the risk model.
1.  A bond’s stripped spread is calculat ed by stripping or subtracting the present 
value of the collateralized cash flow (e scrowed interest payments and collater-
alized principal). The adju sted price is then equate d to the remaining non-col-
lateralized cash flows, which is discounted  at a spread over the base curve. This 
constant spread over the default- free curve is the stripped spread.
2.  The J.P . Morgan EMBI Global is an index of dollar-denominated government 
debt from 26 markets. The index includ es both collateralized restructured 
(Brady) debt and conventional nonco llateralized bonds. For more informa-
tion on J.P . Morgan’s spread estimation methodology, see Introducing the J.P . 
Morgan Emerging Markets Bond Index Global  (August 3, 1999), available from 
J.P . Morgan.
3.  The eight-week half-life was chosen  on the basis of out-of-sample tests.
4.  The numbers in the conversion constant, 52 and 12, are respectively the num-
ber of weeks and months in a year.Emerging Market 
Model Estimation Process
1. Data acquisition and factor 
return estimation
2. Covariance matrix 
estimation
3. Model updating

---
## Page 95

Chapter 6
Spread Risk Modeling81 
Factor Exposure Calculation
An emerging-market bond issued in an external currency is 
exposed to the spread indicated by  the issuer. The exposure is the 
bond stripped-spread duration.1 This is expressed as:
(EQ 6-4)
where
Updating the Model
We estimate the latest month’s fact or returns with the most recent 
market data. We use monthly fa ctor return data for the swap 
1.  Stripped-spread duration is the exposu re of a bond to the credit spread. It 
takes into account any collaterization.Pdirty = dirty price of bond
Sspr = parallel stripped spread shift
Latin America
Africa
Eastern Europe and Russia
Latin America ex Ecuador
Asia
SwapJun 1999
Dec 1999
Jun 2000
Dec 20001200
1000
800
600
400
200
0Annualized Volatility (bps)Figure 6-6
Annual Volatility Forecasts for Dif-
ferent Regions of the EMBI Glo-bal 
Realized volatility was fairly stable 
from June 1999 to December 2000 in Asia, less so in Africa. It 
declined by roughly a factor of 
two in Latin America (because of 
Ecuador) and a factor of four in 
Eastern Europe and Russia. The eight-week half-li fe is considerably 
shorter than the time scale of vol-
atility decrease in these markets, so the risk forecasts have only 
slightly lagged the changes in the 
markets.


---
## Page 96

Barra Risk Model
Handbook82spread and detailed credit market spread, and weekly factor return 
data for the emerging-market spre ad. We update the covariance 
matrix with these factor returns every month. 

---
## Page 97

Chapter 7
Specific Risk Modeling837. Specific Risk Modeling
Common factors do not completel y explain asset return. Return 
not explained by the common factors—shift-twist-butterfly and 
spread factors—is called specific return . The risk due to the 
uncertainty of the specific return is called specific risk . Specific 
returns of bonds from different issuers are assumed to be approxi-
mately uncorrelated with one another, as well as with common 
factor returns. 
Specific risk tends to be relati vely small for government, agency, 
and high-quality corporate bonds.  For corporate bonds, specific 
risk includes event risk , which is the risk that a company’s debt 
may be repriced due to real or perceived changes in the company’s business fundamentals. This compo nent of risk can be rather 
large for bonds with low credit quality.
We forecast specific risk with three models: a heuristic model for 
sovereign bonds, a heuristic model for corporate bonds, and a transition-matrix-based model for bonds in U.S. dollar, sterling, 
and euro markets. 
Heuristic Models
Except for the U.S. dollar, ster ling, and euro corporate markets, 
all markets—including the yen, U.S. agency, and mortgage-
backed security (MBS) market s—use the heuristic models. 
The heuristic model for sovereign bonds has only one parameter 
to account for sovereign market ris k. The heuristic model for cor-
porate bonds has an additional  parameter to account for the 
credit riskiness of the corporat e issuer. The heuristic models 
assume that specific risk of the bond is proportional to spread duration. 
Data Acquisition
We obtain the terms and conditions (TNC) and the daily price 
data on sovereign and corporate bo nds issued in 25 domestic mar-Heuristic Model Estimation 
Process
1. Data acquisition2. Specific risk estimation
a. Sovereign parameter 
determination
b. Corporate parameter 
determination
3. Model updating

---
## Page 98

Barra Risk Model
Handbook84kets, inflation-protected bonds (I PBs) issued by four sovereigns,1 
as well as agency bonds and MB S generics issued in the United 
States. The option-adjusted spre ads (OAS) for all bonds and MBS 
generics are calculated using local market term structure and daily 
prices. 
Sovereign, U.S. Agency, and MBS Specific Risk Estimation
Underlying the model of specific risk of domestic government 
bonds, U.S. agency bonds, and U. S. MBS is the assumption that 
specific risk is constant  across assets of the same class, and can be 
captured by a single parameter.  Expressed as price return,2 specific 
risk is:
(EQ 7-1)
where
The parameter ba is the standard deviation of the specific spread 
returns of bonds of a given class or a given market. A different ba 
is calculated for each market or asset class. U.S. agency bonds, 
U.S. MBS, and sovereign bonds of 25 domestic markets would 
each have a different value for ba . The parameter incorporates his-
torical information using an expo nential weighting scheme with a 
24-month half-life.
1.  We collect daily price data on IPBs issued by the governments of the United 
States, Great Britain, Canada, and France.
2.  Price return is related to spre ad return through spread duration:
, where rprice is the price return variance due to spread 
change, rspr is the spread return, and Dspr is the spread duration.σi = monthly specific risk of bond i
Di = spread duration of bond i
ba = monthly specific-return risk parameter for 
asset class a or domestic market a


---
## Page 99

Chapter 7
Specific Risk Modeling85 
Corporate Bond Specific Risk Estimation
For non-government bonds outside the U.S. dollar, sterling, and 
euro markets, an extended issue- specific risk model is used. A sec-
ond term is added to address the additional risk surrounding 
credit events. Expressed as return volatility, this specific risk is: 
(EQ 7-2)
where
σi = monthly specific risk of corporate bond i
Di = spread duration of bond  i
ba = constant spread return risk for government 
bonds in domestic market a
ca = constant to account for additional specific 
spread return volatility of corporate bonds in 
market a
si = OAS of bond i020406080100120140
Basis Points per YeaAustraliaAus
tria
BelgiumCanada
Denmark
FinlandFranceGreece
GermanyJapanNew ZealandNorwayPortugalSouth
 Africa
SpainSweden
Switzerland
United Kingdom
EMUIrelandItalyNetherlands
United StatesNew ZealandBasis Points Figure 7-1
Monthly Specific Risk Forecasts 
for Five-Year Duration Government 
Bonds
The forecasts have a monthly hori -
zon and are reported in annual-
ized terms.


---
## Page 100

Barra Risk Model
Handbook86In the estimation of ca, ba is considered to be a constant baseline 
of volatility. The ca parameter is then scaled by OAS for the same 
reason that the OAS is used to  scale the swap spread exposure. 
The premise is that the specific  return volatility  of corporate 
bonds is proportional to the OAS level. Bonds with lower credit 
ratings are subject to higher spreads and greater volatility.
The constants b and c are fitted with a maxi mum likelihood esti-
mation. 
Transition-Matrix-Based Model 
For the U.S. dollar, sterling, and e uro credit market s, a more elab-
orate model of specific risk is used . We estimate the specific risk 
with rating spread level difference s and with a rating transition 
matrix, whose entries are probabil ities of bonds migrating from 
one rating to anothe r (from AAA to BB, for example) in a month. 
We compute the rating spread leve ls from averages of OAS values 
of bonds bucketed by  market and rating. 020406080100120140160180
Australia
Canada
EMU
Japan
Switzerland
United Kingdom
United StatesBasis Points per Yea
Domestic Government Eurobond or CorporateBasis Points Figure 7-2
Monthly Specific Risk Forecasts 
for Five-Year Duration Bonds
The graph gives a comparison 
between specific risk forecasts for domestic government bonds and 
other bonds denominated in the 
same currency.
Transition-Matrix-Based 
Model Estimation Process
1. Data acquisition
2. Transition matrix generation3. Rating-specific spread level 
calculation
4. Credit migration forecasting
a. Spread migration 
estimation
b. Recovery rate estimation
5. Model updating

---
## Page 101

Chapter 7
Specific Risk Modeling87Data Acquisition
We obtain bond data from data vendors and historical average 
issuer credit migration matrices  from credit rating agencies.1 
Transition Matrix Generation
Historical credit migra tion rates determine a transition matrix , 
whose entries are estimated probab ilities of bonds migrating from 
one rating to another over a one-year horizon.
Next, we standardize and analyze the data for inconsistencies. 
First, any firm that transitions to “non-rated” is removed and the 
matrix elements are rebalanced so  that each column once again 
sums to 100%. Next, we resolve inconsistent ranking data and 
obtain an improved estimate of the true transition matrix.2 The 
transition matrix is finally scal ed to a monthly horizon according 
to the formula:
(EQ 7-3)
where 
In Equation 7-3, the matrix expo nential and logarithm are power 
series of matrix multiplications. Fo r example, as long as the right-
hand side of the equation is  defined and converges, the log Λ1 is 
given by:
1.  We obtain annual repo rts showing historical rating changes of issuers from 
credit rating agencies. The rating agen cies monitor business  fundamentals in 
relation to a firm’s debt payment obliga tions. They assign debt ratings based 
on their estimate of the li kelihood of repayment. Ev ent risk includes, but is 
not limited to, occurrences that may caus e rating agencies to change the issu-
er’s debt rating. 
2.  The best transition ma trix is determined by leas t-square minimization. The 
valid matrix closest to the or iginal matrix is selected.Λt = transition probability matrix for horizon t
t = horizon (in years)
G =l o g  Λ1


---
## Page 102

Barra Risk Model
Handbook88(EQ 7-4)
Underlying the model is the Mark ov assumption that the proba-
bility of a firm’s rating change de pends only on its current rating, 
not on its history.1 
Rating Spread Level Calculation
If past experience of rating chang es is a reasonable forecast of 
their future likelihood, then the transition matrix and the esti-
mates of rating spreads can be used  to forecast the contribution of 
changes in credit quality to the volatility of bond spread returns. 
To forecast the risk associated wi th rating migration, the size of 
the impact that a rating change ha s on spread level is estimated. 
To estimate the spread level, bo nds are grouped by rating and 
market on each analysis date. The  spread level is the average 
spread over the benchmark curve of all the bonds within each rat-ing group. This is simply: 
(EQ 7-5)Initial Rating
AAA AA B BBB BB B CCCFinal RatingAAA 99.36 0.05 0.04 0.02 0.02 0.02 0.02
AA 0.61 99.28 0.21 0.02 0.01 0.01 0.00
A 0.02 0.61 99.24 0.49 0.03 0.03 0.03
BBB 0.00 0.04 0.45 98.94 0.07 0.13 0.13
BB 0.00 0.00 0.04 0.45 98.33 0.58 0.15
B 0.00 0.00 0.02 0.06 0.78 98.36 11.73
CCC 0.00 0.00 0.00 0.00 0.11 0.44 96.22
D 0.00 0.00 0.00 0.01 0.05 0.44 2.28
1.  For details on Markov’s “memory-less process,” see D.R. Cox and H.D. Mill-
er, The Theory of Stochastic Process  (London: Chapman & Hall, 1965).
Table 7-1
The Resulting One-Month Transi-
tion Matrix for Corporate Bonds
 

---
## Page 103

Chapter 7
Specific Risk Modeling89where 
 
 wi = bond weights
Srating, i = OAS of bond  i with a given rating in a given 
market 
-500050010001500200025003000
Jun-94
Oct-95
Mar-97
Jul-98
Dec-99
Apr-01
Sep-02Basis Point sCCC
B
BBBBB
AA
AAAABasis PointsFigure 7-3
U.S. Dollar Rating Spreads to 
Swap
A time series of rating spread lev-
els for U.S. dollar-denominated 
bonds shows that the average 
spread for a bond below invest-ment grade dwarfs the invest-
ment-grade spreads.
-50050100150200
Jun-94
Oct-95
Mar-97
Jul-98
Dec-99
Apr-01
Sep-02Basis Point sBBB
A
AA
AAABasis PointsFigure 7-4
U.S. Dollar Investment-Grade Rat-
ing Spreads to Swap (Magnified) 

---
## Page 104

Barra Risk Model
Handbook90 
The difference between rating spre ad levels gives a measure of the 
impact of a given rating change on spread. For ex ample, an esti-
mate of the spread change for a bo nd initially rated AAA and then 
downgraded to AA is computed as the difference in the AAA 
spread level and the AA spread level. 
If the rating at the final period is different from the one at the 
initial period, one can forecast th at the spread of the bond will 
have changed significantly as we ll. The spread changes are zero 
when the initial and final ratings agree; they are negative if the 
initial rating is higher than the final rating. Rating Spread Level
AAA 23
AA 45A7 9
BBB 146
BB 313B 687
CCC 1919Table 7-3
U.S. Dollar Rating Spread Levels, 
March 31, 2001 (in Basis 
Points)
Spreads increase as credit quality 
diminishes.
-2500-2000-1500-1000-50005001000150020002500
Initial RatingBasis Point s
AAA AA ABBB BB BCCCAAA AA A BBB BB B CCC
Final RatingBasis PointsFigure 7-5
Returns Generated by Spreads
The chart shows typical rating 
spread return values for the U.S. corporate market. 

---
## Page 105

Chapter 7
Specific Risk Modeling91Credit Migration Forecasting
The credit migration model predicts that specific risk of corporate 
bonds arises primarily from events affecting the issuer’s credit 
quality. The impact of such events on return is assumed to be per-
fectly correlated for all the bonds of an issuer. To calculate the 
risk, we aggregate the issuer’s bonds to form a subportfolio, then 
the impact of various credit migrati on events on the subportfolio 
is calculated. 
The approximate return variance for a bond due to credit migra-
tion is expressed as:
(EQ 7-6)
where
The formula has two main compo nents. The first component 
accounts for credit migration from  one rating to another. The sec-
ond accounts for default. The pa rameter depends on the recovery 
rate and the curren t market value. σ2
credit = price return variance due to spread change or 
default
Λfi = probability of bond ra ting transition from i 
to f
Dspr = the aggregate spread duration of all bonds 
from a given issuer in the portfolio
sf = final spread level (the final rating) 
si = initial spread level (the initial rating)
= mean price return due to spread change or 
default 
Λdi = probability of a transition from i to default
R = recovery rate in default


---
## Page 106

Barra Risk Model
Handbook92The default recovery factor, R, is the fraction of the value of the 
bond that would be recovered in the event of default. If R were 1, 
then 100% of the bond’s value would be recovered, and this com-
ponent would have no effect. The recovery rate is uncertain and situation dependent. However, studies by Moody’s have shown 
that a typical recovery rate for senior debt is roughly 50%. The 
recovery value has only a small impact on the risk forecast for 
investment-grade bonds, but the recovery model may have a pro-
nounced impact on bonds that are below investment grade. 
In practice, the effect of the me an price return term, , is negli-
gibly small. This allows a simpler form of the equation:
(EQ 7-7)
Using this form, the two terms of the formula,
 and , 
can be computed separately each month and stored for use in the 
application. The seven different ratings1 in the model give seven 
aj parameters and seven bj parameters. 
So, the specific risk of a bond wi th a particular rating is given by:
(EQ 7-8)
Due to the dependence of σ2
credit on current spread levels, the 
credit risk formula is very respon sive to changes in market expec-
tations. In circumstances where low-grade credit spreads signifi-
cantly widen relative to high-grade ones (due perhaps to expectation of increased default risk), the credit risk forecast 
would increase immediately by a corresponding amount. 
In the parametric context, the main difference in calculation 
method between the empirical sp ecific risk for sovereign bonds 
and the specific risk due to credit  migration for corporate bonds is 
that the contributions of the former add independently (that is, 
are diversified) at the security le vel, while the contributions of the 
latter add independently at the issuer level.
1.  The seven ratings are: AAA, AA, A, BBB, BB, B, and CCC.


---
## Page 107

Chapter 7
Specific Risk Modeling93Figure 7-6 and 7-7 show a history of credit risk forecasts using 
the transition-matrix approach. Note  that the risk values have 
been converted from price-return risk to spread-return risk by 
dividing by spread duration. 
 Figure 7-6
Credit Risk Forecasts for a U.S. 
Dollar-Denominated Five-Year Duration Bond, by Rating, Based 
on the Transition Matrix (AAA to 
BBB)
Sharp jumps in risk forecasts for 
all rating classes are apparent in 
the credit crash of mid-1998, due to the significant widening of 
spreads.
020406080100120140
January-97 January-98 January-99 January-00Credit Risk Forecast (bps )BBB
A
AAAAATreasuryCredit Risk Forecast (bps)
0100200300400500600700800900
January-97 January-98 January-99 January-00Credit Risk Forecast (bps )
CCC
B
BBCredit Risk Forecast (bps)Figure 7-7
Credit Risk Forecasts for a U.S. 
Dollar-Denominated Five-Year Duration Bond, by Rating, Based 
on the Transition Matrix (BB to 
CCC).

---
## Page 108

Barra Risk Model
Handbook94 
An interesting observation from this  table is that the classification 
of issuers into investment (BBB an d above) and speculative grade 
(below BBB) neatly corresponds to the split between bonds whose 
common factor and credit risk are ea ch less than their interest rate 
risk, and those for which they ar e greater. That is, the common 
factor and credit risks for rating s of BBB and above are all less 
than the 82 basis points of risk du e to spot rate volatility, while 
those of lower-grade bonds are above th is level. Interest rate risk is 
dominant for investment-grade bo nds while credit risk is domi-
nant for high-yield bonds. 
Updating the Model 
The specific risk parameters for the heuristic models and the tran-sition-based models are calculated monthly. Type of Issue Common Factor 
RiskSpecific/Credit 
Risk
Treasury/Spot 82 8
Agency 15 14AA 22 18A2 2 3 3
BBB 34 79
BB 92 155B 164 287
CCC 296 582Table 7-6
Model Forecasts as of January 
31, 2000 
The forecasts are expressed as 
annualized standard deviation of 
interest rates or spreads. For the 
rating-based credit risk forecasts, a spread duration of five years is 
assumed. The first column shows 
average factor volatility forecasts for factors in different groups. The 
second column shows the specific 
or credit risk forecast for a single 
security.

---
## Page 109

Section FourCurrency Risk
Section Four discusses the extensive, 
detailed process of creating Barra 
currency models.
Chapter 8: Currency Risk Modeling

---
## Page 111

Chapter 8
Currency Risk Modeling978. Currency Risk Modeling
The fluctuation of currency exchange rates is a significant source 
of risk faced by in ternational investors.1 Consider a Norway-
based investor with a portfolio of U.S. treasuries. U.S. treasuries 
belong to the U.S. dollar local market and their interest rate risk comes from changes in U.S. T reasury rates, yet our Norwegian 
investor is still subject to the ri sk that comes from changes in the 
U.S. dollar/Norwegian kroner exchange rate.
Often, more than half the variation  of a well-diversified portfolio 
of global equities or investment-grade bonds can be attributed to 
currencies. Consequently, for an  international investor making 
currency bets or trying to hedge cu rrency risk entirely, it is essen-
tial to have accurate and reliab le risk forecasting models that 
include currency risk. 
Model Structure
Because currency risk is time se nsitive, the variances and covari-
ances of currency factors are es timated using high-frequency data 
and models with short memories . The correlations between cur-
rencies are derived from weekly da ta weighted exponentially with 
a 17-week half-life. A GARCH (1,1) model based on daily data is 
used to forecast currency volatility.
Since currency risk must be integr ated with other sources of risk, 
Barra also estimates co variances between currency factors and all 
other Barra risk factors. And becaus e most Barra factor returns are 
based on monthly data, these “cross-block” covariances are based 
on monthly data as well.2 
1.  For related discussions, see the Barra Research article, “Forecasting Currency 
Return Volatility.” It is av ailable at http://www.barra.com.
2.  Covariances between factors with diff erent frequencies are constrained by the 
coarser time resolution.

---
## Page 112

Barra Risk Model
Handbook98Data Acquisition and Return Calculation
The first step in model estimati on is acquiring daily currency 
prices for more than 50 currenci es from data vendors. The incep-
tion dates of the histories vary  from January 1973 to July 2002, 
but, for most currencies, Barra ha s historical data dating from the 
early 1980s. The exchange rates are not consistent across vendors 
due to discrepancies in sampling time. 
The returns are then calculated with:
(EQ 8-1)
where
Currency exchange rates are quoted  in U.S. dollars per local cur-
rency. In these terms, a positive return means that the local cur-
rency became stronger rela tive to the U.S. dollar. 
Estimation of the Covariance Matrix
The Barra currency risk factor block is a combination of two 
models: a correlation model and a volatility model. We use weekly 
returns to estimate correlations between currencies and daily data 
to estimate currency  volatilities. We generate the covariance 
matrix used to forecast risk with both models.
The final covariance matrix is formed with:
(EQ 8-2)
wherert = return at time t
Pt+1 = current spot exchange rate 
Pt = previous exchange rate
Correlation (i,j) = correlation estimate of  weekly currency data
Model Estimation Process
1. Data acquisition and return 
calculation
2. Estimation of covariance 
matrix:
a. Correlationsb. Volatility forecasts: 
GARCH (1,1) or IGARCH 
3. Time-scaling 
4. Model updating


---
## Page 113

Chapter 8
Currency Risk Modeling99Currency Correlation Model
The correlation matrix is estimate d using weekly currency return 
data1 relative to the U.S. dollar, exponentially weighted with a 
half-life of 17 weeks. This half-lif e is fitted with a maximum like-
lihood estimation2. σk = GARCH volatility estimate based on daily 
return
1.  Barra uses weekly data instead of daily data to avoid spurious correlations. 
Besides being less volatile , weekly data allows Barr a to compare different mar-
kets with various local holidays and different opening and closing times. 
2.  Maximum likelihood estimation (MLE ) estimates the parameter values that 
make observed data most likely, given a choice of parame tric distribution. 
Figure 8-1
Currency Covariance Matrix
The diagonal elements in the 
covariance matrix are the cur-
rency variances, while the off-
diagonal elements are the covari-ances between currencies.
Figure 8-2
Currency Correlation 
The weekly currency return data is used to estimate correlations 
between currencies.

---
## Page 114

Barra Risk Model
Handbook100Currency Volatility Model
Currency volatility levels behave like many other economic time 
series in that they vary  dramatically over ti me. Changes in volatil-
ity range from gradual to abrupt.
General auto-regressive condi tional heteroskedastic (GARCH) 
models are standard tools used to forecast risk for variable volatil-
ity time series.1 
Barra’s currency risk factor  block uses a GARCH (1,1) model2 for 
currencies against the U.S. dollar. The curr ency model directly 
incorporates the previous variance  forecast and squared return. 
The optimal GARCH parameters for each currency are fitted with 
maximum likelih ood estimation. 
An underlying assumption of th e GARCH (1,1) model is that the 
currency returns have an uncond itional variance. For currencies 
whose returns against the dollar do not exhibit an unconditional 
variance, we use a degenerate form for GARCH (1,1) known as 
integrated GARCH. 
GARCH (1,1) Model
When properly calibrated, a GARCH (1,1) model responds quickly to new information. Daily da ta are used in order to facili-
tate convergence of GARCH parameters and to minimize stan-
dard errors. Daily exchange ra te data are available for all 
currencies.
The functional form of the GARCH (1,1) model is:
1.  For more informatio n on GARCH models, see Covariance Matrix Scaling: 
Computing Market Volatility  on page 29.
2.  A GARCH ( p,q) model has terms that depend upon the previous p forecasts 
and q squared returns.Figure 8-3
Currency Volatility 
Currency volatility is stripped from 
the weekly covariance matrix, 
then implemented with GARCH to refine daily volatility forecasts. 
These volatility forecasts (black) 
are later overlaid on the covari-ance matrix (gray).


---
## Page 115

Chapter 8
Currency Risk Modeling101(EQ 8-3)
where 
and 
The formula has three parameters. The unconditional variance of 
the series is denoted by ω2. If no new information arrives, the 
variance forecast tends to revert to this value. The sensitivity con-stant γ measures responsiveness to  the most recent (squared) 
return. The persistence constant β
 measures the importance of the 
previous forecast in the current forecast.
The parameters β and γ must be positive, or else the variance 
forecasts could become negative in response to a sequence of large 
events. Similarly, β+γ >1 could lead to a nega tive variance fore-
cast in the wake of a long seque nce of relatively small events. The 
special case where β+γ =1 leads to a degenerate form of the 
GARCH(1,1) model known as an integrated GARCH (IGARCH), which is an exponentially weighted model. = conditional variance forecast for time t
ω
2= unconditional variance forecast
β = persistence constant
= variance forecast for the previous period
γ = sensitivity constant
= previous period squared return
β > 0
γ > 0
β + γ < 1


---
## Page 116

Barra Risk Model
Handbook102IGARCH Model (Exponentially Weighted)
The case where β+γ=1 is commonly referred to as an integrated 
GARCH (IGARCH). This model fits a series with variable volatil-
ity but no uncond itional variance.1 Replacing γ with 1– β yields a 
single parameter:
Repeated substitutions for  yields:
(EQ 8-6)
In other words, the ith term in the series is  multiplied by the con-
stant (1– β )β i–1. The weighting scheme ca n also be specified by 
its half-life. 
Volatility Across Markets
Monthly risk forecasts for variou s markets show the relationship 
between sensitivity ( γ), persistence ( β), and currency returns. 
The higher the value for γ, the more responsive a currency is to 
recent events. If β is higher, more weight is given to past events. 
Figure 8-4 through 8-8 show Barra currency risk forecasts and 
monthly currency returns for the U. S. dollar against a variety of 
other currencies. The circular plot points show the ±1 standard 
deviation risk forecasts. The da rk lines with square plot points 
show the monthly returns. The assumption of conditional nor-
1.  Note that ω2 drops out of Equation 8-3 when β+ γ =1.(EQ 8-4)
(EQ 8-5)


---
## Page 117

Chapter 8
Currency Risk Modeling103mality suggests that we should see roughly two-thirds of the 
returns between the ±1 standard  deviation risk forecasts. 
 -8.00-6.00-4.00-2.000.002.004.006.008.00
Jun-94
Oct-95
Mar-97
Jul-98
Dec-99
Apr-01Percent
Return RiskFigure 8-4
Euro Model
The chart depicts monthly risk and 
returns of the U.S. dollar against 
the euro.
ω2 = 8.81%; β = .97; γ = .024
-15.00-10.00-5.000.005.0010.0015.0020.00
Jun-94
Oct-95
Mar-97
Jul-98
Dec-99
Apr-01Percent
Return RiskFigure 8-5
Japanese Yen Model
The chart depicts monthly risk 
and returns of the U.S. dollar 
against the yen.
ω2 = 11.34%; β = .96; γ = .03
The yen model has a higher 
unconditional volatility (11.34% 
annualized) than the euro (8.81%) and is slightly more reactive.

---
## Page 118

Barra Risk Model
Handbook104 
 Figure 8-6
South African Rand Model
The chart depicts monthly risk 
and returns of the U.S. dollar 
against the South African rand.
ω2 = 9.97%; β = .711; γ = .272
The sum  β+γ is quite close to 
1. This means that this GARCH model is nearly degenerate . Since 
it closely resembles an IGARCH 
model, the long-term variance plays only a little role in the fore-
cast. As 
γ is relatively large 
(.272), the forecasts are very reactive .-20.00-15.00-10.00-5.000.005.0010.0015.00
Jun-94
Oct-95
Mar-97
Jul-98
Dec-99
Apr-01Percent
Return Risk
-10.00-8.00-6.00-4.00-2.000.002.004.006.00
Oct-95
May-96
Dec-96
Jun-97Jan-98
Jul-98
Feb-99
Aug-99
Mar-00
Oct-00Percent
Return RiskFigure 8-7
Polish Zloty Model
The chart depicts monthly risk 
and returns of the U.S. dollar 
against the Polish zloty.
β = .972; half-life = 24 days
The risk and return plot of the 
Polish zloty has an IGARCH 
model with a 24-day half-life.

---
## Page 119

Chapter 8
Currency Risk Modeling105Time-Scaling Currency Risk Forecasts
The daily currency forecasts ar e time-scaled to conform with 
other Barra risk forecasts, which are based on a monthly horizon. 
For GARCH (1,1), this is accomplis hed with an aggregation for-
mula that takes the variance reversion into account. Conditional 
on today’s information, GARCH (1,1) forecasts for the next n 
periods are calc ulated with:
(EQ 8-7)
The value of n is usually 20 or 21, which is the number of busi-
ness days in a month. Note that if the single-period current fore-cast is close to the unconditional forecast ω
2, the n-period current 
forecast is close to nω2. Similarly, if β+γ<1, the n-period forecast 
quickly leans towards nω2.
Integrated GARCH models have no variance reversion. The n-
period forecast is equal to the one-period forecast scaled by n.
(EQ 8-8)Figure 8-8
Canadian Dollar Model
The chart depicts monthly risk 
and returns of the U.S. dollar against the Canadian dollar.
ω2 = 4.53%; β = .321; γ = .192
The risk forecast for the Canadian 
dollar is nearly flat and equal to the unconditional volatility. Here 
β+γ sum to much less than 1, 
resulting in forecasts that are nearly constant at the level of 
unconditional volatility.-4.00-3.00-2.00-1.000.001.002.003.004.00
Jun-94
Oct-95
Mar-97
Jul-98
Dec-99
Apr-01Percent
Return Risk


---
## Page 120

Barra Risk Model
Handbook106Updating the Model
The currency risk model is upda ted monthly to incorporate the 
latest currency exchange rate volatility estimates. 

---
## Page 121

Section FiveIntegrated Risk
Section Five discusses the innovative 
methods used to couple broad asset 
coverage with detailed analysis of 
single markets.
Chapter 9: Integrated Risk Modeling

---
## Page 123

Chapter 9
Integrated Risk Modeling1099. Integrated Risk Modeling
Barra’s chief goal is to provide a single model that best forecasts 
the risk of a wide range of port folios, from those concentrated in 
a single market to those diversifie d over multiple assets across dif-
ferent markets. The model must o ffer both in-depth analysis and 
broad coverage. It should be detailed enough to allow portfolio 
managers to drill down to their assets in a local market and 
obtain an insightful and accurate  analysis, and yet broad enough 
to let plan sponsors have a high-lev el view of risk that they face 
across multiple market s and asset classes. 
Unfortunately, these objectives ar e conflicting. As new markets are 
added to a global model, the complexity needed to maintain a fine level of detail increases, posing a serious econometric chal-
lenge. Until now, this goal has been elusive.
Model Integration Overview 
We employed a novel methodology to  achieve this goal. First, to 
provide the needed level of detail, we use Barra factor models of 
all the local equity an d fixed-income markets.1 These models 
attribute the expl ainable portion of an asse t’s return to the local 
factors at work in each market . The factors, which may differ 
from market to market, include risk indices and industries for 
equities and interest-rate term structure movements and credit 
spreads for fixed-income securi ties. By modeling each market 
individually, we enable investors to see their exposures to the risk 
factors of each particular market and to have the most accurate 
forecasts of local market risk.
Next, we combined the local equity models and the local fixed-
income models. Since asset returns are driven, in part, by local 
factors, the key to developing  each model is determining the 
1.  Examples of local models are the Australia Equity Mo del and Japan Bond 
Model. While single-country equity or bond models are possible choices for 
local models, they are not the only poss ible local models. For example, the Eu-
rope Equity Model, a regional model that  covers securities listed in 16 West-
ern European markets, is used as th e local model for the Western European 
markets (except the United Kingdom). 

---
## Page 124

Barra Risk Model
Handbook110covariances between these factors across different markets. The 
excessive number of factors complic ates the estimation of factor 
covariances. Fortunately, within each asset class, a much smaller 
set of global factors accounting for much of the cross-market cor-relation can be identified. By buil ding structural models of how 
these global factors link local fa ctors across markets, more accu-
rate estimates can be obtained.
1
The use of structural models pro vides a new framework for global 
analysis. These models decompose local factor returns into a part 
due to global factors , or factors that are shared across markets, 
and a part due to purely local factors , or factors that only affect 
the securities within each market . This explains, for example, why 
the industry risk of a U.S. bank is better hedged with another U.S. bank than with a Japanese bank.
Finally, the global equity, fixed-i ncome, and currency risk models 
are combined to form the complete Barra Integrated Model 
(BIM). Leveraging our earlier work , we use the global factors to 
estimate the correlation structure across asset classes.
Building Global Asset Class Models
Single-market equity models have  factors that differ in number, 
character, and behavior across markets. For example, the U.S. 
equity market is well characterized  by 13 risk index (or style) fac-
tors and 55 industries, and is significantly concentrated in tech-
nology, finance, and health care. In  contrast, the Au stralian equity 
market can be captured with nine risk index factors and 14 indus-
tries, and is more exposed to basic materials. 
Fixed-income models, on the other hand, are more uniform in 
structure. Each model incorporates three factors to account for interest rate (term structure) movements, and one or more credit 
spread factors.
1.  The term “global” simply refers to the role of these fa ctors in determining 
cross-market covariances. It does not i mply that these factors are applicable to 
all assets. It just means that these are the factors responsible for the global cor-
relation structure of the covariance matrix.Model Estimation Process
1. Local model development2. Equity: Global factor return 
estimationFixed-Income: Local factor 
to global factor exposure 
estimation
3. Covariance matrix 
calculation
a. Estimation of purely 
local covariances for individual markets
b. Calculation of global 
covariance matrix within 
each asset class
c. Calculation of cross-
asset covariances via 
core factors
4. Scaling
a. Scaling to individual 
asset class models
b. Scaling to local markets
5. Model updating

---
## Page 125

Chapter 9
Integrated Risk Modeling111The Structure of Local Models
The local models, which are the building blocks of the global 
model,1 decompose an asset’s local exce ss return into a part due to 
local factors and a part that is unique to the underlying asset, the 
specific return.2 
Let us take Australian equities as  an example. The risk of the 
portfolio is computed with a forecast covariance matrix of Austra-
lian asset returns, Vaus. Using the factor covariance matrix, Faus, 
and the matrix of asset-specific variances, Δaus, the portfolio risk 
can be expressed as:
(EQ 9-1)
Thus, the risk of a portfolio arises from its exposure to factors in the market as well as from the id iosyncratic behavior of individual 
securities it contains.
Aggregating Local Models
Barra Integrated Model is a multip le-factor risk model that gives 
the covariances between returns to equities and fixed-income 
assets in different markets. The fa ctors of this new model are all 
the local market factors. Further, each asset is exposed only to its 
own market’s factors. Using global equities as an example, the fac-
tor XE, factor covariance, FE, and specific matrices, ΔE, of this 
model can be written as:
(EQ 9-2)
1.  For full details on loca l models, see the Equity Risk  Modeling section in this 
book, the appropriate hand book (for example, the United States Equity Risk 
Model Handbook ), or the single market model data sheets.
2.  For equities, the exce ss return of an asset is r–rf, where r is the asset’s total
return and rf is the risk-free rate. For bond s, excess returns are computed as:
, where Pt+1 is the price at time t+1, Pt is the price at time t, and 
Ft+1/t is the forward price for time t+1 computed at time t. Ft+1/t is computed 
using a valuation model.


---
## Page 126

Barra Risk Model
Handbook112The global equity asset covaria nce matrix takes th e familiar form:
(EQ 9-3)
The global fixed income covaria nce matrix takes a similar form:
(EQ 9-4)
Modeling Covariances of Local Factors in Different Markets
To complete the global model, we fully specify the factor covari-
ance matrices FE and FF . The diagonal blocks  of these matrices 
contain covariances between the lo cal factors within each market; 
the local models have already provided these. What remains to be 
specified is the covariance between local factors in different  mar-
kets. This involves estimating a si gnificant number of covariances 
since there are more than 1 ,000 local equity and almost 300 
fixed-income factors. The underlying data is available at monthly intervals and, in many cases, goes back fewer than 15 years.
With such a small sample size comp ared to the number of factors, 
the covariance forecasts will show a large degree of spurious linear 
dependence among the factors. One consequence is that it becomes possible to create portfolio s with artificially  low risk fore-
casts. The structure of these portfolios would be peculiar. For 
example, the forecasts might show an overweight in U.K. AA financials apparently hedged by an underweight in U.S. munis 
and Canadian automobiles.
Rather than computing these cova riances directly, we use a struc-
tural model for each asset class that  establishes a sensible relation-
ship between factors in different ma rkets. In place of local factors, 
we specify a much smaller number of global factors that are 
responsible for the correlations be tween factor groups. The idea is 
that the behavior of local factors may be accounted for, in part, by 
a much smaller set of global fa ctors. This method appreciably 
reduces the degree of spurious li near dependence among the fac-
tors in the covariance matrix.
For example, part of the return to the local U.S. and U.K. oil fac-
tors is due to an underlying glob al oil factor which captures global 
oil prices, cartel activity, and so  forth. In similar fashion, spreads 
on corporate bonds of different credit qualities in the United 
States and United Kingdom are par tly driven by a common spread 


---
## Page 127

Chapter 9
Integrated Risk Modeling113factor for these countri es. These global factor s link local factors 
across markets, accounting for any correlation between them. 
Thus, estimating the covariance be tween such local market factors 
requires a much smaller set of gl obal factor covariances, thereby 
improving the reliabi lity of the estimates.
Implementing Global Factor Models
The global factor models for eq uities and fixed-income securities 
differ in the global fact ors used and the calcul ation of local factor 
exposures to global factors, but the structural models for equities 
and fixed-income securities have the same form:
(EQ 9-5)
where
The structural models not only overcome the econometric prob-
lem, but also provide a new fram ework for global analysis. They 
decompose each local factor return into a part due to global fac-
tors and a part that is purely loca l. These purely local returns are 
not correlated across markets b ut may be correlated within each 
market. This construction allows the factors in different markets 
to be correlated but not identical.
From the structural models, an es timate of the asset class factor 
covariance matrix, , consisting of two parts, can be obtained:
(EQ 9-6)fac = vector of local asset class (that is, E for 
equities, F for fixed-income securities) factor 
returns across all markets
Yac = a matrix of exposures of the local factors to the 
global factors 
gac = a vector of global fact or returns for the asset 
class
φac = a vector of the purely local factor return


---
## Page 128

Barra Risk Model
Handbook114where 
Consistency Between Local Models and Global Model
In building , we simply sought good estimates of the covariance 
between factors in different market s. The factor covariance matri-
ces from the local models, which ha ve the best estimates, form the 
diagonal blocks of Fac. Given that the diagonal blocks of  gener-
ally differ from the target, the last  step is to form the final covari-
ance matrix of all the local factors, Fac, by altering  in Equation 
9-6 so that the local blocks are co nsistent with the local models. 
So, for example, the final covaria nces of local factors for the Aus-
tralian market are the same as those in the Australia Equity 
Model. 
Global Equities 
Barra’s new approach to modeling gl obal equities differs markedly 
from that of most global equity  models, which use a single set of 
factors to characterize the risk of  equities throughout the world.1 
Altogether, Barra uses over 1,000 local factors.Gac = covariance matrix of global factors
φac = covariance matrix of pur ely local factors with φ 
= 0 if i and j are not in the same market
1.  Those models assume th at all equities are driven by exactly one parsimonious 
set of factors, implying that returns due to industries and ri sk indices (styles) 
move in lockstep across markets.Local Equity Factor Average Correlation
Materials 0.42
Finance 0.43
Information Technology 0.46Momentum 0.34
Size 0.18
Volatility 0.43
Table 9-1
Local Equity Factor Correlation in 
Nine Major Markets January 
1990 to April 2002
The average pair-wise correlation 
between the same factors (for 
example, U.S. Size, U.K. Size) in 
nine major markets (Australia, Canada, France, Germany, Italy, 
Japan, Switzerland, the United 
Kingdom, and the United States) shows that both industries and 
risk indices across countries share 
some common behavior. Despite this correlation, however, these 
factors behave significantly differ-
ently from market to market.

---
## Page 129

Chapter 9
Integrated Risk Modeling115Global Equity Factors
The global factors that explain cova riances of equity factors across 
local models are:
■A world factor
■Country factors
■Global industry factors
■Global risk index factors: Price Momentum, Size, Value, and Volatility
The world factor captures the gl obal market return, while the 
industry and country factors reflect the return to global industry 
and country influences net of other factors.
1 These factors were 
selected based on their ability to capture common fluctuations 
across local equity factor returns.
Exposures of Local Equity Fact ors to Global Equity Factors
Each local industry factor has unit  exposure to the world factor, 
gwld, its own country factor, gcnty, and the global industry to which 
it belongs, gind; it has no other global exposures.2 Each local risk 
index factor corresponding to one of the four global styles has unit exposure to that style, g
ri, and no exposure to other factors. 
The other local risk index factor s have no global exposure. 
(EQ 9-7)
(EQ 9-8)
Estimating Returns to Global Equity Factors
A history of returns to global equi ty factors is compiled by fitting 
the structural model in Equati on 9-7 and 9-8 to monthly local 
1.   Both the industry factors and the co untry factors render the world factor re-
dundant, creating what is known as an identification proble m. To resolve this, 
we follow the standard prac tice of requiring a weighted combination of the 
countries and the industry fact or returns to sum to zero.
2.  A local industry factor may, in some cases,  be exposed to more than one global 
industry factor with frac tional weights in each.


---
## Page 130

Barra Risk Model
Handbook116factor returns. The global fact or returns were estimated using 
cross-sectional weighted least s quares regression subject to con-
straints. The estimation incudes the period from January 1984 to 
the present. Because many models did not exist until some time after 1984, proxies replaced thes e missing returns from single 
country index returns whenever possible.
Barra Research Methods
European Equities in BIM
Barra Integrated Model (BIM) uses single-co untry models as the lo cal models for most 
countries. It, however, uses the Europe Equity Model (EUE2) for equities in Western Europe excluding the United Kingdom. 
EUE2 has a structure different from other single-country equity models; in particular, it 
has a set of country factors. To fit EUE2 excluding U.K. into BIM, it is useful to restate the EUE2 factors. We do this by forming single-county models that are based on the EUE2 factors.
Consider France as an example. Its risk indi ces are defined to be the same as EUE2's, 
so that the return to the France Value factor is equal to the return to the EUE2 Value factor, and a French asset's exposure to the France Value factor equals its exposure to the EUE2 Value factor; thus, f
ri,France = fri,EUE2 .
When we construct industries for the France model, we combine the return of the 
corresponding EUE2 Continental industry with the EUE2 France country factor return. As such, the return to the France Automobiles industry is the return to the EUE2 Continental Automobiles industry plus the return to the EUE2 France country factor. In other words: f
industry  findustry,France  = findustry,EUE2  + fFrance_country,EUE2 . A French asset exposed to the 
Continental Automobile s industry is now exposed to th is France Automobiles industry. 
More generally, all assets have unit exposure to their local industries. 
It is important to note that these derived si ngle-country models are completely consistent 
with EUE2. Both models produce exactly the same risk forecasts. 
The 15 EUE2-based single-country models are us ed in the estimation of the global factor 
returns, which are the basis for BIM. The risk  indices and industries from these models 
are exposed to the corresponding global factors in the same way in which other countries' factors are. The factor returns are used in the regression to estimate global factor returns.

---
## Page 131

Chapter 9
Integrated Risk Modeling117Computing Covariances of Global Equity Factors
The covariance matrix of the global equity factors (the Gac in 
Equation 9-6) is computed from historical estimates of the 
returns to these factors. 
The covariance matrix employs an exponentia lly weighted scheme 
with a half-life of 48 months. In other words, this month’s factor return is given twice the weight of one four years ago. The covari-
ance matrix of the purely local pa rt of equity fact or returns, the Φ 
in Equation 9-6, was computed in a similar manner—also using a 
half-life of 48 months.
Scaling to Local Markets
The final step is to apply the sc aling procedure to make the cova-
riance block for each local market match that of the correspond-
ing local model. The result is a model for global equities that 
provides analyses consistent with  the local equity models and at 
the same time forecast s cross-market risk.

---
## Page 132

Barra Risk Model
Handbook118Global Bonds
The approach to building a global fixed-income model parallels 
that of the equities. The global fi xed-income model starts with the 
construction of factor models for each of the local fixed-income 
markets. The factors at work in these local markets include shift, 
twist, and butterfly term struc ture movements (STB) and a swap Barra Research Methods
Missing Data
We often need to estimate variances and covariances directly from data series. Occasions 
for this include estimation of the global fact or covariance matrix within a single asset 
class as well as the co re covariance matrix. 
The series used in these estimations are often incomplete for reasons that include 
differing inception dates of series, data  errors, and local holidays. In these 
circumstances, the most naïve approach—estimating the sample covariance between each pair of factors using the maximum num ber of data points available in the two 
series—may result in a matr ix with negative eigenvalues. A matrix with negative 
eigenvalues cannot be a covariance matrix. The opposite extreme—estimating the sample covariances using only data on dates for which there are no missing values—addresses this issue. It generates a matrix  that is free of negative eigenvalues; however, it introduces 
a new problem: far too mu ch data is discarded.
Our approach is to use the method of max imum likelihood estimati on. Unlike the case 
where the data series are complete, there is no closed-form expression for the maximum. 
Instead, we use a numerical estimation pr ocedure called the Expe ctation-Maximization 
(EM) algorithm
1 that converges to the maximum. EM algorithm —an iterative method for 
estimating the covariance matrix of incomple te data sets and inpu tting missing values—
ensures the creation of a positive semi-definit e factor covariance matrix even when some 
of the factors have in complete histories. 
1.  For details on the Expectation-Maximizati on Algorithm, see Geoffrey J. McLachlan and 
Thiriyambakam Krishnan, The EM Algorithm and Extensions  (New York: Wiley-
Interscience, 1996) or Dempster,  Laird, and Rubin, “Maxim um Likelihood  Estimation 
from Incomplete Data Using the EM Algorithm,” Journal of the Royal Statistical Society, 
ser. B, 39 (1977), 1–38.

---
## Page 133

Chapter 9
Integrated Risk Modeling119spread. Four markets—the United States, the United Kingdom, 
Japan, and the euro zone—have more detailed credit factors that 
explain the spread over swap on th e basis of sector or sector-by-
rating classifications.1 In addition, emer ging-market bonds 
denominated in an external cu rrency have country-dependent 
spreads—one spread for all bo nds from each emerging market—
which allows it to be included in  the global model. Altogether, 
there are over 270 local factors.
Global Bond Factors
The factor model that links local equity models is built first by 
specifying local equity factors’ exposures to gl obal factors, then by 
estimating the returns to  these global factors. In contrast, the fac-
tor model that links local bond mode ls is built first by specifying 
the returns to global factors, then by estimating the exposures of 
each local bond factor to these gl obal factors through time-series 
regressions. 
The global factors that capture covariances in bond factors across 
different local markets are:
■The STB factors from ea ch of the local markets
■The swap spread factor from each local market
■An average credit spread factor for each of the U.S., U.K., 
Japan, and the euro zone markets
■An average emerging-market credit spread factor
■An average U.S. municipal factor
■Shift and, where applicable, twist factors for real interest rates 
in the U.S., U.K., Canada, and euro zone markets
1.  For the purposes of modeling corpor ate bonds, we have a single euro-credit 
model that spans twelve markets. The stru cture of this model is similar to that 
of the other markets, so it makes no re al difference for o ur exposition whether 
we consider the euro zone to be one market or twelve individual markets; we 
will think of it as one.

---
## Page 134

Barra Risk Model
Handbook120STB and Swap Spread Factors
The local term structure and swap  factors are themselves global 
factors as well. By this we mean that no factors act as proxies for 
them in estimating their covariance  with the other local factors. 
Some of these variables are signif icantly correlated  across markets 
and the gain from proxying them wi th a reduced set of variables is 
negligible. 
Credit Spread Factors 
Credit spread factors are strongly  correlated within each of the 
U.S., U.K., Japan, and euro zone markets. The magnitude of the 
correlation can be seen in the following tables: 
 Period Shift Twist Butterfly Swap
Jan 1993 to Apr 2002
Average Correlation
% Significantly Positive 0.42 
80% 0.22 
50% 0.02 
3% 0.09
22%
Jan 1993 to Dec 1996
Average Correlation
% Significantly Positive 0.40 
55% 0.16 
15%0.02 
4% 0.07
14%
Jan 1997 to Apr 2002
Average Correlation 
Significantly Positive 0.45
72% 0.27 
51% 0.04 
9% 0.12
26%
AAA AA A BBB
AAA 0.94 0.83 0.77 0.72
AA 0.88 0.89 0.85
A 0.95 0.92
BBB 0.96
AAA AA A BBB
AAA 0.73 0.59 0.39 0.15
AA 0.63 0.59 0.39
A 0.64 0.62
BBB 0.78Table 9-2
Average Pair-wise Factor Correla-
tions Across Markets
The average pair-wise correlations 
between each of the STB and swap factors across markets and 
the percentage of significant posi
-
tive correlations over different 
time periods clearly show that 
shift and twist, and to some 
extent, swaps are correlated sig-nificantly across markets.
Table 9-3
Average Correlation of U.K. Credit 
Spread Factors from May 1999 to 
April 2002
Table 9-4
Average Correlation of Euro-Zone 
Credit Spread Factors from June 
1999 to April 2002

---
## Page 135

Chapter 9
Integrated Risk Modeling121Each cell in the table is the average correlation of spread factors, 
either for a single rating categor y or between two rating catego-
ries, but across different sectors.  This is why the diagonals, the 
average correlation within a rati ng category, do not equal one.
An average spread factor captur es this commonality and helps 
account for the correlation of local credit spreads with factors in 
other markets. The return to this factor is defined as:
(EQ 9-9)
where k ∈ local credit factors an d each factor’s weight, wk, is 
inversely proportional to its vola tility. The weights mitigate the 
influence of the lower quality credit factors that tend to have sub-stantially higher volatilities.
Emerging-Market Factors
Emerging-market bond spreads e xplain the risk of emerging-
market debt issues denominated in external currencies. These 
spreads are strongly correlated. Over the period from January 
1998 to April 2002, the average correlation between these factors was 0.38.
1 As with the credit spreads  for markets in the United 
States, the United Kingdom, Japan,  and the euro zone, an average 
emerging-market credit factor re flects the common behavior of 
these markets, defining it to be:
(EQ 9-10)
where k ∈ emerging-market credit factors, and the weight on each 
factor is inversely propo rtional to its volatility.
U.S. Municipal Bond Factors
The risk of U.S. municipal bonds is captured in the local U.S. 
bond model using muni key-rate fa ctors. We calculate the average 
U.S. muni factor as the equally we ighted mean of all key rate fac-
tors—that is, the muni gl obal interest rate factor corresponds to a 
parallel shift of interest rates ca lculated as an equal-weighted aver-
age of the key rate changes. Muni cipal bonds may additionally be 
1.   Omitting the month surrounding th e Russian default, August 1998, reduces 
this correlation to 0.23, which is still substantial.


---
## Page 136

Barra Risk Model
Handbook122exposed to a credit spread factor. However, there is no global fac-
tor for muni credit spreads. 
Shift and Twist Factors for Real Markets
To describe real return risk, we us e market prices in  real terms to 
estimate changes in the real yiel d curve. Standard principal com-
ponents analysis, which is the same  methodology used in nominal 
markets, is then applied to dete rmine risk factors and forecasts. 
Finally, the real returns are a pproximately related to nominal 
returns. So, for the corresponding risk forecasts, the real return 
risk can be treated in the same  manner as a nominal return risk. 
Exposures of Local Bond Fact ors to Global Bond Factors
The exposures of local bond factors to the global bond factors are 
defined as follows:
■The local shift, twist, butterfly, and swap factors each have unit exposure to the corresponding global factors.
■The local credit spread factors in the United States, United 
Kingdom, Japan, and euro market s are exposed to the average 
credit and global swap factors corresponding to their market. The exposures are the coefficients  obtained from regressing the 
time series of local credit spread  factors on the average credit 
and global swap factors.
■The local emerging-market credit  spread factors are exposed to 
the average emerging-market cr edit spread factor. The expo-
sures are the regression coefficients obtained from regressing the time series of the local factor s returns on this global factor.
■The local U.S. muni key rate factors are exposed to the aver-
age U.S. muni factor. The exposu res are calculated by running 
a regression of each local factor on this global factor.
Computing Covariances Of Global Bond Factors
As with equities, the fixed-income  covariance matrix is estimated 
from the global and purely loca l factor returns and is exponen-

---
## Page 137

Chapter 9
Integrated Risk Modeling123tially weighted with a half-lif e of 24 months. We use the EM 
algorithm to cope with missing data.1
After scaling in the local factor covariance blocks, we obtain a 
global fixed-income model that is  consistent with the local mod-
els, yet is appropriate for risk analys is of portfolios of global fixed-
income securities. 
The Currency Model
We decompose the excess return in the numeraire currency into a 
part due to currency fluctuations and a part due to the return of 
the asset in the local market.2 Consider the excess return from a 
U.S. dollar perspective of an in vestment in Sony Corporation on 
the Tokyo Stock Exchange, rsony/$. We can write this as:
(EQ 9-11)
1.  See also, Missing Data  on page 118.
2.  For more information on the curren cy model, see Chapter 8, “Currency Risk 
Modeling”.Figure 9-1
Common Factor Blocks in the 
Fixed-Income Covariance Matrix
Barra’s risk model is flexible, 
allowing the number of currencies, local market factors, and 
emerging-market factors to 
increase or decrease.
Currency 
Factor BlockFixed-IncomeFactor Covariances


---
## Page 138

Barra Risk Model
Handbook124where
The currency return is the excess return to an investment in a for-
eign instrument yielding the short-term rate.
Currency returns are local factors.  Cash holdings have unit expo-
sure to the appropriate  currency factor. Since currencies have sub-
stantially fewer factors than equi ties and fixed-income assets, we 
do not model the covariance of currencies with a smaller set of variables. However, for ease of exposition later, we place the cur-
rencies in the same framework as  equities and bonds. We treat 
currencies as both local (to the currency asset class) and global 
factors (like the bond te rm structure factors).
Thus, we can formally write:
(EQ 9-12)
and 
(EQ 9-13)
wherersony = local return to Sony
rfusa = U.S. risk-free rate
rfjapan = Japan risk-free rate
ex¥/$ = exchange return to an investment in yen from 
a dollar perspective
fC = a vector of local currency returns
YC = the identity matrix 
gC = a vector of global currency returns
GC = the currency covariance matrix


---
## Page 139

Chapter 9
Integrated Risk Modeling125Putting It All Together—A Multi-Asset Class Risk 
Model
The factors in BIM include all th e local equity, fixed-income, and 
currency factors. The exposure matrix, XBIM, and the specific risk 
matrix, ΔBIM are of the form:
(EQ 9-14)
where XE,C, XB,C, and XC are the exposures of equities, fixed-
income securities, and currencies to the currency factors. From 
the decomposition in Equation 9-11, it is clear that each equity 
and fixed-income security has a un it exposure to the currency of 
its own market and no exposure to any other currency.1
To complete our multi-asset clas s model, we specify the covari-
ance between factors in different asset classes. Drawing on our 
earlier work, the natural answer is  that these factors are related 
through the global factors in each asset class. These  global factors 
embody the information that relate s markets within an asset class 
and are therefore likely to capt ure important links across asset 
classes. This implies that the BI M factor covariance matrix is:
(EQ 9-15)
where the notation GX,Y denotes the covariance between the global 
factors of asset classes X and Y.
1.  More precisely, a fixed-income or eq uity investment in a local market incurs 
an implicit exposure to th e currency of that market. 


---
## Page 140

Barra Risk Model
Handbook126 
1. The country return is the country fact or return plus the wo rld factor return. 
The correlation between our measure and the returns to country indices for 
most countries is greater than 0.9.
The correlations of more than 140 global factors—some of which 
have short histories or have little  data available—are too many to 
reliably estimate directly. So, rather  than using all 140 factors, we 
designated a subset of the global  factors—those most likely to 
account for correlations between asset classes—as core factors . 
The core factors are:
■World factor
■Country equity factors
■Shift factors
■Average credit spreads for th e U.S., U.K., Japan, and euro-
zone markets
■Average emerging-market credit spread
The correlations between global fa ctors in different asset classes 
are assumed to be expressed throug h these core factors. The equa-
tion for any set of global factors A is:
(EQ 9-16)Shift Twist SwapAverage 
Emerging- 
Market Credit 
Spread 
Average
Correlation 0.13 0.08 0.09 0.36
% Positive and Significant 40% 12% 13% 66%
% Negative and Significant 0% 4% 0% 5%Table 9-9
Average Correlations Between 
Global Equity Factors and Glo-
bal Fixed-Income Factors in the 
Same Market, January 1993 to April 2002
For each market, we computed 
the correlation between country returns, on the one hand, and 
term structure factor returns 
and the average emerging-mar-ket credit factor returns, on the 
other. 
Among the term structure fac-
tors, shifts are most significantly 
correlated with the equity factor. 
The average emerging-market credit factor is strongly corre-
lated with the country factor.
1


---
## Page 141

Chapter 9
Integrated Risk Modeling127where
The components of τk are assumed to be u ncorrelated with the g’s. 
We also assume that τa,p and τa,q are uncorrelated with each other 
when p and q index global factors are corresponding to different 
asset classes.
The covariances between any tw o sets of global factors A and B is 
calculated with: 
(EQ 9-17)
We use this formula to compute  to a provisional estimate GBIM.1 
To ensure consistency with the as set class models, the covariance 
matrices for global bond and equi ty factors are scaled with the 
same procedure used for individual asset classes.2  gA = a vector of returns to the global factors in A 
ΣA,core = a matrix of covariances between the global 
factors and the core factors 
Σcore = a matrix of the variances and covariances of 
the core factors
gcore = a vector of returns of the core factors
τ = a vector of returns of the global factors residual 
to the core factor returns
1.   The covariance matrices ΣA,core  and Σcore are estimated from the global fac-
tors using an exponentially weighted scheme with a half-life of 36 months.
2.  Currencies are included  with bonds for the scaling.
-Figure 9-2
Barra Integrated Model Factor 
Covariance Matrix 
The matrix contains the two single 
asset class models. The global equity model including both equi-
ties and currencies is shown in 
the upper left corner while the global bond model including both 
bonds and currencies is shown in 
the lower right corner.

---
## Page 142

Barra Risk Model
Handbook128Summary
The Barra Integrated Model is a multi-asset class risk model that 
couples breadth of coverage (global equities, global fixed-income 
securities, and currencies) with th e depth of analysis provided by 
Barra’s local models. Users do not have to choose between granu-
larity of local model analysis, on the one hand, and the broad 
scope of global model analysis, on the other. The model is suitable 
for a wide range of investment n eeds, from analysis of a single-
country equity portfolio to a plan-wide international portfolio of 
equities, fixed-income se curities, and currencies. 
In-depth, accurate local analysis requires choosing factors that are 
effective in the market under s tudy and recognizing that the fac-
tors developed for one market are not always appropriate for use 
in other markets. Thus, we starte d by building individual risk 
models for each market to best ca pture the behavior of the local 
securities. 
For broad global analysis, we de termined how securities in differ-
ent markets co-vary. We accomplis hed this by modeling the rela-
tionships between the factors across  local markets. The number of 
correlations between factors rises sharply with the number of fac-
tors.1 There is simply not enough dat a to estimate so many corre-
lations directly. Fortunately, these relationships may be modeled 
using a smaller set of global factors. Correlations across markets 
are expressed through these global factors, requiring less data for accurate estimation. 
The model is also flexible in its structure, allowing the incorpora-
tion of advances in modeling for different countries or regions. 
For example, if a group of count ries is better modeled as a bloc, 
then a local model for the bloc may replace local models for the 
individual countries. Its design al so enables us to add additional 
asset classes (for example, real  estate, commodities, or hedge 
funds) without changing the model’ s architecture. Its adaptability 
even allows the number of curre ncies and local market factors to 
increase or decrease. Furthermore,  assets belonging to different 
asset classes can be linked. Fixe d-income assets, such as convert-
ible bonds or bonds with high option-adjusted spreads, can be 
exposed to equity factors.
1.   The number of correlations is N(N–1)/2, where N is the number of factors. 

---
## Page 143

Section SixReference
Chapter A: Glossary
Chapter B: ContributorsReference

---
## Page 145

Appendix A
Glossary131Glossary
A
ABS See asset-backed securities .
accrued interest The dollar amount of interest that accumulates 
on an asset between the most recent interest pay-
ment (or the issue date) and the settlement date. 
To calculate accrued inte rest, multiply the coupon 
rate by the number of days that have elapsed 
since the last payment, but do not include the 
settlement date. 
active The portion of the portfolio that differs from its benchmark , and is therefore attributable to man-
aged assets or portfolio characteristics. For exam-
ple, if a portfolio’s return is 5%, and the 
benchmark’s return is 3%, then the portfolio’s active return is 2%. A portfolio’s active risk  is the 
risk associated with the volatility of active returns . 
Active weight is the portfolio’s weight in an asset 
minus the benchmark’s weight in the same asset. Active exposure is the portfolio’s exposure to a 
factor minus the benchmark’s exposure to that 
same factor. 
active return Return relative to a benchmark. If a portfolio’s return is 5%, and the benchmark’s return is 3%, then the portfolio’s active return is 2%.

---
## Page 146

Barra Risk Model
Handbook132active risk Also called tracking error . It is the risk (annualized 
standard deviation) of the active return. It is the 
difference in risk between a managed portfolio and a specified benchmark an d is measured as the 
expected standard deviation of the differential 
return between the portfolio and the benchmark. 
Active risk arises from active management; for 
passively managed portfolios, it is often referred to as tracking error . 
agency security A security issued by an agency of the federal gov-
ernment whose debt issues are not backed by the 
full faith and credit of th e United States govern-
ment, but is nonetheless held in high regard because of the presumption of government back-
ing. Major agencies are farm and home lending 
corporations. The debt of international banks is sometimes placed in this category. 
algorithm A procedure for solving a mathematical problem (for instance, finding the minimum combination 
of risk and return given a utility function) in a 
finite number of steps th at frequently involves 
repetition of an operation.

---
## Page 147

Appendix A
Glossary133alpha ( α) The component of an as set’s total historical 
return that is not attribut able to market effects or 
that is solely unique to the particular asset.
The term alpha is borrow ed from statistics and 
originates from the regression of a stock’s or port-
folio’s excess returns  on the market’s excess returns 
(which also derives a hist orical beta estimate). 
Thus, originally alpha wa s defined as historical 
residual return. When the hi storical asset’s return 
is plotted against the hi storical market return, 
alpha is the Y-intercept an d beta is the slope. His-
torical alpha is estimated as the constant term in a time series regression  of an asset return upon 
market return. For expos itory purposes, alpha is 
usually expressed as percentage annual return; for example, an alpha of 1.25 in dicates that a stock is 
projected to rise 25% in price in a year when the 
return on the market and the stock’s beta are both 
zero. For mathematical purposes, alpha is 
expressed as an adjustment to proportional return 
(or logarithmic return), ag ain expressed as an 
annual rate (for example, 0.01).
When applied to stocks, al pha is essentially syn-
onymous with misvaluatio n: a stock with a posi-
tive alpha is viewed as undervalued relative to 
other stocks with the same systematic risk , and a 
stock with a negative alph a is viewed as overval-
ued relative to other stocks with the same system-atic risk. 
APT See Arbitrage Pricing Theory .
arbitrage To profit from the differences in price of a secu-
rity, currency, or commodity sold in different markets.

---
## Page 148

Barra Risk Model
Handbook134Arbitrage Pricing 
Theory (APT)Theory developed in the late 1970s that asserts 
that securities and portfo lio returns are based on 
the expected returns attributable to an unknown number of underlying factors . APT provides a 
complementary alternative to its precursor, the 
Capital Asset Pricing Model (CAPM) .
asset-backed 
security (ABS) A security whose cash flow  is backed by assets 
other than real estate. Such collaterals can be 
leases, auto loans, and credit lines.
average The arithmetic average is  the sum of a group of n 
items divided by n. 
The geometric average is defined as the nth root 
of the product of n values. The geometric average 
will always be less than or equal to the arithmetic 
average. All data values must be positive to deter-
mine the geometric average. 
B
Barra Integrated 
Model (BIM)A multi-asset class model fo r forecasting asset and 
portfolio level risk of global equities, bonds, and 
currencies.
base currency See numeraire . 
basis The difference between a bond’s price and its 
delivery price (conversion  factor times futures 
price). Basis has two components: net basis and carry.
basis point (bps) One-hundredth of one percent (.01%); thus, 100 basis points equals 1%. A basis point is the small-
est measure used in quoting yields on bills, notes, 
and bonds. A bond’s yield that increased from 
8.00% to 8.50% would be said to have risen 50 
basis points.

---
## Page 149

Appendix A
Glossary135benchmark A reference portfolio or standard of comparison 
for investment performa nce and risk control. 
Benchmarks can be generally accepted market-weighted indexes, customized indexes, liability 
streams tailored to the cash outflow of a pension 
fund, or pure bullet paym ents associated with a 
guaranteed return over a specified holding period. 
The list of assets in a benchmark portfolio repre-
sents the investment manager’s performance tar-get. The goal of the active manager is to exceed 
the benchmark return. The benchmark will typi-
cally contain assets that fall within a manager’s investment style. For example, a largecap growth 
manager of United States  equities may choose the 
S&P 500 Growth Index as a benchmark portfolio since it represents the type of assets that he or she 
would hold in the managed portfolio.
benchmark 
return The total return of the benchmark portfolio.
benchmark risk The total risk of the benchmark portfolio.
benchmark weight Weight of the asset in the benchmark. This allows 
comparison of the weight of a position in the 
portfolio against the weight of the same security in the benchmark.

---
## Page 150

Barra Risk Model
Handbook136beta ( β) A measure of the sensitivity of an asset to move-
ments in the market; thus, a measure of the asset’s 
non-diversifiable or systematic risk . A beta of one 
(1) indicates that, on average, the asset is 
expected to move in ta ndem with the market. 
Beta can be applied to both equity and fixed-
income securities.
Any security with a beta higher than one is more 
volatile than the market; an y security with a beta 
lower than one can be expected to rise and fall 
more slowly than the market. An investor whose 
main concern is the preser vation of capital should 
focus on assets with low betas, whereas an inves-
tor whose chief goal is to earn high returns 
should look for assets wi th high beta. However, a 
beta of zero does not mean that the asset has no 
risk, just that its volati lity has no linkage with 
overall market movement s. For example, gold 
stocks have low betas, yet often have high risk. 
This is because they are driven more by the price 
of gold than by the direction of the overall stock market. 
Beta can be interpreted as  an estimate of the aver-
age change in rate of return that corresponds to a 
1% change in the market. Betas are usually plot-
ted on a scatter diagram which shows the move-
ment of the market as a whole and the return of a 
particular asset on a dai ly, weekly, monthly, or 
quarterly basis. 
See also historical beta  and predicted beta .
BIM See Barra Integrated Model . 
book value A company’s total assets minus intangible assets 
and liabilities, such as debt. A company’s book 
value might be higher or  lower than its market 
value. When referred to as book value per share, it is the ratio of stockhol der equity to the average 
number of common shares.

---
## Page 151

Appendix A
Glossary137bootstrapping The process of creating a theoretical spot rate 
curve using one yield proje ction as the basis for 
the yield of the next maturity.
bps See basis points .
bulldog bond A sterling-denominated bond issued by a non-
British firm or institutio n. An example of a bull-
dog bond is one denomin ated in sterling and 
issued in England by a U.S.-based company. 
butterfly The change in the term structure  where the short 
and long ends of the curve move in the same 
direction, but the intermediate part of the curve moves in the opposite direction. The butterfly 
movement defines curvature in the term struc-
ture. 
Historical regressions have been run to define the 
typical shape and magnitude of a one-standard 
deviation butterfly movement over a one-year 
horizon. The butterfly movement is nearly orthogonal to both shift and twist movements 
within a market.
butterfly risk The part of risk due to  exposure to butterfly 
movements in the term structure .
buyback The purchase of bonds by the issuing company in 
the open market.
C
call option A contract that gives the holder the right to buy a 
security from the person who writes the option at 
a pre-specified price. 

---
## Page 152

Barra Risk Model
Handbook138call price The agreed price at which a security is traded 
when a call option is exerci sed. Also known as the 
strike price.
callable bond A bond whose debt the issuer retains the right to retire before the scheduled maturity. This permits 
the issuer to replace an old bond with a lower-
interest cost issue if intere st rates fall. Typically, a 
callable bond includes a s chedule of call dates and 
strike prices (call schedule), allowing the issuer to 
refinance the issue prior to maturity at specified dates for specified strike prices.
cap 1. The highest level interest  rate that can be paid 
on a floating rate note, expressed as a percent-
age.
2. Abbreviation of capitalization.
capitalization See market capitalization .
capitalization-
weighted A portfolio, typically an index, in which the 
weight invested in each as set is proportional to 
the asset’s market capitalization. 
Capital Asset 
Pricing Model (CAPM)The simplest version states that the expected 
excess return  on securities will be exactly in pro-
portion to their systematic risk  coefficient, or beta. 
CAPM implies that total re turn on any security is 
equal to the risk-free re turn, plus the security’s 
beta, multiplied by the ex pected market excess 
return.
CAPM See Capital Asset Pricing Model .
cash flow 1. For bonds, it is the total of the interest pay-
ments and principal payments received by a 
bond owner. 
2. For stocks, it is the to tal dividends received by 
the stock holder.

---
## Page 153

Appendix A
Glossary139category A class of bonds grouped by  issuer type or rating 
for purposes of analysis. All bonds within a cate-
gory (or all bonds within a cell defined by the intersection of two categories) are customarily 
considered to be identical insofar as the model is 
concerned.
clean price The price of a bond without accrued interest. Also called the flat pri ce. The clean price plus 
accrued interest equals the dirty price . Both prices 
are normally expressed as  a percentage of par 
value.
CMO See Collateralized Mortgage Obligation . 
coefficient of 
determination (R
2)See R-squared .
collateralized 
cash flow Payment backed by an asse t such as real estate or 
credit line. In the case of emerging-market debt, 
the payment is backed by the creditworthiness of 
the government. 
Collateralized 
Mortgage 
Obligation (CMO)An instrument entitling the holder to the under-
lying cash flows from a series of bonds issued with the collateral of long-term mortgage securi-
ties. The nature of the cash flows to be received 
by the holder of a CMO series is uncertain. The magnitude and timing of the cash flows, which 
are fully defined by the terms of the CMO inden-
ture, are highly dependent upon the future pre-payments on the underlyi ng mortgage securities.

---
## Page 154

Barra Risk Model
Handbook140common factor A characteristic shared by a group of securities 
that influences the returns  of those securities. 
Securities with similar cha racteristics exhibit simi-
lar return behavior, which may be distinct from 
the rest of the market. In Barra multiple-factor 
risk models, the common factors determine corre-
lations between asset returns. Examples of com-
mon factors are industry, style, term structure movements, and spread changes. See also risk 
model . 
common factor 
risk The part of total risk due to exposure to common 
factors .
convexity The degree of curvature of the price-to-yield rela-
tion. It describes the rate at which duration 
responds to a change in interest rates. Positive convexity means that when interest rates decrease, 
the price of a bond will increase at a faster rate 
than that predicted by duration alone. For non-optionable securities, conv exity can be computed 
as the second-order Taylor effect of interest rates 
on bond prices. 
core factors A subset of global factors in the Barra Integrated Model that mostly likely accounts for correlations 
between asset classes. The correlations between 
global factors in different  asset classes are assumed 
to be expressed through these core factors. 

---
## Page 155

Appendix A
Glossary141correlation A statistical term giving the strength of a linear 
relationship between two ra ndom variables. It is a 
pure number, ranging from –1 to +1. A correla-tion of +1 indicates perf ect positive linear rela-
tionship; –1, perfect negative linear relationship; 
0, no linear relationship. For jointly distributed 
random variables, correlation is often used as a 
measure of strength of relationship, but it fails when a nonlinear relationship is present. Low or 
negative correlation between  securities or between 
common factors leads to portfolio risk diversifica-tion. 
coupon A periodic interest paymen t a bond issuer makes 
to a bond holder. It is normally expressed as a 
percentage of par. The coupon rate is always 
expressed in annual terms. A semi-annual bond with a coupon rate of 8% pays 4% every six 
months.
coupon currency The currency denominatio n of coupon payments.
coupon 
frequencyNumber of coupon installments paid annually.
coupon type One of three methods for determining coupon 
payments:
■Fixed: coupon payments are fixed in fre-
quency and amount.
■Floating: coupon payments match a current benchmark index rate.
■Scheduled: coupon paym ents that may change 
in amount (for example, to “step up” from 
6% to 7%) or coupon type (for example, fixed rate to floating rate), according to a pre-
defined schedule.

---
## Page 156

Barra Risk Model
Handbook142covariance The tendency of different random investment 
returns to have similar ou tcomes, or to “co-vary.” 
The greater the covariance, the greater the strength of the common movement of assets. 
When two uncertain outcomes are positively 
related, the covariance is positive, and the con-
verse is true. The magnit ude of covariance mea-
sures the strength of the common movement. Covariance can be scaled to obtain the pure num-
ber, or correlation , that measures the closeness of 
the relationship with out its magnitude. 
covariance 
matrixThe square matrix  containing the variances  (along 
the diagonal) and covariances  (off-diagonal) of all 
the common factors  in a risk model . It is a key 
component in the foreca sting of risk measures. 
credit spread The difference in yield be tween a corporate bond 
and a comparable government bond. This spread 
describes bonds in the U.S. dollar, sterling, euro, and yen markets.
cumulative 
returnThe investment return cu mulated over a number 
of periods, ordinarily expressed as a proportional 
return. 
currency The currency in which an asset is denominated.
currency risk The predicted risk of an asset (in one-year stan-
dard deviation) due to its being invested in a for-
eign currency. This risk takes into account the 
exchange rates and short-term interest rates of the foreign country and the numeraire  country.
current yield The ratio of the annual co upon rate to the clean 
price of the bond. For example, an 8% coupon 
bond trading at 91% of pa r has a current yield of 
8/91, or 8.79%.

---
## Page 157

Appendix A
Glossary143D
default The failure of a debtor to make interest or princi-
pal payments in a timely manner. Default occurs 
whenever the payment is not made according to the terms of the original issue. When an issue is 
in default, the holders can make claims against 
the issuer to salvage as much of their principal as possible. The exercise of  these rights often lead 
the company into reorganization or bankruptcy.
default risk 
premiumThe higher yield expected on an issue that is sub-
ject to the risk of defaul t. This anticipated return 
compensates the investor for assuming the default 
risk of the bond.
descriptor A fundamental or market-rel ated data item that is 
used as a fundamental building block of risk 
index or style factors in a Barra equity risk model. 
Most style factors or risk indices are comprised of several descriptors combined using proprietary 
formulas. For example, a volatility risk index, 
which distinguishes high vola tility assets from low 
volatility assets, might co nsist of several descrip-
tors based on short-term volatility, long-term vol-
atility, systematic vo latility, and resi dual volatility, 
and so on. 
dirty price The bond price plus accrued interest.
discount Amount by which a bo nd is trading below par 
value. 
discount bond See zero coupon bond .
discount factor A factor that, when applied to a future payment 
or cash stream, converts it to its present value .

---
## Page 158

Barra Risk Model
Handbook144discount 
functionA complete schedule of discount factors for all 
future dates. Because each discount factor gives 
the present value of a payment at a given future date, a complete schedule of these factors gives 
the present values of all future payments. Future 
interest rates can be expressed in the discount 
function as continuously  or semiannually com-
pounded spot rates, forward rates, or yield-to-par rates. The discount funct ion is therefore one way 
of representing the term structure.
discounting A financial concept whereby  the values of single 
or multiple future cash flows  are computed as of a 
given date in the past or present. This is diametri-
cally opposite to the concept of compounding, 
which is used to compute the future value of a 
present cash flow.
distribution The function which describe s the frequency with 
which a random variable takes on any given value. The distribution of future values for a ran-
dom variable is usually described in terms of its 
mean, standard deviation, skewness, and func-tions. 
diversification The spreading of risk by investing in a number of 
different assets whose returns are not perfectly 
positively correlated. Since the returns are not 
perfectly correlated, losses of any one asset tend to be offset by gains on other assets. In this man-
ner, the risk of a portfolio may well be less than 
the average risk of its constituent assets. Diversi-fied portfolios typically contain assets in several 
categories of investments—stocks, bonds, money 
market instruments, and precious metals, for instance—or several industries in a stock portfo-
lio.
Diversification is the spreading of risk; hedging is 
the offsetting of risk. 

---
## Page 159

Appendix A
Glossary145diversifiable 
returnSee residual return .
dividend A periodic payment an equ ity issuer makes to a 
stockholder.
dividend yield The return of a security or portfolio in the form of dividend cash payments. It is calculated as the 
annual dividend payment of  a security divided by 
the security’s current pr ice. Yield is usually 
described, for expository purposes, in percentage 
terms (for example, 7 percent per annum), but 
for mathematical purposes it is expressed as a dec-
imal fraction (for example, 0.07). Also known as 
the yield.
dollarization A situation in which a country uses foreign cur-
rency alongside its own c urrency, or abandons its 
own currency entirely and adopts another coun-try’s currency as a means of payment and unit of 
account. 
dummy variable A statistical term for a va riable that represents a 
single fixed characteristic; also called an indicator 
variable for that characte ristic. A dummy variable 
is one for all cases where the characteristic occurs, 
and zero otherwise. Consequently, the coefficient 
of the dummy variable in a model tells us the dif-ference between the model value for that charac-
teristic and the model value in the absence of that 
characteristic.

---
## Page 160

Barra Risk Model
Handbook146duration A summary measure of the price responsiveness of 
an interest-sensitive asset to changes in interest 
rates. Duration is a reasonably good predictor as long as the change in intere st rates is small and of 
a parallel nature. 
The maturity duration in  the Barra model is cal-
culated as the modified Macaulay duration : 
Macaulay duration divided by (1 + yield/2). Barra 
computes option-adj usted Macaulay and modified 
duration  (also called effective duration) by simu-
lating future interest rates and modeling the 
change in option value for small changes in inter-est rates.
E
earnings yield The earnings per share di vided by the price per 
share.
effective 
durationSee duration .
emerging-
market spreadThe spread associated w ith bonds issued in an 
external currency by an emerging market sover-
eign or by a company domiciled in an emerging 
market country. In the Barra risk model, emerg-ing- market spread is me asured relative to the 
swap spread. 
emerging-
market riskThe part of risk due to exposure to emerging-mar-
ket spreads .
equal-weighted A portfolio in which approx imately equal value is 
invested in all assets. 

---
## Page 161

Appendix A
Glossary147estimation When a model is fitted to data, the estimated 
value of the model is the one that best fits the 
data, or that “maximizes it s likelihood.” An esti-
mation method, in view of the random nature of 
the data, finds the parameters of the model that 
fit the data best. The estimated model is not 
“true,” but is thought of as a closest approach to 
the underlying or “true” model. The discrepancy between the estimated mo del values and these 
underlying but unknown va lues is called estima-
tion error.
estimation error See estimation .
estimation 
universeSet of assets used in th e estimation of factor 
returns.
Eurobond A bond denominated in a particular currency and 
issued simultaneously in  the capital markets of 
several nations, including nations with different currencies. The Eurobond market is an important 
source of capital for multi national companies and 
foreign governments, including developing coun-tries’ governments.
excess return Return in excess of the risk-free rate. The excess return is computed by subtracting the promised 
risk-free rate from a security’s return. If an asset’s 
return is 3% and the risk-free return is 0.5%, then the asset’s excess return is 2.5%. 
exchange An institution where sec urities or futures trading 
takes place. It regulates the processes by which 
the market operates, part icularly market access, 
formation, settlement of bargains, and dissemina-tion of market intellige nce. Exchanges are often 
organized as associations of major market partici-
pants. The New York Stock Exchange and Ameri-
can Stock Exchange are the largest centralized 
places to trade stocks in the United States. 

---
## Page 162

Barra Risk Model
Handbook148expected return The average return expected from an asset or 
portfolio. Expected return is defined over a par-
ticular investment horizon. The expected value depends upon one’s view of the future, so when 
used as a tool, the expected value will be that 
which relates to the user’s own expectation of 
future scenarios. Expected return is the mean of 
the probability distribution of investment return.
exponential The case in which a number is multiplied to a power, with the power being, in mathematical terminology, the exponent. When any given inter-
est rate is compounded continuously, the present 
value  of a payment declines progressively with 
time along an exponential curve.
exposure A term used to quantify the magnitude of an asset’s (or portfolio’s) sensitivity to factors. 
1. Equity: for style factors or risk indices , expo-
sure is expressed in standard deviation; for 
industries, it is expressed in percent of portfo-lio value. 
2. Fixed-Income: for term structure, spread, and 
emerging market factors, exposures represent 
the sensitivity of the bond or portfolio to 
shocks in those term structure or spread 
curves, and is therefore related to duration . 
F
face amount See face value .
face value The value of a sec urity as it appear s on the certifi-
cate of the instrument. This is the amount of principal due the bondhold er at maturity and also 
the amount on which intere st payments are calcu-
lated. See par value .

---
## Page 163

Appendix A
Glossary149factor A factor of value or factor of return represents an 
underlying construct that influences many securi-
ties. When the existence of a factor is established, 
it becomes a convenient way of isolating common 
elements in securities and of tracking events in 
financial markets. One imp ortant application is 
to attribute elements of value and elements of 
investment returns to un derlying factors. Exam-
ples of fundamental equity factors are: size, value, 
growth, and earnings varia tion. Examples of fun-
damental fixed-income factors are: shift, twist, and butterfly.
factor exposure See exposure .
factor return The return attributable to a particular common 
factor. Barra decomposes asset returns into a com-
mon factor component—ba sed on the asset’s 
exposures to common factors times the factor 
returns—and a specific return .
Fannie Mae 
(FNMA)An acronym for the Federal National Mortgage 
Association. It refers to the mortgages insured by the Federal Housing Admi nistration but managed 
by FNMA. FNMA represents the effort of the 
government to stimulate the development of a secondary market for mortgages in order to 
enhance market liquidity.
FHLMC An acronym for Federal Home Loan Mortgage Corporation. See Freddie Mac .
FNMA An acronym for Federal National Mortgage Asso-
ciation. See Fannie Mae.
fit of estimation The degree of closeness between the data and the 
values predicted by the model. Perfect fit is 
impossible because of the randomness of data, 
which gives rise to noise.

---
## Page 164

Barra Risk Model
Handbook150fitted prices Prices estimated by a mo del which best fit the 
data with minimal expected  discrepancies between 
the estimated values and th e values of the under-
lying random variables.
floating rate 
notes (FRN)Also called a “floater,” an instrument with the 
coupon rate pegged to a predetermined rate and 
reset contractually by formula at a stipulated 
interval. Floor and/or cei ling coupon rates may be 
specified.
FNMA See Fannie Mae .
foreign bond A bond issued by foreign borrowers in a nation’s 
domestic capital market and denominated in the 
nation’s domestic currency. This will also include 
foreign currency-denominated  issues by foreigners 
in the domestic bond market.
forward interest 
rateAn interest rate which is determined at the 
present time for a loan that will occur at a speci-
fied future date. The co mpound interest to any 
future date can be obtain ed by successively com-
pounding the forward rate for all intervals 
between now and that future date. Consequently, 
the schedule of forward rates determines the present value of all future payments, and so it is 
one way of representing the term structure. Usu-
ally abbreviated to forward rate.
forward rate See forward interest rate .
Freddie Mac 
(FHLMC)Federal Home Loan Mortgage Corporation sells 
two types of pass-through  securities: mortgage 
participation certificates and guaranteed mortgage certificates. The investor receives prorated princi-
pal and interest payments based on the underly-
ing pool and its experienced repayments.

---
## Page 165

Appendix A
Glossary151fundamental 
betaSee predicted beta . 
G
GARCH See general auto-regressive c onditional heteroskedas-
tic model .
general auto-
regressive conditional heteroskedastic model (GARCH) Model used in predicting a time series variance 
when volatility is serially dependent (heteroske-dasticity). The GARCH model links the predicted 
(conditional) variance with  past realizations of the 
error process and the variance itself. 
In conventional econometric models, the variance 
of the disturbance term is  assumed to be constant 
(homoskedasticity). However when periods of 
unusually large volatility are followed by periods 
of relative tranquillity, th is assumption is inappro-
priate. 
general 
obligation (GO) bond Municipal securities secure d by the issuer’s pledge 
of its full faith, credit, and taxing power. A gen-
eral obligation bond, or GO bond, as it is more 
commonly called, is repaid with the municipal 
agency’s general revenues and borrowings. Gen-
eral obligation bonds are different than municipal bonds, where payments are based on the revenue 
from a specific facility built with the borrowed 
funds.
Ginnie Mae 
(GNMA)An acronym for the Gove rnment National Mort-
gage Association. It cr eates pools of mortgages 
and sells participations in  these pools to private 
investors.
global bond A bond issued in two or  more countries’ markets 
by organizations such as the World Bank.

---
## Page 166

Barra Risk Model
Handbook152global factor Factors responsible for the global correlation 
structure of the Barra Integrated Model  covariance 
matrix. It does not impl y applicability to all 
assets. 
GNMA See Ginnie Mae .
GO bond See general obligation bond . 
government 
bondSee sovereign bond .
growth stock Stock of a corporation th at has exhibited faster-
than-average gains in earnings over the last few 
years and is expected to continue to show high 
levels of profit growth. Over the long run, growth stocks tend to outperform more slowly growing 
or stagnant stocks. Grow th stocks are riskier 
investments than average stocks, however, since they usually support higher price/earnings ratios 
and make little or no di vidend payments to share-
holders.

---
## Page 167

Appendix A
Glossary153H
hedging The process whereby the ri sks of several opportu-
nities are largely or comp letely (“perfect hedge”) 
offset. Hedging requires either that the two opportunities be negatively  correlated (gold stocks 
and brokerage firm stocks or a put option and its 
underlying security), in which case positive amounts are invested in both opportunities, or 
that the two opportunities are positively corre-
lated (a call option and its underlying security or 
two very similar securities), in which case one 
opportunity is short-sold. Hedging is the offset-
ting of risk; diversification  is the spreading of risk. 
A stockholder worried about declining stock 
prices, for instance, can he dge his or her holdings 
by buying a put option on the stock or selling a 
call option. Someone owning 100 shares of XYZ stock, selling at $70 per sh are, can hedge his posi-
tion by buying a put op tion giving him the right 
to sell 100 shares at $70 any time over the next few months. This investor must pay a certain 
amount of money, called  a premium, for these 
rights. If XYZ stock falls during that time, the investor can exercise his option—that is, sell the 
stock at $70—thereby pres erving the $70 value of 
the XYZ holdings. The same XYZ stockholder can also hedge his position by selling a call 
option. In such a transactio n, he sells the right to 
buy XYZ stock at $70 per share for the next few months. In return, he rece ives a premium. If XYZ 
stock falls in price, th e premium income will off-
set to some extent the drop in value of the stock.

---
## Page 168

Barra Risk Model
Handbook154historical beta Historical measure of the response of a company’s 
excess return  to the market’s excess return. It is 
computed as the slope coefficient in a historical regression (usually 60 months) of the asset’s 
return against the market.
Note that betas for any individual company do 
change, so one cannot rely on historical betas as a 
guide for future betas. Many studies have demon-
strated that predicted betas significantly outper-form historical betas as predictors of future stock 
behavior.
See also predicted beta .
holdings The number of units held in a particular position. 
The face amounts or par values  of the issues held 
in a portfolio. 
horizon The investment period of an investor. Investment 
horizon affects the expect ed changes in interest 
rates and returns, thereb y influencing the risk/
return profile of a portfoli o. As a rule of thumb, 
the longer the horizon, the more volatile the return will be. See also investment horizon .
I
idiosyncratic risk See specific risk .
IGARCH See integrated general auto -regressive conditional 
heteroskedastic model . 
independent risk See specific risk .

---
## Page 169

Appendix A
Glossary155index A target group of assets against which other port-
folios can be tracked and compared. It is also a 
measure of the value and return to a group of assets. The value and return of the index should 
be identical to the value and return of an invest-
ment portfolio whose weights coincide exactly 
with the weights of the index. Thus, the value of 
an index and its return are found by the same accounting rules by which we compute the value 
of the portfolio and its return. 
index rate The rate that serves as a basis for the floating rate 
note. The options include the following:
■LIBOR: London Interbank Offered Rate
■LIBID: London In terbank Bid Rate
■LIMEAN: Calculated from the mean average 
of LIBOR and LIBID
■Prime: Rate at which bank s lend to their most 
favored customers
■Fed Funds: Interest rate on Federal Reserve 
Bank funds. This is a closely watched short-
term interest rate; it signals the Fed’s view on 
the state of the money supply.
■COFI: Cost of Funds Index
■T-bill: Yield on short- term obligations of a 
government. Issued for periods of one year or less.
industry risk The part of risk due to exposure to industries.

---
## Page 170

Barra Risk Model
Handbook156inflation-
protected bond (IPB)A fixed-income security whose principal is period-
ically adjusted to provide a fixed return over infla-
tion. The adjustment lags a pre-specified measure of inflation by an amount of time determined by 
the issuer. 
instrument type The category of investment vehicle to which a 
security belongs; for example: equity, bond 
future, treasury bills.
integrated 
general auto-regressive conditional heteroskedastic model (IGARCH)A GARCH  model that allows for a unit root in 
the conditional variance. Such inclusion allows 
for shocks to have a permanent effect on the con-
ditional variance. See also general auto-regressive 
conditional heteroskedastic model . 
interest Technically, a prespecified amount paid to an 
investor in excess of repayment of the principal. 
In general, interest can be thought of as the reward to the investor for lending purchasing 
power to the borrower.
interest rate 
sensitivityThe responsiveness of a fixed income instrument’s 
price to changes in interest rates. 
interest rate 
swapA contractual obligation entered into by two par-
ties to deliver a fixed sum of money against a 
variable sum of money at  periodic intervals. The 
transaction typically invo lves an exchange of pay-
ments on fixed- and floating-rate debt. If the 
sums involved are in different currencies, the swap is simultaneously an interest rate swap and a 
currency swap.
investment 
gradeThe quality ratings of bonds, extending from 
AAA through BBB (Standard & Poor’s conven-
tion) or Baa (Moody’s convention). 

---
## Page 171

Appendix A
Glossary157investment 
horizonThe period in which a give n portfolio is held. For 
most investment decisions, it is appropriate to 
establish a horizon for whi ch the portfolio is to 
be optimized. The expectation is that the portfo-
lio will be thoroughly re balanced at the end of 
that horizon. In fact, in active investment man-
agement, a portfolio is continually being modi-
fied as expectations change, but it is nevertheless useful to retain a moving  investment horizon with 
respect to which forecasts are defined. In the sce-
nario approach to return forecasting, the end of the investment horizon corresponds with the sce-
nario forecast date.
IPB See inflation-protected bond . 
issue A particular class of sec urity; for example: a bond, 
a convertible instrument, or a stock. The issue 
date is the date on which th e security is publicly 
available. The issue amount is the quantity of securities that enter the market.
issuer The entity that issues a particular security.
K
key rates A set of rates at distingu ished maturities  used to 
model term structure risk .
key rate 
durationThe sensitivity of a bond to a change in a single 
spot or key rate  on the term structure .
kurtosis Characterizes the relative peakedness or flatness of 
a distribution compared with the normal distribu-
tion. The kurtosis of a normal distribution is 0. 
Positive kurtosis indicates a relatively peaked dis-
tribution. Negative  kurtosis indicates a relatively 
flat distribution.

---
## Page 172

Barra Risk Model
Handbook158L
liquidity In its modern usage, the liquidity of an asset is 
the extent to which it can be readily converted 
into cash without paying a large spread or moving 
the market. Thus, the larger the regular volume 
of trade in an issue, the more likely that a holder 
can dispose of his position without being forced to accept a low price to induce someone else to 
buy it. Liquidity is almo st synonymous with a 
large volume of trade. One historical use refers to 
an asset’s ability to hold its value during hard 
times. From that perspect ive, a liquid asset was 
one that could be quickly converted, at or near its par value , during a monetary crisis.
Associated with liquidity  is the concept of the 
“spread,” which is the difference between the bid 
and offer price quoted by market makers. The bid price is what the market maker will pay for your 
shares if you want to sell them. The offer is the 
price at which you can buy them from him. Large, liquid stoc ks have narrow spreads (a good 
thing). Small, illiquid stoc ks have wide spreads (a 
bad thing).
local factor Factor that only affect securities within each mar-ket. See global factor . 
local market The country that Barra uses to model a security. 
For example, a Finnish A DR would have a local 
market of Finland. 
local market risk The part of risk due to exposure to local market factors such as styles, in dustries, term structure 
movements, and changes in spreads. Local market 
risk arises from decisi ons made with local mar-
kets.

---
## Page 173

Appendix A
Glossary159M
Macaulay 
durationThe weighted average time to receipt of a series of 
cash flows, where the weights are the proportions 
of the present values  of the cash flows  to the 
present value of the entire series of cash flows. 
Therefore, the Macaulay duration of a zero-cou-
pon bond  is equal to its time-to-maturity. The 
maturity duration in the Barra model is calcu-
lated as the modified Macaulay duration: 
Macaulay duration divide d by (1 + yield/2). Barra 
computes option-adjusted Macaulay and modified 
duration  (also called effectiv e duration) by simu-
lating future interest rates and modeling the change in option value for small changes in inter-
est rates.
See also duration  and modified duration .
margin Yield spread of the floating rate note over the 
index rate, expressed as a percentage. 
market The economic entity that is  constituted by buyers 
and sellers coming together to effect purchases 
and sales. 
maturity Almost all fixed-income securities carry a speci-fied maturity date at wh ich time the securities 
will be redeemed. The matu rity of an outstanding 
issue is the number of years until the maturity 
date. The exception is a perpetual bond, or con-sol, which has no pr e-announced terminus.
maturity date The date on which the un paid principal balance 
of a security becomes due and payable. For a 
bond without options, this date is stated in the 
prospectus. For a bond with  options, the maturity 
date is affected by calls,  puts, sinking fund sched-
ules, and so on. 

---
## Page 174

Barra Risk Model
Handbook160mean The expected average value of a random variable.
median A statistical term denoting the value of a random 
variable, such that 50 percen t of all possible value 
lies above this value and 50 percent lie below. For 
example the number 5 is the median between the 
numbers 1 and 9, since there are four numbers 
above and below in this sequence.
model A mathematical representation of an economic system or corporate financi al application so that 
the effect of changes can be studied and forecast. 
In general, a model specifies a set of relationships 
among constructs.
modern portfolio 
theory (MPT)The theory of portfolio  optimization which 
accepts the risk/reward tr adeoff of total portfolio 
return as the crucial cr iterion. Derived from 
Markowitz’s pioneering appl ication of statistical 
decision theory to portfolio problems, optimiza-
tion techniques and related analysis are increas-
ingly applied to investments.
modified 
durationThe modified duration is the Macaulay duration  
divided by 1 plus periodic yield. Periodic yield is 
the yield to maturity divided by the discounting frequency per year. Modified duration can be 
used to measure the sensitivity of a bond’s price 
to changes in yield, for securities whose cash flows  
are not sensitive to chan ges in interest rates.
momentum Rate of acceleration of an  economic, price, or vol-
ume movement. An economy with strong growth 
that is likely to continue is said to have a lot of 
momentum. In the stock market, technical ana-lysts study stock momentum by charting price 
and volume trends. 

---
## Page 175

Appendix A
Glossary161mortgage-
backed security (MBS)A fixed-income security backed by collateral of a 
pool of mortgages. The is suer often services the 
pool of mortgages and withholds the cost of ser-vicing from the coupon payments to be passed 
through to the investor.
multiple-factor 
model (MFM)A model where more than one underlying com-
mon factor influences nu merous securities. Each 
factor influences some or all securities in propor-
tion to their responsiveness  to that factor (or their 
loadings upon that factor). Thus, the outcome for any one security is the sum of its responses to 
each of the multiple fact ors, with the contribu-
tion of each factor being the product of the factor 
itself times the responsiveness of the security to 
that factor. The multiple -factor model does not 
ordinarily assume that all events can be associated 
with factors. Instead, there is also a unique event 
associated with each security, called the specific 
event for that security, which is in addition to the contributions of  the factors.
municipal bonds Bonds issued by state or local governments used 
to pay for special projects such as highways or 
sewers. The interest that investors receive is 
exempt from some income taxes. 
N
nominal A term often used to refe r to prices and returns 
expressed in current dollars, in contrast to real 
values, which are expressed in constant dollars—that is, in terms of constant purchasing power.
nominal cash 
flowA bond’s promised cash flow , ignoring option pro-
visions and default risk.
nominal spread Also referred to as the “spread,” this differs from 
option-adjusted spread  in that it does not account 
for the embedded options in a bond.

---
## Page 176

Barra Risk Model
Handbook162nominal yield The yield that is comput ed by determining the 
interest rate  that will make the present value  of the 
cash flow  from the investment equal to the price 
of the investment. The nominal yield is not the 
coupon rate (see coupon ). 
normal A benchmark portfolio.
normal 
distribution The familiar bell-shaped curve which is called the 
“normal” distribution because it is the distribu-
tion that occurs when large numbers of indepen-dent factors are added together. It is a 
symmetrical distributi on, with approximately 
two-thirds of all outcomes  falling within ± 1 stan-
dard deviation and approximately 95 percent of 
all outcomes falling within ± 2 standard devia-
tions.
normalization The process of transforming a random variable into another form with mo re desirable properties. 
One example is standardization in which a con-
stant (usually the mean) is  subtracted from each 
number to shift all numbers uniformly, then each number is divided by an other constant (usually 
the standard deviation) to shift the variance.
numeraire The currency in which an asset or portfolio is val-ued.
O
OAS See option-adjusted spread .

---
## Page 177

Appendix A
Glossary163optimization The best solution among all the solutions avail-
able for consideration. Constraints on the invest-
ment problem limit the r egion of solutions that 
are considered, and the objective function for the 
problem, by capturing th e investor’s goals cor-
rectly, provides a criterion for comparing solu-
tions to find the better ones. The optimal 
solution is the solutio n among those admissible 
for consideration that has the high est value of the 
objective function. The firs t-order conditions for 
optimality express the trade-offs between alterna-tive portfolio characteristi cs to provide the opti-
mum solution.
option An amount paid for the right to buy or sell a security. 
■A call option is an option to buy shares. Call 
options generally rise in price if the underly-
ing shares rise in p rice (and vice versa).
■A put option is an option to sell shares. Put 
options generally rise in price if the underly-
ing shares fall in price (and vice versa).
The holder of the option is not obligated to buy 
the security, but the amount paid for the option is non-refundable. The main criterion for decid-
ing whether to buy the security is whether the 
exercise price of the option is higher or lower than the current price of the underlying share.
option-adjusted 
cash flowA bond’s nominal  cash flows , adjusted for esti-
mated option influence.
option-adjusted 
convexityMeasures a bond’s convexity , explicitly accounting 
for the influence of  embedded options. 
option-adjusted 
durationThe modified duration of a security, calculated 
using a model that accounts for embedded 
options .

---
## Page 178

Barra Risk Model
Handbook164option-adjusted 
spread (OAS)Measures the difference of a bond’s yield to matu-
rity above the default-free term structure , explicitly 
accounting for the influence of embedded options. Option-adjusted spread (OAS) is a mea-
sure of a security’s extra return over the return of 
a comparable default-free government security 
after accounting for embedded options .
option-adjusted 
spread to swapMeasures the difference of a bond’s yield to matu-
rity above the swap curve , explicitly accounting 
for the influence of embedded options .
option-adjusted 
yieldThe yield to maturity ad justed for the value of 
the embedded options  (call, put, sinking fund, 
and so on). Derived by adding the option value 
to the price and recalculating the yield to matu-
rity.
outlier A data observation that is very different from other observations. It is often the result of an extremely rare event or a data error.
P
par 1. See par value .
2. The typical lot size asso ciated with an instru-
ment type. For example, par for bonds is 1000. Par for equities is 1.
par value The value of a sec urity as it appear s on the certifi-
cate of the instrument. This is the amount of 
principal due the bondholder  at maturity. It is the 
amount on which intere st payments are calcu-
lated. 
payout ratio The ratio of dividends to  earnings. The fraction 
of earnings paid out as dividends.
PCA See principal components analysis .

---
## Page 179

Appendix A
Glossary165performance 
attributionThe process of at tributing portfolio returns to 
causes. Among the causes are the normal position 
for the portfolio, as established by the owner of funds or the manager, as well as various active 
strategies, including mark et timing, common fac-
tor exposure, and asset selection. Performance 
attribution serves an anci llary function to the pre-
diction of future performance, in as much as it decomposes past performance into separate com-
ponents that can be analyzed and compared with 
the claims of the manager.
predicted beta A forecast of a stock’s sensitivity to the market. Predicted beta is also known as fundamental beta, because Barra’s risk models are based on funda-
mental risk factors. These risk factors include 
industry exposures as well as various “style” 
attributes called risk indice s, such as Size, Volatil-
ity, Momentum, and Value. Because we re-esti-
mate a company’s exposure to these risk factors frequently, the predicted be ta responds quickly to 
changes in the company’ s underlying risk struc-
ture. 
Predicted systematic risk coefficients (predictive 
of subsequent response to market return) are 
derived, in whole or in part, from the fundamen-
tal operating character istics of a company. 
premium Amount by which a bond trades above the par 
value . In other words, buyers are willing to pay 
more for the bond. 

---
## Page 180

Barra Risk Model
Handbook166present value The present value of a stream of payments is the 
price at which that stream of payments could be 
purchased in the marketplace. It is the sum of the present values of the cons tituent payments in the 
stream.
The present value of a res tless payment is equal to 
the amount of that payment multiplied by the 
discount factor for that date (or, equivalently, dis-
counted for compound inte rest from the present 
through that date). 
pricing error The discrepancy between the market price and Barra’s fitted price. Positi ve pricing error implies 
that the security is overvalued by the market rela-
tive to Barra’s valuation model, and vice versa.
principal The value paid to the issuer  of a bond at the orig-
inal issue date, usually in distinguishable from the 
par value . When the bond is redeemed, the pay-
ment by the issuer to the holder is treated as a 
return of principal.
principal 
componentPossibly correlated variables that have been trans-
formed into uncorrelated variables. The first prin-cipal component accounts for as much of the 
variability in the data as possible, and each suc-
ceeding component accounts for as much of the remaining variability as possible. See also princi-
pal components analysis .

---
## Page 181

Appendix A
Glossary167principal 
components analysis (PCA)A multivariate analys is which maximizes the 
spread of data by plotti ng covariance values on 
sets of axes in multidimensional space. It enables the identification of correlations which may have 
been hidden in the data. The first principal com-
ponent  corresponds to the first axis in multidi-
mensional space and descri bes the majority of the 
spread of the data; subsequent higher-order prin-cipal component axes are orthogonal to the first 
axis. Higher-order axes di splay progressively less 
variation, where the data is less correlated and more representative of statistical noise.
probability The expression of the likelihood of occurrence. A probability may be stated as a proportion of one, 
or sometimes as a percentage of 100%. It may be 
objective, in the sense of  expressing the frequency 
of times that a random even t will occur; or it may 
be subjective, in expres sing the perceived likeli-
hood of occurrence. 
put option An option that gives the holder the right to deliver a security to the person who writes the option at a prespecified pri ce. In the case of fixed-
income securities, a puta ble bond gives the inves-
tor the right to sell the bond to the issuer on a specified date for a previously agreed-upon put 
price.
putable bond A bond that gives the holder the right to sell the bond back to the issuer on specified date(s) for a 
specified price (the “put  price”). A putable bond 
includes a schedule of p ut dates and strike prices 
allowing the investor, typically, to redeem the 
principal at one or more specified dates prior to 
maturity.

---
## Page 182

Barra Risk Model
Handbook168Q
quality ratings Bond ratings assigned by rating services, such as 
Moody’s, Standard and Poor’s, Duff and Phelps/
MCM, and Fitch. Although conventions vary, Barra uses the rating sy stem where the highest 
quality rating is AAA and the lowest investment 
grade rating is BBB. Rati ngs extend downward 
through C, and agency bonds are unrated.
R
R-squared A statistic usually associat ed with regression anal-
ysis. It describes the fraction of variance in the dependent variable that can be explained by the 
independent or explanatory variable(s). It is often 
used to describe the fraction of investment risk in portfolios that can be asso ciated with market risk.
Mathematically, it is the (predicted) market vari-
ance divided by (predicted) total variance. To cal-
culate the coefficient of determination, take the portfolio beta (measured against the market) 
squared times the total ma rket variance forecast, 
and divide the product by the total portfolio vari-
ance forecast. The coeffici ent of determination is 
a pure number ranging from 0 to 1, with 1 indi-
cating perfect explanation. R
2’s for portfolios typ-
ically range from 0.8 up to 1, with a median of 
about 0.95. 
real A term that refers to prices and returns expressed in constant dollars—that is, in terms of constant 
purchasing power—in cont rast to nominal values, 
which are expressed in terms of current dollars.
real return Return expressed in units of purchasing power.

---
## Page 183

Appendix A
Glossary169real yield curve Yield curve based on the prices of inflation-pro-
tected bonds . Real rates are adjusted by inflation to 
give nominal rates. 
regression A statistical technique wh ich examines the corre-
lation between two or more variables in a mathe-
matical model and attempts to prove whether or 
not the past relationships will be the same in the future. Regression finds the linear combination of 
one or more independent variables which best 
explain the variation in a dependent variable. When there is a single independent variable and 
the observations of the independent and depen-
dent variables are plotted on a graph, regression draws the best straight line through the data 
points. Regression analysis is used in the Black-
Scholes option pricing model, portfolio theory, and the Capital Asset Pricing Model . 
residual A statistical term for that part of a variable that is 
unexplained by some underlying factor. For 
example, residual return  is usually defined as that 
part of return that is no t explained by the system-
atic factor (often the mark et portfolio) in a model 
of systematic and residual return. Similarly, resid-
ual risk  is that part of risk that arises in addition 
to risk from the market factor. The term residual 
is also often used to refer to the difference 
between the actual datum and the datum fitted in 
the model. 
residual return The component of return that is uncorrelated with the return on the market portfolio or bench-
mark. Mathematically, it is  the total return minus 
beta times the market return.
Residual return is also called unsystematic or 
diversifiable return. All components of active 
management, except market  timing, contribute to 
residual return at one point in time.

---
## Page 184

Barra Risk Model
Handbook170residual risk Residual risk is the standard deviation of residual 
return . Residual return is return that is not attrib-
utable to market influence. It is the return net of the market-related return.
return The value of an investment at the end of a 
period, plus any payouts during the period, 
divided by the initial va lue. Return is (depending 
on the length of the period) a number close to 
1.0 and represents one plus the rate of return. For 
expository purposes, return is often given as a percentage by subtract ing one and multiplying 
the result by 100. 
risk The uncertainty of investment outcomes. Techni-cally, risk defines all uncertainty about the mean 
outcome, including both upside and downside possibilities. Studies of investment return have 
shown very consistently that when returns are 
centered about their expected  value, there is little 
difference between the extent of upside and 
downside variability relative  to that value. Thus a 
measure of total variability  in both directions is 
typically used to summa rize risk. The more intui-
tive concept for risk measurement is the standard 
deviation of the distributi on, a natural measure of 
the spread. Variance , the square of the standard 
deviation, must be used  in comparing indepen-
dent elements of risk. 
On the other hand, when th e shapes of the upper 
and lower tails of the probability distribution are 
different—as they are in the case of catastrophic 
default risk, or whenever an  option is present—it 
may be necessary to take these into account and 
analyze the risky distrib ution more completely. A 
more complete analysis can be accomplished by taking into account not only the spread of the 
distribution (standard deviation or variance) but 
also the asymmetry or sk ewness of the distribu-
tion. 

---
## Page 185

Appendix A
Glossary171risk index A common factor in equity  models that is typi-
cally defined by some co ntinuous measure, as 
opposed to a common industry membership fac-tor, which is defined as 0 or 1. Risk index factors 
include Volatility, Momentum, Size, and Value. 
risk index 
exposure A variable computed for each equity asset that 
determines the asset’s e xposure to a common fac-
tor. Risk indices includ e Market Variability, Earn-
ings Variability, Size, an d Growth. In each case, a 
higher value of the index exposure implies that a company is more strongly  exposed to that com-
mon factor. Risk index e xposures are expressed as 
standardized numbers that range (usually) from–5 to +5. The average (capitalization-weighted) 
stock in the estimation universe has an exposure 
of zero. 
risk model A model that tries to ex plain asset or portfolio 
risk through one or more factors. The Capital 
Asset Pricing Model  is an example of  a risk model. 
In this model, the asset or portfolio’s risk is 
explained by its sensitivity  to the market and the 
market’s risk. See also multiple-factor model .
risk premium An increased expected return to compensate for 
the undesirability of the riskiness of that return. 
A true risk premium must re sult in an increase in 
expected return, not just an increase in promised 
yield that compensates fo r expected loss from 
default and simply preserves expected return over 
different time periods.
risk-free return The return an investor can lock in with certainty at the beginning of an investment period. Con-ceptually, such an investme nt should have guaran-
teed purchasing power at its termination. In 
practice, this rate is usua lly defined by the rate of 
return on short-term government-issued bonds. 
For example in the U.S. model, the 90-day U.S. T reasury bill is used. 

---
## Page 186

Barra Risk Model
Handbook172RMSE See root mean squared error .
root mean 
squared error (RMSE)A measure of goodness of fit to the data. It takes 
into account both an average error, if any, and the 
variability of errors. In fact, it is a measure of the 
typical magnitude of error. It is equal to the 
square root of the averag e squared error. The root 
mean squared error is always larger than the stan-dard error, except in the case where the average 
error is zero, in which case the two are equal.
S
sector-by-rating Process used by Barra to model credit risk for the 
most active markets. When possible and appropri-
ate, issues are categorized  both by sector and by 
rating, to more accurately capture risk.
shift A near-parallel movement of the term structure (in spot rate  space). Historical regressions have 
been run to define the typical shape as well as 
magnitude of a one-standard deviation shift over 
a one-year horizon. Generally, countries with more volatile term structur es can be expected to 
have larger shift risk .
shift risk The part of risk due to exposure to shift move-
ments in the term structure .
shock Change imposed on the term structure to value a 
bond’s exposures to different factors.
sovereign bond Bond issued by a government.
specific return The part of the excess return  not explained by 
common factors . The specific return is indepen-
dent of (or uncorrelated with) the common fac-tors and specific returns of other assets.

---
## Page 187

Appendix A
Glossary173specific risk The uncertainty in asset or portfolio return that 
arises from unpredictability that is specific to that 
asset. This risk is unrelated to all other assets or common factors. Specific ris k is also called idio-
syncratic, or independent risk.
spot rate A rate prevailing from the present to any particu-
lar future date. There is a different spot rate for every future date. The seri es of spot rates at the 
different maturiti es gives the term structure . Spot 
rates can be calculated using different techniques, such as bootstrapping . Barra estimates every local 
term structure by min imizing the differences 
between market and fitted  prices, subject to a 
smoothing constraint.
 spread The difference between yiel ds on securities with 
different credit qualities. 
The spread used over the sovereign yield curve to 
price non-government bonds is typically derived 
from the swap curve  in each market, although 
some markets have deta iled sector-by-rating 
spreads available and some emerging markets have 
emerging spreads. The standard deviation of changes in spread is us ed to approximately cap-
ture systematic spread risk  for non-government 
securities. 
spread duration The sensitivity of a bond’s  price to a change in its 
option-adjusted spread (OAS)  (with the spot term 
structure  held constant).
For corporate bonds, sp read duration will be 
equivalent to effective duration . For floating-rate 
notes (FRN), spread durati on is likely to be 
longer than term structure duration since a 
change in OAS affects all the cash flows  over the 
life of the instrument, ye t term structure sensitiv-
ity is effectively concentrated in the current cou-
pon period (until reset).

---
## Page 188

Barra Risk Model
Handbook174spread factor A risk factor that captur es typical movements in 
interest rate spread level. Spread factors in Barra’s 
risk model include non-government spread (also known as credit spread  and s wap spread ) and 
emerging-market spread . 
spread risk The risk due to exposure to spread movements.
standard 
deviationA statistical term which measures the spread of 
variability of a probability  distribution. It is the 
square root of variance . Standard deviation is 
widely used as a measure of risk or volatility of 
portfolio investments. A higher standard devia-
tion indicates a product with more risk. A prod-
uct’s portfolio is expected  to differ positively or 
negatively from the mean return by no more than 
the standard deviation am ount for approximately 
68% of its cycle.
standardization The process of scaling descriptors  and risk indices . 
Standardization involves setting a common (stan-
dard) zero point and scale for measuring a vari-
able. The mean value is subtracted from a distribution, then all the values are divided by the 
standard deviation. The result is a distribution 
with mean of zero and st andard deviation of one. 
Standardization is typically done to convert 
“apples and oranges” to “apples and apples” so 
that comparisons can be made across data items and across time. Standardization is applied to all 
Barra descriptors before co mbining them into risk 
index values. The risk index values themselves are then standardized. 
stochastic A term synonymous with random—that is, hav-ing unpredictable events that obey a probability 
distribution. It is often us ed in statistics to refer 
to a random process, with the term random itself 
being reserved for the simplest forms of probabil-
ity distributions, which give equal likelihood to 
all outcomes.

---
## Page 189

Appendix A
Glossary175stripped spread A bond’s stripped spread is  calculated by subtract-
ing the present value of the collateralized cash flow  
(escrowed interest payment and collateralized principal). The adjusted price is then equated to 
the remaining non-collateralized cash flows, 
which are discounted at a spread over the base 
curve. This constant spread over the default-free 
curve is the stripped spread.
swap A financial obligation to exchange the cash flows 
of two interest-rate inst ruments. This can happen 
between a floating-rate instrument and a fixed-
rate security, or between bonds of different sec-
tors and maturities. Swaps occur when it is advantageous for both parties to assume the 
swapped financial obligati on because of situations 
unique to the parties concerned.
swap curve A curve that plots swap rates  at different maturi-
ties.
swap rate Interest rate  based on a swap  contract.
swap spread Difference between the swap  and sovereign  curves.
systematic 
return The component of return th at is associated with 
the broad-based market portfolio. Also, the 
reward expected from th e market portfolio and 
the risk of that reward are referred to as system-atic reward and systematic risk . More generally, the 
risk and reward of any asse t that can be associated 
with that asset’s exposure to the market are termed systematic. System atic reward generally 
refers to the excess return, rather than the total 
return, associated with the market.

---
## Page 190

Barra Risk Model
Handbook176systematic risk That part of risk associated with exposure to the 
systematic portfolio. Total risk can always be 
decomposed, for any given definition of system-atic portfolio, into the systematic component that 
is related to that portfolio and the residual com-
ponent that is unrelated to it.
Systematic risk is the standard deviation of system-
atic return . Systematic return is portfolio return 
due to the same forces th at influence the return 
on the benchmark. Systematic risk can be 
thought of as the portfolio risk that can’t be 
diversified away.
T
terms and 
conditions (TNC)All features of a bond th at may be important to 
the investor and that may influence market value. 
These include the payment schedule for the bond, options attached to the bond, marketability 
of the bond, or any othe r characteristics of the 
issuer.
term structure A full schedule of spot rates , forward rates , par 
yields, or pure discount bond prices. Interest rate movements are expressed in terms of changes in 
zero-coupon bond yields inferred from a combi-
nation of money-market rates and coupon bond 
yields. The zero-coupon yield curve is also 
referred to as the “term structure of interest 
rates,” or sometimes just “term structure.” 
term structure 
exposureA mapping of bond or portfolio classifications to 
the Barra term structure  vertices. The weight at 
each vertex represents the percentage of bond or 
portfolio value “thrown off” and is therefore 
related to Macaulay duration . 

---
## Page 191

Appendix A
Glossary177term structure 
factorA factor that describes a typical term structure  
movement. For most markets, the Barra risk 
model defines three movements: shift, twist, and butterfly.
term structure 
riskThe part of risk du e to exposure to term structure  
movements.
time to maturity The length of time betwee n the current date and 
the maturity date of a fixed-income security, 
expressed in years.
TNC See terms and conditions .
total return The total (gross) return to a portfolio including 
capital gains and divide nd income. For global 
equity models, the total return is calculated with respect to a currency perspective or base currency. 
The monthly total return is calculated assuming a 
buy and hold strategy. The holdings at the begin-ning of the month are assumed to be held until 
the end of the month with no transactions. 
total risk The total (gross) risk to an asset, which is the standard deviation of the asset’s total return dis-
tribution. We forecast total risk using Barra’s mul-tiple-factor model. 
tracking error A measure of active port folio risk which indicates 
how closely the portfolio return tracks the bench-
mark return. T racking error is the standard devia-
tion of the difference of returns between a portfolio and the benchma rk position over a spec-
ified holding period. 

---
## Page 192

Barra Risk Model
Handbook178twist The non-parallel change in the term structure  
where the short end of the curve moves in the 
opposite direction of the long end of the curve. 
This is commonly referred to as a flattening or 
steepening of the curve. Hi storical regressions are 
run to define the typica l shape and magnitude of 
a one-standard deviation twist over a one-year 
horizon. By definition, the twist movement is nearly orthogonal to both shift and butterfly  
movements within a market.
twist risk The part of risk due to exposure to twist move-
ments in the term structure .
U
universe The list of all assets eligible for consideration for 
inclusion in a portfolio. 
unsystematic 
returnSee residual return .
V
value at risk 
(VaR) A measure that characterizes  the potential loss in 
currency units in a given time period for a given 
probability level. For example, a VaR of 
–1,000,000 at the 5% probability level indicates there is a 5% probability one would lose up to 
1,000,000 in the coming year. 
value stock A stock is considered to be a value stock based on 
the relationship between its market price and its 
book price. Value stocks are considered attractive because the company is undervalued.

---
## Page 193

Appendix A
Glossary179variance A measure of the variability of variables around 
the mean. Variance is defined as the expected 
squared deviation of the random variable from its mean—that is, the aver age squared distance 
between the mean value and the actually observed 
value of the random variable. When a portfolio 
includes several independen t elements of risk, the 
variance of the total arises as a summation of the variances of the separate components. 
volatility A measure of a share’s propensity to go up and down in price. A volatile share is one which has a 
tendency to move drastically across a broad share 
price range. Mathematically , this is expressed as 
the standard deviation from the average perfor-
mance. 
In general, high volatility means high unpredict-
ability, and therefore greater risk. Numerous attempts have been made to incorporate volatility 
into pricing models, but the problem has always 
been that past volatility is not necessarily a good guide to future volatility.
W
weighting 
schemeA method of assigning importance to each com-
ponent of a summation process. Weights denote the relative importance of various items in an 
average, and the weights are summed up to one.
winsorization A procedure where the outliers are replaced by the two (one positive and one negative) remain-
ing extreme values. That is, the extreme values are moved toward the center of the distribution. This 
technique is sensitive to the number of outliers, 
but not to their actual values.

---
## Page 194

Barra Risk Model
Handbook180Y
yield The return on a security or portfolio in the form 
of cash payments. Most yield comes from divi-
dends on equities, coupons on bonds, or interest on mortgages. In general, yield is defined in 
terms of the component of return that is taxable 
as ordinary income. Conse quently, since the capi-
tal gain on a short-term government bond (trea-
sury bill) or other discount note is viewed for tax 
purposes as a form of inte rest, it is al so included 
in the definition of yield. 
yield curve The plot of yield-to-maturity  against term-to-
maturity. See also term structure .
yield spread The spread in yield between a particular bond 
and a comparabl e liquid government benchmark 
issue. Yield spread reflects the difference in yield 
between a particular bond and its corresponding pricing curve, be it the sovereign spot curve for 
government bonds or the swap curve for Euro-
bonds.
yield-to-maturity The yield if the bond is he ld to maturity. It is the 
yield that equates the net present value  of the 
future cash flows  of the security (as of the matu-
rity date) to its curr ent market price. This 
assumes that the redemptio n date is the maturity 
date and uses the corresponding redemption 
price. Calls and puts are not taken into account.
Z
zero-coupon 
bondA bond that is issued wi thout a coupon. At matu-
rity it is redeemed at its face amount.

---
## Page 195

Appendix B
Contributors181Contributors
Principal Contributors
Dan Stefek
Davide Cis
Greg Anderson
John TaymureeJustine Withers
Kathy Sorge
Lisa GoldbergLudovic Breger
Manjula Lind
Neil GilfedderOren Cheyette
Tim Tomaich
Contributors
Adam CaoAgnes Hsieh
Anton PoutchkovBrian Ascough
Cristin Williams
Darren StovelGreg Connor
Guy Miller
John DibsMichael Lan
Ozlem Peksoy
Peng CaoQue Chu
Mauricio Lara
Vinod ChandrashekaranWenhsyong Lin
Writer/Editor
Kevin G. Lim

---
## Page 196

Barra Risk Model
Handbook182

---
## Page 197

Index183A
APT
see Arbitrage Pricing Theory
Arbitrage Pricing Theory (APT) 19Average specific risk 34
B
Barra
corporate history v
Web site vi
Barra Integrated Model
core and global factors 126–127
covariance matrix 125–127
currency model 123–124global bonds 118–123
global equities 114–117
local models and global models 
110–114
overview 109–110
specific risk 125
Benchmark yield curve 57
Beta 17
Breiman, Leo 15
C
Capital Asset Pricing Model 
(CAPM) 16–19
CAPM
see Capital Asset Pricing Model
Common factors 1
see also risk factors
Connor, Gregory 2
Consumer Price Index (CPI) 53
Corporate risk
see spread risk
Correlation
credit spread 73Credit spread factors in Barra In-
tegrated Model 120currency 99
Emerging-market factors in Bar-
ra Integrated Model 121
Global equity and fixed-income 
factors in Barra Integrat-
ed Model 126
Shift, twist, butterfly, and swap 
spread factors in Barra 
Integrated Model 120
see also covariance matrix
Covariance matrix
Barra Integrated Model 111–
114, 125–127
currency 98–105
emerging-market risk model 80–
81
equity risk model 27–32
global bond factors 122global equity factors 117
interest rate risk model 66–67
methods of esti mation compared 
3–5
overview 8–11
CPI 53Credit spread risk model 46–47, 71–
78
Currency risk model
covariance matrix 98–105
data acquisition 98
factor exposure 42in Barra Integrated Model 123–
124
structure 97time-scaling forecasts 105
updating 106
D
Daily exponentially weighted index Index

---
## Page 198

Barra Risk Model
Handbook184volatility (DEWIV) 29
Data acquisition
credit spread risk model 77
currency risk model 98emerging market risk model 80
equity risk model 24
interest rate risk model 52
specific risk model (fixed-in-
come) 83
swap spread risk model 70
Descriptors (equity)
selection 21, 24standardization 25
DEWIV model 29
Diversification 16Dollar market
see U.S. fixed-income market
Duration 39
E
Effective duration 64
Emerging market risk model 46–47, 
78–81
Equity risk model
common factors 20
covariance matrix 27–32data acquisition 24
descriptors 24–25
estimation process 21–23factors 25–27
in Barra Integrated Model 114–
117
industries 20, 26
multiple-factor model 19
overview 19relationship between returns and 
beta 17
risk indices 20specific risk 20, 33–34
updating 35
Estimation universe 10
Euro zone fixed-income market
benchmark 57in Barra Integrated Model 119, 122, 126
specific risk 86–94
spread risk 69, 71–78
Europe equities in Barra Integrated 
Model 116
Exponential weighting
in currency risk model 102
in equity risk model 28
Exposures
equity 25–26
fixed income 42
multiple-factor models 7sector-by-rating credit spread 78
shift, twist, butterfly 64
swap spread 70
Extended GARCH model for equity 
markets 29
F
Factor exposure
see exposures
Factor returns
estimation in equity model 21, 
27
multiple-factor models 7
shift, twist, butterfly 65swap spread 70
Factors
see risk factors
Fixed-income risk model
see interest-rate risk model
Fundamental factor models 1–2
G
GARCH (general auto-regressive 
conditional heteroskedastici-
ty) model
equity 29–31
in currency risk model 100
integrated GARCH 102
General auto-regressive conditional 
heteroskedasticity
see GARCH

---
## Page 199

Index185Government risk overview 51–52
H
Half-life
see exponential weighting
Heuristic specific risk model (fixed-
income) 83–86
I
IGARCH model 102
Industries
in equity model 20, 26
in interest rate risk model 69, 
71–78
Inflation-protected bonds 53
data acquisition 52interest rate factors 63
term structure specification 58
Integrated risk model
see Barra Integrated Model
Interest rate risk model
alternative models 39, 48benchmark yield curve 57
covariance matrix 66–67
data acquisition 52estimation process 51–52
factor exposure 64
factor returns 65–66factors 41–42
in Barra Integrated Model 118–
123
overview 40–49
specific risk 49
spread risk 46–48term structure specification 43–
45, 55–63
U.S. municipal bonds in 54updating 67
J
Japan Equity Risk Model industry 
exposures 26
Japan fixed-income market
benchmark 57in Barra Integrated Model 119, 
122, 126
spread risk 69, 71–78
JPE3
see Japan Equit y Risk Model
K
Kelly, John L., Jr. 15
Key rate model 48, 54
L
LIBOR 57, 58, 61Local market factors
in interest rate risk model 41–42
see also specific risk, spread risk, 
term structure
M
Macroeconomic factor models 1–2
Market data
for equity risk model 21for interest-rate risk model 52
Market risk 15–17
Market volatility 29Markowitz, Harry 15, 16
Maturities 51, 55
MFM
See multiple-factor model
Model estimation process
Barra Integrated Model 110credit spread risk model 77
currency risk model 98
emerging market risk model 80equity risk model 21–23
heuristic specific risk model 
(fixed-income) 83
interest rate risk model 51–52
swap spread risk model 70
transition-matrix specific risk 
model (fixed-income) 86
Model updates
currency risk 106
equity risk 35
interest rate risk 67

---
## Page 200

Barra Risk Model
Handbook186specific risk (fixed-income) 94
spread risk 81
Models
fundamental factor 1–2macroeconomic factor 1–2
single-factor 6
statistical factor 1
see also Barra In tegrated, curren-
cy, equity, interest rate, multiple-factor model, 
specific, spread
Multiple industry al location in equi-
ty risk model 26
Multiple-factor model (MFM)
advantages 2–3covariance matrix 8–11
definition 1
equations 6, 10example 3–5
excess return 6, 8
exposures 7factor returns 7
limitations 3
risk prediction 2, 8–11types 1
Municipal bonds 54
Munis
see municipal bonds
N
Normalization
of equity risk descriptors 25of term structure factors 64
P
Persistence constant 101–102Pound market
see U.K. fixed-income market
Pricing errors (fixed-income term 
structure) 59
Principal components
see shift, twist, and butterflyPrincipal components analysis 52
Q
Quality control
equity risk descriptors 24
equity risk model 22
term structure 58
R
Real bonds
see inflation-protected bonds
Residual risk 16
Returns
see factor returns
Risk 1
Risk decomposition
equity 20
fixed-income 40
Risk factors 2
credit spread (fixed-income) 42, 
46–47
currency 42emerging market spread (fixed-
income) 42, 46–47
industries (equity) 20interest rate (fixed-income) 42, 
43–45
risk indices (equity) 20swap spread (fixed-income) 42, 
46–47
Risk indices
definition 20
descriptors 24–25
formulation 25
Risk prediction with MFMs 8
Risk, specific
see specific risk

---
## Page 201

Index187Risk, systematic 15–17
Rosenberg, Barr 1, 19
Ross, Stephen A. 19
Russian government default 39, 57
S
Scaling
equity covariance matrix 31equity specific risk 33
global factors to local markets 
117, 123, 127
time-scaling of currency risk fore-
casts 105
Sensitivity constant 101–102Sharpe, William 16, 18
Shift, twist, an d butterfly 43–45, 63
covariance matrix 66–67exposures 64
normalization 64
returns 65
Short-end of term structure 61
Single-factor model 6
Sovereign risk overview 51–52Specific return 83
see also specific risk model
Specific risk model (equity) 20
methodology 33–35
overview 33
updating 35
Specific risk model (fixed-income)
heuristic 83–86
overview 83transition-matrix-based 86–94
Specific risk models (fixed-income)
updating 94
Spread duration
sector-by-rating credit 78
stripped 81swap 70
Spread risk model 46–47, 69
emerging market 78–81
sector-by-rating credit spread 
71–78
swap 70–71updating 81
Statistical factor models 1
STB
see shift, twist, and butterfly
Sterling market
see U.K. fixed-income market
Stock risk model
see equity risk model
Stripped-spread duration 81Swap curve 46–47, 57
Swap spread risk model 46–48, 70–
71
Systematic risk 15–17
Systematic scaling 29
T
Term structure
inflation-protected bonds 58
pricing errors 59
quality control 58short-end of term structure 61
smoothing 59
specification 55–63see also interest rate risk model
TIPS
see inflation-protected bonds
Transition matrix for specific risk 
(fixed-income) 86–94
Treasury inflatio n-protected bonds
see inflation-protected bonds
U
U.K. fixed-income market
benchmark 57in Barra Integrated Model 119, 
122, 126
specific risk 86–94spread risk 69, 71–78
U.S. agency bond benchmark 57
U.S. dollar market
see U.S. fixed-income market
U.S. Equity Risk  Model, Multiple-
Horizon
factors in covariance and variance 

---
## Page 202

Barra Risk Model
Handbook188calculations 9
industry exposures 26
U.S. fixed-income market
in Barra Integrated Model 119, 
122, 126
inflation-protected bonds 53
municipal bonds 54
specific risk 86–94
spread risk 69, 71–78
Updating risk models
currency 106
equity 35interest rate 67
specific (fixed-income) 94
spread 81
USE3
see U.S. Equity Risk Model, 
Multiple-Horizon
V
Variance
see covariance matrix
Vertices (interest rate  term structure) 
55
Volatility
beta 17calculation in multiple-factor 
model 12
currency 100–105equity markets 29
see also spread risk model, specif-
ic risk model (fixed-in-come) 71
W
Weighting
term structure pricing error 59term structure short-end shape 
correction 62
term structure smoothing 60–61
Weighting, exponential
in currency risk model 102in equity risk model 28Y
Yen market
see Japan fixed-income market
Yield curve 57
see also interest rate risk model

