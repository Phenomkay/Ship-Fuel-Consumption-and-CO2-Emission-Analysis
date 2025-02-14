# Ship Fuel Consumption and CO₂ Emission Analysis

## Project Overview
This project analyzes ship fuel consumption and CO₂ emissions based on collected data. The goal is to derive insights into fuel efficiency, engine efficiency, and emissions across different ship routes, ship types, fuel types, and weather conditions. The findings aim to guide stakeholders in improving operational efficiency and reducing environmental impact.

## Project Objective
- Analyze fuel consumption and CO₂ emissions across different ship routes, ship types, and fuel types.
- Identify patterns and inefficiencies in fuel usage and engine performance.
- Provide actionable recommendations to improve fuel efficiency and reduce emissions.
- Investigate the impact of weather conditions on ship fuel consumption and efficiency.

## Problem Statement
Maritime transportation significantly contributes to global CO₂ emissions. Inefficient fuel consumption leads to higher operational costs and increased environmental impact. Understanding the fuel efficiency of different ships under various conditions can help optimize fuel usage, reduce emissions, and enhance overall operational effectiveness.

## Data Overview
The dataset includes information on ship routes, fuel types, fuel consumption, CO₂ emissions, weather conditions, and engine efficiency. Key metrics were calculated and visualized to derive meaningful insights.

## Data Dictionary
| Column Name          | Description |
|----------------------|-------------|
| **ship_id**          | Unique identifier for each ship |
| **ship_type**        | Type of ship (e.g., Tanker, Surfer Boat) |
| **route_id**         | Identifier for the ship route |
| **month**            | Month of the recorded data |
| **distance**         | Distance traveled by the ship (in km) |
| **fuel_type**        | Type of fuel used (e.g., Diesel, HFO) |
| **fuel_consumption** | Amount of fuel consumed (in units) |
| **CO2_emissions**    | CO₂ emissions produced (in units) |
| **weather_conditions** | Weather conditions during travel (e.g., Calm, Moderate) |
| **engine_efficiency** | Efficiency of the ship's engine (%) |


## Data Loading and Preprocessing

### 1. Loading Data
The dataset was loaded and the top 5 rows were displayed to understand its structure.

### 2. Checking for Missing Values
No missing values were found, so we proceeded with the analysis.

### 3. Data Preprocessing
- Converted month names to a categorical type to ensure correct ordering.
- Aggregated total CO₂ emissions by route and total fuel consumption by month.
- These steps allowed us to categorize the months correctly and perform initial aggregations.

## Key Performance Indicators (KPIs)
To summarize overall performance, we computed key performance indicators (KPIs):

| Metric | Value |
|--------|-------|
| Total Fuel Consumption | 6,975,715.01 |
| Total CO₂ Emission | 19,246,255.03 |
| Average Engine Efficiency | 82.58% |
| Average Fuel Efficiency | 0.0405 km/unit |

## Fuel Efficiency Calculation
- We calculated fuel efficiency as distance per unit of fuel.
- Aggregated key metrics by route, including:
  - Average fuel efficiency
  - Average engine efficiency
  - Total fuel consumption

## Visualizations

### CO₂ Emissions by Route
We created a bar chart to visualize the total CO₂ emissions by route. This helped in identifying high-emission routes.

