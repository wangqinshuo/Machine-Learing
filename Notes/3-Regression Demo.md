# Regression Demo
以一个简单的regression为例：y_data = b + w * x_data  
用gradient descent求b，w  
![image](https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/3-Regression%20Demo/pianweifen.jpg)  
规定iteration（迭代次数）和learning rate（学习率），进行第一次尝试  
![image](https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/3-Regression%20Demo/try-1.png)  
发现距离最优解还有一段距离，于是将learning rate增大10倍，再次测试  
![image](https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/3-Regression%20Demo/try-2.png)  
与最优解的距离更近了一步，但是产生了一个剧烈的震荡现象，再次将learning rate增大10倍进行测试  
![image](https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/3-Regression%20Demo/try-3.png)  
参数远远超出标注范围  
lr太小，与最优解距离过远；lr太大，超出标注范围  
解决办法：定制化b和w的learning rate，再次测试  
![image](https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/3-Regression%20Demo/try-4.png)  
#### 成功地在迭代次数以内，从初始值到达最优解
