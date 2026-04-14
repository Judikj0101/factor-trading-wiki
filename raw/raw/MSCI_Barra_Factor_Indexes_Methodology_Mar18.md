# MSCI Barra Factor Indexes Methodology Mar18

> Extracted from: `MSCI_Barra_Factor_Indexes_Methodology_Mar18.pdf` (25 pages)

---
## Page 1

 
 
 MARCH 2018  INDEX METHODOLOGY   
MARCH 2018  
MSCI BARRA FACTOR 
INDEXES METHODOLOGY  
  
March  2018 
  

---
## Page 2

 
 
 
 MSCI.COM | PAGE 2 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
 
 
1 Introduction  ................................ ................................ ................  3 
2 Main Characteristics of MSCI Long -Short Barra Factor Indexes  ... 4 
3 Constructing the MSCI Long -Shor t Barra Factor Indexes  .............  5 
3.1 Specifying the Parent Index, Benchmark and the Barra Equity Model for 
optimization  ................................ ................................ ................................ ........  5 
3.2 Speci fying the Target Factor and optimization objectives  .......................  6 
3.3 Specifying the optimization constraints  ................................ ...................  6 
3.4 Calculating the optimized index  ................................ ...............................  7 
4 Maintaining the MSCI Barra Factor Indexes  ................................  8 
4.1 Monthly index reviews  ................................ ................................ .............  8 
4.2 Ongoing event related changes  ................................ ...............................  8 
Appendix I: Current List of MSCI Barra Factor Indexes as of June 2009
................................ ................................ ................................ .........  10 
Appendix II: Optimization  Settings for Constructing MSCI Long -Short 
Barra Factor Indexes  ................................ ................................ ........  11 
Appendix III: Monthly Rebalancing Timeline  ................................ .... 14 
Appendix IV: Defining Shorting Cost Cutoff  ................................ ...... 15 
Appendix V: Defining Trade Limits  ................................ ...................  16 
Appendix VI: Handling Infeasible Optimizations  ..............................  17 
Appendix VII: New release of Barra Equity Model or Barra Optimizer
................................ ................................ ................................ .........  18 
Appendix VIII: Barra Model Data Delays or Corrections  ...................  19 
Appendix IX: Constructing the MSCI Long -Only Barra Factor Indexes
................................ ................................ ................................ .........  20 CONTENTS  

---
## Page 3

 
 
 
 MSCI.COM | PAGE 3 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
1 INTRODUCTION  
Fundamental factors have become increasingly important in various areas  of the investment 
process, including risk management and portfolio construction. Fundamental factors 
represent sources of systematic risk and return.  
MSCI has done extensive research to identify the common factors driving equity markets 
and build factor m odels to capture these common sources of risk and return. MSCI research 
shows that three types of fundamental factors account for a significant part of the 
commonality in equity returns across different markets and time periods: country factors, 
industry f actors, and style factors. The main style factors include size, value, momentum, 
volatility, and growth, to name just a few.  
MSCI has developed a family of Barra Factor Indexes that aim to capture some of these 
important style factors in an index. The MSCI  Long -Short Barra Factor Indexes are 
constructed by optimizing a parent MSCI Index to achieve a specified  high level of exposure 
to a particular style factor (herein, “Target Factor”), very low exposure to all other style, 
industry and country factors, and  low tracking error to a corresponding MSCI benchmark 
index1 (herein, “Benchmark”). For institutional investors with restrictions on shorting, MSCI 
also calculates MSCI Long -Only Barra Factor Indexes constructed using a similar optimization 
process but des igned to maximize exposure to the Target Factor while controlling exposure 
to other factors and minimizing tracking error relative to the Benchmark. MSCI currently 
offers Barra Factor Indexes that target the momentum, leverage, volatility, value and 
earnin gs yield factors and may expand the index family to cover a wider range of factors.  
This methodology book describes a generic methodology to create MSCI Barra Factor 
Indexes based on the existing MSCI global or domestic equity indexes (herein, “Parent 
Inde xes”) using the Barra Optimizer and the relevant Barra Equity Model. Further  
information about the MSCI Barra Factor Indexes, Barra Optimizer and the various Barra 
Equity Models can be found at  www.msci. com/research -archive . 
                                                      
1 Typically the corresponding MSCI  Standard Index  

---
## Page 4

 
 
 
 MSCI.COM | PAGE 4 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
2 MAIN CHARACTERISTICS  OF MSCI LONG -SHORT BARRA FACTOR 
INDEXES  
The MSCI Long -Short Barra Factor Indexes  aim to have the following characteristics : 
 Performance similar to that of the Benchmark plus the Target Factor  
 Specified high exposure2 to the Target Factor relative to the Benchmark  
 Low exposure to other factors relative to the Benchmark  
 Low tracking error relative to the Benchmark  
 Controlled level of index turnover  
 Monthly rebalancing  
A pure factor replicating index could be composed of all securities present in the estimation 
universe of the relevant Barra Equity Model (typically thousands of large, mid and small 
capitalization securities) with long and short  positions. This index woul d incur high turnover 
with most security weights changing at each monthly update of the model. A methodology 
to create reasonably replicable indexes  needs to incorporate a number of constraints, such 
as constraints on the number of index constituents, mont hly index turnover , trade limit and 
shorting costs to achieve replicability and investability . 
                                                      
