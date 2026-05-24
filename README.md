# DBSCANClustering_Nokta_Alper
On "Nokta" dataset that consists of two groups of clustering dots; dot clustering analysis using DBSCAN algorithm.

The Problem: In many real-world datasets, clusters do not follow a simple spherical shape, making traditional algorithms like K-Means ineffective. DBSCAN (Density-Based Spatial Clustering of Applications with Noise) is a powerful alternative, but it is highly sensitive to its  epsilon parameter. The core problem of this project was to determine how varying epsilon affects the identification of noise (outliers) in a two-group dataset and to find the "best epsilon" that yields a specific, target number of outliers.

The Solution: I developed a dynamic simulation environment using the DBSCAN algorithm from Scikit-learn.

Iterative Analysis: I implemented a loop to test a range of epsilon values while keeping the min_samples parameter constant.
Outlier Monitoring: For each iteration, the model identified points labeled as -1 (outliers).
Optimization: By tracking the inverse relationship between epsilon and the outlier count, I successfully identified the specific "best epsilon" value that satisfied the project's predefined outlier constraints.

Key Technical Challenges:

Parameter Interdependence: Balancing epsilon with min_samples is tricky; a small epsilon might label too many points as noise (outlier), while a large epsilon might merge distinct clusters into one.
Non-Linear Relationship: The rate at which outliers disappear as epsilon increases is non-linear. Visualizing this "elbow" or "knee" point was essential for understanding the stability of the clusters.
Distance Metrics: Selecting the appropriate distance metric (e.g., Euclidean) was critical to ensure that the density calculations accurately reflected the spatial distribution of the two groups.

Results: 

Epsilon vs. Outliers inverse correlation: The project clearly demonstrated that as the epsilon value increases, the number of outliers decreases exponentially before plateauing, as more points fall within the reach of core samples.
Optimal Clustering: I successfully isolated the two primary groups while maintaining the desired outlier threshold, proving that DBSCAN is highly effective for noise filtering when tuned correctly.
Strategic Insight: The results provided a clear "best epsilon" value that maximizes cluster integrity, offering a data-driven blueprint for handling noise in density-based spatial data.

Project Architecture:

EDA and Feature Engineering
Model: Random Forest Classification
Train Test Split
Applying StandardScaler 
Model training
Evaluation of Performance
Results
