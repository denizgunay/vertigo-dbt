# Daily Metrics Analytics Pipeline

This project demonstrates a simple analytics pipeline using Google Cloud Platform, dbt, and Looker Studio.

## 🔄 Data Flow Overview

1. **Raw Data Upload**  
   The raw event-level data was first uploaded to a **Google Cloud Storage bucket**.

2. **Loading into BigQuery**  
   The uploaded data was then ingested into **BigQuery**, where it resides under the `raw.data` table.

3. **dbt Integration**  
   The project was connected to BigQuery using **dbt (data build tool)**. A dbt model named `daily_metrics.sql` was created to perform daily aggregations, such as:

   - Daily Active Users (DAU)
   - Total in-app and ad revenue
   - ARPDAU
   - Win/loss ratios
   - Match and error metrics

   The model is materialized as a **table** in BigQuery for performance optimization.

4. **Looker Studio Dashboard**  
   The output of the `daily_metrics` model is visualized through a **Looker Studio dashboard**, offering a simple and interactive way to explore the data.

   🔗 [View the Dashboard](https://lookerstudio.google.com/reporting/68396851-730f-461f-92d2-5bfe17e13aee)


