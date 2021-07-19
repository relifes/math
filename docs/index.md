# Welcome to 知远数学分享

:material-feather: 分享优秀题目与解题方法

## 题目分享

* **典型题目** - 通过题目可以得出一个一般性结论，更快更好的解题
* **方法总结** - 求解一类题目的常用方法
* **知识总结** - 汇总常用公式（不等式、三角函数、函数图形与性质）
* **经典的错误，标准的零分** - 总结常见的易错点并分析原理

## 今日更新

`2021-7-18` 

1. 



## 如何分享题目

- 添加微信将 **题目来源**、**题目以及完整的解答过程**、**推荐理由** 发送给我
- 自习室 **1 - 215** 号座位
- 在 **github** 上直接对本项目提交 **PR**

## 题目模板

---

**题目来源：** 武钟祥 - 《高等数学辅导讲义》P53 例2

**题目：** 设 $f(0) = 0$，则 $f(x)$ 在点 $x=0$ 可导的 **充要条件** 为：

（A）$\lim\limits_{h \to 0} {\cfrac{1}{h^2}f(1-\cos h) }$ 存在

（B）$\lim\limits_{h \to 0} {\cfrac{1}{h}f(1-e^h) }$ 存在

（C）$\lim\limits_{h \to 0} {\cfrac{1}{h^2}f(h-\sin h) }$ 存在

（D）$\lim\limits_{h \to 0} {\cfrac{1}{h}  \left [ f(2h) - f(h) \right ]}$ 存在

