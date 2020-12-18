# Consists of .h5 files which have model weights that are saved using the model.save API from Keras.

# Title

- Image_Denoising_v5.{bucket_num-1}_Bucket{bucket_num}_{datetime(IST)}.h5

# Training

  - A total of 7 training steps is planned, each step having 120 epochs.
  - Weights are saved after 25, 50, 70, 90 and 120 epochs in each training step.

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
