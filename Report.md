# Report
---

## Introduction

A rumour is an unsubstantiated claim that is widely spread.

With the rapid development of social media, the internet, with its speed and convenience, also provides a good environment for the spread of rumours. However, online rumour detection platforms require reports from users and review and identification by experts in various fields, which not only consumes a lot of manpower and time, but also has a certain delay in information, and often the rumours are only dispelled after they have spread widely, causing certain social impacts. Early detection of rumour outbreaks is therefore one of the many challenges facing rumour detection today.

The popular rumor detection methods are divided into the following four categories: 

(1) Knowledge-based methods, which detect fake news by verifying whether the knowledge in the news content (text) is consistent with the facts (real knowledge); 

(2) Style-based methods, which focus on the writing style of fake news. For example, whether extreme emotions ar e written; 

(3) Propagation-based approach, which detects fake news based on how it is spread online;

(4) Source-based approach, which investigates the credibility of news sources by investigating different stages, created, posted on the web and spread on social media, to detect fake news.

The evaluation will predict the trigger categories of messages on the message level annotated PHEME dataset, with a view to aiding subsequent rumour detection.Our team added an LSTM module to the baseline model and added a dropout mechanism, with the end result exceeding the baseline model.

## Model Architecture

![model](/Img/model.bmp)

## Requirements

### Environment
```
nltk==3.6.5
numpy==1.21.3
pandas==1.3.4
pytorch-lightning==1.5.0
torchmetrics==0.6.0
scikit-learn==1.0.1
tensorboard==2.7.0
tqdm==4.62.3
transformers==4.12.3
wandb==0.12.6

(These are included in the requirement.txt)
```

### Dataset
```
http://fudan-disc.com/sharedtask/social22/task
```

### File Architecture (Selected important files)
```
-- main.py                                  ---> start to train
-- data.py                                  ---> preprocess raw text
-- config.py                                ---> basic settings of the model
-- model_pipeline.py                        ---> rough model architecture
-- model_wrapper.py                         ---> model wrapper
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

Phase1(test1):

Model|Batch Size|Epochs|Seeds|Metrics|Trigger_maF|Verify_maF
:---:|:---:|:----:|:----:|:----:|:----:|:----:
Baseline|8|30|0|1.194|0.508|0.686
BERT+LSTM|16|30|0|**1.261**|**0.523**|**0.738**

Phase2(test2):

Model|Batch Size|Epochs|Seeds|Metrics|Trigger_maF|Verify_maF
:---:|:---:|:----:|:----:|:----:|:----:|:----:
BERT+LSTM|4|16|0|1.311|**0.521**|0.790
BERT+LSTM+Dropout|4|16|0|**1.317**|0.520|**0.796**

## Acknowledgement

Here we would like to thank for BERT implementation of HuggingFace and the baseline model provided by SH-HK. Also, thanks for the dataset release of Shanghai-HK Interdisciplinary Shared Tasks (2022).
