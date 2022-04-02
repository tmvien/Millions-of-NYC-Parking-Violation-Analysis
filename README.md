# Millions-of-NYC-Parking-Violation-Analysis
  
Almost 1,000,000 data points from [this link](https://data.cityofnewyork.us/widgets/nc67-uf89) is loaded into kibana API using opensearch API. The analysis was focused on the last 10 years, March 24, 2012 - March 24, 2022.

Here are all the command line arguments to deploy our script using Docker:

docker build -t project1:1.0 .

docker run \
-e DATASET_ID="nc67-uf89" \
-e APP_TOKEN=<app_token> \
-e ES_HOST=<domain_endpoint> \
-e ES_USERNAME=<master_username> \
-e ES_PASSWORD=<master_password> \
-e INDEX_NAME=<index_name> \
project1:1.0 --page_size=1000 --num_pages=1000

## Analysis 1 - Top 10 Types of Violations

<img src="1.png" width=500>

## Analysis 2 - Violation Trend in past 10 years

<img src="2.png" width=500>

## Analysis 3 - The Number of Violations by County

<img src="3.png" width=500>

## Analysis 4 - Distribution of Parking Violations in 24 Hours

<img src="4.png" width=500>


## Analysis 5 - Distribution of Fine Amount 

<img src="5.png" width=500>
