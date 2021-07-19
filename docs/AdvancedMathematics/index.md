# 高等数学

## 测试

这里是中文测试。

这里是`lalala`中文测试。这里是中文测试。这里是中文测试。这里是中文测试。这里是中文测试。这里是中文测试。这里是中文测试。

This is English Test.This is English Test.This is English Test.This is English Test.This is English Test.This is English Test.This is English Test.

> 重点标记测试

公式测试：

$$y(n)=(f\ast g)(n)=\sum_{\tau =\infty}^{\infty}f(\tau )g(n-\tau )d\tau $$

$$
\begin{bmatrix}
1& 2& 3\\ 
4& 5& 6\\ 
7& 8& 9
\end{bmatrix}\Rightarrow \begin{bmatrix}
3& 2& 1\\ 
6& 5& 4\\ 
9& 8& 7
\end{bmatrix}\Rightarrow \begin{bmatrix}
9& 8& 7\\ 
6& 5& 4\\ 
3& 2& 1
\end{bmatrix}
$$

$$
\begin{align}
\lim_{x \to 0} \frac{x-\arctan x}{x^3} & = 1
\end{align}
$$

$$
\operatorname{ker} f=\{g\in G:f(g)=e_{H}\}{\mbox{.}}
$$

The homomorphism $f$ is injective if and only if its kernel is only the 
singleton set $e_G$, because otherwise $\exists a,b\in G$ with $a\neq b$ such 
that $f(a)=f(b)$.



## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

分组代码

=== "C"

    ``` c
    #include <stdio.h>
    
    int main(void) {
      printf("Hello world!\n");
      return 0;
    }
    ```

=== "C++"

    ``` c++
    #include <iostream>
    
    int main(void) {
      std::cout << "Hello world!" << std::endl;
      return 0;
    }
    ```


分组其他内容

=== "A选项"

    $\begin{align}\lim_{h \to 0}\cfrac{f(1-\cos h)}{h^2} &= \lim_{h \to 0}\cfrac{f(1-\cos h) - f(0)}{1-\cos h}\cdot \cfrac{1-\cos h}{h^2}\\&= \cfrac{1}{2}\lim_{h \to 0}\cfrac{f(1-\cos h) - f(0)} {1-\cos h}=\cfrac{1}{2}f'_+(0).\end{align}$

=== "Ordered list"

    1. Sed sagittis eleifend rutrum
    2. Donec vitae suscipit est
    3. Nulla tempor lobortis orci


嵌入内容

!!! example

    === "Unordered List"
    
        _Example_:
    
        ``` markdown
        * Sed sagittis eleifend rutrum
        * Donec vitae suscipit est
        * Nulla tempor lobortis orci
        ```
    
        _Result_:
    
        * Sed sagittis eleifend rutrum
        * Donec vitae suscipit est
        * Nulla tempor lobortis orci
    
    === "Ordered List"
    
        _Example_:
    
        ``` markdown
        1. Sed sagittis eleifend rutrum
        2. Donec vitae suscipit est
        3. Nulla tempor lobortis orci
        ```
    
        _Result_:
    
        1. Sed sagittis eleifend rutrum
        2. Donec vitae suscipit est
        3. Nulla tempor lobortis orci


!!! note ""
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

??? note
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
