# TriggerIdentification

# 引言

对社交网络中消息的真实性进行检验，可以借助信源的评论转发作为辅助特征。
根据消息的转发消息可形成信息传播树，如何组织和利用相关文本特征是目前的一大难点。
复旦大学数据智能与社会计算实验室基于现有的谣言检测语料集PHEME，完成了消息级别的标注，
以期在消息级别上对消息的引爆点类别进行预测，来辅助后续的谣言检测。

## 概览
一、简介

二、任务描述

三、数据集

四、实验

五、结论

参考文献


---

# 一、简介

简介：

我们的贡献是：


# 二、任务描述

评价指标：trigger和verify两个子任务上的宏平均F1值（macro F1）

排名指标：trigger和verify两个子任务上评价指标的加和

我们的目标是：在Macro F1上取得比baseline模型更好的效果

# 三、数据集

![dataset](/Img/dataset.bmp)

# 四、实验 

![runsummary](/Img/runsummary.bmp)


## 4.1 基线方法

所采用的基线模型是基于bert-base-uncased进行消息表示，使用平均池化进行传播树表示的分类模型，
所采用的评价指标为两个分类任务上宏平均F1值（macro F1），排名依据为两个任务上评价指标的加和。

## 4.2 改进方法1 

提高数据集质量（DataCLUE）以获得更好的模型性能，3个有效的基线将macroF1提高了5.7个百分点；

基于训练遗忘的标签矫正方法；

项目地址：

https://github.com/CLUEbenchmark/DataCLUE

文章地址：

https://arxiv.org/pdf/2111.08647.pdf

---
1. 现有数据集存在标注缺失文章信息杂乱等情况，能被有效利用于训练的数据量可能不是特别大，使data质量提升能否提高baselinemodel的效果？  
2. 能否通过算法或程序或者结合人工的方式来改进数据集？ 是否存在标签错标的情况？ 
3. 


## 4.3 改进方法2
从数据集中提取更多特征

## 4.4 改进方法3
从传播树结构入手

# 五、结论

## 参考文献 
