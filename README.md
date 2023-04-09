# ANALYZING-CUSTOMER-CHURN
Analyzing customer churn using Tableau and gain insights into the reasons behind customer attrition.

_**Tableau Dashboard**_ - https://public.tableau.com/shared/GXG7Z2BPT?:display_count=n&:origin=viz_share_link

### 1 -Creating Calculated Fields

#### 1.1  No. of customers
```
COUNT([Customer ID])
#All customer id 
```

#### 1.2 Unique Customers

```
=countd([No. of Customers])
#Distinct customer id's
```
#### 1.3 Datacheck for verifying customer id is unique

Checking both calculating fields 'No. of customers' and 'Unique Customers' for values.                                                                                    
**Result** - 6,687                                                                                                                                                      
Both calulated fields are equal.                                                                                                                                       

#### 1.4 Convert churn label to binomial

```
If [Churn Label]= 'Yes'
THEN 1
ELSE 0
END

```
This calculated field converts 'Yes' & 'No' for churned label into binomial '1' and '0' respectively, to make further analysis and calculations feasible.

#### 1.5 Calculate Churn Rate
Churn rate is calulated by ;- [Churned customers] / [No. of customers]
```
#Churned customers 
Sum([churn label])
```
Then the calculated field is formated into 'Percentage of Total' for churn rate.

## 1.6 Churn Reasons
Analyzing 'Churn Reasons' across 'No. of customers' as a Percentage of Total. 

## 1.7 Churn categories
Analyzing churners by 'churn rate' across 'churn categories'

## 1.8 Churn Region
Analyzing 'churn reasons', 'churn rate', 'churned customers' with 'No. of customers' across state region  

_**Tableau Dashboard **_ - https://public.tableau.com/shared/GXG7Z2BPT?:display_count=n&:origin=viz_share_link

## Key highlights of Data visualization



