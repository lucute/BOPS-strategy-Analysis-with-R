# BOPS-strategy-Analysis-with-R
The data is from a retailer which has both online and brick and motar stores, the objective for this analysis is to figure out below business questions related to BOPS(buy online,pick-up in store): <br>
- What is the impact of adopting BOPS strategy on online channel sales/returns?
- What is the impact of adopting BOPS strategy on online customers purchase/returns behavior?

### Data Description <br>
- Data set: <br>
  - Transaction data: cover all transactions made between August 1st, 2010 and July 31st, 2013 among three different stores
    - Total 1,671,502 transactions
    - 29 variables
  - fy12: the transactions used bops service in 2012
  - fy13: the transactions used bops service in 2013

### Analysis Process:
**For answering What is the impact of adopting BOPS strategy on online channel sales/returns?**
- Data preparation:
  - Generate bops12 and bops13 column to indicate whether this transaction happen after adopting bops or not
  - Generate dummy variables - bops for whether this transaction used bops or not
 
- Analysis Strategy:
  - By store -> compare the impact on sales for each store
  
