# Dataset Information

## Source

The dataset used in this project is the **Beijing PM2.5 Air Quality Dataset**, publicly available from the UCI Machine Learning Repository.

It contains hourly meteorological observations collected in Beijing over multiple years.

---

## Target Variable

- **PM2.5**: fine particulate matter concentration (µg/m³)

This variable is the prediction target of the model.

---

## Input Features

The dataset includes multiple meteorological features such as:

- Temperature
- Atmospheric pressure
- Dew point
- Wind speed
- Wind direction
- Precipitation indicators

These variables influence air pollution dynamics and are used as model inputs.

---

## Missing Values

- PM2.5 contains missing values due to sensor unavailability.
- These missing values are intentionally preserved to simulate real-world conditions.
- Input features contain minimal or no missing values and are handled during preprocessing.

---

## Preprocessing Summary

- Time-based ordering is preserved.
- Features are standardized using statistics computed only on the training set.
- Sequences are constructed using a sliding window approach.
- No synthetic data is introduced.

---

## Notes

The dataset is used strictly for educational and research purposes.

For original licensing and attribution, please refer to the UCI Machine Learning Repository.
