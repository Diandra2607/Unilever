# Background
This dataset contains comprehensive supply chain data for Unilever products, covering various aspects of the supply chain process from product details to logistics and manufacturing. The dataset includes 23 columns, providing valuable insights for analysis and optimization. From this dataset, it will be used multiple linear regression and clustering for market segmentation. 

# Data Preprocessing
The first thing after import needed libraries and the data is to do data preprocessing. The first step is check if there is a missing data. After checking it, there are no missing data on this dataset. The next step is creating dummy variables from Product type, Customer demographics, and Transportation models. After that, choose Product type, Customer demographics, Transportation models, Price, Availability, Stock Levels, Lead Times, Order Quantities, and Revenue Generated as Relevant variables with Product type, Customer demographics, Transportation models, Price, Availability, Stock Levels, Lead Times, and Order Quantities as independent variables and Revenue Genereated as dependent variable. Next, standardize all the variables needed.

# Decriptive Statistics
Based on the descriptive statistics for Price, Availability, Stock Levels, Lead Times, Order Quantities, and Revenue Generated, for price, the highest price is 99.2, while the lowest is 1.7, and the price's average is 49.5. For Availability, the highest availability is 1, the lowest availabity is 100, and the average number of items available is 48 items. For stock levels, the highest is 100, the lowest is 0, and the average stock levels are 48. For Lead Times, the highest lead time is 30, the lowest lead time is 1, and the lead time average is 16. For Revenue Generated, the highest is 9866.465458, the lowest is 1061.618523, and its average is 5776.048187.

# Correlation
The next step is calculate the correlation for all variables needed and make the correlation plot. Based on the correlation plot, there are some variables that has negative correlation, which means, their relationships are weak.

# Regression
After calculate the correlation, create a regression model with all variables needed. After create a regression model, do the simultaneous and partial test. Based on the regression simultaneous result, Product type, Customer demographics, Transportation models, Price, Availability, Stock Levels, Lead Times, and Order Quantities don't influence the Revenue Generated. However, stock leves influence the revenue generated more than Product type, Customer demographics, Transportation models, Price, Availability,  Lead Times, and Order Quantities. 

# Clustering
The next step is clustering. Before clustering, the first thing to do is to determine the optimum number of clusters with Silhouette method. Based on the Silhouette method, the optimum number of cluster is three clusters. After that, create the cluster with K-Means Method. 

* Segment 1:
1. High Price: Has the highest average price (59.86).
2. Moderate Availability: Has moderate product availability (46%).
3. Low Stock Levels: Has the lowest stock levels (33.82%).
4. Low Lead Times: Has the lowest lead times (12.18%).
5. Moderate Order Quantities: Has moderate order quantities (50.18%).
6. Moderate Revenue: Generates a moderate amount of revenue (5739.05).
7. Focus on Skincare: Has a higher proportion of skincare product purchases (0.41) compared to haircare (0.24).
8. Mix of Demographics: Has a mix of male (0.24), non-binary (0.18), and unknown (0.35) customer demographics.
9. Sea Transportation: Primarily uses sea transportation (1.0).
10. Interpretation: This segment represents customers who purchase higher-priced items, are less sensitive to availability, and likely order in moderate quantities. They seem to prefer skincare products and rely heavily on sea transportation. This could indicate international or bulk shipping.

* Segment 2:
1. Moderate Price: Has a moderate average price (50.61).
2. Moderate Availability: Has moderate product availability (45.98%).
3. Moderate Stock Levels: Has moderate stock levels (47.37%).
4. Moderate Lead Times: Has moderate lead times (16.52%).
5. Moderate Order Quantities: Has moderate order quantities (49.69%).
6. High Revenue: Generates the highest revenue (5939.37).
7. Balanced Product Preference: Has a relatively balanced preference for haircare (0.33) and skincare (0.41) products.
8. Mix of Demographics: Has a mix of male (0.20), non-binary (0.24), and unknown (0.33) customer demographics.
9. Rail Transportation: Significantly uses rail transportation (0.52).
10. Interpretation: This segment represents a high-value group that purchases mid-priced items in moderate quantities. They use a mix of transportation modes, including a significant proportion using rail. This could indicate domestic shipping or larger distribution centers.

* Segment 3:
1. Low Price: Has the lowest average price (41.23).
2. High Availability: Has the highest product availability (54.31%).
3. High Stock Levels: Has the highest stock levels (56.69%).
4. High Lead Times: Has the highest lead times (17.14%).
5. Moderate Order Quantities: Has moderate order quantities (47.79%).
6. Moderate Revenue: Generates a moderate amount of revenue (5493.63).
7. Focus on Haircare: Has a higher proportion of haircare product purchases (0.41) compared to skincare (0.38).
8. Mix of Demographics: Has a mix of male (0.21), non-binary (0.24), and unknown (0.24) customer demographics.
9. Road Transportation: Primarily uses road transportation (1.0).
10. Interpretation: This segment represents customers who purchase lower-priced items, are highly sensitive to availability, and likely order in moderate quantities. They favor haircare products and rely on road transportation, suggesting local or regional distribution.

# Insights
* Inventory Management: Segment 0 could benefit from improved stock management to avoid stockouts, even if they are less sensitive to availability. Segment 2, on the other hand, seems to prioritize availability, so maintaining high stock levels is crucial for this segment.
* Logistics: Different transportation modes are preferred by different segments. Optimizing logistics based on segment preferences could improve efficiency and reduce costs.
* Marketing and Product Strategy: Tailoring marketing messages and product offerings to each segment's preferences (e.g., focusing on skincare for Segment 0 and haircare for Segment 2) could increase sales and customer satisfaction.
* Pricing Strategy: Consider different pricing strategies for each segment based on their price sensitivity.