2 The target factor exposure may be positive or negative depending on the Target Factor. Please refer to Appendix I.  

---
## Page 5

 
 
 
 MSCI.COM | PAGE 5 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
3 CONSTRUCTING THE MSC I LONG -SHORT BARRA FACTOR I NDEXES3 
The MSCI Long -Short Barra Factor Indexes  are constructed by optimizing an MSCI Parent 
Index to achieve a s pecified stable level of exposure to the Target Factor and a controlled 
level of exposure to all other style, industry and country factors, while minimizing the 
tracking error relative to the Benchmark, for a given set of constraints. Constructing the 
MSCI  Barra  Factor Indexes  involves the following steps:  
 Specifying the Parent Index , Benchmark  and the Barra Equity Model for optimization  
 Specifying the Target Factor and optimization objective  
 Specifying the optimization constraints  
 Calculating the optimized  index  
The steps for constructing the MSCI Long -Short Barra Factor Indexes  are described below.  
3.1 SPECIFYING  THE PARENT INDEX, BE NCHMARK AND THE BARR A EQUITY MODEL 
FOR OPTIMIZATION  
Constructing  the MSCI Barra Factor Indexes begins with selecting the Parent Index, 
Benchmark and the relevant Barra Equity Model for the optimization. For the MSCI Long -
Short Barra Factor Indexes:  
 the Parent Index is the corresponding MSCI Investable Market Index and serves as the 
universe of eligible securities for the optimization ; 
 the Benchmark for the optimization is the corresponding MSCI Standard Index;  and 
 the Barra Equity Model is the corresponding global, regional or single country Barra 
Equity Model . 
For exam ple, to construct the MSCI Europe Long -Short Barra Factor Indexes, the MSCI 
Europe Investable Market Index would be used as the universe of eligible securities, MSCI 
Europe Index would be used as the Benchmark for the optimization, and the Barra Europe 
Short-Term Model would be used as the risk model for the optimization.  
The optimization relies on the factor exposures for all the securities in the Parent Index and 
the factor co -variance matrix of the relevant Barra Equity Model. The optimization is 
perform ed from a base currency perspective (e.g., Euro for the MSCI Europe Barra Factor 
Indexes) and allows short selling of securities.   
                                                      
3 Please refer to Appendix IX for the construction of MSCI Long -Only Factor Indexes.  

---
## Page 6

 
 
 
 MSCI.COM | PAGE 6 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
3.2 SPECIFYING THE TARGE T FACTOR AND OPTIMIZ ATION OBJECTIVES  
The optimization objective of the MSCI Long -Short Barra Factor Index  is to have the lowest 
tracking error relative  to the Benchmark, subject to the optimization constraints specified in 
Section 3.3.  
Depending on the Target Factor, the MSCI Long -Short Barra Factor Index will target 1 or -1 
standard deviation of exposure rel ative to the Benchmark. Please refer to Appendix I for the 
current list of MSCI Long -Short Barra Factor Indexes and their Target Factor Exposure.  
3.3 SPECIFYING THE OPTIM IZATION CONSTRAINTS  
At each monthly index rebalancing, a number of optimization constraint s are employed in an 
effort to control the level of active exposure to other factors, as well as to achieve a balance 
between the objectives of replicability and investability, high exposure to the Target Factor, 
low tracking error  to the Benchmark , limite d stock specific risk, and low index turnover . 
 At each monthly index rebalancing, the Target Factor exposure of the MSCI Long -Short 
Barra Factor Index will be fixed at a pre -defined level as specified in Appendix I (i.e., one 
standard deviation above or be low the Target Factor exposure of the Benchmark, in 
absolute terms).  
 At each monthly index rebalancing, the Barra style factor exposure of the MSCI Long -
Short Barra Factor Index will not deviate more than +/ - 0.1 standard deviations from the 
Barra style fa ctor exposure of the Benchmark, in absolute terms,  with the exception of 
the Target Factor.  
 At each monthly index rebalancing, the Barra industry factor exposure of the MSCI Long -
Short Barra Factor Index will not deviate more than +/ - 0.5% from the Barra i ndustry 
factor exposure of the Benchmark, in absolute terms.  
 At each monthly index rebalancing, the Barra country factor exposure of the MSCI Long -
Short Barra Factor Index will not deviate more than +/ - 0.5% from the Barra country 
factor exposure of the B enchmark, in absolute terms.  
 At each monthly index rebalancing, the MSCI Long -Short Barra Factor Index will only 
include securities that are constituents of the Parent Index . 
 At each monthly index rebalancing, the MSCI Long -Short Barra Factor Index will have 
short positions only  in securities whose Shorting Cost is below the Shorting Cost Cutoff 
defined in Appendix IV  
 At each monthly index rebalancing, the leverage of the MSCI Long -Short Barra Factor 
Index  will be fixed at a pre -defined level as specified  in Appendix I.  

---
## Page 7

 
 
 
 MSCI.COM | PAGE 7 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
 At each monthly index rebalancing, the number of index constituents is constrained to a 
