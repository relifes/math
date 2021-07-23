# 函数，极限，连续


## 极限计算

---

**题目来源：** 武钟祥 - 《高等数学辅导讲义 严选题》P3 T22

**题目：** 极限 $\lim\limits_{x \to 0} \left [ \cfrac{1}{\ln {(x+\sqrt[]{1+x^2} )}}- \cfrac{1}{\ln{(1+x)}}  \right ] =$

??? note "答案与解析"
	$$\begin{align}
	\text{原式} &=  \lim_{x \to 0} \cfrac{\ln{(1+x)-\ln{(x+\sqrt[]{1+x^2} )}}}{\ln{(1+x)}\ln {(x+\sqrt[]{1+x^2} )}}\\
	&= \lim_{x \to 0} \cfrac{\ln{(1+x)-\ln{(x+\sqrt[]{1+x^2} )}}}{x^2}\text{这里} (\ln{(x+\sqrt[]{1+x^2})\sim x })\\
	&= \lim_{x \to 0} \cfrac{\cfrac{1}{\xi} (1+x-x-\sqrt[]{1+x^2} )}{x^2}  ( \xi\text{在}1+x\text{与}x+\sqrt[]{1+x^2}\text{之间} )\\
	&= \lim_{x \to 0} \cfrac{-\cfrac{1}{2}x^2 }{x^2} = -\cfrac{1}{2}  
	\end{align}$$

---

## 数列极限

---
**题目来源：** 武钟祥 - 《高等数学辅导讲义 严选题》P4 T26

**题目：** 极限 $\lim\limits_{n \to \infty}\cfrac{\sqrt{1}+\sqrt{2}+\cdots+\sqrt{n}}{\sqrt{n(1+2+\cdots+n)}}=$

??? note "答案与解析"
	夹逼不出来，考虑定积分定义
	
	$$\begin{align}\text{原式} &= \lim_{n \to \infty }\cfrac{\sqrt[]{1}+\sqrt[]{2}+\cdots +\sqrt[]{n}}{\sqrt[]{\dfrac{n^2(n+1)}{2}}} \\&= \sqrt[]{2}\lim_{n \to \infty }\sqrt[]{\frac{n}{n+1}}\cdot    \cfrac{1}{n}  \sum_{k=1}^{k}\sqrt[]{\frac{k}{n}} \\&= \sqrt[]{2}\int_{0}^{1}\sqrt[]{x}\mathrm{d}x=\cfrac{3\sqrt[]{2} }{3}      \end{align}$$
	

---


## 间断点及其类型

---

**题目来源：** 武钟祥 - 《高等数学辅导讲义 严选题》P3 T18

**题目：** 设 $f(x) = \lim\limits_{n \to \infty} \dfrac{2e^{(n+1)x}+1}{e^{nx}+x^n+1}$，则 $f(x)$

（A）仅有一个可去间断点

（B）仅有一个跳跃间断点

（C）有两个可去间断点

（D）有两个跳跃间断点

??? note "答案与解析"
    答案：D
    
    利用结论：
    
    $$\begin{array}{l}\lim\limits_{n \to \infty } =  \left\{\begin{matrix} 0,&x<0,\\1,&x=0,\\+\infty ,&x>0.\end{matrix}\right.\lim\limits_{n \to \infty } =  \left\{\begin{matrix} 0,& \left |x \right | < 1,\\ \infty ,&\left |x \right |>1,\\1,&x=1,\\ \text{不存在},&x=-1. \end{matrix}\right.\\ \end{array}$$
    
    当 $x< -1$ 时， $f(x) = \lim\limits_{n \to \infty} \dfrac{2e^{(n+1)x}+1}{e^{nx}+x^n+1}=0$;
    
    当 $-1<x<0$ 时， $f(x) = \lim\limits_{n \to \infty} \dfrac{2e^{(n+1)x}+1}{e^{nx}+x^n+1}=1$;
    
    当 $x>0$ 时， $f(x) = \lim\limits_{n \to \infty} \dfrac{2e^{(n+1)x}+1}{e^{nx}+x^n+1}=\lim\limits_{n \to \infty} \dfrac{2e^x+\cfrac{1}{e^{nx}}}{1+{(\cfrac{x}{e^x})}^n+\cfrac{1}{e^{nx}} }=2e^x (\text{这里因为}e^x \ge x + 1)$;
    
    则，
    
     $\begin{array}{l}f(x) = \left\{\begin{matrix} 0,&x<-1,\\1,&-1<x<0,\\2e^x ,&x>0.\end{matrix}\right.\end{array}$
    
    显然 $x = -1, x= 0$ 都是跳跃间断点，故选择D


---
