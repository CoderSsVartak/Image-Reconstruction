This folder consists of the pickle files with the training logs after completion of each bucket training.

Format of data:

Date and time is stored according to IST time.
logs => dictionary where key is {bucket_num}_logs_{date and time of storage}
logs[key] => dictionary where keys are the metrics and the loss.