maximum of 4 00. 
 At each monthly index rebalancing, the one -way index turnover of the MSCI Long -Short 
Barra Factor Index is constrained to a maximum of 5 % of the gross initial portfolio (Sum 
of absolute value of the long and short equity position).  
 At each monthly index rebalancing, the weight of each index constituent will not change 
more than a predefined Trade Limit4 linked to the stock’s Average Daily Traded Value.  
 At each monthly index rebalancing, the weight of an index constituent will not deviate 
more than +/ - 2% from its weight in the Benchmark. When this constraint is in conflict 
with the Trade Limit constraint defined above, the Trade Limit const raint takes 
precedence.  
3.4 CALCULATING THE OPTI MIZED INDEX  
The MSCI Barra Factor Index is constructed using the Barra Optimizer in combination with 
the relevant Barra Equity Model. The optimization uses the MSCI Parent Index as the 
universe of eligible securi ties and the specified optimization objective and constraints to 
determine the optimal Barra Factor Index. Please refer to Appendix II for the optimization 
settings for constructing the MSCI Long -Short Barra Factor Indexes. In the event of an 
infeasible op timization, the rules outlined in Appendix VI will be followed.  
                                                      
4 Please refer to Appendix V  for the calculation of the Trade Limit.  

---
## Page 8

 
 
 
 MSCI.COM | PAGE 8 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
4 MAINTAINING THE MSCI  BARRA FACTOR INDEXES  
4.1 MONTHLY INDEX REVIEW S 
The index review of the MSCI  Barra  Factor Indexes  is scheduled for the beginning of each 
month following the release by Barra to its clients of the monthly updates of the security 
exposure data and factor co -variance data of the relevant Barra Equity Model. The 
rebalancing date for the MSCI Barra Factor Indexes is as specified in Appendix III (the 
“Rebalancing Date”).  The Rebala ncing Date of the MSCI Barra Factor Indexes may vary 
depending on the release date of the monthly update of the corresponding Barra Equity 
Model . The release date of the monthly update of the relevant Barra Equity Model will be 
announced to all Barra Facto r Index clients on or before the release.  
The rebalancing of the MSCI  Barra  Factor Indexes  is conducted as of the close of the 
Rebalancing Date. The changes resulting from the index rebalancing will be announced on 
the close of the Rebalancing Date and wil l be implemented as of the close of the second 
business day following the Rebalancing Date and will be effective from the third business 
day following the Rebalancing Date.  
Please refer to Appendix III for further information about the monthly rebalancing timeline.  
4.2 ONGOING EVENT RELATE D CHANGES  
The general treatment of corporate events in the MSCI Barra Factor Index es aims to 
minimize turnover outside of Index Reviews. The methodology aims to appropriately 
represent an investor’s participation in an event b ased on relevant deal terms and pre -event 
weighting of the index constituents that are involved.  Further, changes in index market 
capitalization that occur as a result of corporate event implementation will be offset by a 
corresponding change in the Varia ble Weighting Factor (VWF) of the constituent.  
Additionally, if the frequency of Index Reviews in the Parent Index is greater than the 
frequency of Index Reviews in the MSCI Barra Factor Index , the changes made to the Parent 
Index during intermediate Inde x Reviews will be neutralized in the MSCI Barra Factor Index .  
 
The following section briefly describes the treatment of common corporate events within 
the MSCI Barra Factor Index es.  
 
No new securities will be added (except where noted below) to the Index  between Index 
Reviews. Parent Index deletions will be reflected simultaneously.  
 
 
 
 

---
## Page 9

 
 
 
 MSCI.COM | PAGE 9 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
EVENT TYPE      EVENT DETAILS    
 
New additions to the Parent Index  A new security added to the parent index 
(such as IPO and other early inclusions) 
will not be added to the index.  
 
Spin -Offs All securities created as a result of the 
spin-off of an existing Index constituent 
will be added to the Index at the time of 
event implementation. Reevaluation for 
continued inclusion in the Index will occur 
at the subsequent Index R eview.  
 
Merger/Acquisition  For Mergers and Acquisitions, the 
acquirer’s post event weight will account 
for the proportionate amount of shares 
involved in deal consideration, while cash 
proceeds will be invested across the 
Index.  
 
If an existing Index const ituent is acquired 
by a non -Index constituent, the existing 
constituent will be deleted from the Index 
and the acquiring non -constituent will not 
be added to the Index.  
 
Changes in Security Characteristics  A security will continue to be an Index 
constituen t if there are changes in 
characteristics (country, sector, size 
segment, etc.) Reevaluation for continued 
inclusion in the Index will occur at the 
subsequent Index Review.  
 
Further detail and illustration regarding specific treatment of corporate events r elevant to 
this Index can be found in the MSCI Corporate Events Methodology book under the sections 
detailing the treatment of events in Capped Weighted and Non -Market Capitalization 
Weighted indexes.  
  
The MSCI Corporate Events methodology book is availa ble at:  
https://www.msci.com/index -methodology  

---
## Page 10

 
 
 
 MSCI.COM | PAGE 10 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
APPENDIX I : CURRENT LIST OF MSCI  BARRA FACTOR INDEXES  AS OF 
JUNE 2009  
MSCI Long -Short Barra Factor Index  Target Factor  Target Factor 
Exposure5 Leverage  
MSCI Europe Barra Momentum Index  Momentum  1 130/30  
MSCI Europe Barra Value Index  Value  1 130/30  
MSCI Europe Barra Low Volatility Index  Volatility  -1 150/50  
MSCI Europe Barra Low Leverage Index  Leverage  -1 130/30  
MSCI Europe Barra Earnings Yield Index  Earnings Yield  1 130/30  
MSCI USA Barra Momentum Index  Momentum  1 130/30  
MSCI USA Barra Earnings Yield Index  Earnings Yield  1 130/30  
MSCI USA Barra Low Volatility Index  Volatility  -1 150/50  
MSCI USA Barra Low Leverage Index  Leverage  -1 130/30  
MSCI USA Barra Value Index  Value  1 130/30  
 
MSCI Long -Only  Barra Factor Index  Target Factor  Target Factor 
Exposure  Leverage  
MSCI Europe Momentum Tilt Index  Momentum  Positive  Long -only  
MSCI Europe Value Tilt Index  Value  Positive  Long -only  
                                                      
5 Relative to the Benchmark  

---
## Page 11

 
 
 
 MSCI.COM | PAGE 11 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
APPENDIX II : OPTIMIZATION SETTING S FOR CONSTRUCTING M SCI 
LONG -SHORT BARRA FACTOR I NDEXES  
The MSCI Barra Factor Indexes  are currently constructed using the Barra Optimizer in 
combination with the relevant Barra Equity Model. The following optimization settings are 
appli ed to construct the MSCI Long -Short Barra Factor Indexes.  
The Barra Equity Model is selected so that the region of the model corresponds to the region 
of the index being calculated.  MSCI currently uses the Barra EUE 3S model  to construct the 
MSCI Europe Ba rra Factor Indexes and the Barra USE3S model to construct the MSCI USA 
Barra Factor Indexes . 
1.0 Specify “Benchmark”, “ Initial  Portfolio” and “Trade Universe” settings on the Barra 
Optimizer  
 “Benchmark” is set to be the corresponding MSCI Standard Index, u sing the index 
constituent weights as of the close of the Rebalancing Date (before the rebalancing) 
updated for corporate actions up to the effective date of the rebalancing . 
 “Initial Portfolio” is set to be the current Barra Factor Index, using the index constituent 
weights as of the close of the Rebalancing Date (before the rebalancing) updated for 
corporate actions up to the effective date of the rebalancing . When there is n o current 
Barra Factor Index (for example, when no optimization has been applied to the Parent 
Index yet), the Initial Portfolio is set to be the Parent Index.  
 “Trade Universe” is set to be the index constituents of the Parent Index (i.e., the 
correspondin g MSCI Investable Market Index).  
2.0 Specify risk model  
 The factor exposures of all securities in the Initial Portfolio and Benchmark are set using 
the most recent monthly release of factor exposure data of the relevant Barra Equity 
Model  
 The common factor  co-variances are set using the most recent monthly release of factor 
co-variance data of the relevant Barra Equity Model  
 The specific co -variances of all securities in the Initial Portfolio and Benchmark are set 
using the most recent monthly release of sp ecific co -variances data of the relevant Barra 
Equity Model  

---
## Page 12

 
 
 
 MSCI.COM | PAGE 12 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
3.0 Setup  utility function  
The optimization objective is to find a pro forma Barra Factor Index that minimizes the 
active risk of the pro forma Barra Factor Index relative to the Benchmark, as det ermined by 
the relevant Barra Equity Model.  
4.0 Setup constraints  
 The Target Factor exposure of the pro forma Barra Factor Index will be fixed at a pre -
defined level as specified in Appendix I (i.e., one standard deviation above or below the 
Target Factor exposure of the Benchmark, in absolute terms)  
 The Barra style factor exposure of the pro forma  Barra Factor Index wi ll not deviate 
more than +/ - 0.1 standard deviations from the Barra style factor exposure of the 
Benchmark , in absolute terms,  with the exce ption of the Target Factor  
 The Barra industry factor exposure of the pro forma Barra Factor Index will not deviate 
more than +/ - 0.5% from the Barra industry factor exposure of the Benchmark, in 
absolute terms  
 The Barra country factor exposure of the pro f orma Barra Factor Index will not deviate 
more than +/ - 0.5% from the Barra country factor exposure of the Benchmark, in 
absolute terms  
 The pro forma  Barra Factor Index will only include securities in the Trade Universe  
 The pro forma Barra Factor Index will  have short positions only in securities whose 
Shorting Cost is below the Shorting Cost Cutoff defined in Appendix IV  
 The leverage of the pro forma Barra Factor Index will be fixed at a pre -defined level as 
specified in Appendix  I 
 The number of index const ituents of the pro forma Barra Factor Index is constrained to 
a maximum of 400  
 The one -way index turnover from the Initial Portfolio (i.e., the current Barra Factor 
Index) to the pro forma Barra Factor Index is constrained to a maximum of 5%  of the 
gross i nitial portfolio (Sum of absolute value of the long and short equity position).  
 For each Barra Factor Index constituent, its weight in the pro forma Factor Index will not 
change more than a predefined Trade Limit6 from its weight in the Initial Portfolio ( i.e., 
the current Barra Factor Index)  
                                                      
6 Please refer to Appendix V  for the calculation of the Trade Limit.  

---
## Page 13

 
 
 
 MSCI.COM | PAGE 13 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
 The weight of an index constituent of the pro forma Barra Factor Index will not deviate 
more than +/ - 2% from its weight in the Benchmark. When this constraint is in conflict 
with the Trade Limit constraint defined abo ve, the Trade Li mit constraint takes 
precedence  

---
## Page 14

 
 
 
 MSCI.COM | PAGE 14 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
APPENDIX III: MONTHL Y REBALANCING  TIMELINE  
The Rebalancing of the MSCI Barra Factor Indexes  occurs after the monthly update of the 
corresponding Barra Equity Model.  
The target release date of the Barra European Equity Model  and the Barra US Equity Model  
monthly update is the first calendar day after the last business day of the previous month . 
The Rebalancing Date for the MSCI Barra Factor Indexes  is the close of the second  business 
day of the rebalancin g month. The changes resulting from the index rebalancing will be 
announced as of the close of the second  business day, implemented as of the close of the 
fourth  business day, and effective from the fifth business day of the rebalancing month.  

---
## Page 15

 
 
 
 MSCI.COM | PAGE 15 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
APPENDIX IV:  DEFINING SHORTING CO ST CUTOFF  
For a currently shorted constituent, if a security’s Shorting Cost at the monthly index review 
exceeds a Shorting Cost Cutoff of 300 basis points, the security will be excluded from the 
short position of the MSCI Barra Factor  Index . For a new security, the Shorting Cost cut off is 
250 basis points.  If a security is not covered by the shorting cost data, it will also be excluded 
from the short position of the MSCI Barra Factor Index.  

---
## Page 16

 
 
 
 MSCI.COM | PAGE 16 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
APPENDIX V : DEFINING TRADE LIMIT S 
In the monthly index review, the Trade Limit for each security (i.e., the maximum security 
weight change) is calculated as 10% of its Average Daily Traded Value, assuming a portfolio 
value of 1 billion USD:  
Trade Limit = (10% * Average Daily Traded Value) / 1 bil lion 
The Average Daily Traded Value of a security is calculated as the average of the daily traded 
values in the one month prior to the Rebalancing Date. The daily traded value of a security is 
equal to the number of shares traded during the day, multiplie d by the closing price of that 
security.  

---
## Page 17

 
 
 
 MSCI.COM | PAGE 17 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
APPENDIX VI : HANDLING INFEASIBL E OPTIMIZATIONS  
During the monthly index review, in the event that there is no optimal solution that satisfies 
all the optimization constraints defined in Section 3.3, the constraints will be relaxed 
sequentially as follows, until an optimal solution is found:  
1. Relax the turnover constraint  and factor exposure constraints on style, industry and 
country factors, with violation of the constraint s discouraged by penalties. This is 
achieved automatically using the Soft Constraint feature of the Barra Optimizer , by 
setting both turnover constraint and factor exposure constraints as Soft Constraint . 
2. Relax the trade limit constraint by allowing two times the original Trade Limit for each 
securit y. 
3. Relax the constraint on index constituent weight by constraining the weight of an index 
constituent to deviate no more than +/ - 2.5% from its weight in the Benchmark, instead 
of no more than +/ - 2.0%  
4. Relax the maximum number of index constituents to 1.2 5 times the original maximum 
number of stocks.  
The above constraint relaxation sequence is followed mechanically. In the event that no 
optimal solution is found after all the above constraints have been relaxed, the relevant 
Barra Factor Index will not be rebalanced for that month.  

---
## Page 18

 
 
 
 MSCI.COM | PAGE 18 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
APPENDIX VII : NEW RELEASE OF BARRA  EQUITY MODEL OR BARRA 
OPTIMIZER  
A new release of the relevant Barra Equity Model or Barra Optimizer may  replace the former 
version within a suitable timeframe . 

---
## Page 19

 
 
 
 MSCI.COM | PAGE 19 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
APPENDIX VIII : BARRA MODEL DATA DELAYS OR CORRECTION S 
If there is a delay in the monthly release of security exposure data and factor co -variance 
data of the relevant Barra Equity Model, all MSCI Barra Factor Index clients will be notified, 
and the monthly index review of the relevant MS CI Barra Factor Indexes  will be delayed until 
the relevant Barra model data is available. In the event that the relevant Barra model data is 
delayed for more than 5 business days after the target release date, the index review of the 
relevant MSCI Barra Factor Indexes  will not be conducted for that month.  
If there is a correction of the relevant Barra model data within 5 business days following the 
Rebalancing Date, and the impact of the correction is determined to be significant , a new 
index review will be  conducted for the relevant MSCI Barra Factor Indexes . The impact of 
the correction will be considered significant when either the impact on the  Target Barra 
Factor exposure of the relevant MSCI Barra Factor Indexes is above a threshold of 0.1, or the 
impa ct on the Active Risk of the relevant MSCI Barra Factor Indexes is above a threshold of 
0.5% in absolute terms.  
All MSCI Barra Factor Index clients will be notified at the time of a relevant Barra model data 
correction. The new index review will be conduc ted and announced on the close of the 
second  business day following the Barra data correction. The changes resulting from the 
new index review will be implemented as of the close of the fourth  business day following 
the Barra data correction (effective on the fifth business day following the Barra data 
correction). The index levels of the relevant MSCI  Barra  Factor Indexes  prior to the new 
index review will not be restated.  

---
## Page 20

 
 
 
 MSCI.COM | PAGE 20 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
APPENDIX IX: CONSTRUCTING THE MSC I LONG -ONLY BARRA 
FACTOR INDEXES  
The MSCI Long -Only  Barra Factor Indexes  aim to have the following characteristics:  
 Performance similar to that of the Benchmark with a tilt towards the Target Factor  
 High exposure to the Target Factor relative to the Benchmark  
 Low exposure to other factors relative to the B enchmark  
 Low tracking error relative to the Benchmark  
 Controlled level of index turnover  
 Monthly rebalancing  
The MSCI Long -Only Barra Factor Indexes  are constructed by optimizing an MSCI Parent 
Index to maximize exposure to the Target Barra Factor while controlling exposure to other 
factors and minimizing tracking error relative to the Benchmark, for a given set of 
constraints. Constructing the MSCI Barra Factor Indexes  involves the following steps:  
 Specifying the Parent Index , Benchmark  and the Barra Equity Model for optimization  
 Specifying the Target Factor and optimization objective  
 Specifying the optimization constraints  
 Calculating the optimized index  
The steps for constructing MSCI Long -Only Barra Factor Indexes  are described below.  
1. Specifying the Parent Index, Benchmark and the Barra Equity Model for optimization  
Constructing the MSCI Barra Factor Indexes  begins with selecting the Parent Index, 
Benchmark and the relevant Barra Equity Model for the optimization. For the MSCI Long -
Only  Barra  Factor Indexes : 
 the Parent Index is the corresponding MSCI Standard Index and serves as the universe of 
eligible securities for the optimization ; 
 the Benchmark for the optimization is also the corresponding MSCI Standard Index;  and 
 the Barra Equity Model is the corresponding global, regional or single country Barra 
Equity Model . 
For example, to construct the MSCI Europe Long -Only Barra Factor Indexes , the MSCI Europe 
Index would be used as the universe of eligible securities as well as the Benchmark for the 

---
## Page 21

 
 
 
 MSCI.COM | PAGE 21 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
optimization, and the Barra Europe Short -Term Model would be used as the risk model for 
the optimization.  
The optimization relies on the factor exposures for all the securities in the Parent Index and 
the factor co -variance matrix of the relevant B arra Equity Model. The optimization is 
performed from a base currency perspective (e.g., Euro for the MSCI Europe  Barra  Factor 
Indexes ) and does not allow short selling of securities.  
2. Specifying the Target Factor and optimization objectives  
The optimiz ation objective of the MSCI Long -Only Barra Factor Index is to have high factor 
exposure to the Target Factor and low tracking error relative to the Benchmark, which is 
achieved through maximizing the following utility function:  
Maximize: Target Factor Exp osure * 0.01 – Risk Aversion Parameter * Active Risk  
A risk aversion parameter of 0.015 is used to balance the objective of maximizing exposure 
to the Target Factor and the objective of minimizing tracking error relative to the 
Benchmark.  
3. Specifying the  optimization constraints  
At each monthly index rebalancing, a number of optimization constraints are employed in an 
effort to control the level of active exposure to other factors, as well as to achieve a balance 
between the objectives of replicability an d investability, high exposure to the Target Factor, 
low tracking error to the Benchmark, limited stock specific risk, and low index turnover.  
 At each monthly index rebalancing, the Barra style factor exposure of the MSCI Long -
Only Barra Factor Index will not deviate more than +/ - 0.25 standard deviations from the 
Barra style factor exposure of the Benchmark, in absolute terms,  with the exception of 
the Target Factor.  
 At each monthly index rebalancing, the Barra industry factor exposure of the MSCI Long -
Only Barra Factor Index will not deviate more than +/ - 5% from the Barra industry factor 
exposure of the Benchmark , in absolute terms.  
 At each monthly index rebalancing, the Barra country factor exposure of the MSCI Long -
Only Barra Factor Index will not devi ate more than +/ - 5% from the Barra country factor 
exposure of the Benchmark , in absolute terms.  
 At each monthly index rebalancing, the MSCI Long -Only Barra Factor Index will only 
include securities that are constituents of the Parent Index . 
 At each monthl y index rebalancing, the number of index constituents is constrained to a 
maximum of 200. 

---
## Page 22

 
 
 
 MSCI.COM | PAGE 22 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
 At each monthly index rebalancing, the one -way index turnover of the MSCI Long -Only 
Barra Factor Index is constrained to a maximum of 5%.  
 At each monthly index rebala ncing, the weight of each index constituent will not change 
more than a predefined Trade Limit7 linked to the stock’s Average Daily Traded Value.  
 At each monthly index rebalancing, the weight of an index constituent will not deviate 
