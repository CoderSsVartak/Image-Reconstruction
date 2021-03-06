# Description
  - This is my final year project which commenced from September 2020.
  - I Have added the current methods used for image denoising which will be applied on the facial images. Also, Image Outpainting methodology report is added for facial image reconstruction.m
  - The project was completed in Google Colab, so if it is imported locally, make sure to download GoogleAPI to handle Drive data and also alter the path as required.


# Concepts used:

  - [Curriculum learning](https://github.com/CoderSsVartak/Image-Reconstruction/blob/master/literature_survey/Curriculum%20based%20learning.pdf)

  - [Image Super-Resolution model](https://github.com/CoderSsVartak/Image-Reconstruction/blob/master/literature_survey/Garber_Grossman_Johnson-Yu.pdf)

  - [Image Outpainting](https://github.com/CoderSsVartak/Image-Reconstruction/blob/master/literature_survey/image_outpainting.pdf)

  - [Noise Addition Algorithms](https://github.com/CoderSsVartak/Image-Reconstruction/blob/master/literature_survey/noisy%20images.pdf)

  ### Static Noise Filtering Algorithm:

   - [Median Filtering](https://github.com/CoderSsVartak/Image-Reconstruction/blob/master/literature_survey/median_filtering.pdf)

   - [Average Filtering](https://github.com/CoderSsVartak/Image-Reconstruction/blob/master/literature_survey/average_filtering.pdf)

   - [Weiner Filtering with Directional Domain](https://github.com/CoderSsVartak/Image-Reconstruction/blob/master/literature_survey/weiner_filtering_with_directional_domain.pdf)




# Libraries required:

  1. Tensorflow/Keras

  2. OpenCV

  3. Numpy

  4. GoogleAPI (for downloading dataset from google drive)
  - Available only on Google Colab. If running on local device, download the dataset from the google drive and use joblib to load file. 
  
  5. PIL

  6. Joblib, pickle

  7. random

  8. matplotlib

  9. random, datetime

# Note: Dataset is present on Google Drive and is automatically downloaded from your google drive. Make sure to copy the dataset into your drive from the link mentioned below. 
# In order to run the code on local system, download the dataset in your local system from the link mentioned below. Make sure to hide out the Google libraries imported as they are available only on Colab. No need to run Google account authentication code cell.

# Dataset

  [Google Drive Dataset Link](https://drive.google.com/file/d/1QZv7mWvvF8mnT0A2mA4OFSvxF1eqPd8g/view?usp=sharing)
  ## Steps to load dataset on Google Colab:
  - Copy this file in the root directory of your Google Drive.
  - Authenicate your google account on which the dataset is stored on google colab (Run the cells of google colab, it contains automated code to authenticate your account).

  ## Description: 
   - Data is stored in the form of a dictionary, function is present in the code file to convert it from dictionary to numpy array.
   - Images are pickled using Joblib.

## GAN weights are uploaded on Drive:
   - [Generator Weight](https://drive.google.com/file/d/1MTh4vtXPkZVNxOoHgYzdNo-u4yIFyFD0/view?usp=sharing)
   - [Discriminator Weight](https://drive.google.com/file/d/1qBrLrgz8Xvk56Pujzsrxb8dF8_KM_qvk/view?usp=sharing)
   - [Log File](https://drive.google.com/file/d/1TrQX-av3s0Vg608rTdhkGZhPvGAZtyol/view?usp=sharing)

  To load the Image Reconstruction weights, download them from the link above and upload them on the google colab before executing the code. For Image Denoising Weights, the weights are uploaded [here](https://github.com/CoderSsVartak/Image-Reconstruction/tree/master/weights/v9)

# Algorithm Description:

  - Bucket size = 300
  - Total buckets = 6 (Limited due to Higher Storage unavailability)
  - For each training step j, combine bucket B1, B2, B3,......., Bi where i<=j
  - Vary sigmoid to increase the difficulty of the image dataset after each step.
  - Difficulty is determined by percentage of noise present in the image.
  - Quality of Image is determined using Peak Signal to Noise Ratio (PSNR).
  - Total Model loss = cosine_distance + Mean_Squared_Error.
  - Optimizer used = Stochastic Gradient Descent 
 
# Future Works:
        
  - Train Image Denoising model using Curriculum learning on different sigmoid values and hyperparameters.
  - Train Image Reconstruction model on larger dataset for better generalization
 
# Results:
  
  ## Image Denoising Model Output on unseen faces (Validation Dataset)
  <img src="/results/Result.png">
  
  ## Image Reconstruction Model Output on unseen faces
  <img src="/results/actual.png">
  <img src="/results/reconstructed.png">
  <img src="/results/masked.png">
