# Steam-Data-Analysis

## Introduction
This project focuses on analyzing Steam [dataset](https://www.kaggle.com/datasets/hatoonaloqaily/steam-system-requirements-dataset ), specifically examining the system requirements of top selling games to determine their suitability for a user's system. 
By comparing game requirements with user specifications, we aim to provide insights into which games can be smoothly run on a user's hardware. 
This analysis is crucial for gamers looking to optimize their gaming experience by matching their system's capabilities with the demands of various games available on Steam.

## Dataset Synopsis and Origin
- **Dataset Overview:** The dataset contains detailed information about the system requirements for users interested in downloading or assessing the compatibility of the top-selling games. This data is crucial for gamers who want to ensure that their hardware meets the necessary specifications to enjoy these games without issues.
- **Origin of the Data:** The data was scraped from the [Steam](https://store.steampowered.com/search/?filter=topsellers) website, specifically the top sellers games.
- **Key Features:** The system requirements features in Steam platform are:
  - OS: The operating system required by the game.
  - Processor: The CPU specifications necessary to run the game smoothly.
  - Memory: The amount of RAM needed for optimal performance.
  - Graphics: The GPU requirements for rendering the game effectively.
  - DirectX: The version of DirectX required for the game.
  - Storage: The amount of disk space required to install and run the game.
  - Price: The cost of purchasing the game.
  - Date: The release date of the game.
  - Game Name.
  - Additional Notes: Additional recommendations or notes about the system requirements.
  - Link: The URL to the game's official page or store listing.
- In our analysis we only focused on (Game Name, Processor, Memory, Storage, Date, Price).

## Model Selection
- **Initial Models Considered:** We are considereing on using K-means for grouping similar games based on their system requirements, DBSCAN because it identifies clusters of games that have similar system requirements, while also identifying outliers that don't fit well into any cluster.
- **Models Selection:** We will use both because we want to see which one gives good results.

## Feature Engineering
- **Techniques Used:** Memory and storage conversion from textual descriptions (like GB) into numerical values, this allows the model to compute and cluster.

## Hyperparameter Optimization
- **Approach:** For K-means; we used the elbow method to determine the optimal number of clusters. And for DBSCAN; 'eps=0.5' and 'min_samples=5' to control the density threshold for forming clusters.
- **Results:** THe process gives us unexpected great results, especially the elbow method!

## Performance Metric Visuals
- **Metrics Considered:** The performace metric used is the Silhouette Score, it measures how similar an object is to its own cluster from -1 to 1.
- **Visuals:** Include plots or charts that illustrate the performance of the models across different metrics.

## Best Model Determination
- **Final Model:** We used the K-means algorithm because we the clustering to be based on the requirements and we don't want the algorithm to ignore other requirements that might be considered as outliers (ex: in DBSCAN).

## Feature and Prediction Insights
- **Feature Importance:** Discuss which features were most important in making predictions.

  
- **Prediction Analysis:** Provide insights into the predictions made by the model and any interesting patterns or observations.

![insight1](https://github.com/user-attachments/assets/67da3c33-f05b-49f5-b70f-b018f1c70e16)
(1****)
![insight2](https://github.com/user-attachments/assets/b76a39b2-a4f0-49e9-b61a-2b86f240a8d2)
(2****)

![insight3 1](https://github.com/user-attachments/assets/93b87198-598b-4e8b-bdbb-ea5284c632a5)
(3.1**)

![insight3 2](https://github.com/user-attachments/assets/ef41d1ee-7f1a-43f3-9df5-ba1d359629de)
(3.2**)

## Team Members
- Raghad Almalki 
- Ahmed Alsubhi 
- Fahad Alsaadi
- Ali Alfares
- Hatoon Aloqaily


