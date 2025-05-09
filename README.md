# UROP Bias Correction with DeepSensor

This Undergraduate Research Opportunities Program (UROP) project evaluates DeepSensor's ability to correct biases in climate forecast datasets using a convolutional Gaussian Neural Process (ConvGNP) model. Specifically, we focus on two climate variables: accumulated precipitation and temperature.

## Overview

We explore how well DeepSensor removes artificially injected biases in precipitation data from the Climate Forecast System (CFS) data. Two types of synthetic biases are tested for accumulated precipitation (more for temperature):
- **Random Noise Bias**: Random values added uniformly to the dataset.
- **Gaussian Blob Bias**: Structured noise resembling localized weather distortions.

## Data

- **Source**: CFS Precipitation data (2012–2014)
- **Format**: Zarr files
- **Variables**: Precipitation (accumulated), with lat/lon grid coordinates

## Methodology

1. Inject synthetic biases into the original CFS data.
2. Use DeepSensor's ConvGNP model to perform spatiotemporal predictions on both clean and biased datasets.
3. Evaluate performance using:
   - Root Mean Square Error (RMSE)
   - Standard Deviation of model outputs
   - Visual comparison via heatmaps

## Results

- The model performs significantly better on Gaussian Blob biases, which retain spatial patterns.
- Performance degrades with Random Noise biases due to loss of structure.
- Evaluation plots demonstrate lower uncertainty and error in corrected outputs under structured biases.

## Author
- [Zhichen Yang](mailto:yangtom@umich.edu)  
- [Haorui Wang](mailto:whruiray@umich.edu)  
- [Dani Jones (Project Instructor)](mailto:dannes@umich.edu)
