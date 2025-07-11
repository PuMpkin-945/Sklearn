# 多层感知器(Multi-Layer Perceptron)

* 可在不增加高次项数据情况下实现非线性分类预测

# Keras
    Keras是一个用Python编写的用于神经网络开发的应用接口，调用开接口可以实现神经网络、卷积神经网络、循环神经网络等常用深度学习算法的开发

[转到Keras](heeps://keras.io/zh/)

## Keras建立MLP模型
```python
* 建立一个Sequential顺序模型
from  keras.models import Sequential
model = Sequential()
* 通过.add()叠加各层网络
from keras.layers import Dense
model.add(Dense(units=3,activation='sigmoid',input_dim=3))
model.add(Dense(units=1,activation='sigmoid'))
* 通过.compile()配置模型求解过程参数
model.compile(loss='categorical_crossentropy',optimizer='sgd')
* 训练模型
model.fit(x_train,y_train,epochs=5)
```
[30s上手Keras](https://keras-cn.readthedocs.io/en/latest/#30skeras)
[mnist数据集](http://yann,lecun.com/exdb/mnist/)
