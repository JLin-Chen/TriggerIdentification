# Report
---

## Introduction

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

### Preprocessing
