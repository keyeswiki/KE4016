# Mixly


## 1. Mixly简介  

Mixly是一款基于图形化编程的编程工具，类似于Scratch，旨在为用户提供一个可视化的编程环境。它特别适合初学者，尤其是儿童，让他们能够通过简单的拖放操作，轻松构建与Arduino等硬件的项目。Mixly支持多种硬件组件，包括传感器和模块，通过可视化编程，用户可以理解编程逻辑，同时节省了编码学习中可能遇到的繁琐语法时间。Mixly不仅能够提升用户的编程技能，还能激发他们的创造力和解决问题的能力。  

## 2. 连接图  

![](media/11260e390f75ed8459d191d4407b26cb.png)  

## 3. 测试代码  

1. 在变量栏找到声明全局变量模块，将item变量名改为“button”，并设置button初始变量为整数，赋值为0。  

   ![](media/4f94f6d1e76574b25f6fe616cdcdab3c.png)  

2. 初始化设置波特率为9600，表示9600bit每秒的串口通信速度。  

   ![](media/87b7c2535b1e8327f48ff8c03fc1e96d.png)  

3. 在变量栏拖出button赋值模块，并在输入/输出栏拖出数字引脚输入模块，设置引脚为3。  

   ![](media/288865dd68c9cfcb87b8f99c6eda74e3.png)  

4. 拖出串口栏下的打印并自动换行模块，然后在变量下找到定义的变量button，放入打印模块后面。  

   ![](media/97a311f9bc5861a8c97fa523317ff101.png)  

5. 在控制栏拖出判断模块，并点击模块上的设置图案，增加一个“否则”部分。  

   ![](media/64f8573b79bd000de8657185996afa05.png)  

6. 在逻辑栏拖出一个等于模块，并在其中添加变量button和数字0。  

   ![](media/a5e6549443aa946c0ffcd73048e48373.png)  

7. 在输入/输出栏拖出设置引脚模块，设置引脚为13，高电平，随后拖出一个延时模块，延时为100ms。  

   ![](media/34ce1cebb194a08763a1652405d03818.png)  

8. 再次在输入/输出栏拖出设置引脚模块，设置引脚为13，低电平，最后拖出一个延时模块，延时为100ms。  

   ![](media/0cc576abc46c54d1e22b79e890e8a940.png)  

## 4. 测试结果  

按照上图接好线，烧录好代码，通电后，当感应到磁铁时，D13灯亮起。  

结果

上传代码后，当感应一次时 LED 灯亮起，再次感应时 LED 灯熄灭。实现这个功能的关键在于变量time，值得深入思考。



