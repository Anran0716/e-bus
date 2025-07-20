# Optimization of E-bus Charging Stations in Florida

The goal of this project is to help **City of Gainesville** site and optimize E-bus charging stations, as the local transit agency will realize the goal of future bus electrification. This project analyzes real-time operational data, predicts energy needs, and designs an optimal model that can balance cost, convenience, and service coverage.

## Data Ingestion 
The real-time bus GPS data (Oct 2022 - Mar 2023) is extracted from **Public APIs** (acquired by the City of Gainesville) with Python. Then stored in the **Postgres database on AWS RDS.**

Code: [`ingest_realtime_data.ipynb`](ingest_realtime_data.ipynb).


## Modeling
- **Energy Consumption Predictive Modeling**: we developed a predictive model to estimate electric energy consumption by route, time of day, and geographic patterns, helping forecast charging demands accurately. Code: [`energy consump.ipynb`](Modeling/energy%20consump.ipynb).

- **Optimization Modeling of E-bus charging stations**: We applied **weighted K-means clustering** and **scenario-based modeling** to identify optimal charging station locations, maximizing coverage and operational efficiency. Hyperparameter tuning improved the model performance, achieving 95% service coverage with minimal cost trade-offs. Code: [`KMeans.ipynb`](Modeling/KMeans.ipynb).

The findings are presented in the conference: 
![image](https://github.com/Anran0716/e-bus/blob/main/poster.jpg)

## Dashboard

We are now designing a dashboard using JavaScript, HTML/CSS to show real-time bus activity, predicted coverage, and optimized charging station sites: [`Link to the Github`](https://github.com/Anran0716/Ontime-dashboard)