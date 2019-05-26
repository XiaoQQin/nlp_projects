# nlp_projects :yum:
some demos for nlp

## CBOW
根据文本训练一个CBOW模型，即固定窗口的上下文token预测目标token  
由于训练的文本过少，所以准确率不高，但可以作为一个小demo


## Document_classifier
即简单的文本分类，采用预训练的词向量  要使用的话,在/data/glove 里加入下载的glove 文件即可  
有两个版本，第一个版本自己创建vocabulary,vectorizer,第二个版本使用keras的tokenizer和pad_sequence 减少代码量  
doc_classifier_v2 计算loss时没有加入样本权重，准确率偏低
