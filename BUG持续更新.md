# BUG持续更新...

## 2.27

1. p24 代码块一9行 inti = 0 => int i = 0
2. p34 代码块二10行 voidInitial() => void Initial()
3. p108

## 2.28

1. 前言 第三段第二行 授 => 受
2. p54 代码块二42行  hOutput. &cci=> hOutput,&cci

## 3.6

1. P64 3 局部绘制 代码块 81行 fruitFlash 未进行定义
2. P81 代码块游戏重新开始 将nTail=1重新初始化否则导致无法重新开始

## 3.8

1. P87 5.3 代码维护与管理 宏定义的颜色 0和O需要注意区分
2. p54 代码块一第一行注释 "共享写权限"语义不明

## 3.12

1. p88 5.3.2代码的可维护性 83行和175行（根据p87的define）THICHKNESS改为THICKNESS
2. p107  第二代码块 spSnack与p108 35行spSnackHead冲突

## 3.22

1. 截止7.2.6 游戏I/O频率的调整，delay的初始化为0，但是在前面的代码来看，并未在initial()处将x和y的值赋给spSnackHead，这将导致游戏界面开始前会有0.5s左右的时间蛇头在左上角出现。	解决措施：1 在initial的位置对蛇头进行初始化 2 delay可以初始化为9，在第一轮循环时就能执行Logic()里面的赋值