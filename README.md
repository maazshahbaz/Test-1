# Test-1




TFT_Anomalies
 
Code for the Temporal Fusion Transformer applied to detection of anomalies in Flight data
 
## Introduction
 
This repository contains code for training and testing the Temporal Fusion Transformer (TFT) model. The TFT is a powerful forecasting model used to analyze time-series data. We use the TFT for flight anomaly detection.
 
## Dependencies
 
All required libraries and their versions are listed in the `requirements.txt` file.
 
 
```sh
pip install -r requirements.txt
```
## Files Overview
 
- **`train.py`**: Script to train the TFT model.
- **`test.py`**: Script to perform inference and test the model on multiple flights.
- **`test_one_flight.py`**: Script to perform inference and test the model on a single flight.
- **`data_functions.py`**: Contains functions for preprocessing data.
- **`inference_functions.py`**: Contains functions related to inference.
- **`test_notebook.ipynb`**: Notebook to perform both training/inference.
## Usage
 
### `train.py`
 
The `train.py` script is used to train the TFT model.
 
**Usage**:
```sh
python train.py --max_prediction_length <prediction_window_length> --max_encoder_length <history_window_length>
--data_path <path/to/data> --save_path <path/to/save/model> --n_test <N_test_flights> --n_validation <N_VALIDATION>
--batch_size <BATCH_SIZE> --epochs <EPOCHS>
```
 
 
### `test.py`
 
The `test.py` script is used to perform inference and test the model on nominal and anomalous flights.
 
**Usage**:
 
```sh
python test.py --max_prediction_length <prediction_window_length> --max_encoder_length <history_window_length>
--data_path <path/to/data> --save_path <path/to/saved/min&max> --n_test <N_test_flights> --best_model_path <path/to/tft_model>
 
```
