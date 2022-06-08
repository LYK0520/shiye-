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

## 4.3

1. p119 27 和 48 headLocation的定义与p163 headRotation冲突（应该是一个变量）并且与p134的 385和397的headRotation出现冲突
2. p151 此段代码并不能完成该页下图的显示，原因步进移动那一行之后要把颜色改回去，包括后面的CharacterSize的大小也要重新调整回24
3. p138 水平跟随 竖直跟随 以及拐角跟随 在遇到穿墙的情况 会因为tailX[i-1]-tailX[i]以及tailY[i-1]-tailY[i]的跨度太大，导致蛇身的显示出现bug具体更改为（加上类似于&& abs(tailX[i]-tailX[i-1])<=2的判断

## 4.10

1. p184 imgBGNo imgSkinNo 需要赋初值为1 否则无法找到文件
2. p208 i和j的赋值并不严谨 建议增强条件 否则在区域外面一点点也会出现点击的现象
3. p212 MOUSEFUNTION的mouseAction建议添加STOP属性 并在p213 break前面增加mouseAction的赋值STOP
4. p219 P1 P2等等getposition并不严密，可能在全屏之后出现响应区域不一致的问题
5. p224 第二块代码9-17可能出现点击重来无法点击的情况 （代码不一定相同，情况不一定相同）
6. p225 30line 条件没有写完
7. p228 DrawGrid函数需要重新对mCornPoint进行赋值
8. p239 66 67行似乎没啥用 如果出现问题也可以看后面确定版的代码 不要直接抄
9. p251 需要自己定义~Tetris（） 和~Game（）
10. p253 没有对DALAYVALUE和b7Int进行定义和赋值
11. p253 31line currentShape-eNum改为 currentShapeNum
12. p261 12 这一行不需要 （代码不一定相同，情况不一定相同）
13. p285 imgSetNo需要赋值为1
14. p298 line13 newShape改为newShapeFunc
15. p305 gameOver=true 并不会使得游戏结束 需要将gameOver传递给Game：：gameOver 即gameOver=(player1.gameOver||player2.gameOver)
16. p307 TextOut（）有一个这个函数了可以换一个名字
17. p309 有彩蛋！！爱你们的李仕