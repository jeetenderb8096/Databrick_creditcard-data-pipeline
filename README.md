This project focuses on real-time Change Data Capture (CDC) feed processing for UPI transactions using Databricks and Spark Structured Streaming. The objective is to efficiently track updates in transactional data and perform aggregations for merchant payment settlement.

Tech Stack

1) GCP cloud and GCP Storage
2)  Databricks
3) Apache Spark (Structured Streaming)
4) Delta Lake


Key Features & Implementation

Create Source Delta Table

Ingest mock UPI transactions data using an Update Merge query.

Enable CDC Feed

Configure Change Data Capture (CDC) on the Source Delta table.






![image](https://github.com/user-attachments/assets/67a3d6e5-6957-4379-bc4a-e0af003687d4)



Process CDC Feed Using Spark Structured Streaming




![image](https://github.com/user-attachments/assets/9112b35a-582f-44be-9656-8dea5ffa0058)

Implement a Spark Structured Streaming pipeline to consume the CDC feed from the Source Delta table.


![image](https://github.com/user-attachments/assets/db8d5875-0ab7-4d4d-b587-a8351cd4e0b2)


Run Aggregations on Micro Batches

Perform aggregations on incoming micro-batches.





![image](https://github.com/user-attachments/assets/3138978a-a993-4e7f-8cf1-521dbd0ae026)

Update the Target Delta table using a Merge query to maintain the latest aggregated data.

Query Target Delta Table


![image](https://github.com/user-attachments/assets/d6f1dcc4-13c5-41c1-ba9f-d4eab0cc11e7)




Use SQL Data Warehouse Serverless Compute to query and analyze the aggregated transaction data efficiently.










