## This is my final year project which commenced from September 2020.

## I Have added the current methods used for image denoising which will be applied on the facial images. Also, Image Outpainting methodology report is added for facial image reconstruction.


# Concepts used:

    Curriculum learning => refer "/literature-survey/Curriculum based learning.pdf"

    Image Super-Resolution model => refer "/literature-survey/Garber_Grossman_Johnson_Yu.pdf"

    Static Filtering Algorithms => refer "/literature-survey/median_filtering.pdf", 
                                        "/literature-survey/average_filtering.pdf", 
                                         "/literature-survey/weiner-filtering_with_directionlet_domain.pdf"

    Image Outpainting => refer "/literature-survey/Image-Outpainting.pdf"



# Libraries required:

    1. Tensorflow/Keras

    2. OpenCV

    3. Numpy

    4. GoogleAPI (for downloading dataset from google drive)

    5. PIL

    6. Joblib, pickle

    7. random

    8. matplotlib

    9. random, datetime



# Dataset

    [ Google Drive Dataset Link ] ( https://drive.google.com/file/d/1QZv7mWvvF8mnT0A2mA4OFSvxF1eqPd8g/view?usp=sharing )

    ##Description: 
        Add the file id when dataset is to be downloaded. 
        Data is stored in the form of a dictionary, function is present in the code file to convert it from dictionary to numpy array.

# Algorithm Description:

        * Bucket size = 300
        * Total buckets = 7
        * Total epochs done on each bucket = 120
        * For each training step j, combine bucket B1, B2, B3,......., Bi where i<=j
        * Vary sigmoid to increase the difficulty of the image dataset after each step.
        * Difficulty is determined by percentage of noise present in the image.
        * Quality of Image is determined using Peak Signal to Noise Ratio (PSNR).
        * Total Model loss = cosine_distance + Mean_Squared_Error.
 
# Future Works:
        
        - [ X ] Design Image Denoising model and start training
        - [ X ] Formulate metrics for evaluation of quality of images
        - [ ] Train model on harder dataset
        - [ ] Work on Image Reconstruction model
