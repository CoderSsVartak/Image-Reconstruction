# This folder consists of the pickle files with the training logs after completion of each bucket training.

# 1. Format of data:

  - Date and time is stored according to IST time.

  - logs => dictionary where key is {bucket_num}_logs_{date and time of storage}

  - logs[key] => dictionary where keys are the metrics and the loss.
 
# Training stage:
  
  - [X] Bucket 1: noisy images stats: mean = 0.0, sigmoid = 0.05
  - [X] Bucket 2: noisy images stats: mean = 0.0, sigmoid = 0.12
  - [ ] Bucket 3: noisy images stats: mean = 0.0, sigmoid = 0.35
  - [ ] Bucket 4: noisy images stats: mean = 0.0, sigmoid = 0.50
  - [ ] Bucket 5: noisy images stats: mean = 0.0, sigmoid = 0.65
  - [ ] Bucket 6: noisy images stats: mean = 0.0, sigmoid = 0.80
  - [ ] Bucket 7: noisy images stats: mean = 0.0, sigmoid = 0.95
