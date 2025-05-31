# wastewater-flow-anomaly-prediction
# Project Goals
- Predict future wastewater flow rates and water depth values
- Detect anomalies such as pipeline blockages or sensor failures in real-time
- Utilize spatial and temporal data for robust, intelligent monitoring of wastewater networks
  
# Dataset Overview
The project uses the following files:

- Flow rate.xlsx: Historical inflow rates at different nodes
- WW01 v3.xlsx: Water depth measurements
- WW01 node.csv: Node metadata for network structure
- WW01 edge.csv: Edge connections between nodes
  
# Install dependencies
```bash
!pip install -r requirement.txt
```
# Key Libraries and Imports
- pandas, numpy: Data manipulation
- torch, torch.nn, torch_geometric: Deep learning and graph modeling -sklearn: Preprocessing and evaluation metrics
- matplotlib: Visualization
- openpyxl: Excel file reading
  
# Model Architecture
- LSTM Block: Captures long-term temporal dependencies in flow data Produces temporal embeddings

- GNN Block; Models spatial dependencies between nodes using GCN or GAT Produces spatial embeddings for each node

- Combined Prediction Uses a joint model for flow prediction using MSE loss Anomaly detection is handled via:

Autoencoder reconstruction error Clustering (e.g., DBSCAN, k-means) Statistical thresholding (z-scores)

# Experiments
Baseline Models for Comparison:

- For Flow Prediction: ARIMA,Random Forest Regressor,Single LSTM,Temporal Convolutional Network (TCN)

- For Anomaly Detection: Autoencoders,Isolation Forest,Class SVM,Single GRU

- Preprocessing Steps Missing value imputation Min-Max feature scaling Merging flow and depth data Graph construction using node and edge metadata

# Output
- Predicted flow and water depth over time
- Anomaly flags per node and timestamp
- Evaluation metrics: MAE, RMSE, Precision, Recall, F1-Score

