# E-commerce-Recommendation-Engine

This project implements a sophisticated recommendation system designed for modern e-commerce platforms. It explores two major paradigms: Latent Factor Models (SVD) and Neural Embedding Models (Two-Tower Architecture) to predict the most relevant products for any given user.
🎯 Problem Statement

E-commerce platforms face "information overload." This engine solves the problem by filtering millions of products into a personalized "Top 5" list for every user, increasing engagement and sales through data-driven discovery.
🏗️ System Architecture
1. Collaborative Filtering (The SVD Approach)

Using Singular Value Decomposition (SVD), we represent the user-item interaction matrix as a product of two lower-rank matrices. This allows the system to uncover "hidden" patterns—such as a user's affinity for specific brands or price points—even if they have never interacted with those specific items before.
2. Modern Deep Learning (The Two-Tower Model)

To handle complex data (like product descriptions or user demographics), we use a Two-Tower Neural Network:

    User Tower: Encodes User ID and behavioral history into a vector.

    Item Tower: Encodes Product ID, category, and metadata into a vector.

    Similarity: The model is trained to maximize the dot product between the vectors of users and the items they actually purchased.

🛠️ Tech Stack

    Modeling: scikit-surprise (SVD), TensorFlow/Keras or PyTorch (Neural Networks)

    Clustering: scikit-learn (K-Means/DBSCAN)

    Data Processing: Pandas, NumPy

    Evaluation: Recall@K, Precision@K, Mean Average Precision (MAP)

🚀 Key Features

    Cold Start Handling: Uses K-Means clustering to recommend popular items from a user's cluster if they have zero history.

    Real-time Retrieval: Optimized for speed, the get_recommendations function can serve the top 5 items in milliseconds.

    Diversity & Serendipity: Balanced logic to ensure users aren't just seeing the same brands repeatedly.

📂 Project Structure
Plaintext

├── data/                   # User-item interaction logs
├── models/                 # Saved SVD and Neural weights
├── notebooks/              # SVD experiments & Two-Tower training
├── src/                    # Recommendation function & logic
└── README.md               # Documentation

📊 Evaluation

The system was evaluated on a test set of historical interactions:

    SVD RMSE: [Insert value, e.g., 0.89]

    Top-5 Precision: [Insert value, e.g., 18%]

    Inference Latency: [Insert value, e.g., <50ms]
