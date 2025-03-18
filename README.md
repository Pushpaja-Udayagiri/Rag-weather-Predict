# Rag-weather-Predict
This project aims to predict the weather for the next hour using vector search on time-series climate data. It utilizes Pinecone, a vector database, to store and retrieve similar past weather patterns for forecasting. The dataset used is the Jena Climate Dataset, which contains hourly measurements of air temperature, atmospheric pressure, humidity, wind direction, etc.

Instead of using traditional machine learning models, the project applies similarity search through RAG, allowing it to retrieve and compare past weather conditions based on a given query vector (current weather data).
USES:-
Real-time Weather Prediction: Traditional models may require extensive training; vector search allows real-time retrieval of similar past conditions for quick forecasting.
Efficient Time-Series Analysis: Works well for analyzing large climate datasets by indexing weather vectors.
Utilizing Pinecone for RAG: Instead of training an ML model, Pinecone enables efficient similarity search among time-series weather patterns.
Scalability: Vector databases scale well and allow fast retrieval without requiring expensive computational resources for training large models.
Steps of Project Implementation
The implementation follows a structured pipeline in a left-to-right format:

1️⃣ Install Dependencies → 2️⃣ Load Dataset → 3️⃣ Initialize Pinecone → 4️⃣ Prepare & Index Data → 5️⃣ Query Similar Weather Patterns → 6️⃣ Predict Weather → 7️⃣ Evaluate & Visualize

1️⃣Install Dependencies
Install required Python libraries:

2️⃣Load the Jena Climate Dataset
The dataset includes weather measurements taken every 10 minutes over several years.
It is processed into time-series feature vectors, where each column represents a different weather metric.

3️⃣Initialize Pinecone for Vector Search
Set up Pinecone with an API key to store and retrieve weather vectors.

4️⃣Prepare and Index the Data
Convert each time-stamped weather data point into a feature vector.
Store these vectors in Pinecone for efficient retrieval.

5️⃣Query for Similar Weather Patterns
Given current weather conditions, generate a feature vector.
Perform similarity search in Pinecone to retrieve past conditions that closely match.
Use retrieved results to predict the next hour’s weather.

6️⃣Evaluate Performance
Compare predictions with actual weather data.
7️⃣Visualize the results using scatter plots.
