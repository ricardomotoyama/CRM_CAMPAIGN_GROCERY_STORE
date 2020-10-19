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

# Outliers for feature Income
The boxplot shows there are some outliers for the feature Income

![income_before_treat_outliers](https://user-images.githubusercontent.com/52208793/96518357-1d60f600-1241-11eb-8253-1c904f273849.jpg)

Treatment outliers:
1) Drop Income greater than 666.666
2) Applying interquartile range





