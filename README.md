# 🏨 Hotel Booking Cancellation Analysis

## About
This project analyzes hotel booking cancellation data to uncover patterns, trends, and factors influencing cancellations. The primary objective is to provide actionable insights for hotels to reduce cancellation rates, improve customer retention, and optimize revenue management strategies. The dataset utilized in this project is sourced from the Kaggle Hotel Booking Demand dataset.

## Purposes of the Project
The main goal of this project is to understand the dynamics of hotel booking cancellations, identify key drivers behind cancellations, and provide recommendations for improving booking policies and customer satisfaction.

## About Data
This project's data was obtained from the Kaggle Hotel Booking Demand dataset. It encompasses booking records from two hotel types: **City Hotel** and **Resort Hotel**.  
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
| booking_changes          | Number of changes made to the booking                                     | INT              |
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
