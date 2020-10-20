# CRM CAMPAIGN GROCERY STORE
Predicting the customers will accept a campaign.

### The Company
Consider a well-established company operating in the retail food sector. Presently they have around several hundred thousand registered customers and serve almost one million consumers a year. They sell products from 5 major categories: wines, rare meat products, exotic fruits, specially prepared fish and sweet products. These can further be divided into gold and regular products. The customers can order and acquire products through 3 sales channels: physical stores, catalogs and company’s website. Globally, the company had solid revenues and a healthy bottom line in the past 3 years, but the profit growth perspectives for the next 3 years are not promising... For this reason, several strategic initiatives are being considered to invert this situation. One is to improve the performance of marketing activities, with a special focus on marketing campaigns.

### The marketing department
The marketing department was pressured to spend its annual budget more wisely. The CMO perceives the importance of having a more quantitative approach when taking decisions, reason why a small team of data scientists was hired with a clear objective in mind: to build a predictive model which will support direct marketing initiatives. Desirably, the success of these activities will prove the value of the approach and convince the more skeptical within the company.

### The objective
The objective of the team is to build a predictive model that will produce the highest profit for the next direct marketing campaign, scheduled for the next month. The new campaign, sixth, aims at selling a new gadget to the Customer Database. To build the model, a pilot campaign involving 2.240 customers was carried out. The customers were selected at random and contacted by phone regarding the acquisition of the gadget. During the following months, customers who bought the offer were properly labeled. The total cost of the sample campaign was 6.720MU and the revenue generated by the customers who accepted the offer was 3.674MU. Globally the campaign had a profit of -3.046MU. The success rate of the campaign was 15%. The objective is of the team is to develop a model that predicts customer behavior and to apply it to the rest of the customer base. Hopefully, the model will allow the company to cherry pick the customers that are most likely to purchase the offer while leaving out the non-respondents, making the next campaign highly profitable. Moreover, other than maximizing the profit of the campaign, the CMO is interested in understanding to study the characteristic features of those customers who are willing to buy the gadget.

### Dataset
The data set contains socio-demographic and firmographic features about 2.240 customers who were contacted. Additionally, it contains a flag for those customers who responded the campaign, by buying the product.


