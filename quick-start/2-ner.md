# 2-NER

## Packages

* 分词package:  spacy (支持中英), jieba(中文分词工具)
* 评估工具：seqeval.metrics&#x20;
* 模型package： transformers， torch
* 数据集package:  datasets



## Datasets

1. Feedback Prize dataset

{% embed url="https://www.kaggle.com/competitions/feedback-prize-2021" %}



## Objective

1. Model For Token Classification
   1. 输入数据是一个句子， 每个单词1个token
   2. label是 这个句子的1个单词对应1个label， label类型定义为
      1. entity 类型有N种， 每种entity都有Begin, Inside, End 3种位置状态
      2. 所以总共label数量为3N
   3. 训练方式：Next Token Prediction, 预测下一个token的类型
   4. 推理：
      1. 模型预测输出shape: \[batch, sentence\_len, labels]
      2. 预估每个word对应的label， 按照word维度和ground truth 对比 算f1 score, recall等



## Steps

1. 预处理
   1. 文本抓取， 清洗（脏，空字符串）
   2. spacy 分词
   3. label定义
   4. 每个word的label对齐 token位置
2. 数据集
   1. 创建train/test Dataset 对象， batching
3. 加载pre-train model和对应的tokenizer
   1. 用tokenizer 创建对应的Data Collator 数据整合器
   2. 创建TrainingArguments类， 设置：
      1. 输出路径
      2. learning rate
      3. validation steps
      4. metrics
      5. 等
   3. 创建Trainer 类输入model， dataset，data collator, tokenizer等参数
   4. trainer.train()
4. inference



## Coding

{% embed url="https://www.kaggle.com/code/wenkangw/practise-learning-ner-with-feedback-dataset/edit" %}

