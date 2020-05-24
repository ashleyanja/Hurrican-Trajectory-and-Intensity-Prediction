# Hurrican-Trajectory-and-Intensity-Prediction
An LSTM neural network trained to forecast hurricane trajectory and intensity 24 hours in advance.

# Data used for training and testing
- Used the National Oceanic and Atmosphere Administration IBTRACS database of tropical storms and hurricanes
- Includes data from 6 hurricane storm basins worldwide 
- Contains over 200,000 data points for 7,367 storms starting from 1848.
- From this we reduce the number of storms down to 464, by filtering out small storms, ones with incomplete data, and ones not from the North Atlantic basin
- Each data point indicates location of storm center (latitude and longitude), storm basin, wind intensity, atmospheric pressure

# Parameters
Created 5 different LSTM models for each input parameter:
Latitude
Longitude
Wind Speed
Wind Pressure
Storm Direction

Input: Latitude, Longitude, Wind Speed, Wind Pressure, Storm Direction at 0h, 6h, 12h, 18h intervals
Hidden Layers: Two layers with 32 and 16 nodes respectively
Loss function: Mean Absolute Error
Optimizer: Adam
Learning Rate = 0.001
Epochs: 100
Terminating Condition: Max epochs or 10 iterations with no improvement to validation data loss

