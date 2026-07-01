Sales Revenue Analysis – Figuring Out What Actually Drives Sales

I built this project because I wanted to dig deep into e-commerce data to find out what really makes an order profitable. Is it the product category? The discount size? How fast we ship? Or is it just about slapping a high price tag on electronics?

To answer that, I took a dataset of 5,000 retail orders and went full detective mode on it using Python, stats, and a bit of machine learning.

The  Questions I Wanted to Answer

- Which categories (Electronics, Clothing, Home, Beauty) bring in the most cash?
- Are some regions happier with their orders than others?
- Do big discounts actually drive more revenue, or do they just hurt our margins?
- How much does delivery time matter?
- Can I build a model that accurately predicts order revenue?

What  Used
- Pandas for cleaning and wrangling the data.
- Matplotlib & Seaborn for charts and visualizations.
- SciPy for running ANOVA and T-tests (to separate real trends from random noise).
- Scikit-learn for building a Linear Regression model.
- SQLite to store and query the transformed data.

- Small discounts win. Big discounts lose.
  I ran both ANOVA and a T-test comparing 0-10% discounts vs 30-50% discounts. The p-values came back as < 0.001 for both tests. That’s a 99.9% confidence level huge Turns out, bigger discounts actually reduce revenue. Who knew? The data is crystal clear on this one.

- Electronics and Clothing are the cash cows.
  Together, they make up ~65.8% of total revenue. Electronics takes the crown at 35.8%, followed by Clothing at 30.0%. Home and Beauty trail behind. The difference isn't statistically bulletproof (p = 0.429), but it’s still a solid directional signal for where to focus.

- Customer satisfaction is surprisingly even across regions.
  Every region sits around a solid 3/5 star rating. The West makes the most money, but everyone keeps the customers equally happy.

- Delivery times are consistent, averaging around 6 days everywhere. There's room to optimize that to 4–5 days to boost the experience.
The Prediction Model
I trained a Linear Regression model using features like quantity, unit_price, discount, delivery_days, and customer_rating. It achieved an R² score of 0.8946, meaning it explains 89% of the variance in revenue.

The RMSE was 0.1073, which means it’s really accurate. "Quantity" and "Unit Price" ended up being the heavy hitters for prediction power.

My Recommendations 
1. Stop the big discounts: Stick to small discounts (0-10%). This is statistically proven and the  actionable insight.
2. Double down on Electronics & Clothing: they're clearly the fan favorites.
3. Use those high ratings to run loyalty programs and get repeat buyers.
4. Try to shave 1-2 days off delivery to make customers even happier.
5. Integrate the model into business planning it’s accurate enough to forecast sales, plan inventory, and set smarter prices.
