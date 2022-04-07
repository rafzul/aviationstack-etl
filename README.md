# aviationstack-etl
Pipelines to process Aviationstack data from source till sink in BQ. Kenapa pesawat, soalnya gw seneng pesawat wqwq

Objective
- Make basic analytics pipeline to get flight data from Aviationstack API til finally being shown in Tableau)

Data to get:
- Flight data (take off time, landing time, source airport coordinate, destination airport coordinate, flight code, etc)

Step (Batching)
- Get Flight data from Aviationstack API
- Ingest the data w Airflow + PythonOperator scripts hourly, probably use Spark given longer development time (to learn)
- Dump the data in GCS as Data Lake
- Load to BigQuery as Data Warehouse
- Connect BigQuery to Tableau 

Pipeline planning (Batch Processing)
![Untitled drawing(1)](https://user-images.githubusercontent.com/61845166/162224206-e2427fa3-ddad-4b1f-9d90-a3c2b4dbbb88.jpg)



Backlog for future refinement:
- Adding Spark for batch processing (given nambah waktu belajar)
- Build kappa architecture
  - Adding Kafka as the real-time layer and future sources for all needs (batching and streamings)
  - Put on another path to process the streaming data (analyze the need first)
