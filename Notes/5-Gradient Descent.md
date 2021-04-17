# Gradient Descent  
gradient descent中要注意的问题：  
### 1、小心调整learning rate的大小  
![image](https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/5-Gradient%20Descent/learning%20rate.png)  
* learning rate太小，如蓝线，最终能到达local minimal，但是速度很慢  
* learning rate太大，如绿线，永远无法到达最低点，一直在振荡  
* learning rate过大，如黄线，参数更新后，loss反而逐渐增大
* learning rate刚刚好，如红线，则顺利地并且速度较快地到达local minimal  
#### 调整learning rate，最基本、简单的原则：learning rate随参数的更新而逐渐减小  
最好给每个参数设置不同的learning rate  
最简单的方法————Adagrad  
#### Adagrad————learning rate除以参数之前微分值的均方根（N个项的平方和除以N后开平方的结果）  
![image](https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/5-Gradient%20Descent/Adagrad.png)  
### 2、Stochastic Gradicent Descent（随机梯度下降）  
随机梯度下降的方法可以让训练更快速，传统的gradient descent的思路是看完所有的样本点之后再构建loss function，然后去update参数；而stochastic gradient descent的做法是，看到一个样本点就update一次，因此它的loss function不是所有样本点的error平方和，而是这个随机样本点的error平方
