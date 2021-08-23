[BERT 的数据处理](https://albertauyeung.github.io/2020/06/19/bert-tokenization.html)


# BERT 的训练
训练任务：以 15% 的概率对 Tokens 进行 Masked, 
1. Masked Language Modeling
> 猜出被 mask 的 Token

2. Next Sentence Prediction (NSP)
> 给出两个句子，预测第二个句子是否是第一个句子的 Next Sentence (binary classification)





# BertConfig

vocab_size: Bert词典大小

hidden_size: encoder layer 和 pooler layer 的维度

num_hidden_layers: Transformer encoder 中 hidden layer 的数量

num_attention_heads: T_encoder 中 每个 atten layer 的 atten heads 的数量

intermediate_size:  T_encoder 中 feed-forward 的维度

hidden_act:  encoder 和 pooler 中 非线性激活函数

hidden_dropout_prob: embeddings, encoder 和 poller 中 dropout probability 

attention_probs_dropout_prob: 

**type_vocab_size**: 2. token_type_ids 
> 这个就是 NSP 认为中 segA 和 segB 的数量
> [博客](https://zhuanlan.zhihu.com/p/69106080)
> [Github](https://github.com/google-research/bert/issues/16)

initiali