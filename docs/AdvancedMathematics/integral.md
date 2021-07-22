# 一元积分学

## 不定积分的计算

---

关于 $\int \sqrt []{1+x^2}\mathrm{d}x$ 的多种计算方法

!!! note "答案与解析"
    
    === "解法一"
    
        令 $x=\tan \theta, \theta \in (-\cfrac{\pi}{2},\cfrac{\pi}{2})$
    
        $$\begin{array}{l}&\int \sqrt[]{1+x^2}\mathrm{d}x \\&= \int \cfrac{1}{\cos^3 \theta}\mathrm{d}x=\int \cfrac{\cos \theta }{\cos ^4\theta }\mathrm{d}x=\int \cfrac{\mathrm{d}\sin \theta  }{(1-\sin ^2 \theta )^2}\\&= \cfrac{1}{4}\int \left[ -\cfrac{1}{\sin \theta -1} +\cfrac{1}{(\sin \theta -1)^2} +\cfrac{1}{\sin \theta +1} +\cfrac{1}{(\sin \theta +1)^2} \right] \mathrm{d}\sin\theta \\&= \cfrac{1}{4} \left( -\ln_{}{(1-\sin \theta )} -\cfrac{1}{\sin \theta -1} +\ln_{}{ (\sin \theta +1)} - \cfrac{1}{\sin \theta +1} \right ) + C\\&= \cfrac{1}{4} \left( \ln _{}{\cfrac{\sin \theta +1}{1-\sin \theta }} - \cfrac{2\sin \theta }{\sin ^2 \theta -1}\right ) + C\\&= \cfrac{1}{4} \left (  \ln _{}{\cfrac{\cfrac{x}{\sqrt[]{1+x^2}+1}}{1-\cfrac{x}{\sqrt[]{1+x^2}}} } + 2x\sqrt[]{1+x^2} \right ) +C\\&= \cfrac{1}{2} \ln_{}{(x+\sqrt[]{x^2+1})} + \cfrac{1}{2}x\sqrt[]{1+x^2} +C.   \end{array}$$
    
    
    === "解法二"
    
    	$$\begin{array}{l}\int \sqrt[]{1+x^2}\mathrm{d}x &= \int \cfrac{1+x^2}{\sqrt{1+x^2}}\mathrm{d}x = \int \cfrac{1}{\sqrt[]{1+x^2}}\mathrm{d}x + \int \cfrac{x^2}{\sqrt[]{1+x^2} }\mathrm{d}x  \\&=\ln _{}{(x+\sqrt{x^2+1})} + \int x\mathrm{d}\sqrt[]{1+x^2}\\&=\ln{(x+\sqrt{x^2+1})} + x\sqrt[]{1+x^2}-\int \sqrt[]{1+x^2}\mathrm{d}x\\\text{故}\int \sqrt[]{1+x^2}\mathrm{d}x  &= \cfrac{1}{2} \ln_{}{(x+\sqrt[]{x^2+1})} + \cfrac{1}{2}x\sqrt[]{1+x^2} +C.            \end{array}$$
    
    === "解法三"
    
    	令 $x=\tan \theta, \theta \in (-\cfrac{\pi}{2},\cfrac{\pi}{2})$
    	
    	$$\begin{array}{l}I&=\int \cfrac{1}{\cos ^3 \theta }\mathrm{d}x=\int(\tan ^2 \theta +1)\sec \theta \mathrm{d}\theta \\&= \int \tan ^2 \theta \sec \theta \mathrm{d}\theta +\int \sec \theta \mathrm{d}\theta \\&= \int \tan \theta \mathrm{d}\sec \theta +\int \sec \theta \mathrm{d}\theta \\&= \tan \theta \sec \theta - \int \sec ^3\theta \mathrm{d}\theta +\ln {\left | \sec \theta +\tan \theta \right |}\\\therefore I &= \cfrac{1}{2} \tan \theta \sec \theta +\cfrac{1}{2} \ln {\left | \sec \theta +\tan \theta \right |}\\&= \cfrac{1}{2} x\sqrt[]{1+x^2} + \cfrac{1}{2}\ln_{}{(x+\sqrt[]{x^2+1})} +C.\end{array}$$
    	