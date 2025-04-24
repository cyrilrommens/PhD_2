# Overview of the structural organisation of the code
This project involves simulating new, and utelising existing, multivariate time series data, analyzing them using information-theoretic and network-theoretic metrics, and visualizing the results. The code is organized into four primary components:

1. **Data Preparation**
2. **Analysis**
3. **Visualization**
4. **Implementation**

---

## 1. Data Preparation

Implemented in **`Data_preparation.ipynb`**, uses different models and databases to generate multivariate timeseries for specific complex systems that present self-organising behaviour.

### Kuramoto Simulation
- **Inputs:**  
  `number_of_nodes`, `coupling`, `number_of_timesteps`
- **Output:**  
  Multivariate time series as a `pandas.DataFrame`

### Perceptron Simulation
- **Inputs:**  
  `system_size`, `learning_rate`, `time` *(TBD)*
- **Output:**  
  Multivariate time series as a `pandas.DataFrame`

### Human Connectome Data
- **Input:**  
  Path to the desired HCP data folder
- **Output:**  
  Multivariate time series as a `pandas.DataFrame`

---

## 2. Analysis

Implemented in **`Computation.py`**, defines functions to compute the information-theoretic and network-theoretic metrics for a given multivariate timeseries

### Function: `information_metrics`
- **Input:**  
  Multivariate dataset (`pandas.DataFrame`)
- **Output:**  
  - TSE, MI, TC, Ω, \<TC^{y_i}\>, S, R, U, I (plus means and standard deviations)

### Function: `network_metrics`
- **Input:**  
  Multivariate dataset (`pandas.DataFrame`)
- **Output:**  
  - Clustering coefficient  
  - Average path length  
  - Small-world propensity (SWP)

### Function: `sliding_window`
- **Input:**  
  Time series dataset (`pandas.DataFrame`)
- **Output:**  
  Metrics over time (`pandas.DataFrame`)

---

## 3. Visualization

Implemented in a `.py` file, defines functions to plot the dynamics of the computed metrics against the systems self-organising behaviour

### Function: `information_plots`
- **Plots:**  
  - TSE, MI, TC, Ω, <TCyi>, S, R, U, I  
  - Mean values of metrics  
  - Standard deviations of metrics

### Function: `network_plots`
- **Plots:**  
  - Small-world (SW) plot  
  - Small-world propensity (SWP)
  - ΔClustering vs ΔPath Length

---

## 4. Implementation

Implemented in an **`.ipynb`** file, demonstrates the use of computation and visualization functions and includes annotated explanations for each function call and use
"""
