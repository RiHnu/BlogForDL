# 0. Cross-Entropy

# 1. 作用
Cross-entropy loss: 对于一个用于分类的 Model（这类模型的输出是概率值）, CEloss的值 衡量了 Model 的性能

# 2. 性质
- Model 的输出越接近1，CEloss的值越接近0
- Model 的输出越接近0，CEloss的值越接大

# 3. 数学公式
$$
-\sum_{c=1}^{M} y_{o, c} \log \left(p_{o, c}\right)
$$
其中：
- M 是类别的数量
- y Binary Indicator. 如果预测的 label c 是正确的，y=1，否则为0
- p 针对观测值 o 所预测出其标签为 c 的概率


# 4. 具体应用

## 4.1 Softmax Loss
>Softmax activation + CEloss

> 特点：所有值之和为 1
这种情况下，模型对输入的 IMG，输出其分别在 C 个 label 上的概率

对于 IMG-1, 它的 Label 有且仅有1个

## 4.2 Binary Cross-Entropy Loss
>Sigmoid activation + CEloss

> 与 Softmax Loss，它的值相互之间是独立的. 因此，它适合于 Multi-label classification

对于 IMG-1， 它的 Label 可能有多个



# Reference
- [1-Machine Learning Glossary](https://ml-cheatsheet.readthedocs.io/en/latest/loss_functions.html)
- [2-Blog](https://gombru.github.io/2018/05/23/cross_entropy_loss/)