*This project was team project for my econometrics class; after another quarter's learning, I redid this dataset.
# BOPS-strategy-Analysis-with-R
The data is from a retailer which has both online and brick and motar stores, the objective for this analysis is to figure out below business questions related to BOPS(buy online,pick-up in store): <br>
- What is the impact of adopting BOPS strategy on online channel sales?
- What is the impact of adopting BOPS strategy on online channel returns?


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
  - By store -> compare the impact on sales/returns for each store <br>
  - Among each group, BOPS has biggest impact when (which month) and on what kind of products(which summary)
  - For each kind of analysis, I separate them into two layers: <br>
    - whole data set and put implementing bops, using bops as independent variables
    - Only look at the transaction after implementing bops, and "using bops" is the key independent variables.
 
- **Findings and Suggestion**:
  - **In general**<br>
  ![alt text](https://github.com/lucute/BOPS-strategy-Analysis-with-R/blob/master/general_intepretation_whole.png)
    - The transaction with bops in general spend more net_purchase_amount in store 2 than other 2 stores.
    - Store 2 and store 6 have positive coefficients on implementing bops variable, however, store 5998 has negative sign.
  - **Store2**
    - Interaction term of bops and month captures the differences impact of bops on different month. From the result, bops has positive impact in the months except APR and JAN. Further more, in AUG and SEP, BOPS service had significant positive impact on purchase amount per transaction.
    - Interaction term of bops and summary indicates that for summary 3 and 10, the gap between adopting bops and before is worth noting.
    - Adopting BOPS increase the probabilty for return
  - **Store6**
    - Similarily to store2, bops has positive impact in the months except APR and JAN. Further more, in AUG and SEP, BOPS service had significant positive impact on purchase amount per transaction. But the trend for store 6 seems more dramatically changes over month.
    - Different from store 2, for store 6, summary 8 is worth noting.
    - Adopting BOPS doesn't play a big role on whether customers returned products or not.
     
  - **Store5998**
    - From the result of analysis, store 5998 is different from other two stores, this store implemented bops latest and doesn't have much information about their customers. Also, the bops service in general has negative impact on sales amount.
 
  
