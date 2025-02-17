# Water Permeability Prediction in Forestry

This project estimates the **spatial prediction performance** of a **7-nearest neighbor regression model (7NN)** for predicting **water permeability** in forestry. The analysis is conducted using **spatial leave-one-out cross-validation (SKCV)**, where the number of folds equals the number of data points.

## Objective

The key question addressed:  
*"What happens to the prediction performance of water permeability using a 7-nearest neighbor regression model when the geographical distance between known and unknown data increases?"*

## Data Description

The dataset consists of **1691 data points** across three files:

- **input.csv**: Contains **75 predictor features**.  
- **output.csv**: Contains the **water permeability values**.  
- **coordinates.csv**: Contains the **geographical coordinates** (in meters) of the data points. **Euclidean distance** is used for spatial calculations.

## Methodology

1. **Z-score Standardization**:  
   - Normalize the predictor features in `input.csv` to have a mean of 0 and a standard deviation of 1.

2. **Spatial Leave-One-Out Cross-Validation (SKCV)**:  
   - Use a **7NN regression model**.
   - Evaluate the **C-index** at different geographical distances.
   - Distance parameter values: **d = {0, 20, 40, ..., 300}** meters.

3. **Visualization**:  
   - Plot **C-index (y-axis) vs. Distance (x-axis)** to analyze the relationship between spatial separation and prediction performance.

## Requirements

- Python 3.x
- Jupyter Notebook
- NumPy, Pandas, Scikit-Learn
- Matplotlib, Seaborn

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/junaidraz1/permeability-spatial-analysis.git
