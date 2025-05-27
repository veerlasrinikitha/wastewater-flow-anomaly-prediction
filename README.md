# wastewater-flow-anomaly-prediction
Hybrid deep learning pipeline using LSTM and GNN for flow prediction and anomaly detection in wastewater systems. Leverages multivariate time-series data from interconnected nodes and edges to capture both temporal and spatial patterns for accurate forecasting.

Data set

The dataset includes wastewater system node/edge metadata (pipe connections, hydraulic properties) and time-series measurements (flow rates, water depth) from sensor networks. It undergoes temporal alignment, MinMax normalization, and SMOTE balancing to handle class imbalances for anomaly detection.

Dependencies and Setup:

Mounts Google Drive for accessing datasets.
Installs necessary libraries like torch-geometric, imbalanced-learn, and openpyxl.
Imports:

Utilizes Python libraries including pandas, numpy, torch, and sklearn for data handling and preprocessing.
Includes PyTorch Geometric for graph-based operations.
Imports tools for metrics evaluation and visualization (e.g., matplotlib, sklearn.metrics).
Data Loading:

Loads node and edge data from .csv files.
Reads time-series data for flow rate and water depth from Excel files.
Please confirm if you'd like the README to be focused on setting up and running this project, including descriptions of dependencies, dataset preparation, and a brief overview of the goals of the notebook. 