![CO₂ Emissions by Route](https://github.com/Phenomkay/Ship-Fuel-Consumption-and-CO2-Emission-Analysis/blob/4dd324786dba4ffc208e1490f0826e4b9759ea7b/total%20CO2%20emission%20by%20route.png)

#### **Chart Description**:
- **Title**: Total CO₂ Emissions by Route
- **X-axis**: Total CO₂ Emissions (0 to ~5.5 million units)
- **Y-axis**: Routes (Warri-Bonny, Escravos-Lagos, Port Harcourt-Lagos, Lagos-Apapa)
- **Color Scheme**: Shades of red (Warri-Bonny darkest, Lagos-Apapa lightest)
- **Insight**: Lagos-Apapa has the highest CO₂ emissions, followed by Port Harcourt-Lagos, Escravos-Lagos, and Warri-Bonny.

### Fuel Consumption by Month
We plotted total fuel consumption per month to observe trends.

![Fuel Consumption by Month](https://github.com/Phenomkay/Ship-Fuel-Consumption-and-CO2-Emission-Analysis/blob/df75d56c4059a441dbea407fe0c27b877325245f/total%20fuel%20consumption%20by%20month.png)

#### **Chart Description**:
- **Title**: Total Fuel Consumption by Month
- **X-axis**: Month (January to December)
- **Y-axis**: Total Fuel Consumption (475,000 to 675,000 units)
- **Color Scheme**: Blue line with markers
- **Insight**: Peaks in March and makes a significant drop in August.

### Fuel Consumption by Fuel Type
We visualized total fuel consumption for Diesel and HFO.

![Fuel Consumption by Fuel Type](https://github.com/Phenomkay/Ship-Fuel-Consumption-and-CO2-Emission-Analysis/blob/df75d56c4059a441dbea407fe0c27b877325245f/fuel%20consumption%20by%20fuel%20type.png)

#### **Chart Description**:
- **Title**: Total Fuel Consumption by Fuel Type
- **X-axis**: Fuel Type (Diesel, HFO)
- **Y-axis**: Total Fuel Consumption (0 to ~4,000,000 units)
- **Color Scheme**: Shades of blue
- **Insight**: Diesel has higher total fuel consumption (~3,800,000 units) than HFO (~3,200,000 units).

### Fuel Efficiency by Fuel Type
A bar chart compared Diesel and HFO efficiency.

![Fuel Efficiency by Fuel Type](https://github.com/Phenomkay/Ship-Fuel-Consumption-and-CO2-Emission-Analysis/blob/df75d56c4059a441dbea407fe0c27b877325245f/fuel%20efficiency%20by%20fuel%20type.png)

#### **Chart Description**:
- **Title**: Average Fuel Efficiency by Fuel Type
- **X-axis**: Fuel Type (Diesel, HFO)
- **Y-axis**: Fuel Efficiency
- **Color Scheme**: Shades of green
- **Insight**: Diesel has higher average fuel efficiency than HFO, meaning Diesel-powered ships travel farther per unit of fuel.

### CO₂ Emissions by Ship Type
We visualized total CO₂ emissions by ship type.

![CO₂ Emissions by Ship Type](https://github.com/Phenomkay/Ship-Fuel-Consumption-and-CO2-Emission-Analysis/blob/df75d56c4059a441dbea407fe0c27b877325245f/CO2%20emission%20by%20ship%20type.png)

#### **Chart Description**:
- **Title**: Total CO₂ Emissions by Ship Type
- **X-axis**: Ship Type (Fishing Trawler, Oil Service Boat, Surfer Boat, Tanker Ship)
- **Y-axis**: Total CO₂ Emissions (0 to ~12,000,000 units)
- **Color Scheme**: Shades of red
- **Insight**: Tanker Ships have the highest CO₂ emissions, while Surfer Boats have the lowest.

### Fuel Efficiency by Weather Condition
We analyzed how different weather conditions impact fuel efficiency.

![Fuel Efficiency by Weather Condition](https://github.com/Phenomkay/Ship-Fuel-Consumption-and-CO2-Emission-Analysis/blob/df75d56c4059a441dbea407fe0c27b877325245f/fuel%20efficiency%20by%20weather%20type.png)

#### **Chart Description**:
- **Title**: Fuel Efficiency by Weather Condition
- **X-axis**: Weather Condition (Calm, Moderate, Stormy)
- **Y-axis**: Average Fuel Efficiency
- **Color Scheme**: Shades of orange
- **Insight**: Stormy conditions showed slightly higher fuel efficiency compared to Calm and Moderate conditions.


Here’s the analysis of the **Fuel Type and Ship Type Analysis**, summarized in a structured table format:  

---

### **Fuel Type Analysis Summary**  
| Fuel Type | Total Fuel Consumption | Avg. Fuel Efficiency (km/unit) | Avg. Engine Efficiency (%) | Total CO₂ Emission |
|-----------|------------------------|-------------------------------|----------------------------|---------------------|
| Diesel    | 3,879,336.49           | 0.045357                      | 82.31                      | 10,692,594.67       |
| HFO       | 3,096,378.52           | 0.032545                      | 83.04                      | 8,553,660.36        |

#### **Insights**  
- Diesel is the dominant fuel type in terms of consumption (3.88M units vs. 3.10M for HFO).  
- Diesel-powered ships have higher fuel efficiency (0.045 km/unit) compared to HFO (0.032 km/unit).  
- However, HFO engines are slightly more efficient (83.04% vs. 82.31% for Diesel).  
- Diesel contributes more to CO₂ emissions, meaning efforts to optimize Diesel usage would have a bigger impact on reducing emissions.  

---

### **Ship Type Analysis Summary**  
| Ship Type          | Total Fuel Consumption | Avg. Fuel Efficiency (km/unit) | Avg. Engine Efficiency (%) | Total CO₂ Emission |
|--------------------|------------------------|-------------------------------|----------------------------|---------------------|
| Fishing Trawler   | 968,751.28              | 0.040181                      | 82.14                      | 2,673,927.18        |
| Oil Service Boat  | 1,068,729.68            | 0.033390                      | 83.42                      | 2,932,635.15        |
| Surfer Boat       | 539,827.31              | 0.069055                      | 82.44                      | 1,483,154.25        |
| Tanker Ship       | 4,398,406.74            | 0.025323                      | 82.18                      | 12,156,538.45       |

#### **Insights**  
- **Tanker Ships** consume the most fuel (4.4M units) and contribute **the highest CO₂ emissions (12.16M units)**.  
- **Surfer Boats** are the most fuel-efficient (0.069 km/unit) despite their low total consumption.  
- **Oil Service Boats** have the highest **engine efficiency (83.42%)**.  
- The data suggests **Tanker Ships should be prioritized for emission reduction strategies**, possibly through improved fuel efficiency or alternative fuels.  


## Deeper Analysis

### Top 5 Routes with Highest CO₂ Emissions
We identified the highest CO₂-emitting routes and their contributions to total emissions.

| Route | CO₂ Emissions | % Contribution to Total CO₂ |
|--------|--------------|----------------------------|
| Warri-Bonny | 3,549,575.71 | 18.44% |
| Escravos-Lagos | 5,045,208.21 | 26.21% |
| Port Harcourt-Lagos | 5,135,239.40 | 26.68% |
| Lagos-Apapa | 5,516,231.71 | 28.66% |

- **Insight**: Lagos-Apapa is the highest CO₂-emitting route, contributing almost 29% of total emissions.

### Monthly Fuel Consumption Trends
This table presents month-over-month percentage changes in fuel consumption.

| Month | % Change from Previous Month |
|--------|----------------------------|
| January | NaN |
| February | 6.90% |
| March | 4.97% |
| April | -0.64% |
| May | -2.43% |
| June | -12.35% |
| July | 11.47% |
| August | -22.44% |
| September | 18.07% |
| October | -3.48% |
| November | 5.42% |
| December | -7.72% |

- **Insight**: August saw the largest drop (-22.44%), while September had the highest increase (18.07%).

### Best and Worst Routes by Efficiency

| Metric | Best Route | Worst Route |
|--------|------------|------------|
| Fuel Efficiency | Port Harcourt-Lagos | Escravos-Lagos |
| Engine Efficiency | Lagos-Apapa | Escravos-Lagos |

- **Insight**: Port Harcourt-Lagos is the most fuel-efficient, while Lagos-Apapa has the best engine efficiency.

### Efficiency Outliers
We identified routes with significant efficiency gaps.

| Route | Avg Fuel Efficiency | Avg Engine Efficiency | Efficiency Gap |
|--------|--------------------|--------------------|----------------|
| Escravos-Lagos | 0.0401 | 82.50% | 82.46% |
| Lagos-Apapa | 0.0403 | 82.68% | 82.64% |
| Port Harcourt-Lagos | 0.0410 | 82.51% | 82.47% |
| Warri-Bonny | 0.0407 | 82.65% | 82.61% |

- **Insight**: Lagos-Apapa has the largest efficiency gap, indicating significant room for optimization.


## Key Insights
### Total CO₂ Emissions by Route
Top 5 CO₂ Emitting Routes:
- **Warri-Bonny:** 3,549,575.71 units (18.44%)
- **Escravos-Lagos:** 5,045,208.21 units (26.21%)
- **Port Harcourt-Lagos:** 5,135,239.40 units (26.68%)
- **Lagos-Apapa:** 5,516,231.71 units (28.66%)

### Monthly Fuel Consumption Trends
- Highest fuel consumption in **July (+11.47%)** and **September (+18.07%)**.
- Significant drops in **June (-12.35%)** and **August (-22.44%)**.

### Fuel Type Analysis
#### Diesel:
- Total Fuel Consumption: **3,879,336.49** units
- Average Fuel Efficiency: **0.045357 km/unit**
- Average Engine Efficiency: **82.31%**
- Total CO₂ Emissions: **10,692,594.67** units

#### Heavy Fuel Oil (HFO):
- Total Fuel Consumption: **3,096,378.52** units
- Average Fuel Efficiency: **0.032545 km/unit**
- Average Engine Efficiency: **83.04%**
- Total CO₂ Emissions: **8,553,660.36** units

### Ship Type Analysis
- **Tanker Ship:** Highest CO₂ emissions (**12,156,538.45 units**) but lowest fuel efficiency (**0.025323 km/unit**).
- **Surfer Boat:** Lowest CO₂ emissions (**1,483,154.25 units**) and highest fuel efficiency (**0.069055 km/unit**).

### Weather Condition Analysis
- **Calm Conditions:**
  - Total Fuel Consumption: **2,602,228.86** units
  - Average Fuel Efficiency: **0.039316 km/unit**
  - Average Engine Efficiency: **82.43%**
  - Total CO₂ Emissions: **7,189,515.13** units
- **Moderate Conditions:** Higher average engine efficiency (**83.31%**).

### Efficiency Analysis
- **Best Fuel Efficient Route:** Port Harcourt-Lagos (**0.0410 km/unit**).
- **Worst Fuel Efficient Route:** Escravos-Lagos (**0.0314 km/unit**).
- **Best Engine Efficient Route:** Lagos-Apapa (**82.68%**).
- **Worst Engine Efficient Route:** Escravos-Lagos (**82.50%**).

## Recommendations
### Optimize Routes:
- Improve fuel efficiency on low-performing routes like **Escravos-Lagos**.
- Explore alternative routes or schedules to minimize fuel consumption.

### Engine Efficiency Programs:
- Implement regular maintenance and efficiency improvement programs.
- Invest in engine upgrades or retrofits for better performance.

### Fuel Type Transition:
- Encourage the use of **Diesel over HFO**, as it shows higher fuel efficiency and lower overall emissions.

### Weather Condition Adaptation:
- Develop strategies to optimize operations during adverse weather conditions.

### Monitor and Manage Outliers:
- Investigate routes with significant efficiency gaps to identify underlying causes and address them.

Here's the updated conclusion with your Power BI dashboard link included:  

---

## Conclusion  

This analysis has provided valuable insights into the fuel consumption and CO₂ emissions of various ships and routes. By addressing the highlighted issues and implementing the recommendations, stakeholders can achieve improved fuel efficiency, reduced emissions, and overall better performance. The problem of high CO₂ emissions and suboptimal fuel efficiency has been addressed through detailed analysis and actionable recommendations.  

For an interactive visualization of the analysis, explore the **Power BI Dashboard**: [View Dashboard](https://app.powerbi.com/links/chsxST3aAM?ctid=4ae26b74-8d47-481a-a074-fcd2bc5db7f9&pbi_source=linkShare).  
