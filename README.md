# Retail-Store-EDA-discount-weekend
## Exploratory Analysis of Kroger 10.000 sales during one of their "Super Saver Weekend"

![A Kroger worker](https://www.modernretail.co/wp-content/uploads/sites/5/2019/05/Kroger.jpg?w=1280&h=601&crop=1)

##### Kroger is a major retail chain, often referred to as a supermarket or grocery store, offering a wide range of food and household products. It operates numerous stores across the United States.

##### In this Exploratory Data Analysis, we break down nearly 10,000 sales transactions that occurred during Kroger's Super Saver Weekend.

## Data acquisition and formats

##### The data was obtained from Kaggle in .csv format and was later on imported as a DataFrame using Pandas library. Once imported, we have transaction data, where each row corresponds to a transaction and each column corresponds to a product. Cells contain the name of the product.

##### As explained in the code (.ipynb) this wasn't very optimized upon later analysis so we had to wrangle the data and transorm the structure.

##### First things first, we import NumPy, Pandas, Matplotlib.pyplot, and Seaborn libraries. 
##### After creating a copy to avoid any modifications in the raw data, we use methods like .info(), .mean(), .shape() and .columns(), .dtypes() to start analyzing. Owing to these methods we are able to observe that the DataFrame has 9835 rows (transactions) and 32 columns (maximum quantity of transactions, one column per product purchased). The .dtypes() method indicates string data in the Dataframe.

##### We then manage the null values by applying a value to them of '0' so we can proceed with the analysis. Later on we melt the Dataframe, this way we have a product (variable) per column and each row is still a transaction (a tidier dataset).

## Exploratory analysis: insights and conclusions

##### During the "Super Saving Weekend" at Kroger, each customer bought an average of 4.40 products and range of 170 different products are sold.

##### Through the utilization of a histogram, we are afforded the opportunity to meticulously examine the 50 most sold products during this weekend with special discounts. 

##### Whole milk stands out as the highest-selling product by a significant margin, followed by vegetables, rolls/buns, soda, and yogurt. Except shopping bags, the totality of the 50 most sold products are food items. This is understandable as Kroger mainly sells groceries, including fresh produce, meat, and dairy products.

##### There is a presence of four high-sugar foods and one alcoholic beverage among the top 20 best-selling products: rolls/buns, soda, pastry, bottled beer, and whipped/sour cream. 

##### Let's take a look:
![Image Title](https://github.com/vicenclleixa/Retail-Store-EDA-discount-weekend/blob/main/images/Product%20Top-Sellers.png?raw=true)

##### The least sold products are generally cleaning products, snacks, personal care items, and specialized frozen or fresh foods. The least sold product is baby food. Meanwhile, sound storage medium, preservation products, bags, kitchen utensils, and frozen chicken are among the least sold. 

##### Here we can see the histogram depicting the 50 least sold products during the Super Saver weekend:
![Image Title](https://github.com/vicenclleixa/Retail-Store-EDA-discount-weekend/blob/main/images/Least%20sold%20products.png?raw=true)

##### Which products have the highest probability of being purchased together? 

##### We calculate the correlation between the most bought products and this is result:
![Image Title](https://github.com/vicenclleixa/Retail-Store-EDA-discount-weekend/blob/main/images/Correlation%20Heatmap%20of%20Top%2030%20products.png?raw=true)

![Image Title](https://github.com/vicenclleixa/Retail-Store-EDA-discount-weekend/blob/main/images/Most%20commonly%20purchased%20products.png?raw=true)
## Most commonly bought pairs of products:
##### 1-Root vegetables and other vegetables
##### 2-Beef and root vegetables
##### 3-Root vegetables and whole milk
##### 4-Pip fruit and tropical fruit
##### 5-Other vegetables and whole milk
##### 6-Whipped/sour cream and other vegetables
##### 7-Tropical fruit and yogurt
##### 8-Yogurt and whole milk
##### 9-Butter and whole milk
##### 10-Citrus fruit and tropical fruit
##### 11-Domestic eggs and whole milk
##### 12-Tropical fruit and other vegetables
##### 13-Curd and whole milk
##### 14-Curd and yogurt
##### 15-Whipped/sour cream and whole milk
##### 16-Whipped/sour cream and yogurt
##### 17-Yogurt and other vegetables
##### 18-Citrus fruit and other vegetables
##### 19-Sausage and rolls/buns
##### 20-Tropical fruit and whole milk