more than +/ - 2% from its weight in the Benchmark . When this constraint is in conflict 
with the Trade Limit constraint defined above, the Trade Limit constraint takes 
precedence.  
4. Calculating the optimized index  
The MSCI Barra Factor Index is constructed using the Barra Optimizer in combination with 
the relevant Barra Equity Model. The optimization uses the MSCI Parent Index as the 
universe of eligible securities and the specified optimization objective and constraints to 
determ ine the optimal Barra  Factor Index. In the event of infeasible optimization, the rules 
outlined in Appendix VI will be followed.  
                                                      
7 Please refer to Appendix V  for the calculation of the Trade Limit.  

---
## Page 23

 
 
 
 MSCI.COM | PAGE 23 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
The following sections have been modified since November  2013:                                   
 
 Appendix I X in the previous version of the methodology book describing the Corporate 
Events treatment has been deleted. The details on the Corporate Events treatment are 
now included in Section 4.2. 
 
The following sections have been modified since June 2017 :                                   
 
 
Appendix II: Optimization Settings for Constructing MSCI Long -Short Barra Factor Indexes  
 
 Updates to the description.  
 
Appendix IV: Defining Shorting Cost Cutoff  
 
 Updates to the description.  
 
Appendix VII: New Release of Barra Equity Model or Barra Optimizer  
 
 Updates to the description.  
 
 
The following sections have been modified since September  2017 :                                   
 
 
Appendix IV: Defining Shorting Cost Cutoff  
 
 Updates to the description.  
 
  

---
## Page 24

 
 
 
 MSCI.COM | PAGE 24 OF 25 
 © 2017 MSCI Inc. All rights reserved. Please refer to the disclaimer at the end of this document.  
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
 
AMERICAS  
 
Americas  1 888 588 4567 *  
Atlanta   + 1 404 551 3212  
Boston   + 1 617 532 0920  
Chicago   + 1 312 675 0545  
Monterrey  + 52  81 1253  4020  
New York  + 1 212 804 3901  
San Francisco  + 1 415 836 8800  
Sao Paulo  + 55  11 3706  1360  
Toronto   + 1 416 628 1007  
 
 
EUROPE, MIDDLE EAST & AFRICA  
 
Cape Town  + 27  21 673 0100  
Frankfurt  + 49  69 133 859 00 
Geneva   + 41  22 817 9777  
London   + 44  20 7618  2222  
Milan   + 39  02 5849  0415  
Paris   0800  91 59 17 * 
 
 
ASIA PACIFIC  
 
China North  10800  852 1032 * 
China South  10800  152 1032 * 
Hong Kong  + 852  2844  9333  
Mumbai   + 91 22 6784 9160  
Seoul   00798  8521  3392 * 
Singapore  800 852 3749 * 
Sydney   + 61  2 9033  9333  
Taipei   008 0112  7513 * 
Tokyo   + 81  3 5290  1555  
 ABOUT MSCI  
 
For more than 40 years, MSCI’s research -
based indexes and analytics have helped 
the world’s leading investors build and 
manage better portfolios.  Clients rely on 
our offerings for deeper insights into the 
drivers of performance and risk in their 
portfolio s, broad asset class coverage and 
innovative research.  
Our line of products and services includes 
indexes, analytical models, data, real estate 
benchmarks and ESG research.   
MSCI serves 98 of the top 100 largest 
money managers, according to the most 
rece nt P&I ranking.  
For more information, visit us at 
www.msci.com . 
* =  toll free  
 CONTACT US  
 
clientservice@msci.com  

---
## Page 25

 
 
 
MSCI BARRA FACTOR IN DEXES METHODOLOGY  | MARCH 2018  
MSCI.COM | PAGE 25 OF 25 
 © 201 7 MSCI Inc. All rights reserved.  
 • This document and all of the information contained in it, including withou t limitation all text, data, graphs, charts (collectively, the “Information”) is 