??? note "答案与解析"
    答案：B

    === "A选项"
    
        $$\begin{align}\lim_{h \to 0}\cfrac{f(1-\cos h)}{h^2} &= \lim_{h \to 0}\cfrac{f(1-\cos h) - f(0)}{1-\cos h}\cdot \cfrac{1-\cos h}{h^2}\\&= \cfrac{1}{2}\lim_{h \to 0}\cfrac{f(1-\cos h) - f(0)} {1-\cos h}=\cfrac{1}{2}f'_+(0).\end{align}$$
    
        由于当 $h \to 0$ 时，$(1-\cos h) \to 0^+$，则只能推出右导数存在，故A不正确。
    
    === "B选项"
    	$$\begin{align}\lim_{h \to 0} \cfrac{1}{h}f(1-e^h)  &= \lim _{h \to 0}\cfrac{f(1-e^h)-f(0)}{1-e^h}\cdot \cfrac{1-e^h}{h}\\&= -\lim _{h \to 0} \cfrac{f(1-e^h)-f(0)}{1-e^h} = -f'(0).\end{align}$$
    
    === "C选项"
    	$$\begin{align}\lim_{h \to 0} \cfrac{1}{h^2}f(h-\sin h) &=\lim_{h \to 0} \cfrac{f(h-\sin h) - f(0)}{h - \sin h}\cdot \cfrac{h-\sin h}{h^2}.\end{align}$$
    	
    	由于 $\lim\limits_{h \to 0} \dfrac{h-\sin h}{h^2} = 0$，极限C存在时， $\lim\limits_{h \to 0}\dfrac{f(h-\sin h) - f(0)}{h - \sin h}$ 不一定存在，故C选项错误
    
    === "D选项"
    	D选择错误类型与其他选项不同，$f(2h)-f(h)$ 是两个动点，不符合导数定义。反例如下：
    	
    	取$f(x) = \left\{\begin{matrix} 1 ,x \ne 0\\  0 , x = 0 \end{matrix}\right.$，显然 $f'(0)$ 不存在，因为 $f(x)$ 在 $x = 0$ 处不连续，但该极限存在。

??? danger "总结"

	$f'(x_0)$ 存在 $\to  \lim \dfrac{f(x_0 + \Box )-f(x_0)}{\Box}$ 存在
	
	1. $\Box \to 0$
	2. $\Box \ne 0$
	
	$\lim \dfrac{f(x_0 + \Box )-f(x_0)}{\Box}$ 存在 $\to f'(x_0)$ 存在
	
	1. $\Box \to 0$
	2. $\Box \ne 0$
	3. $\Box$ 可正可负
	
	$\lim\limits_{h \to 0} \dfrac{f(\varphi(h))-f(0)}{\psi(h)}$ 存在 $\to f'(0)$ 存在
	
	1. $\varphi(x) \to 0，\varphi(x) \ne 0$
	2. $\varphi(x)$ 可正可负
	3. $\varphi(x)$ 与 $\psi(x)$ 同阶

---

## 题目MarkDown模板

```markdown
**题目来源：** 武钟祥 - 《高等数学辅导讲义》P53 例2

**题目：** 设 $f(0) = 0$，则 $f(x)$ 在点 $x=0$ 可导的 **充要条件** 为：

（A）$\lim\limits_{h \to 0} {\cfrac{1}{h^2}f(1-\cos h) }$ 存在

（B）$\lim\limits_{h \to 0} {\cfrac{1}{h}f(1-e^h) }$ 存在

（C）$\lim\limits_{h \to 0} {\cfrac{1}{h^2}f(h-\sin h) }$ 存在

（D）$\lim\limits_{h \to 0} {\cfrac{1}{h}  \left [ f(2h) - f(h) \right ]}$ 存在

??? note "答案与解析"
    答案：B

    === "A选项"
    
        $$\begin{align}\lim_{h \to 0}\cfrac{f(1-\cos h)}{h^2} &= \lim_{h \to 0}\cfrac{f(1-\cos h) - f(0)}{1-\cos h}\cdot \cfrac{1-\cos h}{h^2}\\&= \cfrac{1}{2}\lim_{h \to 0}\cfrac{f(1-\cos h) - f(0)} {1-\cos h}=\cfrac{1}{2}f'_+(0).\end{align}$$
    
        由于当 $h \to 0$ 时，$(1-\cos h) \to 0^+$，则只能推出右导数存在，故A不正确。
    
    === "B选项"
    	$$\begin{align}\lim_{h \to 0} \cfrac{1}{h}f(1-e^h)  &= \lim _{h \to 0}\cfrac{f(1-e^h)-f(0)}{1-e^h}\cdot \cfrac{1-e^h}{h}\\&= -\lim _{h \to 0} \cfrac{f(1-e^h)-f(0)}{1-e^h} = -f'(0).\end{align}$$
    
    === "C选项"
    	$$\begin{align}\lim_{h \to 0} \cfrac{1}{h^2}f(h-\sin h) &=\lim_{h \to 0} \cfrac{f(h-\sin h) - f(0)}{h - \sin h}\cdot \cfrac{h-\sin h}{h^2}.\end{align}$$
    	
    	由于 $\lim\limits_{h \to 0} \dfrac{h-\sin h}{h^2} = 0$，极限C存在时， $\lim\limits_{h \to 0}\dfrac{f(h-\sin h) - f(0)}{h - \sin h}$ 不一定存在，故C选项错误
    
    === "D选项"
    	D选择错误类型与其他选项不同，$f(2h)-f(h)$ 是两个动点，不符合导数定义。反例如下：
    	
    	取$f(x) = \left\{\begin{matrix} 1 ,x \ne 0\\  0 , x = 0 \end{matrix}\right.$，显然 $f'(0)$ 不存在，因为 $f(x)$ 在 $x = 0$ 处不连续，但该极限存在。

??? danger "总结"

	$f'(x_0)$ 存在 $\to  \lim \dfrac{f(x_0 + \Box )-f(x_0)}{\Box}$ 存在
	
	1. $\Box \to 0$
	2. $\Box \ne 0$
	
	$\lim \dfrac{f(x_0 + \Box )-f(x_0)}{\Box}$ 存在 $\to f'(x_0)$ 存在
	
	1. $\Box \to 0$
	2. $\Box \ne 0$
	3. $\Box$ 可正可负
	
	$\lim\limits_{h \to 0} \dfrac{f(\varphi(h))-f(0)}{\psi(h)}$ 存在 $\to f'(0)$ 存在
	
	1. $\varphi(x) \to 0，\varphi(x) \ne 0$
	2. $\varphi(x)$ 可正可负
	3. $\varphi(x)$ 与 $\psi(x)$ 同阶

---

```

