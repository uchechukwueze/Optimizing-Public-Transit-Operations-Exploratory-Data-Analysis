<img width="1920" height="1080" alt="1" src="https://github.com/user-attachments/assets/e906f064-cb57-4fed-a596-bfb07f2c5218" />

<img width="1920" height="1080" alt="15" src="https://github.com/user-attachments/assets/fcf7a87e-8c95-4257-b3b2-e8c019597dda" />

# Optimizing-Public-Transit-Operations-Exploratory-Data-Analysis
What if the busiest transport route is not the most efficient one?  That was one of the questions I explored in my latest Python EDA capstone project: Optimizing Public Transit Operations for MetroMove Transit Solutions.

## Project Overview

This project explores how data analytics can be used to improve public transit operations for **MetroMove Transit Solutions**, a transport service provider operating across buses, trains, ferries, and trams.

The analysis focuses on understanding passenger demand, fare patterns, trip duration, station activity, transport mode performance, and route-level efficiency. The goal was to turn messy, inconsistent trip records into clear operational insights that can support better scheduling, capacity planning, route optimization, and demand stimulation.

## Business Problem

MetroMove had a large volume of trip data, but the records contained several quality issues, including:

- Missing values in important fields such as passenger count, fare amount, and trip duration
- Inconsistent transport mode names
- Whitespace and formatting errors in station names
- Date and time columns that required proper conversion
- Incomplete and inconsistent records affecting analysis quality

The key business question was:

> How can MetroMove use trip data to improve service efficiency, passenger experience, and operational decision-making?

## Dataset Description

The dataset contained trip-level public transportation records, including:

| Column | Description |
|---|---|
| `Trip_ID` | Unique identifier for each trip |
| `Mode_of_Transport` | Type of transport used: Bus, Train, Ferry, or Tram |
| `Departure_Station` | Station where the trip starts |
| `Arrival_Station` | Station where the trip ends |
| `Departure_Time` | Exact date and time of departure |
| `Passenger_Count` | Number of passengers on the trip |
| `Fare_Amount` | Fare paid for the trip |
| `Trip_Duration_Minutes` | Duration of the trip in minutes |
| `Trip_Date` | Date of the trip |
| `Day_of_Week` | Day on which the trip occurred |

## Data Methodology

A structured data analysis pipeline was followed:

1. **Data Cleaning**
   - Handled missing values
   - Corrected inconsistent transport mode names
   - Standardized station names
   - Removed whitespace errors
   - Converted date and time columns to appropriate formats

2. **Feature Engineering**
   - Extracted departure hour from departure time
   - Prepared time-based features for hourly and daily analysis

3. **Exploratory Data Analysis**
   - Analyzed passenger demand by hour, day, station, and mode of transport
   - Compared fare revenue across stations and transport modes
   - Examined route performance using average trip duration
   - Investigated the relationship between trip duration and fare amount

4. **Visualization**
   - Used bar charts, line charts, scatter plots, and heatmaps to communicate patterns clearly

## Tools Used

- **Python**
- **Pandas** for data cleaning and manipulation
- **NumPy** for numerical calculations
- **Matplotlib** and **Seaborn** for visualization
- **Jupyter Notebook** for analysis and documentation

## Key Findings

### 1. Transport Mode Performance

Buses recorded the highest number of trips, followed by ferries. This suggests that buses are the most used transport mode, while ferries also play an important role, especially for shorter trips.

<img width="1920" height="1080" alt="7" src="https://github.com/user-attachments/assets/c7d89fa1-5b31-4c1f-9bca-2c2e36ea1350" />


### 2. Station Performance

Central Station recorded the highest passenger volume and generated the most fare revenue, making it the busiest and most profitable station. South Point had the lowest passenger activity and fare revenue.

<img width="1920" height="1080" alt="18" src="https://github.com/user-attachments/assets/96c18808-6e60-44e9-beac-0fbc468c0f60" />


### 3. Day-of-Week Trip Patterns

