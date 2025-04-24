# Overview of the structural organisation of the code
readme_content = """# Coding Plan

## Overview

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

Implemented in **`Computation.py`**

### Function: `information_metrics`
- **Input:**  
  Multivariate time series (`pandas.DataFrame`)
- **Output:**  
  - TSE, MI, TC, Ω, \<TC^{y_i}\>, S, R, U, I (plus means and standard deviations)

### Function: `network_metrics`
- **Input:**  
  Multivariate time series (`pandas.DataFrame`)
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

Implemented in a `.py` file (name TBD)

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

Implemented in an **`.ipynb`** file

- Demonstrates the use of computation and visualization functions
- Includes annotated explanations for each function call and use
"""

# Save the content to a file
file_path = "/mnt/data/README.md"
with open(file_path, "w") as file:
    file.write(readme_content)

file_path
