# Gradient Descent  
gradient descent中要注意的问题：  
### Tip1、小心调整learning rate的大小  
<img src=https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/5-Gradient%20Descent/learning%20rate.png width="60%">  
* learning rate太小，如蓝线，最终能到达local minimal，但是速度很慢  
* learning rate太大，如绿线，永远无法到达最低点，一直在振荡  
* learning rate过大，如黄线，参数更新后，loss反而逐渐增大
* learning rate刚刚好，如红线，则顺利地并且速度较快地到达local minimal  
#### 调整learning rate，最基本、简单的原则：learning rate随参数的更新而逐渐减小  
最好给每个参数设置不同的learning rate  
最简单的方法————Adagrad  
#### Adagrad————learning rate除以参数之前微分值的均方根（N个项的平方和除以N后开平方的结果）  
<img src=https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/5-Gradient%20Descent/Adagrad.png width="60%">  
### Tip2、Stochastic Gradicent Descent（随机梯度下降）  
随机梯度下降的方法可以让训练更快速，传统的gradient descent的思路是看完所有的样本点之后再构建loss function，然后去update参数；而stochastic gradient descent的做法是，看到一个样本点就update一次，因此它的loss function不是所有样本点的error平方和，而是这个随机样本点的error平方  
<img src=https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/5-Gradient%20Descent/stochastic%20gradient%20descent.png width="60%">  
### Tip3、Feature Scaling  
特征缩放————多个特征分布不一样时，将它们的范围缩放成一样的  
原理：假设y=b+w1*x1+w2*x2，x1的值都很小，x2的值都很大，那么对w1、w2做同样的变动时，w1对y的影响比较小，w2对y的影响比较大，如图左  
如果x1，x2有同样的范围，则w1，w2对y有差不多的影响力，loss的图像接近于原型，如图右 
<img src=https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/5-Gradient%20Descent/feature%20scaling.png width="60%">  
#### 做feature scaling的方法  
假设有R个example(上标i表示第i个样本点)，每一笔example，它里面都有一组feature(下标j表示该样本点的第j个特征)
对每一个demension i，都去算出它的平均值mean=mi，以及标准差standard deviation=σi
对第r个example的第i个component，减掉均值，除以标准差，如图  
<img src=https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/5-Gradient%20Descent/fl.png width="60%">  
### Gradient Descent的限制 
gradient descent会停在local minimal处  
但是微分值为0的点并不都是local minimal，saddle point处微分值也是0  
实践时，当微分值接近0时，我们就停止，但它有可能是处于高原，如图  
<img src=https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/5-Gradient%20Descent/limitation.png width="60%">
