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

## $f(x)$ 在 $x=0$ 的某邻域可导，求导数与极限

---

**题目来源：** 武钟祥 - 《高等数学辅导讲义 严选题》P4 T37

**题目：** 已知函数 $f(x)$在$x=0$的某邻域内可导，且$\lim\limits_{x\to0}\left(\dfrac{\sin x}{x^2}+\dfrac{f(x)}{x}\right)=2$，试求$f(0),f'(0),\lim\limits_{x\to0}\cfrac{x}{f(x)+e^x}$.

??? note "答案与解析"
	因为题目只告诉了$f(x)$ 在 $x=0$ 的某邻域内可导，所以不可以直接洛必达对$f(x)$求导。考虑凑 $f'(0)$ 的导数定义，或者将 $f(x)$ 在0点处泰勒展开。
	
	$$
	\begin{align}
	2 &= \lim\limits _{x\to 0}\left (\cfrac{\sin x}{x^2}+\cfrac{f(x)}{x} \right )=\lim_{x \to 0}\cfrac{\sin x+xf(x)}{x^2} \\
	&= \lim_{x \to 0}\cfrac{x+o(x^2)+x[f(0)+f'(0)x+o(x)]}{x^2}\\
	&= \lim_{x \to 0}\cfrac{x[1+f(0)]+f'(0)x^2+o(x^2)}{x^2}     
	\end{align}
	$$
	
	则$1+f(0)=0,f'(0)=2$.
	
	$\lim\limits_{x\to0}\dfrac{x}{f(x)+e^x}=\lim\limits_{x\to0}\dfrac{x}{[f(0)+f'(0)x+o(x)]+[1+x+o(x)]}=\lim\limits_{x\to0}\dfrac{x}{3x+o(x)}=\dfrac{1}{3}$


## 数列极限

---
**题目来源：** 武钟祥 - 《高等数学辅导讲义 严选题》P4 T26

**题目：** 极限 $\lim\limits_{n \to \infty}\cfrac{\sqrt{1}+\sqrt{2}+\cdots+\sqrt{n}}{\sqrt{n(1+2+\cdots+n)}}=$

??? note "答案与解析"
	夹逼不出来，考虑定积分定义
	
	$$\begin{align}\text{原式} &= \lim_{n \to \infty }\cfrac{\sqrt[]{1}+\sqrt[]{2}+\cdots +\sqrt[]{n}}{\sqrt[]{\dfrac{n^2(n+1)}{2}}} \\&= \sqrt[]{2}\lim_{n \to \infty }\sqrt[]{\frac{n}{n+1}}\cdot    \cfrac{1}{n}  \sum_{k=1}^{k}\sqrt[]{\frac{k}{n}} \\&= \sqrt[]{2}\int_{0}^{1}\sqrt[]{x}\mathrm{d}x=\cfrac{3\sqrt[]{2} }{3}      \end{align}$$


---

**题目来源：** 武钟祥 - 《高等数学辅导讲义 严选题》P5 T40

**题目：** 求极限 $\lim\limits _{n \to \infty} \left ( \cfrac{n+1}{1^2+n^2} +\cfrac{n+\cfrac{1}{2} }{2^2+n^2}+\cdots +\cfrac{n+\cfrac{1}{n} }{n^2+n^2}   \right ) =$

??? note "答案与解析"
	分子是 **次量级**（ $\lim\limits_{n \to \infty}\cfrac{1}{n}=0$ ）考虑夹逼定理，分母是 **同量级** （ $\lim\limits_{n \to \infty}\cfrac{n^2}{n^2}=1$ ）考虑定积分定义。
	
	$$\begin{align}
	\cfrac{1}{n} \sum\limits_{k = 1}^{n} \cfrac{1}{1+(\cfrac{k}{n} )^2}  <
	\sum\limits _{k = 1}^{n}\cfrac{n+\cfrac{1}{k}}{k^2+n^2}  <
	\cfrac{n+1}{n}\cdot \cfrac{1}{n} \sum\limits _{k = 1}^{n}\cfrac{1}{1+(\cfrac{k}{n} )^2} 
	\end{align}$$
	
	$$\begin{align}
	\lim_{n \to \infty }\cfrac{1}{n}\sum_{k=1}^{n}\cfrac{1}{1+(\cfrac{k}{n} )^2}
	&= \lim_{n \to \infty }\cfrac{n+1}{n} \cdot \cfrac{1}{n}\sum_{k=1}^{n}\cfrac{1}{1+(\cfrac{k}{n} )^2}   \\
	&= \int_{0}^{1}\cfrac{1}{1+x^2}\mathrm{d}x=\cfrac{\pi}{4}    
	\end{align}$$


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