![metadados](https://user-images.githubusercontent.com/52208793/96514789-8e50df80-123a-11eb-8579-67b48752120d.jpg)



# Libraries
![libraries](https://user-images.githubusercontent.com/52208793/96515593-f94ee600-123b-11eb-8d03-c668d13b299e.jpg)

# Import dataset
![import_dataset](https://user-images.githubusercontent.com/52208793/96515800-53e84200-123c-11eb-9d1d-6905c4753bb1.jpg)

# Dropping Features
![drop_features](https://user-images.githubusercontent.com/52208793/96516070-d2dd7a80-123c-11eb-9d5d-74693abeddf1.jpg)

# Looking for missing values
![missing_values](https://user-images.githubusercontent.com/52208793/96516361-6a42cd80-123d-11eb-9a2b-2ea3397d4c7e.jpg)

# Treatment Missing Values
![treatment_missing_values](https://user-images.githubusercontent.com/52208793/96516509-b0982c80-123d-11eb-94cd-bc8fe47b9c07.jpg)

# Analysing the feature Income
The boxplot shows there are some outliers for the feature Income

![income_before_treat_outliers](https://user-images.githubusercontent.com/52208793/96518357-1d60f600-1241-11eb-8253-1c904f273849.jpg)

Treatment outliers:
1) Drop Income greater than 666.666
2) Applying interquartile range

![income_before_treat_outliers_acc_1](https://user-images.githubusercontent.com/52208793/96518665-c0197480-1241-11eb-9b1b-8c287d382ab7.jpg)

After treatment by median you can see a better result.
![income_before_treat_outliers_acc_2](https://user-images.githubusercontent.com/52208793/96518981-5f3e6c00-1242-11eb-8fc2-c02531570933.jpg)

# Analysing the feature Year_Birth and creating a new feature called Age
![age_1](https://user-images.githubusercontent.com/52208793/96519578-b0029480-1243-11eb-84d7-c91ba238f7bc.jpg)
![age_2](https://user-images.githubusercontent.com/52208793/96519755-14255880-1244-11eb-8df9-49cc67c90ae4.jpg)

# Analysing the feature Dt_Customer and creating a new feature called Member_Months
![member_months_1](https://user-images.githubusercontent.com/52208793/96520113-bcd3b800-1244-11eb-8401-9c22320fed41.jpg)
![member_months_2](https://user-images.githubusercontent.com/52208793/96520273-189e4100-1245-11eb-82ae-243a409db171.jpg)
![member_months_3](https://user-images.githubusercontent.com/52208793/96520438-7c286e80-1245-11eb-9974-3e29df1066a1.jpg)
![member_months_4](https://user-images.githubusercontent.com/52208793/96520657-e4775000-1245-11eb-8fdc-4e4013876dae.jpg)
![member_months_5](https://user-images.githubusercontent.com/52208793/96520839-52237c00-1246-11eb-960a-7e1717e73af3.jpg)

# Analysing the feature Recency
There aren't any outliers for this feature.
![recency_1](https://user-images.githubusercontent.com/52208793/96521101-dd047680-1246-11eb-8700-eb78bdd3e30e.jpg)
![recency_2](https://user-images.githubusercontent.com/52208793/96521313-5c924580-1247-11eb-98c3-88dbedb6a6b9.jpg)

# Analysing the feature MntWines
The boxplot shows there are some outliers for the feature MntWines

![mntwines_1](https://user-images.githubusercontent.com/52208793/96521647-15588480-1248-11eb-9c41-cd8dcc2ad592.jpg)
![mntwines_2](https://user-images.githubusercontent.com/52208793/96521787-66687880-1248-11eb-8874-20c488a83260.jpg)
![mntwines_3](https://user-images.githubusercontent.com/52208793/96522088-0de5ab00-1249-11eb-94b9-3a46f319052c.jpg)
![mntwines_4](https://user-images.githubusercontent.com/52208793/96522150-2bb31000-1249-11eb-8198-a95f50146cbd.jpg)

# Analysing the feature MntFruits
The boxplot shows there are some outliers for the feature MntFruits

![mntfruits_1](https://user-images.githubusercontent.com/52208793/96522368-a1b77700-1249-11eb-8a63-4c85146f2de4.jpg)
![mntfruits_2](https://user-images.githubusercontent.com/52208793/96522498-dc211400-1249-11eb-9f66-4dfc0533aeb7.jpg)
![mntfruits_3](https://user-images.githubusercontent.com/52208793/96522612-168ab100-124a-11eb-9115-90c6a651f877.jpg)

Applying interquartile range

![mntfruits_4](https://user-images.githubusercontent.com/52208793/96522843-b2b4b800-124a-11eb-9c0b-ce14bd66c6c9.jpg)
![mntfruits_5](https://user-images.githubusercontent.com/52208793/96523052-21921100-124b-11eb-8efe-0a492f60f951.jpg)
![mntfruits_6](https://user-images.githubusercontent.com/52208793/96523122-4ab2a180-124b-11eb-88da-ab8c312532ad.jpg)

# Analysing the feature MntMeatProducts
The boxplot shows there are some outliers for the feature MntFruits

![MntMeatProducts_1](https://user-images.githubusercontent.com/52208793/96523327-ce6c8e00-124b-11eb-854e-1a40047c85de.jpg)
![MntMeatProducts_2](https://user-images.githubusercontent.com/52208793/96523440-1be8fb00-124c-11eb-8614-c4176ac77f9a.jpg)
![MntMeatProducts_3](https://user-images.githubusercontent.com/52208793/96523594-78e4b100-124c-11eb-8587-a11ffb76cfad.jpg)
![MntMeatProducts_4](https://user-images.githubusercontent.com/52208793/96523677-b2b5b780-124c-11eb-85c8-085bb1db1933.jpg)

# Analysing the feature MntFishProducts
The boxplot shows there are some outliers for the feature MntFishProducts

![MntFishProducts_1](https://user-images.githubusercontent.com/52208793/96523834-12ac5e00-124d-11eb-9247-1318e4ad72b6.jpg)
![MntFishProducts_2](https://user-images.githubusercontent.com/52208793/96523939-5f903480-124d-11eb-88a1-45f74ed704ff.jpg)

Applying interquartile range

![MntFishProducts_3](https://user-images.githubusercontent.com/52208793/96524176-e513e480-124d-11eb-9feb-818b2413b53c.jpg)
![MntFishProducts_4](https://user-images.githubusercontent.com/52208793/96524290-3623d880-124e-11eb-8122-aa3d1e80c62b.jpg)

Median of Amount spent on Fish Products by customers accepted the 6th campaign is bigger than Median of Amount spent on Fish Products by customers didn't accept it.
Standard deviation of amount spent on Fish Products by customers accepted the 6th campaign is bigger than Standard deviation of amount spent on Fish Products by customers didn't accept it.
Look at skewness. The histogram of amount spent on Fish Products by customers accepted the 6th campaign has positive skew.

# Analysing the feature MntSweetProducts
The boxplot shows there are some outliers for the feature MntSweetProducts

![MntSweetProducts_1](https://user-images.githubusercontent.com/52208793/96524443-af233000-124e-11eb-8bc9-a5a00cfc7169.jpg)
![MntSweetProducts_2](https://user-images.githubusercontent.com/52208793/96524539-f27d9e80-124e-11eb-898c-e6747963c1c5.jpg)

Applying interquartile range
![MntSweetProducts_3](https://user-images.githubusercontent.com/52208793/96524707-6750d880-124f-11eb-8de4-8bf09020acde.jpg)
![MntSweetProducts_4](https://user-images.githubusercontent.com/52208793/96525685-04147580-1252-11eb-8c6f-efa142450b53.jpg)

# Analysing the features MntGoldProds
The boxplot shows there are some outliers for the feature MntGoldProds

![MntGoldProducts_1](https://user-images.githubusercontent.com/52208793/96525877-7a18dc80-1252-11eb-8470-3185c92e6775.jpg)
![MntGoldProducts_2](https://user-images.githubusercontent.com/52208793/96525986-c3692c00-1252-11eb-8db5-9b0b3bf6d273.jpg)

Applying interquartile range
![MntGoldProducts_3](https://user-images.githubusercontent.com/52208793/96526140-29ee4a00-1253-11eb-931b-014f09daf09e.jpg)
![MntGoldProducts_4](https://user-images.githubusercontent.com/52208793/96526307-8fdad180-1253-11eb-8087-bba83af0123b.jpg)

# Analysing the feature NumDealsPurchases
The boxplot shows there are some outliers for the feature NumDealsPurchases

![NumDealsPurchases_1](https://user-images.githubusercontent.com/52208793/96526491-17284500-1254-11eb-8276-3e361e283ef5.jpg)
![NumDealsPurchases_2](https://user-images.githubusercontent.com/52208793/96526560-55bdff80-1254-11eb-8b88-69f487f29907.jpg)

Applying interquartile range
![NumDealsPurchases_3](https://user-images.githubusercontent.com/52208793/96526735-d0871a80-1254-11eb-9dfe-3da0403abf2d.jpg)
![NumDealsPurchases_4](https://user-images.githubusercontent.com/52208793/96526876-2c51a380-1255-11eb-84cb-ae072a2e720b.jpg)

# Analysing the feature NumWebPurchases
The boxplot shows there are some outliers for the feature NumDealsPurchases

![NumWebPurchases_1](https://user-images.githubusercontent.com/52208793/96527029-85b9d280-1255-11eb-8a92-a93179708408.jpg)
![NumWebPurchases_2](https://user-images.githubusercontent.com/52208793/96527123-c74a7d80-1255-11eb-8057-30d4be36437f.jpg)

Applying interquartile range
![NumWebPurchases_3](https://user-images.githubusercontent.com/52208793/96527342-3f18a800-1256-11eb-86a7-70b33823609e.jpg)
![NumWebPurchases_4](https://user-images.githubusercontent.com/52208793/96527488-8ef76f00-1256-11eb-81f4-7ae7877f2f9c.jpg)






