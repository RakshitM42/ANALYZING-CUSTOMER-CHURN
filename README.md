# ANALYZING-CUSTOMER-CHURN
#### Analyzing customer churn using Tableau and gain insights into the reasons behind customer attrition.

In this Tableau case study, I will investigate a dataset from an example telecom company called Databel and analyze their churn rates. My objective is not only to determine the churn rate but also to understand why customers are churning. I aim to gain valuable insights that can help Databel to make informed decisions about improving customer retention strategies and reducing churn. Ultimately, the goal is to help Databel improve customer satisfaction, increase loyalty, and drive long-term growth.



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

** Churn reasons - https://public.tableau.com/views/ChurnReasons_16811025661850/ChurnReasons?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link

## 1.7 Churn categories
Analyzing churners by 'churn rate' across 'churn categories'

**Churn categories(Graph)** - https://public.tableau.com/views/Churncategories-Graph/ChurnCategoriesgraph?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link

**Churn categories(Table)** - https://public.tableau.com/views/Churncategories-Table/Churncategories?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link

## 1.8 Churn Region
Analyzing 'churn reasons', 'churn rate', 'churned customers' with 'No. of customers' across state region  

**Churned Region** - https://public.tableau.com/views/ChurnedRegion/ChurnedRegion?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link


## 2 - Key highlights of Data visualization

**2.1 Churn Categories**
1. Competitor
2. Dissatisfaction
3. Attitude
4. Price
5. Other


**2.2 Top Churn reasons**
1. Competitor made better offer
2. Competitor had better devices 
3. Attitude of support person
4. Competitor offered more data

**2.3 Regions with most churns**
1. CA - California
2. PA - Pennsylvania
3. AK - Alaska
4. OR - Oregon
5. TX - Texas

**Considering the key highlights of Databel, top recommendation to improve churn rates are** -

1. Focus on improving customer satisfaction levels, especially in regions that have high churn rates.
2. Consider top churn reasons and could offering competitive pricing, better devices, and more data to retain customers.
3. Addressing any negative attitude or experinces with customer service as it was identified top reasons for churn.

Thereafter, company should constantly monitor all the top churn reasons on an ongoing basis, in order to stay competitive and respond quickly to changes in the market. 