the property of MSCI Inc. or its subsidiaries (collectively, “MSCI”), or MSCI’s licensors, direct or indirect suppliers or an y third party involved in making 
or compiling any Information (collectively, with MSCI, the “Information Providers”) and is provided for informational purposes only.  The Info rmation 
may not be modified, reverse -engineered, reproduced or redisseminated in whole or in part without prior written permission from MSCI.  
• The Information may not be used to create derivative works or to verify or correct other data or information.   For example  (but without limitation), 
the Information may not be used to create indexes, databases, risk models, analytics, softwa re, or in connection with the issuing, offering, 
sponsoring, managing or marketing of any securities, portfolios, financial products or other investment vehicles utilizing or  based on, linked to, 
tracking or otherwise derived from the Information or any ot her MSCI data, information, products or services.   
• The user of the Information assumes the entire risk of any use it may make or permit to be made of the Information.  NONE O F THE INFORMATION 
PROVIDERS MAKES ANY EXPRESS OR IMPLIED WARRANTIES OR REPRESEN TATIONS WITH RESPECT TO THE INFORMATION (OR THE RESULTS TO BE 
OBTAINED BY THE USE THEREOF), AND TO THE MAXIMUM EXTENT PERMITTED BY APPLICABLE LAW, EACH INFORMATION PROVIDER EXPRESSLY 
DISCLAIMS ALL IMPLIED WARRANTIES (INCLUDING, WITHOUT LIMITATION, ANY IMPL IED WARRANTIES OF ORIGINALITY, ACCURACY, TIMELINESS, 
NON -INFRINGEMENT, COMPLETENESS, MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE) WITH RESPECT TO ANY OF THE 
INFORMATION.  
• Without limiting any of the foregoing and to the maximum extent permitted b y applicable law, in no event shall any Information Provider have any 
liability regarding any of the Information for any direct, indirect, special, punitive, consequential (including lost profits ) or any other damages even if 
notified of the possibility of  such damages. The foregoing shall not exclude or limit any liability that may not by applicable law be excluded or limited, 
including without limitation (as applicable), any liability for death or personal injury to the extent that such injury resul ts fro m the negligence or 
willful default of itself, its servants, agents or sub -contractors.   
• Information containing any historical information, data or analysis should not be taken as an indication or guarantee of an y future performance, 
analysis, forecast or prediction.  Past performance does not guarantee future results.   
• The Information sh ould not be relied on and is not a substitute for the skill, judgment and experience of the user, its management, employees, 
advisors and/or clients when making investment and other business decisions.  All Information is impersonal and not tailored to the  needs of any 
person, entity or group of persons.  
• None of the Information constitutes an offer to sell (or a solicitation of an offer to buy), any security, financial produc t or other investment vehicle 
or any trading strategy.  
• It is not possible to i nvest directly in an index.  Exposure to an asset class or trading strategy or other category represented by an index is only  
available through third party investable instruments (if any) based on that index.   MSCI does not issue, sponsor, endorse, m arket , offer, review or 
otherwise express any opinion regarding any fund, ETF, derivative or other security, investment, financial product or trading  strategy that is based on, 
linked to or seeks to provide an investment return related to the performance of any  MSCI index (collectively, “Index Linked Investments”). MSCI 
makes no assurance that any Index Linked Investments will accurately track index performance or provide positive investment r eturns.  MSCI Inc. is 
not an investment adviser or fiduciary and MSCI makes no representation regarding the advisability of investing in any Index Linked Investments.  
• Index returns do not represent the results of actual trading of investible assets/securities. MSCI maintains and calculates  indexes, but does not 
manage actu al assets. Index returns do not reflect payment of any sales charges or fees an investor may pay to purchase the securities u nderlying the 
index or Index Linked Investments. The imposition of these fees and charges would cause the performance of an Index L inked Investment to be 
different than the MSCI index performance.  
• The Information may contain back tested data.  Back -tested performance is not actual performance, but is hypothetical.  There are frequently 
material differences between back tested perfor mance results and actual results subsequently achieved by any investment strategy.   
• Constituents of MSCI equity indexes are listed companies, which are included in or excluded from the indexes according to t he application of the 
relevant index methodolo gies. Accordingly, constituents in MSCI equity indexes may include MSCI Inc., clients of MSCI or suppliers to MSCI.  Inclusio n 
of a security within an MSCI index is not a recommendation by MSCI to buy, sell, or hold such security, nor is it considered to be investment advice.  
• Data and information produced by various affiliates of MSCI Inc., including MSCI ESG Research LLC and Barra LLC, may be use d in calculating certain 
MSCI indexes.  More information can be found in the relevant index methodologies on w ww.msci.com.  
• MSCI receives compensation in connection with licensing its indexes to third parties.  MSCI Inc.’s revenue includes fees ba sed on assets in Index 
Linked Investments. Information can be found in MSCI Inc.’s company filings on the Investor Re lations section of www.msci.com.  
• MSCI ESG Research LLC is a Registered Investment Adviser under the Investment Advisers Act of 1940 and a subsidiary of MSCI  Inc.  Except with 
respect to any applicable products or services from MSCI ESG Research, neither MSCI nor any of its products or services recommends, endorses, 
approves or otherwise expresses any opinion regarding any issuer, securities, financial products or instruments or trading st rategies and MSCI’s 
products or services are not intended to constit ute investment advice or a recommendation to make (or refrain from making) any kind of investment 
decision and may not be relied on as such. Issuers mentioned or included in any MSCI ESG Research materials may include MSCI Inc., clients of MSCI 
or supplier s to MSCI, and may also purchase research or other products or services from MSCI ESG Research.  MSCI ESG Research materials,  including 
materials utilized in any MSCI ESG Indexes or other products, have not been submitted to, nor received approval from, th e United States Securities 
and Exchange Commission or any other regulatory body.  
• Any use of or access to products, services or information of MSCI requires a license from MSCI.  MSCI, Barra, RiskMetrics, IPD, FEA, InvestorForce, 
and other MSCI brands and  product names are the trademarks, service marks, or registered trademarks of MSCI or its subsidiaries in the United 
States and other jurisdictions.  The Global Industry Classification Standard (GICS) was developed by and is the exclusive pro perty of MSCI and 
Standard & Poor’s.  “Global Industry Classification Standard (GICS)” is a service mark of MSCI and Standard & Poor’s.  
 NOTICE AND 
DISCLAIMER  

