# Gradient Descent  
gradient descent中要注意的问题：  
### 小心调整learning rate的大小  
![image](https://github.com/wangqinshuo/Machine-Learing/blob/main/Pictures/5-Gradient%20Descent/learning%20rate.png)  
* learning rate太小，如蓝线，最终能到达local minimal，但是速度很慢  
* learning rate太大，如绿线，永远无法到达最低点，一直在振荡  
* learning rate过大，如黄线，参数更新后，loss反而逐渐增大
* learning rate刚刚好，如红线，则顺利地并且速度较快地到达local minimal  