Sunday recorded the highest total trips, followed by Tuesday, while Thursday had the lowest number of trips. This shows that demand varies significantly across the week.

<img width="1920" height="1080" alt="10" src="https://github.com/user-attachments/assets/761605d5-9184-4943-af7b-b63de46bccd0" />


### 4. Demand and Revenue Trends

Passenger demand and revenue fluctuated over time, with visible peaks around the beginning and middle of January, followed by a decline around February.

<img width="1920" height="1080" alt="13" src="https://github.com/user-attachments/assets/886d9638-0195-4d25-8a66-a865050fd663" />

<img width="1920" height="1080" alt="9" src="https://github.com/user-attachments/assets/426aaf29-b124-436b-9cdf-18c218805e5d" />

### 5. Fare Patterns

Train had the highest average fare at **$26.16**, followed by bus at **$25.60**, while ferry had the lowest average fare at **$24.48**.

<img width="1920" height="1080" alt="10" src="https://github.com/user-attachments/assets/9b2e27d1-06e3-4072-aff2-a29d45636b03" />


### 6. Trip Duration and Fare Relationship

The analysis did not show a strong relationship between trip duration and fare amount. Longer trips did not always result in higher fares.

<img width="1920" height="1080" alt="12" src="https://github.com/user-attachments/assets/87e5a603-af4e-483b-9639-75d6f6a7380a" />



### 7. Time-Based Demand Patterns

Average trip duration was highest around **8 AM** and **6 PM**, aligning with typical commute periods. Passenger demand peaked around **8 AM** and again at **9 PM**, while demand dropped sharply after **10 PM**.
<img width="1920" height="1080" alt="15" src="https://github.com/user-attachments/assets/7fbb649a-78b1-4d76-8e76-cdf4d6528992" />


### 8. Mode Demand by Hour

Demand was strongly shaped by both transport mode and time of day:

- Buses dominated afternoon and evening travel, especially between **5 PM and 9 PM**
- Ferries peaked around **8 AM**
- Trains showed smaller spikes around **7 AM** and **2 PM**
- Trams remained consistently underutilized across most hours

<img width="1920" height="1080" alt="16" src="https://github.com/user-attachments/assets/7ea1943a-86fd-422d-9792-6d9fd47fda89" />


### 9. Route Efficiency

Although trains are generally expected to be the fastest mode of transport, some routes showed inconsistencies. On selected routes, trains were slower than buses, ferries, or trams, suggesting possible inefficiencies in train routing, operations, or service design.

<img width="1920" height="1080" alt="17" src="https://github.com/user-attachments/assets/240cafe2-f518-44b9-a717-343fc74d5a13" />


## Recommendations

### Capacity and Demand Optimization

- Increase bus capacity between **5 PM and 9 PM** to meet strong evening demand
- Optimize ferry schedules around the **8 AM** morning peak
- Deploy additional train services around **7 AM** and **2 PM**
- Review tram schedules due to consistent underutilization
- Use historical trip patterns to forecast demand shifts and adjust service frequency

### Route and Operational Efficiency

- Investigate underperforming train routes where trains are slower than buses, ferries, or trams
- Deploy trains mainly on routes where they provide a clear speed advantage
- Introduce express train services on routes with poor train travel-time performance
- Review route design, stop frequency, and operational delays

### Pricing and Demand Stimulation

- Align fare strategies with demand patterns, especially on low-demand days such as Thursday
- Introduce targeted promotions during low-demand periods
- Stimulate usage at South Point through discounted fares, loyalty rewards, or route-based promotions
- Apply flexible pricing to balance passenger demand, revenue generation, and service utilization

## Project Structure

```text
metromove-public-transit-eda/
│
├── assets/
│   └── slides/
│       ├── slide_01.png
│       ├── slide_02.png
│       └── ...
│
├── data/
│   └── README.md
│
├── notebooks/
│   └── 01_public_transit_eda.ipynb
│
├── src/
│   └── data_cleaning.py
│
├── .gitignore
├── requirements.txt
└── README.md
