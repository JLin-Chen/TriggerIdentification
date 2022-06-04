# Report
---

## Introduction

A rumour is an unsubstantiated claim that is widely spread.

With the rapid development of social media, the internet, with its speed and convenience, also provides a good environment for the spread of rumours. However, online rumour detection platforms require reports from users and review and identification by experts in various fields, which not only consumes a lot of manpower and time, but also has a certain delay in information, and often the rumours are only dispelled after they have spread widely, causing certain social impacts. Early detection of rumour outbreaks is therefore one of the many challenges facing rumour detection today.

The evaluation will predict the trigger categories of messages on the message level annotated PHEME dataset, with a view to aiding subsequent rumour detection.Our team added an LSTM module to the baseline model and added a dropout mechanism, with the end result exceeding the baseline model.

## Model Architecture

![model](/Img/model.bmp)

## Requirements

### Environment
```
hello
```

### Dataset
```
http://fudan-disc.com/sharedtask/social22/task
```

### File Architecture (Selected important files)
```
-- main.py                                  ---> start to train
-- data.py                                  ---> preprocess raw text
-- /model_encoder/bert.py                   ---> input preprocessed data to BERT
-- /model_interact/none.py                  ---> detailed model architecture
-- /data_trigger                            ---> datasets
-- /bert-base-uncased                       ---> BERT part
```

## Get Started

### Preparing Environment
```
pip install -r requirements.txt
pip install tensorflow-gpu==2.1.0
pip3 install tensorflow==1.15.0
```

### Training
```
start training the model with running main.py
```

## Checkpoints
For reproducity and usability, we provide checkpoints and the original training settings to help you reproduce.
```
Link of overall result folder: https://pan.baidu.com/s/1P98jqvcE7JVPToOENhCKUQ?pwd=2022
```

The implementation details and results are shown below:

