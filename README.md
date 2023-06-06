# Document-Streaming

This is a full end-to-end example project. The project uses e-commerce data that contains invoices for customers and items on these invoices.

Our goal is to ingest the invoices one by one, as they are created, and visualize them in a user interface. The technologies we use are FastAPI, Apache Kafka, Apache Spark, MongoDB and Streamlit.

Sections
Project Introduction
To give you an overview, we first have a look at the layout of the end-to-end pipeline and the data visualization that i have  built in this project. We also go through the steps of how to build it and which tools you will use at which point. As this project is very Docker based, I recommend you to go through the Docker Fundamentals training as well before proceeding.

Preparing the Data
For this project you are going to use some e-commerce dataset from Kaggle, on which we have a quick look at. Then you download your data, save it as a base CSV file and transform it into individual JSONs in VS Code.

Data API
First you create an APIs with FastAPI, write some data to the APIs and test them via Postman.

Apache Kafka & API as Docker
next install and set up Apache Kafka as a Docker container and run it with Zookeeper. Then  configure your topics that you are going to run within your Kafka environment using important Kafka commands.
You will also prepare and build another API that writes data into Apache Kafka with FastAPI. Then  deploy it as a Docker container and test it with Kafka and Postman.

Apache Spark Structured Streaming into Kafka
Here, you first set up your Apache Spark Docker container and connect it to Kafka and your API. we will also use this container with Jupyter notebooks to process the streaming data from Kafka via a readStream and write the data back into Kafka.
To make sure that everything works, you set up a test environment. For that set up a local consumer in Kafka, check your topics, and finally execute your test for Spark streaming into Kafka.

MongoDB
In this section, setup and use MongoDB and Mongo-Express UI with Docker as the storage backend of your pipeline. You configure your MongoDB Docker compose file first and then start up MongoDB and Mongo-Express. After that,  prepare your MongoDB database and invoice collection so you can work with your Spark code.

Spark Streaming into MongoDB
Apache Spark structured streaming in connection with MongoDB. Spark code streaming to MongoDB by doing several transformations. This way, you  write complete Kafka messages as nested documents to MongoDB.

The API Client Writing JSONs
Here, you create a python script as input client for the API to stream data into MongoDB. After writing your API client using JSON files, you create some test data and successfully write the data into the API and see it getting stored in MongoDB. 

Streamlit Dashboard
As the last part of the end-to-end project, you will set up your own data visualization. For that, you create an interactive user interface with Streamlit to select and view invoices for customers and the items on these invoices.
