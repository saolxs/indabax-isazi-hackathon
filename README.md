## Isazi IndabaX 2024 Hackathon Challenge

### Problem Domain

In the fast-paced retail sector, understanding and predicting sales volumes is crucial for effective inventory management, pricing strategy, and promotional planning. Accurately forecasting sales not only optimizes operational efficiencies but also enhances customer satisfaction by ensuring product availability and competitive pricing. 

### Challenge Description

Participants are tasked with developing a predictive model that forecasts the future sales volumes of various products based on historical sales data. The dataset provided includes daily sales figures, promotional activities, and pricing information. The primary objective is to predict the volume of product sales for upcoming dates, which is critical for managing supply chain and marketing strategies.

### Objectives

- **Model Development**: Build robust time series forecasting models that can accurately predict sales volumes.
- **Feature Engineering**: Identify and harness the influence of promotional activities and pricing strategies on sales volumes.

### Dataset Description

The problem dataset provides daily sales data for various products, capturing both sales performance and promotional activities. Each row in the dataset represents a single day's performance for a specific product. Below is an overview of each column in the dataset:

- `sales_date`: The date of sale, indicating when the transaction occurred.
- `product_code`: A unique identifier for each product. Each product code corresponds to an individual time series in the dataset.
- `volume`: The quantity of the product sold on the given day. This is our response variable which we want to forecast.
- `rsp`: Retail Standard Price on the day of sale. It indicates the standard price of the product without any promotions.
- `is_promo`: A binary flag (1 or 0) that denotes whether any promotion was applied on the product for that day. A value of 1 indicates a promotion was in effect, while 0 indicates no promotion.
- `is_single_price_promo`: A binary flag indicating whether the promotion was a single product discount (e.g., 10% off). This is the most common type of promotion.
- `is_multibuy_promo`: A binary flag indicating whether the promotion required purchasing multiple items (e.g., buy 2 get 1 free). This kind of promotion encourages bulk purchases.
- `rel_promo_price`: The relative price of the product during a promotion compared to the standard retail price. This measure helps understand the discount depth provided during promotional periods.
- `planned_promo_vol`: An estimation of the sales volume the retailer planned to achieve through the promotion.
  
### Evaluation Criteria

The evaluation of forecasting models in this challenge uses two primary metrics: Overall Forecast Accuracy and Relative Bias. These metrics are calculated as follows:

1. **Total Sales Volume**: Sum the actual sales volumes across all time series to obtain the total actual volume.
2. **Total Predicted Volume**: Sum the predicted sales volumes across all time series.
3. **Total Error**: Compute the absolute error between predicted and actual sales volumes for each prediction, and then sum these errors across all time series.
4. **Relative Error**: Divide the total error by the total actual volume to obtain the relative error.
5. **Forecast Accuracy**: Calculate forecast accuracy as `1 - Relative Error`.
6. **Relative Bias**: Compute the relative bias by subtracting the total actual volume from the total predicted volume and dividing the result by the total actual volume. This metric indicates the tendency of the models to overestimate or underestimate the sales volumes.

These metrics ensure a comprehensive evaluation of model performance:
- **Forecast Accuracy** emphasizes the precision of individual predictions and is weighted towards time series with higher sales volumes, which are more significant for overall business performance.
- **Relative Bias** measures the overall tendency of the predictions to be higher or lower than actual values, providing insight into the systemic accuracy of the models.

Models will be judged not only on how accurately they predict sales volumes but also on how well they maintain balance, avoiding systematic overestimation or underestimation of sales.

### Usefulness of the Challenge

The solutions developed during this hackathon will help businesses:
- **Enhance Decision Making**: Improve inventory and pricing decisions by predicting demand more accurately.
- **Optimize Promotional Strategies**: Understand the impact of various promotional tactics on sales and adjust these strategies to maximize profitability.
- **Reduce Waste and Shortages**: Better demand forecasts lead to more efficient supply chain management, reducing both excess stock and product shortages.

### Outcome

This challenge offers participants the opportunity to apply machine learning techniques to a real-world problem, enhancing their skills in data manipulation, model building, and evaluation. The top-performing models could potentially be implemented in real retail environments, demonstrating the practical value of predictive analytics in business contexts.