# Where does the error come from?
不同的function set，对应不同的error；更复杂的model，可能会导致更差的表现  
这种error有两处来源：
* bias（偏差）
* variance（方差）  
知道error的来源，即可挑选适当的方法来提升model  
简单的model比复杂的受数据的影响更小  
  
* 对较简单的model，会有较大的bias和较小的variance
* 对较复杂的model，会有较小的bias和较大的variance  
![image](https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/4-Where%20does%20the%20error%20come%20from/1.jpg)  
![image](https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/4-Where%20does%20the%20error%20come%20from/2.jpg)  
### 判断目前是bias大还是variance大  
如果model不能fit数据样本，则该model有较大的bias，underfitting（欠拟合）  
如果model能fit训练集，但在测试集上产生较大的error，则该model上可能有较大的variance，overfitting（过拟合） 
  
针对bias产生的error，需要重新设计model：  
* 在输入增加更多的特征  
* 设计更复杂的model
针对variance产生的error：  
* 增加更多数据：有效但不总是可操作
* regularization（正则化）：参数值选择尽可能小，对应更平滑的函数，但可能会影响bias  
需要一些操作来使bias和variance都比较小  
1、将training set分成training set和validation set  
2、用training set来训练model，然后看这些model在validation set上的表现来选择model  
如何划分training set和validation set————N-fold Cross Validation  
将training set分成N份，取training set和validation set的不同的排列组合，计算不同组合下每种model的error及average error，选择最好的model
