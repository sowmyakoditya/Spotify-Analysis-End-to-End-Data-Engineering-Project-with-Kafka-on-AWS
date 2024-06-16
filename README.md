# Spotify-Analysis-End-to-End-Data-Engineering-Project-with-Kafka-on-AWS

# Project Overview
The Spotify Analysis project focuses on processing and analyzing the Spotify Dataset 2023. This dataset has been meticulously cleaned and preprocessed to derive meaningful insights. The project leverages Apache Kafka for real-time data streaming, AWS services for scalable data processing and storage, and Visual Studio Code as the development environment.

# Project Structure
**Data Files:** The cleaned dataset is organized into three CSV files: albums.csv, artists.csv, and track.csv.
**Code Structure:** The project is structured into three main directories within a parent directory named PROJECT: artist, albums, and tracks. Each directory contains the respective producer.py and consumer.py files.
# Data Flow
**Kafka Integration:** Three Kafka topics (albums, artist, and tracks) were created using Upstash for data streaming.
**Data Processing:** Kafka producers write data to the respective topics, and Kafka consumers load this data into an S3 bucket named de-project-kafka. The S3 bucket includes a staging area with subfolders for tracks, artist, and albums.
# Data Transformation
**AWS Glue:** Used for data transformation and loading into a data lake (S3). This involved performing necessary transformations such as joins and removing unnecessary columns.
**Glue Catalog Crawler:** Used to fetch schema and metadata from S3, facilitating the creation of respective tables.
**AWS Athena:** Connected to these tables for querying and analyzing the data.
# Deployment
**Infrastructure:** The project was deployed on an EC2 instance, where all local files were transferred using an SCP request. This instance served as the environment for running the Kafka producers and consumers.
This project exemplifies an end-to-end data engineering pipeline for analyzing Spotify data, showcasing the integration of Kafka for real-time data streaming and AWS services for scalable data processing and storage.





