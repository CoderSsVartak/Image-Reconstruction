# This folder consists of the pickle files with the training logs after completion of each bucket training.

# 1. Format of data:

  - Date and time is stored according to IST time.

  - logs => dictionary where key is {bucket_num}_logs_{date and time of storage}

  - logs[key] => dictionary where keys are the metrics and the loss.
 

Logs are saved only after the model is trained on the final bucket of the version. The training is stopped when the model does not produce efficient results for the specified values of sigmoid of noise.
