  - ## Model architecture
  
  1. ### Input Layer:
  
     - Input Layer: shape = (224, 224, 3)
  
  2. ### Layer 1:
     - Convolution 2D Layer: filters = 64, kernel_size = (9, 9), padding = same, activation = relu, output_shape = (224, 224, 3)
     - Batch Normalization = True
     
  3. ### Layer 2:
     - Convolution 2D Layer: filters = 32, kernel_size = (1, 1), padding = same, activation = relu, output_shape = (224, 224, 3)
  
  4. ### Layer 3:
     - Convolution 2D Layer: filters = 3, kernel_size = (5, 5), padding = same, activation = relu, output_shape = (224, 224, 3)


  - ## Hyper Parameters
    - Optimizer: Stochastic Gradient Descent
    - Epochs = 120
    - Learning Rate = 0.01 for the first 90 epochs and 0.001 for the next 30 epochs
    - Momentum = 0.2 for the first 50 epochs, 0.4 for the next 40 epochs and 0.6 for the next 30 epochs.
    
  
  - ## Dataset Noise Sigmoid
    - Bucket 1: mean = 0.0, sigmoid = 0.01
    - Bucket 2: mean = 0.0, sigmoid = 0.05
    - Bucket 4: mean = 0.0, sigmoid = 0.12
    - Bucket 5: mean = 0.0, sigmoid = 0.35
    - Bucket 6: mean = 0.0, sigmoid = 0.50
    - Bucket 7: mean = 0.0, sigmoid = 0.74

