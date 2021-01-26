# Instacart-Market-Basket-Analysis  
## Objective  
- Recommend products based on products in users shopping cart  
- Develop marketing strategies by clustering customers based on their shopping habits  
- Predict products that a customer will have in their next order for sure  
## Exploratory Data Analaysis  
### Data - [Instacart](https://www.kaggle.com/c/instacart-market-basket-analysis/data)  
### Relationship between files  
![RelationalData](https://user-images.githubusercontent.com/56847819/105785614-51873980-5f49-11eb-84fc-edc1cf2c4b85.jpg)  
Customer shopping habits - 	Most of the orders are placed on Sunday morning and Saturday evening  
![Frequency](https://user-images.githubusercontent.com/56847819/105786208-9e1f4480-5f4a-11eb-967b-c44020db9eb3.png)  
Reorder Interval - Most of the users will reorder weekly and monthly  
![Reorder](https://user-images.githubusercontent.com/56847819/105786316-d3c42d80-5f4a-11eb-8015-b8c978415cbe.png)  
Aisle and Department- This plot shows product counts in Departments and Aisles. Count is represented by size. Produce department has the highest product count, fresh fruits and vegetables aisles within this department are ordered more.  
![treemap](https://user-images.githubusercontent.com/56847819/105786731-a2982d00-5f4b-11eb-890b-5fe9725cecd9.png)
## Association Rule Mining  
Recommendations are made on aisle level as having 39K unique products made it difficult to visually represent. 20k rules are generated with aisle level which is again difficult to represent visually. To overcome this rules are categorized into 3 categories based on lift. Lift here is ranging from 0 to 5.25.  
### Low Impact  
These product combinations have lift less than 1 which means they should not be recommended together.  
![lowimpact](https://user-images.githubusercontent.com/56847819/105786851-d2473500-5f4b-11eb-8737-aa688f64c2d6.png)  
### Medium Impact  
These products have lift values ranging from 1 to 2. They can be recommended together but will not generate high revenue.  
### High Impact  
These products have lift values ranging from 5 to 5.25. These products have to be recommended together and will generate high revenue to instacart.  
## Customer Segementation  
Ideal number of clusters are determined by elbow method and checking there is no overlap after visualizing.  
### Cluster-0  
These are customers where instacart should concentrate a lot and develop marketing strategies so they order frequently. Whenever they order they have low average number of orders and lower number of products  
### Cluster-1  
These cluster customer visit instacart often but they don't bring great revenue as they have less orders and products. 
### Cluster-2  
These are the favorite customers of instacart as they keep ordering often and have good total orders and products. Strategies should be developed in a way to reward the customer loyalty and retain the customers.  
## Predict Products In Next Order  
Created 12 new features to run XGBoost and LightGB algorithms. XGBoost has given highest F1 score at a probability threshold of 0.17  




