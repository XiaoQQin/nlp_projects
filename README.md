# nlp_projects :yum:
some demos for nlp

## [CBOW](https://github.com/XiaoQQin/nlp_projects/tree/master/CBOW)
根据文本训练一个CBOW模型，即固定窗口的上下文token预测目标token  
由于训练的文本过少，所以准确率不高，但可以作为一个小demo


## [Document_classifier](https://github.com/XiaoQQin/nlp_projects/tree/master/Document_classifier)
即简单的文本分类，采用预训练的词向量  要使用的话,在/data/glove 里加入下载的glove 文件即可  
有两个版本，第一个版本自己创建vocabulary,vectorizer,第二个版本使用keras的tokenizer和pad_sequence 减少代码量  
doc_classifier_v2 计算loss时没有加入样本权重，准确率偏低

## [Surname_generation](https://github.com/XiaoQQin/nlp_projects/tree/master/Surname_generation)
简单的字符生成模型，即训练一个模型，生成surname ，以字向量为基础。由于模型的简单(只使用了一层字向量层，GRU和FC)，并且训练样本不多， 所以准确度不高.
其中第二个模型加入在GRU层时，将h_0(即第一个时间步的隐藏输出)初始化为训练时该样本的类别，由此添加条件约束


## [NMT](https://github.com/XiaoQQin/nlp_projects/tree/master/NMT)
使用attention机制的基于sequence to sequence 的英文-法语 翻译模型，数据集经过裁剪，准确率不高。encoder采用word-embedding和bi-GRU，decoder采用attention和GRU，由于decoder有目标语言文本作为词向量word-embedding输入，因此没法直接传入文本就能翻译。后续改进。
