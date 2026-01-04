# 🏨 Hotel Booking Cancellation Analysis

## About
This project analyzes hotel booking cancellation data to uncover patterns, trends, and factors influencing cancellations. The primary objective is to provide actionable insights for hotels to reduce cancellation rates, improve customer retention, and optimize revenue management strategies. The dataset utilized in this project is sourced from the Kaggle Hotel Booking dataset : https://www.kaggle.com/datasets/mojtaba142/hotel-booking

## Purposes of the Project
The main goal of this project is to understand the dynamics of hotel booking cancellations, identify key drivers behind cancellations, and provide recommendations for improving booking policies and customer satisfaction.

## About Data
This project's data was obtained from the Kaggle Hotel Booking dataset. It encompasses booking records from two hotel types: **City Hotel** and **Resort Hotel**.  
The dataset contains 32 columns and over 40,000 rows, covering details such as booking dates, customer demographics, stay duration, and cancellation status.

| Column                  | Description                                                                 | Data Type        |
|--------------------------|-----------------------------------------------------------------------------|------------------|
| hotel                    | Type of hotel (City Hotel or Resort Hotel)                                 | VARCHAR(30)      |
| is_canceled              | Whether the booking was canceled (1 = Yes, 0 = No)                         | INT              |
| lead_time                | Number of days between booking and arrival                                 | INT              |
| arrival_date_year        | Year of arrival                                                            | INT              |
| arrival_date_month       | Month of arrival                                                           | VARCHAR(15)      |
| arrival_date_week_number | Week number of arrival                                                     | INT              |
| stays_in_weekend_nights  | Number of weekend nights stayed                                            | INT              |
| stays_in_week_nights     | Number of weekday nights stayed                                            | INT              |
| adults                   | Number of adults                                                           | INT              |
| children                 | Number of children                                                         | INT              |
| country                  | Country of origin                                                          | VARCHAR(50)      |
| market_segment           | Booking source (e.g., Online TA, Direct, Corporate)                        | VARCHAR(50)      |
| distribution_channel     | Distribution channel (e.g., TA/TO, Direct)                                 | VARCHAR(50)      |
| is_repeated_guest        | Whether the guest has booked before                                        | INT              |
| reserved_room_type       | Type of reserved room                                                      | VARCHAR(5)       |
| assigned_room_type       | Type of assigned room                                                      | VARCHAR(5)       |
| rservation_status        | Status of reservation :**Booked** or **Cancelled**                         | VARCHAR(50)              |
| deposit_type             | Type of deposit made                                                       | VARCHAR(30)      |
| customer_type            | Type of customer (Transient, Group, Contract)                              | VARCHAR(30)      |
| adr                      | Average Daily Rate                                                         | DECIMAL(10, 2)   |

## Analysis List:

1. **Cancellation Analysis**  
   > Explore cancellation rates across hotel types, booking channels, and customer segments to identify high-risk areas.

2. **Customer Behavior Analysis**  
   > Understand customer demographics, booking lead times, and repeat guest behavior to evaluate loyalty and predict cancellations.

3. **Revenue Analysis**  
   > Assess the impact of cancellations on Average Daily Rate (ADR), revenue loss, and seasonal trends.

4. **Seasonality & Trends**  
   > Identify peak months, weekdays, and seasonal patterns influencing cancellations and bookings.

## Approach Used

***1. Data Transformation***  
- Using PowerQuery, we drop unwanted columns (lead_time, arrival_date_weekend_number, stays_in_weekend_nights, stays_in_week_nights).  
- Other dropped columns are : market_segment, distribution_channel .  
- Remove outliers in lead_time and ADR where necessary.
- 
***1. Data Cleaning***  
- Handle missing values (e.g., children column, country codes).  
- Standardize categorical variables for consistency.  
- Remove outliers in lead_time and ADR where necessary.  

***2. Feature Engineering***  
- Create new columns such as:  
  - **stay_duration** = stays_in_weekend_nights + stays_in_week_nights  
  - **is_family** = flag for bookings with children  
  - **season** = categorize months into seasons (Winter, Summer, etc.)  
- Add calculated fields in Excel for cancellation percentages and revenue impact.  

***3. Exploratory Data Analysis (EDA)***  
- Used **Pivot Tables** to summarize cancellation rates by hotel type, country, and booking channel.

- Built **Dashboards** in Excel to visualize:  
  - Cancellation trends over time  
  - ADR distribution by hotel type  
  - Customer type vs. cancellation likelihood  
---

<h2><a class="anchor" id="research-questions--key-findings"></a>Research Questions & Key Findings</h2>

1. **Cancellation Hotspots**: City Hotel shows 15% higher cancellation rate than Resort Hotel  
2. **Lead Time Effect**: Bookings with lead time > 60 days → 2.3x more likely to cancel  
3. **Customer Type Impact**: Transient customers account for 76% of cancellations  
4. **Revenue Loss**: Estimated $1M+ lost due to cancellations in peak months  
5. **Deposit Type Influence**: Refundable deposits → 3x higher cancellation rate than non-refundable  
6. **Seasonality Trends**: August and January show peak cancellation volumes across both hotel types  

---

<h2><a class="anchor" id="dashboard"></a>Dashboard</h2>

- Excel Dashboard includes:
  - KPI Cards: Total Bookings, Cancellation Rate, ADR, Revenue Loss  
  - Charts:  
    - Cancellation Rate by Hotel Type  
    - Monthly Cancellation Trends  
    - Lead Time vs Cancellation Probability  
    - Customer Type vs Cancellation  
    - Country-wise Cancellation Map  
    - Deposit Type Impact Pie Chart  
  - Pivot Table Insights:
    - Distribution Channel vs Cancellation  
    - ADR by Hotel Type and Month  
    - Repeat vs New Guest Behavior  

![Hotel Cancellations Dashboard](images/hotel_dashboard.png)

---

<h2><a class="anchor" id="how-to-run-this-project"></a>How to Run This Project</h2>

1. Download the dataset from Kaggle:  
   - [Hotel Booking Dataset](https://www.kaggle.com/datasets/mojtaba142/hotel-booking)  
2. Open the Excel workbook:  
   - `Hotel_Cancellations_Analysis.xlsx`  
3. Navigate to the following sheets:  
   - `Raw_Data` → Cleaned dataset  
   - `Pivot_Insights` → Pivot tables for analysis  
   - `Dashboard` → Interactive visuals and KPIs  
4. Use slicers to filter trends by different years (2017-19) 

---

<h2><a class="anchor" id="final-recommendations"></a>Final Recommendations</h2>

- Introduce incentives for early bookings with shorter lead times  
- Promote non-refundable deposit options to reduce cancellations  
- Target transient customers with loyalty programs  
- Monitor seasonal trends to adjust pricing and policies  
- Improve booking experience for high-cancellation countries  

---

<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

**Deepesh Vanjani**  
Data Analyst  
📧 Email: connectwithyoungceo@gmail.com  
🔗 [LinkedIn] : (https://www.linkedin.com/in/deepeshvanjani/)
