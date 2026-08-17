# **BingePlay – Streaming Platform SQL Analytics**

**Author:** Somyajeet Satapathy

## 📌 Project Overview

BingePlay is a SQL-based data analytics project designed to analyze user behavior, subscriptions, content performance, and engagement patterns for a fictional streaming platform.

The project uses a relational database containing information about users, subscriptions, shows, watch sessions, and ratings.

The objective of this project is to answer practical business questions using SQL and transform raw streaming-platform data into meaningful analytical insights.

---

## 🎯 Project Objectives

The project focuses on analyzing:

- Active subscriptions and monthly revenue
- User signup trends
- Device-wise viewing behavior
- Rating distribution
- Original vs acquired content
- Binge-watching behavior
- Users who signed up but never watched
- Premium/Family users with potentially low plan utilization
- Subscription upgrade behavior
- Viewer comeback behavior after unfinished shows
- Consecutive-week engagement
- Potential churn signals based on declining watch time

---

## 🗄️ Database

**Database:** `bingeplay`

The analysis uses the following main tables:

- `users`
- `subscriptions`
- `shows`
- `watch_sessions`
- `ratings`

The dataset represents streaming-platform activity during 2024 and is used to perform SQL-based business analysis.

---

## 📊 Business Questions Answered

### Q1 – Active Revenue

Identifies active subscriptions and calculates the corresponding monthly subscription revenue.

The analysis considers subscriptions with:

- `status = 'active'`
- An end date that is either `NULL` or later than June 30, 2024.

---

### Q2 – Signup Momentum

Analyzes the number of new users signing up during each month of 2024.

This helps identify signup momentum and variations in customer acquisition over time.

---

### Q3 – Device Analytics

Analyzes viewing behavior by device type.

Metrics include:

- Total sessions
- Total watch minutes
- Average watch minutes per session
- Completion rate

This provides insight into how users consume content across different devices.

---

### Q4 – Rating Distribution

Analyzes the distribution of content ratings from users.

The analysis calculates:

- Number of ratings for each star level
- Percentage of total ratings represented by each star level
- Percentage of ratings that are 4 or 5 stars

This helps evaluate overall audience satisfaction.

---

### Q5 – Originals vs Acquired Content

Compares BingePlay's original content with acquired content.

Metrics include:

- Number of shows
- Average IMDb rating
- Average release year

This provides a high-level comparison of content quality and catalog characteristics.

---

### Q6 – Binge Day Detection

Identifies users who watched the same show at least five times on the same day.

The analysis determines:

- The user with the highest number of binge days
- The total number of binge days during Q2 2024

This helps identify highly engaged viewing behavior.

---

### Q7 – Q1 Signups Who Never Watched

Measures users who signed up during Q1 2024 but never recorded a watch session.

This identifies a potentially important activation problem where newly acquired users do not begin consuming content.

---

### Q8 – Over-Paying Premium/Family Users

Identifies users currently on Premium or Family plans who have not watched content requiring those higher-tier plans.

This can highlight users who may not be receiving enough value from their current subscription tier.

---

### Q9 – Upgrade Success Cohort

Analyzes users who:

1. Signed up during January 2024
2. Initially subscribed to the Basic plan
3. Later upgraded to Premium or Family
4. Upgraded before the end of June 2024

The analysis calculates:

- Number of users who upgraded
- Average number of days from signup to first upgrade

---

### Q10 – Cliffhanger Comebacks

Identifies comeback viewing behavior.

A comeback event occurs when a user:

1. Watches a show without completing the session
2. Returns to the same show between 1 and 7 days later

The analysis calculates the total number of comeback events and identifies the show associated with the highest number of comeback events.

---

### Q11 – Consecutive-Week Engagement

Analyzes weekly viewing activity to identify users who maintain engagement across consecutive weeks.

The analysis determines:

- Number of users with at least a 4-week viewing streak
- Longest consecutive-week viewing streak
- User associated with the longest streak

This provides a measure of sustained user engagement.

---

### Q12 – Churn Signal Detection

Identifies users whose watch time decreased significantly from May to June 2024.

The analysis:

- Calculates total watch minutes in May
- Calculates total watch minutes in June
- Compares May and June activity
- Flags users whose June watch time is 50% or less of their May watch time
- Calculates the percentage decline

Users showing a substantial decline in viewing activity can be considered potential churn-risk users.

---

## 🛠️ Technologies Used

- **MySQL**
- **SQL**
- Relational Database Concepts
- Aggregations
- Joins
- Subqueries
- Common Table Expressions (CTEs)
- Window Functions
- Date Functions
- Conditional Aggregation

---

## 🧠 SQL Concepts Demonstrated

This project demonstrates practical usage of:

- `SELECT`
- `WHERE`
- `GROUP BY`
- `ORDER BY`
- `HAVING`
- `JOIN`
- `LEFT JOIN`
- `UNION ALL`
- `CASE`
- `COALESCE`
- `COUNT`
- `SUM`
- `AVG`
- `ROUND`
- `MIN`
- `MAX`
- `DISTINCT`
- `EXISTS`
- `NOT EXISTS`
- Correlated subqueries
- Common Table Expressions (`WITH`)
- Window functions
- `ROW_NUMBER()`
- `YEAR()`
- `MONTH()`
- `YEARWEEK()`
- `DATEDIFF()`
- `DATE_ADD()`

---

## 📈 Analytical Insights

The project demonstrates how SQL can be used beyond simple data retrieval to answer real-world business questions.

The analysis covers multiple stages of the streaming customer lifecycle:

**Acquisition → Subscription → Engagement → Content Consumption → Upgrade → Retention → Churn Risk**

This makes the project useful as an example of business-oriented SQL analytics rather than only database querying.

---

## 🔍 Key Analytical Areas

### Customer Acquisition
Signup trends are analyzed to understand when users join the platform.

### Monetization
Active subscriptions and subscription pricing are used to estimate recurring monthly revenue.

### Engagement
Watch sessions, watch minutes, binge behavior, and weekly streaks are used to measure user engagement.

### Content Performance
Ratings and original/acquired content comparisons provide insight into the content catalog.

### Subscription Behavior
Upgrade analysis helps understand how users move from Basic to higher subscription tiers.

### Retention & Churn
Comeback behavior and declining watch time are used to identify retention patterns and potential churn signals.

---

## 💡 Business Value

A streaming platform could use analyses like these to:

- Improve customer acquisition strategies
- Understand user engagement
- Optimize subscription plans
- Identify users at risk of churn
- Improve content recommendations
- Evaluate original content
- Understand device usage
- Improve retention strategies
- Identify opportunities for subscription upgrades

---

## 👨‍💻 Author

**Somyajeet Satapathy**

This project was created as a practical SQL analytics project focused on applying database querying and analytical techniques to a realistic streaming-platform business scenario.

---

## ⭐ Conclusion

The BingePlay SQL Analytics project demonstrates the use of SQL to convert raw relational data into actionable business analysis.

By combining subscription, user, content, rating, and viewing-session data, the project explores the complete streaming-platform user journey and demonstrates practical SQL skills applicable to real-world data analyst and business intelligence roles.
