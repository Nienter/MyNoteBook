---
title: 提高as开发效率
date: 2021-03-11 12:00:00
tags: 
---

### 1.快速生成main方法并打印

- 用`psvm`命令能快速生成`main`方法。
- 用`sout`命令能快速生成打印方法`System.out.println`。

- 两个命令相结合的效果如下：

![图片](https://mmbiz.qpic.cn/mmbiz_gif/uL371281oDGPIdY8rfMW5JICc6pYBDevibxzdTEYNBqm8o6via8hoIo0vIoQF7fvIOXRyTb3XficJaDbQObias7EWA/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

### 2.给new出来的对象快速赋值

在new出来的对象后面加上`.var`，就能实现快速赋值，效果如下：

![图片](https://mmbiz.qpic.cn/mmbiz_gif/uL371281oDGPIdY8rfMW5JICc6pYBDevPU2qGBicqvY9CAuAVlOVMLUHBRIHSapIiccvKmS5lHWSgEUNZc5dwfVw/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

### 3.快速for循环 

1.基本变量

比如：int，long，byte等，在需要进行for循环遍历的变量后加上`.for`，就能快速实现for循环功能，效果如下：

![图片](https://mmbiz.qpic.cn/mmbiz_gif/uL371281oDGPIdY8rfMW5JICc6pYBDev4HiaIInl5KQQxwLf5vpMdlNB6NJV5oTQhY1SEEDXNKG2UWbgsrjxhfQ/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

2.集合

在需要进行forEach循环遍历的集合后加上`.for`，就能快速实现forEach循环功能，效果如下：

![图片](https://mmbiz.qpic.cn/mmbiz_gif/uL371281oDGPIdY8rfMW5JICc6pYBDevJrRV40qkYodZHb4rKvoDLs9RKBJLOAIt4uAv2iaDibgySbk6AqTnonibw/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

### 4.快速判断

判断条件在开发过程中使用频率非常高，如何快速的写出判断条件呢？

- `boolean.if` 可以生成if(boolean)
- `boolean.else` 可以生成if(!boolean)
- `string.null` 可以生成if(string==null)
- `string.nn` 可以生成if(string!=null)

具体实现效果如下：

![图片](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)

此外`.switch`也有类似的功能。

### 5.快速try...catch

有时候我们有异常需要捕获，手动写try...catch比较麻烦，这时快速try...catch可以给我们节省不少时间，只需加`.try`即可，效果如下：

![图片](https://mmbiz.qpic.cn/mmbiz_gif/uL371281oDGPIdY8rfMW5JICc6pYBDevJ7luBPwh1ZvYLTzzP0xygEggZlesMEdtYnGHHkmxXcSPsHT6TCmrYg/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

### 6.快速类型转换

有时候我们需要做类型转换，必须手写括号和赋值参数，同样有些麻烦，这时快速类型转换，可以帮我们搞定，只需加`.castvar`即可，效果如下：

![图片](https://mmbiz.qpic.cn/mmbiz_gif/uL371281oDGPIdY8rfMW5JICc6pYBDevCZtZtfVmRHo48UgHYQWVVQVnj9iaJ2vZsyrHp792He5JkM4THibbMbzA/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

### 7.快速抽取变量

有时候我们需要把方法中的`局部变量`，抽取成`成员变量`，或者`全局变量`，快速抽取变量可以帮你搞定，只需加`.field`即可，具体效果如下：

![图片](https://mmbiz.qpic.cn/mmbiz_gif/uL371281oDGPIdY8rfMW5JICc6pYBDev4qbv6OcrHJH49ZMbVJ2l9rCG1sZqUExF7B5ISbficOdOfaLB07QwhPQ/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

### 8.快速定义Optional

有时候我们想把某个对象转换成`Optional`，避免出现空指针问题，只需加`.opt`即可，具体效果如下：

![图片](https://mmbiz.qpic.cn/mmbiz_gif/uL371281oDGPIdY8rfMW5JICc6pYBDevFPibOI03Ro3UfF8DZI8uTlMIng1hgN24SNFkzKJia9AnhxtKINBDribDA/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

### 9.快速生成lambda语句

如果你在用`jdk1.8`以上的版本，那么lambda表达式必不可少，因为用它可以极大的提高开发效率，少写很多代码。

使用`.lambda`就能快速生成lambda语句，具体效果如下：

![图片](https://mmbiz.qpic.cn/mmbiz_gif/uL371281oDGPIdY8rfMW5JICc6pYBDevfGevScgpUsZ9wsevXj2sw2uSXqrNZRqku0vYibHyyib1JiaFffjr9BhgA/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)

### 10.快速迁移代码到新方法

在代码重构时，经常需要把某段代码迁移到一个新方法中，这时使用快捷键`ctrl + alt + m`，具体效果如下：

![图片](https://mmbiz.qpic.cn/mmbiz_gif/uL371281oDGPIdY8rfMW5JICc6pYBDev9qfOL7Ns6Cic0EmGAOf7Cnt7fdD7vJXOrqQsicqZ082MuMjYbwszkBpw/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1)