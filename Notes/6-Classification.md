# Classification（分类）  
classification的目标：判断输入的具体数值所属的类别  
#### 注：regression定义model好坏的方式，对classification来说并不适用  
理想的classification做法：  
* Function：要寻找的f（x）中有另一个g（x）。输入x后，若g（x）>0，则f（x）输出class 1；否则f（x）输出class 2  
* Loss Function（与回归中的有所不同）：该Function在训练集上得到错误结果的次数  
* 找出最好的Function  
假定现有的数据是从一个Gaussian的distribution里面sample取样出来的，现在要根据现有的数据，找到Gaussian distribution函数  
要找这个Gaussian，只需要找出它的μ和∑即可  
### 用到的方法是————极大似然估计法(Maximum Likelihood)  
极大似然估计法的思想是，找出最特殊的那对μ和∑，从它们共同决定的高斯函数中再次采样出数据，使“得到的分布情况与当前已知数据的分布情况相同”这件事情发生的可能性最大  
![image](https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/6-Classification/maximum%20likelihood.jpg)  
极大似然函数L(μ，∑)等于所有数据项的乘积，分别求偏导，解出微分为0的点即可，或直接套用公式  

### modify model  
比较常见的做法是，不同的class可以共用一个cocovariance matrix  
