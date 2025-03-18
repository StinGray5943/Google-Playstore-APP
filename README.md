# Google Play Store App Analysis
 ##📌 Project Overview
Imagine walking into a vast digital marketplace—millions of apps, billions of downloads, and countless user experiences. The Google Play Store is more than just a collection of apps; it’s a dynamic ecosystem where user engagement, ratings, and revenue define success.

In this Power BI project, I built an interactive dashboard that dives into key metrics, revealing insights into app performance, user sentiment, revenue trends, and engagement levels. With bookmarks, tooltips, and drill-through pages, navigating insights has never been smoother.

## 📂 Data Sources & Cleaning Process

📍 Source: Kaggle

📍 File Type: CSV

📍 Data Structure: Multiple tables

Before I could uncover insights, I had to clean the dataset—which, as expected, came with a few surprises!

## 🧼 Data Cleaning Challenges & Fixes
✅ Installs Column Issues

The "Installs" column had values like "10,000+", making it non-numeric.
Fix: Removed commas (,) and plus signs (+) and converted it into a numeric format.

✅ Unexpected Value in Installs

Discovered a "Free" value in the Installs column—obviously, an error!
Fix: Replaced "Free" with 0, assuming those apps had no recorded installs.

✅ Price Column Issue

Found an unusual value "Everyone" under Price. Turns out, row 10472 was misaligned!
Fix: Identified and removed the corrupted row before proceeding with price conversion.
Now that the dataset was clean, it was time to transform raw numbers into meaningful insights! 🚀

## 📊 Key Performance Indicators (KPIs)
What defines app success? These KPIs help answer that question:

📈 Total Installs → How many times have apps been downloaded?

⭐ Average Rating → Are users satisfied with the apps?

💬 Number of Reviews → Which apps generate the most feedback?

😊 Sentiment Analysis → What are users saying? (Positive, Neutral, Negative)

💰 Revenue Per User → Are paid apps making money?


📊 Retention Rate → How many users continue using the app after downloading?

📌 Dashboard Pages & Visualizations

### 📍 1. Overview Page (Big Picture of the App Market)
👀 Key Insights:

📊 168 billion total installs across all apps!

💰 Paid app revenue: **$388.45M**

⭐ Average rating: **4.19** (Users seem generally satisfied!)

🎮 **Games** category dominates in installs—no surprise there!

🚀 Visuals Used:

✔ **KPI Cards** → Display total installs, revenue, and ratings.

✔ **Bar Chart** → App distribution by category.

✔ **Gauge Chart** → Tracks average rating trends.


### 📍 2. App Insights (Deep Dive into Top Apps)

👀 Key Insights:

🏆 Highest Rated App: Bowmaster **(4.7 ⭐)**

📥 Most Downloaded App: **Subway Surfers**

😃 Most app sentiments are **positive!**

📆 **July** had the highest number of downloads per year!

🚀 Visuals Used:
✔ **Waterfall Chart** → Top 10 most rated apps.

✔ **Column Chart** → Top 10 most installed apps.

✔ **Pie Chart** → Sentiment analysis breakdown (Positive, Neutral, Negative).

✔ **Line Chart** → Installs over time (Yearly trend).

### 📍 3. User Engagement (How Active Are Users?)
👀 Key Insights:

🎮 **Game apps** received the highest number of reviews and ratings.

📸**Instagram** had the highest number of review counts!

🔄 Higher ratings correlate with more reviews.

🚀 Visuals Used:
✔ **Scatter Plot** → Review count vs. Rating distribution per category.

✔ **Column Chart** → Number of reviews per app.

✔ **Column Chart** → Content rating distribution (Everyone, Teen, Mature).


⚡ DAX Calculations Used
```   ✅ Average Rating Calculation

Avg_Rating = AVERAGE(googleplaystore[Rating])

```

 ```  ✅ Total Installs Calculation

Total_Installs = SUM(googleplaystore[Installs]) ```



```   ✅ Revenue Per User Calculation


Revenue_Per_User = DIVIDE(SUM(googleplaystore[Revenue]), SUM(googleplaystore[Active Users]), 0) ```


```   ✅ Sentiment Count Calculation

Sentiment_Count = COUNT(googleplaystore_user_reviews[Sentiment]) ```



## Interactivity Features
📍 Bookmarks & Navigation → Easily switch between different analysis pages.

📍 Tooltips → Hover over charts to see hidden insights (e.g., revenue per app).

📍 Drill-Through Pages → Click on an app to explore its detailed statistics.


📍 Slicers → Filter data by category, price type (free/paid), sentiment, and year.


### 🔍 Final Insights & Takeaways
✅ High-rated apps tend to have more reviews. This suggests that positive user experience leads to higher engagement.

✅ Paid apps generate more revenue per user but struggle with installs. Free apps dominate downloads, but monetization is harder.

✅ Sentiment analysis shows gaming apps get mixed feedback. Some users love them, while others complain about ads and in-app purchases.

✅ Retention rates vary by category. Productivity apps keep users engaged longer, while entertainment apps see higher churn rates.

### 🚀 Next Steps & Future Improvements

🔹 Real-Time Data Updates: Implement API integration to keep insights fresh.

🔹 Predictive Analytics: Use machine learning models to forecast app success.

🔹 Geo-Analysis of Installs: Map downloads by country to uncover market trends.

This is just the beginning—data keeps evolving, and so do insights! 📊✨

