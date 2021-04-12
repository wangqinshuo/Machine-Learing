# Regression  
机器学习中，step 3选择最好的function的方法：gradient descent（梯度下降法）。只要loss function，L（f）对输入参数可微分，便可使用gradient descent方法  
### gradient descent步骤：  
1、随机选择参数的初始值，例w0  
2、计算L（f）在w=w0处的微分，即w0处曲线的斜率。若微分为负，则增大w的值；若微分为正，则减小w的值  
公式：w1=w0-η dL/dw|w=w0, 其中η称为learning rate（学习速率）  
3、重复步骤2，直到某处微分得0  
  
对多参数的function，求其各参数的偏微分  
linear regress（线性回归）的loss function（损失函数）是碗状，凹函数；更复杂的模型，则要考虑L（f）的形状  
overfitting  
在训练集上误差较小的model，在测试集上误差不一定小，这种现象就是overfitting（过拟合）  
### 针对过拟合现象的解决办法：  
1、减少特征的数量  
2、regularization（正则化）——参数值尽量小，对应更平滑的函数。多数情况下，平滑的function更可能是正确的。

