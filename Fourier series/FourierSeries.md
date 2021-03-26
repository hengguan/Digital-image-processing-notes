## Fourier Series

<center>

![5](https://latex.codecogs.com/svg.latex?f(t)=A_0+\sum_{n=1}^{\infty}a_{n}\cos{(n\omega{t})}+b_{n}\sin{(n\omega{t})})  
</center> 

---

### 1、麦克劳林待定系数法：
- 泰勒级数：  
任意函数可由一个多项式来逼近：
<center>  

![5](https://latex.codecogs.com/svg.latex?f(x)=A_0+A_{1}x+A_{2}x^2+A_{3}x^3...)  
</center>

- 麦克劳林：
<center>  

![5](https://latex.codecogs.com/svg.latex?f'(x)=A_{1}+2A_{2}x+3A_{3}x^2...)  
![5](https://latex.codecogs.com/svg.latex?f''(x)=2A_{2}+6A_{3}x...)  
......
</center>

- 待定系数法解系数：  
<center>  

![5](https://latex.codecogs.com/svg.latex?A_0=f(0),A_{1}=f'(0),A_{2}=f''(0)/2,...)  
![5](https://latex.codecogs.com/svg.latex?A_n=f^{(-n)}(0)/n!)  
</center>

---

### 2、三角函数的正交性：
- 三角函数系:  
![5](https://latex.codecogs.com/svg.latex?1,\cos{x},\sin{x},\cos{2x},\sin{2x},...)  
**任意两个不同**函数的乘积在区间![5](https://latex.codecogs.com/svg.latex?[-\pi,\pi])上的积分都等于0，即这两个函数在区间上正交：
<center>  

![5](https://latex.codecogs.com/svg.latex?\int_{-\pi}^{\pi}\cos{(nx)}dx=0)  
![5](https://latex.codecogs.com/svg.latex?\int_{-\pi}^{\pi}\sin{(nx)}dx=0)   
![5](https://latex.codecogs.com/svg.latex?\int_{-\pi}^{\pi}\cos{(nx)}\cdot\sin{(kx)}dx=0)  
![5](https://latex.codecogs.com/svg.latex?\int_{-\pi}^{\pi}\cos{(nx)}\cdot\cos{(kx)}dx=0)  
![5](https://latex.codecogs.com/svg.latex?\int_{-\pi}^{\pi}\sin{(nx)}\cdot\sin{(kx)}dx=0,)  
其中![5](https://latex.codecogs.com/svg.latex?n,k\in\(1,2,3,...\),n\not=k)
</center>

- 验证：  
<center>  
  
![5](https://latex.codecogs.com/svg.latex?\cos{(nx)}\cdot\cos{(kx)}dx=\frac{1}{2}[\cos{(k+n)x}+\cos{(k-n)x}])  
![5](https://latex.codecogs.com/svg.latex?\sin{(nx)}\cdot\sin{(kx)}dx=-\frac{1}{2}[\cos{(k+n)x}-\cos{(k-n)x}])  
![5](https://latex.codecogs.com/svg.latex?\cos{(nx)}\cdot\sin{(kx)}dx=\frac{1}{2}[\cos{(k+n)x}+\cos{(k-n)x}])
</center>

当 ![5](https://latex.codecogs.com/svg.latex?k\not=n)时：  

![5](equation.svg)

---  

### 3、函数展开成傅里叶级数：
- 傅里叶级数：
<center>

![5](https://latex.codecogs.com/svg.latex?f(t)=A_0+\sum_{n=1}^{\infty}a_{n}\cos{(n\omega{t})}+b_{n}\sin{(n\omega{t})})  
</center>  

对傅里叶级数在[-π, π]范围积分，得：  
<center>  

![5](equation2.svg)
</center>

解得:  
![5](https://latex.codecogs.com/svg.latex?A_0=\frac{1}{2\pi}\int_{-\pi}^{\pi}f(t))  

用![5](https://latex.codecogs.com/svg.latex?\cos(k\omega{t}))乘傅里叶级数等号两边得：  
![6](equation3.svg)  
然后对上式进行[-π, π]范围积分：  

![6](equation4.svg)  
根据三角函数系的正交性，红色积分为0，蓝色项中仅当 [公式] 时积分不为0，其余项积分为0，所以有：
![6](equation5.svg)  

解得：  
![5](https://latex.codecogs.com/svg.latex?a_n=\frac{1}{\pi}\int_{-\pi}^{\pi}\cos(n\omega{t})f(t)dt,(k\not=n))  
同理用得：  
![5](https://latex.codecogs.com/svg.latex?b_n=\frac{1}{\pi}\int_{-\pi}^{\pi}\sin(n\omega{t})f(t)dt,(k\not=n))  

---

### 4、复指数形式的傅里叶级数：

- 欧拉公式：  
<center>

![5](https://latex.codecogs.com/svg.latex?cos(n\omega{t})=\frac{e^{in\omega{t}+e^{-in\omega{t}}}}{2})  
![5](https://latex.codecogs.com/svg.latex?sin(n\omega{t})=\frac{e^{in\omega{t}-e^{-in\omega{t}}}}{2i})  
</center> 

带入傅里叶级数：
<center>

![5](https://latex.codecogs.com/svg.latex?f(t)=a_0+\sum_{n=1}^{\infty}[\frac{a_n-ib_n}{2}e^{in\omega{t}}+\frac{a_n+ib_n}{2}e^{-in\omega{t}}])  
</center> 
可得：  
<center>

![5](https://latex.codecogs.com/svg.latex?f(t)=\sum_{n=-\infty}^{\infty}c_{n}e^{-in\omega\{t}})  
</center> 

其中![5](https://latex.codecogs.com/svg.latex?c_n)称为离散频谱：
<center>

![5](https://latex.codecogs.com/svg.latex?c_n=\frac{1}{T}\int_{\frac{-T}{2}}^{\frac{T}{2}}f(t)e^{-in\omega\{t}}dt)  
</center> 