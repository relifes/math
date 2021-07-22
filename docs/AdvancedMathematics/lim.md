# 函数，极限，连续

## 间断点及其类型

---

**题目来源：** 武钟祥 - 《高等数学辅导讲义 严选题》P3 T2

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