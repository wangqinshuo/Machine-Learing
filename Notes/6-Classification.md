# Classification（分类）  
classification的目标：判断输入的具体数值所属的类别  
#### 注：regression定义model好坏的方式，对classification来说并不适用  
理想的classification做法：  
* Function：要寻找的f（x）中有另一个g（x）。输入x后，若g（x）>0，则f（x）输出class 1；否则f（x）输出class 2  
* Loss Function（与回归中的有所不同）：该Function在训练集上得到错误结果的次数  
* 找出最好的Function  
