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



### Libraries
![libraries](https://user-images.githubusercontent.com/52208793/96515593-f94ee600-123b-11eb-8d03-c668d13b299e.jpg)

### Import dataset
![import_dataset](https://user-images.githubusercontent.com/52208793/96515800-53e84200-123c-11eb-9d1d-6905c4753bb1.jpg)

### Dropping Features
![drop_features](https://user-images.githubusercontent.com/52208793/96516070-d2dd7a80-123c-11eb-9d5d-74693abeddf1.jpg)

### Looking for missing values
![missing_values](https://user-images.githubusercontent.com/52208793/96516361-6a42cd80-123d-11eb-9a2b-2ea3397d4c7e.jpg)

### Treatment Missing Values
![treatment_missing_values](https://user-images.githubusercontent.com/52208793/96516509-b0982c80-123d-11eb-94cd-bc8fe47b9c07.jpg)

### Analysing the feature Income
The boxplot shows there are some outliers for the feature Income

![income_before_treat_outliers](https://user-images.githubusercontent.com/52208793/96518357-1d60f600-1241-11eb-8253-1c904f273849.jpg)

Treatment outliers:
1) Drop Income greater than 666.666
2) Applying interquartile range

![income_before_treat_outliers_acc_1](https://user-images.githubusercontent.com/52208793/96518665-c0197480-1241-11eb-9b1b-8c287d382ab7.jpg)

After treatment by median you can see a better result.
![income_before_treat_outliers_acc_2](https://user-images.githubusercontent.com/52208793/96518981-5f3e6c00-1242-11eb-8fc2-c02531570933.jpg)

### Analysing the feature Year_Birth and creating a new feature called Age
![age_1](https://user-images.githubusercontent.com/52208793/96519578-b0029480-1243-11eb-84d7-c91ba238f7bc.jpg)
![age_2](https://user-images.githubusercontent.com/52208793/96519755-14255880-1244-11eb-8df9-49cc67c90ae4.jpg)

### Analysing the feature Dt_Customer and creating a new feature called Member_Months
![member_months_1](https://user-images.githubusercontent.com/52208793/96520113-bcd3b800-1244-11eb-8401-9c22320fed41.jpg)
![member_months_2](https://user-images.githubusercontent.com/52208793/96520273-189e4100-1245-11eb-82ae-243a409db171.jpg)
![member_months_3](https://user-images.githubusercontent.com/52208793/96520438-7c286e80-1245-11eb-9974-3e29df1066a1.jpg)
![member_months_4](https://user-images.githubusercontent.com/52208793/96520657-e4775000-1245-11eb-8fdc-4e4013876dae.jpg)
![member_months_5](https://user-images.githubusercontent.com/52208793/96520839-52237c00-1246-11eb-960a-7e1717e73af3.jpg)

### Analysing the feature Recency
There aren't any outliers for this feature.
![recency_1](https://user-images.githubusercontent.com/52208793/96521101-dd047680-1246-11eb-8700-eb78bdd3e30e.jpg)
![recency_2](https://user-images.githubusercontent.com/52208793/96521313-5c924580-1247-11eb-98c3-88dbedb6a6b9.jpg)

### Analysing the feature MntWines
The boxplot shows there are some outliers for the feature MntWines

![mntwines_1](https://user-images.githubusercontent.com/52208793/96521647-15588480-1248-11eb-9c41-cd8dcc2ad592.jpg)
![mntwines_2](https://user-images.githubusercontent.com/52208793/96521787-66687880-1248-11eb-8874-20c488a83260.jpg)
![mntwines_3](https://user-images.githubusercontent.com/52208793/96522088-0de5ab00-1249-11eb-94b9-3a46f319052c.jpg)
![mntwines_4](https://user-images.githubusercontent.com/52208793/96522150-2bb31000-1249-11eb-8198-a95f50146cbd.jpg)

### Analysing the feature MntFruits
The boxplot shows there are some outliers for the feature MntFruits

![mntfruits_1](https://user-images.githubusercontent.com/52208793/96522368-a1b77700-1249-11eb-8a63-4c85146f2de4.jpg)
![mntfruits_2](https://user-images.githubusercontent.com/52208793/96522498-dc211400-1249-11eb-9f66-4dfc0533aeb7.jpg)
![mntfruits_3](https://user-images.githubusercontent.com/52208793/96522612-168ab100-124a-11eb-9115-90c6a651f877.jpg)

Applying interquartile range

![mntfruits_4](https://user-images.githubusercontent.com/52208793/96522843-b2b4b800-124a-11eb-9c0b-ce14bd66c6c9.jpg)
![mntfruits_5](https://user-images.githubusercontent.com/52208793/96523052-21921100-124b-11eb-8efe-0a492f60f951.jpg)
![mntfruits_6](https://user-images.githubusercontent.com/52208793/96523122-4ab2a180-124b-11eb-88da-ab8c312532ad.jpg)

### Analysing the feature MntMeatProducts
The boxplot shows there are some outliers for the feature MntFruits

![MntMeatProducts_1](https://user-images.githubusercontent.com/52208793/96523327-ce6c8e00-124b-11eb-854e-1a40047c85de.jpg)
![MntMeatProducts_2](https://user-images.githubusercontent.com/52208793/96523440-1be8fb00-124c-11eb-8614-c4176ac77f9a.jpg)
![MntMeatProducts_3](https://user-images.githubusercontent.com/52208793/96523594-78e4b100-124c-11eb-8587-a11ffb76cfad.jpg)
![MntMeatProducts_4](https://user-images.githubusercontent.com/52208793/96523677-b2b5b780-124c-11eb-85c8-085bb1db1933.jpg)

### Analysing the feature MntFishProducts
The boxplot shows there are some outliers for the feature MntFishProducts

![MntFishProducts_1](https://user-images.githubusercontent.com/52208793/96523834-12ac5e00-124d-11eb-9247-1318e4ad72b6.jpg)
![MntFishProducts_2](https://user-images.githubusercontent.com/52208793/96523939-5f903480-124d-11eb-88a1-45f74ed704ff.jpg)

Applying interquartile range

![MntFishProducts_3](https://user-images.githubusercontent.com/52208793/96524176-e513e480-124d-11eb-9feb-818b2413b53c.jpg)
![MntFishProducts_4](https://user-images.githubusercontent.com/52208793/96524290-3623d880-124e-11eb-8122-aa3d1e80c62b.jpg)

Median of Amount spent on Fish Products by customers accepted the 6th campaign is bigger than Median of Amount spent on Fish Products by customers didn't accept it.
Standard deviation of amount spent on Fish Products by customers accepted the 6th campaign is bigger than Standard deviation of amount spent on Fish Products by customers didn't accept it.
Look at skewness. The histogram of amount spent on Fish Products by customers accepted the 6th campaign has positive skew.

### Analysing the feature MntSweetProducts
The boxplot shows there are some outliers for the feature MntSweetProducts

![MntSweetProducts_1](https://user-images.githubusercontent.com/52208793/96524443-af233000-124e-11eb-8bc9-a5a00cfc7169.jpg)
![MntSweetProducts_2](https://user-images.githubusercontent.com/52208793/96524539-f27d9e80-124e-11eb-898c-e6747963c1c5.jpg)

Applying interquartile range
![MntSweetProducts_3](https://user-images.githubusercontent.com/52208793/96524707-6750d880-124f-11eb-8de4-8bf09020acde.jpg)
![MntSweetProducts_4](https://user-images.githubusercontent.com/52208793/96525685-04147580-1252-11eb-8c6f-efa142450b53.jpg)

### Analysing the features MntGoldProds
The boxplot shows there are some outliers for the feature MntGoldProds

![MntGoldProducts_1](https://user-images.githubusercontent.com/52208793/96525877-7a18dc80-1252-11eb-8470-3185c92e6775.jpg)
![MntGoldProducts_2](https://user-images.githubusercontent.com/52208793/96525986-c3692c00-1252-11eb-8db5-9b0b3bf6d273.jpg)

Applying interquartile range
![MntGoldProducts_3](https://user-images.githubusercontent.com/52208793/96526140-29ee4a00-1253-11eb-931b-014f09daf09e.jpg)
![MntGoldProducts_4](https://user-images.githubusercontent.com/52208793/96526307-8fdad180-1253-11eb-8087-bba83af0123b.jpg)

### Analysing the feature NumDealsPurchases
The boxplot shows there are some outliers for the feature NumDealsPurchases

![NumDealsPurchases_1](https://user-images.githubusercontent.com/52208793/96526491-17284500-1254-11eb-8276-3e361e283ef5.jpg)
![NumDealsPurchases_2](https://user-images.githubusercontent.com/52208793/96526560-55bdff80-1254-11eb-8b88-69f487f29907.jpg)

Applying interquartile range
![NumDealsPurchases_3](https://user-images.githubusercontent.com/52208793/96526735-d0871a80-1254-11eb-9dfe-3da0403abf2d.jpg)
![NumDealsPurchases_4](https://user-images.githubusercontent.com/52208793/96526876-2c51a380-1255-11eb-84cb-ae072a2e720b.jpg)

### Analysing the feature NumWebPurchases
The boxplot shows there are some outliers for the feature NumDealsPurchases

![NumWebPurchases_1](https://user-images.githubusercontent.com/52208793/96527029-85b9d280-1255-11eb-8a92-a93179708408.jpg)
![NumWebPurchases_2](https://user-images.githubusercontent.com/52208793/96527123-c74a7d80-1255-11eb-8057-30d4be36437f.jpg)

Applying interquartile range
![NumWebPurchases_3](https://user-images.githubusercontent.com/52208793/96527342-3f18a800-1256-11eb-86a7-70b33823609e.jpg)
![NumWebPurchases_4](https://user-images.githubusercontent.com/52208793/96527488-8ef76f00-1256-11eb-81f4-7ae7877f2f9c.jpg)

### Analysing the features NumCatalogPurchases
The boxplot shows there are some outliers for the feature NumCatalogPurchases

![NumCatalogPurchases_1](https://user-images.githubusercontent.com/52208793/96527627-edbce880-1256-11eb-9931-eabe35ffe96f.jpg)
![NumCatalogPurchases_2](https://user-images.githubusercontent.com/52208793/96527707-2e1c6680-1257-11eb-850a-1781a302d3a7.jpg)

Applying interquartile range
![NumCatalogPurchases_3](https://user-images.githubusercontent.com/52208793/96527873-9408ee00-1257-11eb-9e0c-b809f172a503.jpg)
![NumCatalogPurchases_4](https://user-images.githubusercontent.com/52208793/96527936-bc90e800-1257-11eb-9c47-c8eabaec5509.jpg)

### Analysing the feature NumStorePurchases
The boxplot shows there aren't any outliers for the feature NumStorePurchases

![NumStorePurchases_1](https://user-images.githubusercontent.com/52208793/96528068-201b1580-1258-11eb-94b6-49da8013927c.jpg)
![NumStorePurchases_2](https://user-images.githubusercontent.com/52208793/96528212-78521780-1258-11eb-9dcf-624ac7e96b49.jpg)

Median of Purchases made directly on stores by customers accepted the 6th campaign is bigger than Median of Purchases made directly on stores by customers didn't accept it.
Standard deviation of Purchases made directly on stores by customers accepted the 6th campaign is similar of Standard deviation of Purchases made directly on stores by customers didn't accept it.
Look at skewness. The histogram of Purchases made directly on stores by customers that accepted the 6th campaign has positive skew.
There aren't any outliers when you look at boxplot of Purchases made directly on stores by customers.

### Analysing the feature NumWebVisitsMonth
The boxplot shows there are some outliers for the feature NumWebVisitsMonth

![NumWebVisitsMonth_1](https://user-images.githubusercontent.com/52208793/96528371-f0204200-1258-11eb-94fe-29af9cf3b48b.jpg)
![NumWebVisitsMonth_2](https://user-images.githubusercontent.com/52208793/96528475-3bd2eb80-1259-11eb-9e52-e3bbea87a54d.jpg)

Applying interquartile range
![NumWebVisitsMonth_3](https://user-images.githubusercontent.com/52208793/96528618-98360b00-1259-11eb-8973-39c8e8a9faf7.jpg)
![NumWebVisitsMonth_4](https://user-images.githubusercontent.com/52208793/96528807-efd47680-1259-11eb-805d-c1d31953c5d5.jpg)


Median of Visits on Web Site last month by customers accepted the 6th campaign and Median of Visits on Web Site last month by customers didn't accept are the same.
Standard deviation of Visits on Web Site last month by customers accepted the 6th campaign is bigger than Standard deviation of Purchases made directly on stores by customers didn't accept it.

### Analyzing the features Education and Marital_Status

![education_and_marital_status_1](https://user-images.githubusercontent.com/52208793/96528961-52c60d80-125a-11eb-85d2-34f9a412c501.jpg)
![education_and_marital_status_2](https://user-images.githubusercontent.com/52208793/96529051-81dc7f00-125a-11eb-9911-7f80bb70ab0e.jpg)
![education_and_marital_status_3](https://user-images.githubusercontent.com/52208793/96529120-b2bcb400-125a-11eb-8ea0-91c65cecb8d8.jpg)
![education_and_marital_status_4](https://user-images.githubusercontent.com/52208793/96529184-e0096200-125a-11eb-839e-b3ec737cbd61.jpg)
![education_and_marital_status_5](https://user-images.githubusercontent.com/52208793/96529242-05966b80-125b-11eb-8c8f-e2ed474356b4.jpg)

### Analyzing the feature Complain

![Complain_1](https://user-images.githubusercontent.com/52208793/96529352-51e1ab80-125b-11eb-9f40-9c10836ef9c2.jpg)
![Complain_2](https://user-images.githubusercontent.com/52208793/96529437-89505800-125b-11eb-8d09-9aae932d7818.jpg)

### Analysing the features Kidhome and Teenhome

![Kidhome_Teenhome_1](https://user-images.githubusercontent.com/52208793/96529560-e64c0e00-125b-11eb-8f63-13e93fbce635.jpg)
![Kidhome_Teenhome_2](https://user-images.githubusercontent.com/52208793/96529657-28754f80-125c-11eb-959a-85fdd178ad63.jpg)

### Transforming categorical features into dummy variable

![Transform_1](https://user-images.githubusercontent.com/52208793/96529805-6d998180-125c-11eb-86a0-eb0f476c7623.jpg)
![Transform_2](https://user-images.githubusercontent.com/52208793/96529894-a8031e80-125c-11eb-941a-50335cd74c8b.jpg)

### Correlation Matrix

![Correlation_Matrix_1](https://user-images.githubusercontent.com/52208793/96530102-19db6800-125d-11eb-908d-d1cce5c6171e.jpg)
![Correlation_Matrix_2](https://user-images.githubusercontent.com/52208793/96530221-55763200-125d-11eb-876b-6fd04c69d010.jpg)

### Pre-processing
![Pre_Processing_1](https://user-images.githubusercontent.com/52208793/96530381-b69e0580-125d-11eb-8c50-9dcf211c7268.jpg)
![Pre_Processing_2](https://user-images.githubusercontent.com/52208793/96530663-49d73b00-125e-11eb-84cc-2f7239dea835.jpg)
![Pre_Processing_3](https://user-images.githubusercontent.com/52208793/96530799-902c9a00-125e-11eb-9ec7-c98dfbdb5122.jpg)
![Pre_Processing_4](https://user-images.githubusercontent.com/52208793/96530931-e7cb0580-125e-11eb-978d-52caadcbbb07.jpg)
![Pre_Processing_5](https://user-images.githubusercontent.com/52208793/96531048-252f9300-125f-11eb-88e8-93d6583227e4.jpg)
![Pre_Processing_6](https://user-images.githubusercontent.com/52208793/96531134-4f815080-125f-11eb-9015-6f1c4706f59c.jpg)

### Decision Tree Classifier
![Decision_Tree_Classifier_1](https://user-images.githubusercontent.com/52208793/96531297-ae46ca00-125f-11eb-8c64-1845b39d7ab0.jpg)
![Decision_Tree_Classifier_2](https://user-images.githubusercontent.com/52208793/96531625-77bd7f00-1260-11eb-9eb2-458192c9f1ea.jpg)
![decision_tree](https://user-images.githubusercontent.com/52208793/96531518-34631080-1260-11eb-9e0e-51934de7ae0f.png)
![Decision_Tree_Classifier_3](https://user-images.githubusercontent.com/52208793/96531842-e995c880-1260-11eb-9ef5-c41edf43546c.jpg)

![Decision_Tree_Classifier_4](https://user-images.githubusercontent.com/52208793/96531967-42fdf780-1261-11eb-9d9e-344b4f7d48aa.jpg)
![Decision_Tree_Classifier_5](https://user-images.githubusercontent.com/52208793/96532072-750f5980-1261-11eb-8a91-e7639f740664.jpg)
![Decision_Tree_Classifier_6](https://user-images.githubusercontent.com/52208793/96532677-c66c1880-1262-11eb-913b-e782e6462a4a.jpg)
![decision_tree_max_depth_6](https://user-images.githubusercontent.com/52208793/96532477-61b0be00-1262-11eb-86c7-60873fad6139.png)

![Decision_Tree_Classifier_7](https://user-images.githubusercontent.com/52208793/96532937-485c4180-1263-11eb-834d-34522219d9cd.jpg)
![decision_tree_max_depth_7](https://user-images.githubusercontent.com/52208793/96532480-62e1eb00-1262-11eb-9ccd-e64ab2acd0c9.png)
![Decision_Tree_Classifier_8](https://user-images.githubusercontent.com/52208793/96533136-b56fd700-1263-11eb-8134-f11979b34495.jpg)
![Decision_Tree_Classifier_9](https://user-images.githubusercontent.com/52208793/96533335-1b5c5e80-1264-11eb-82fb-099be1bbffcc.jpg)
![decision_tree_max_depth_8](https://user-images.githubusercontent.com/52208793/96532486-64abae80-1262-11eb-9c7d-6d15e9ab2528.png)
![Decision_Tree_Classifier_10](https://user-images.githubusercontent.com/52208793/96533436-58285580-1264-11eb-86ef-30bfb17c9027.jpg)

![Decision_Tree_Classifier_11](https://user-images.githubusercontent.com/52208793/96533688-b2291b00-1264-11eb-8847-0465dbf7de7a.jpg)
![decision_tree_max_depth_9](https://user-images.githubusercontent.com/52208793/96532462-59f11980-1262-11eb-8d41-606f5c8c9be3.png)
![Decision_Tree_Classifier_12](https://user-images.githubusercontent.com/52208793/96534048-5f9c2e80-1265-11eb-9a3e-73f35b581126.jpg)

![Decision_Tree_Classifier_13](https://user-images.githubusercontent.com/52208793/96534266-befa3e80-1265-11eb-9bc2-77b7880572cc.jpg)
![decision_tree_max_depth_10](https://user-images.githubusercontent.com/52208793/96534334-dfc29400-1265-11eb-9843-b516cce01b3d.png)
![Decision_Tree_Classifier_14](https://user-images.githubusercontent.com/52208793/96534427-14365000-1266-11eb-9e79-bde2f5e39e2a.jpg)

It is very important to try another kind of classifier, so let's do it.

### Support Vector Classification

![SVC_1](https://user-images.githubusercontent.com/52208793/96534541-5364a100-1266-11eb-928f-092a454dbc80.jpg)
![SVC_2](https://user-images.githubusercontent.com/52208793/96534689-9de61d80-1266-11eb-9595-25298f48617b.jpg)

### Naive Bayes

![Naive_Bayes_1](https://user-images.githubusercontent.com/52208793/96534851-f1f10200-1266-11eb-89ab-13906e26d2b7.jpg)

### Logistic Regression

![Logistic_Regression_1](https://user-images.githubusercontent.com/52208793/96535377-113c5f00-1268-11eb-88d4-e42d9f3de490.jpg)
![Logistic_Regression_2](https://user-images.githubusercontent.com/52208793/96535470-447eee00-1268-11eb-9ffc-9eb655223786.jpg)

### Random Forest Classifier

![Random_Forest_Classification_1](https://user-images.githubusercontent.com/52208793/96535649-a7708500-1268-11eb-9cfd-e0583a49f276.jpg)
![Random_Forest_Classification_2](https://user-images.githubusercontent.com/52208793/96535789-fe765a00-1268-11eb-8ff5-53c196619dc0.jpg)
![Random_Forest_Classification_3](https://user-images.githubusercontent.com/52208793/96535853-2cf43500-1269-11eb-93e4-a300bffa6b84.jpg)

### XGBoost Classifier

![XGBoost_Classification_1](https://user-images.githubusercontent.com/52208793/96536067-a0964200-1269-11eb-9b65-1009a8871222.jpg)
![XGBoost_Classification_2](https://user-images.githubusercontent.com/52208793/96536149-cf141d00-1269-11eb-9300-032953482073.jpg)
![XGBoost_Classification_3](https://user-images.githubusercontent.com/52208793/96536258-071b6000-126a-11eb-82d4-e815b7985093.jpg)
![XGBoost_Classification_4](https://user-images.githubusercontent.com/52208793/96536327-2f0ac380-126a-11eb-8433-08126159c12b.jpg)

### Conclusion

Random Forest Classifier and XGBoost Classifier presented very similar accuracy but XGBoost Classifier presents a better
performance than Random Forest Classifier
Therefore I will choose XGBoost Classifier to do the new Campaign

![the_office_3](https://user-images.githubusercontent.com/52208793/96536909-6fb70c80-126b-11eb-8a19-e67fb174828e.gif)

