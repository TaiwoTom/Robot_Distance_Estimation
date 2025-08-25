## Distance Estimation of Robot Using IMU Data

## Overview
This project implements a machine learning pipeline to estimate the distance traveled by a robot using IMU (Inertial Measurement Unit) sensor data. The system processes accelerometer data, applies data augmentation techniques, and uses two regression models (Random Forest and Support Vector Regression) to predict distance traveled.

## Dataset
The dataset consists of CSV files recording robot motions at different speeds and paths:
- `curve_slow_Accelerometer.csv`
- `curve_slow_Gyroscope.csv`

Each file contains sensor data collected using the Sensor Logger Android app, with the robot moving in 5-meter segments for a total of 50 meters per motion type.

## Features
- **Data Preprocessing**: Normalization, smoothing, and resampling of sensor data
- **Data Augmentation**: Jittering, scaling, and time warping techniques
- **Feature Engineering**: Integration of acceleration to velocity and distance
- **Model Training**: Random Forest Regression and Support Vector Regression
- **Evaluation**: MAE, RMSE, and R² metrics

## Requirements
- Python 3.7+
- pandas
- numpy
- scikit-learn
- scipy

## Installation
```bash
pip install pandas numpy scikit-learn scipy
```

## Usage
1. Place your sensor data CSV files in the `/content/sample_data/` directory
2. Run the Jupyter notebook `CPSC_5616EL_A3_G18.ipynb`
3. The code will process the data, train models, and output performance metrics

## Results
The models were evaluated on curve_slow motion data:
- Random Forest: MAE=47826.09, RMSE=55414.04, R²=-0.26
- SVR: MAE=42742.80, RMSE=49356.32, R²=-0.0001

## File Structure
```
├── CPSC_5616EL_A3_G18.ipynb      # Main implementation notebook
├── sample_data/                  # Directory for sensor data
│   ├── curve_slow_Accelerometer.csv
│   └── curve_slow_Gyroscope.csv
└── README.md                     # This file
```

## Contributors
- Rutul Hemantkumar Trivedi 
- Tom-Ayegunle Taiwo Anuoluwapo 

## License
This project was created for academic purposes as part of CPSC-5616EL course at Laurentian University.
