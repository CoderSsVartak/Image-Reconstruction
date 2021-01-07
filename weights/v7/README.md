  - ## Model architecture
  
  1. ### Input Layer:
  
     - Input Layer: shape = (224, 224, 3)
  
  2. ### Layer 1:
     - Convolution 2D Layer: filters = 64, kernel_size = (11, 11), padding = same, activation = relu, output_shape = (224, 224, 3)
     - Batch Normalization = True
     
  3. ### Layer 2:
     - Convolution 2D Layer: filters = 32, kernel_size = (1, 1), padding = same, activation = relu, output_shape = (224, 224, 3)
  
  4. ### Layer 3:
     - Convolution 2D Layer: filters = 3, kernel_size = (7, 7), padding = same, activation = relu, output_shape = (224, 224, 3)
    
    
  - ## Hyper Parameters
    -- Optimizer: Stochastic Gradient Descent
    -- Epochs = 100
    -- Learning Rate = 0.01 for the first 50 epochs and 0.001 for the next 50 epochs
    -- Momentum = 0.4 for the first 50 epochs and 0.6 for the next 50 epochs.
    
  
  - ## Dataset Noise Sigmoid
    -- Bucket 1: mean = 0.0, sigmoid = 0.05
    -- Bucket 2: mean = 0.0, sigmoid = 0.1
    -- Bucket 3: mean = 0.0, sigmoid = 0.2
