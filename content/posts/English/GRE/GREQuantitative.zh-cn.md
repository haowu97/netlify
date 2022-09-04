---
title: "GRE Quantitative 数量知识点与解题方法"
date: 2021-08-09T14:14:45+08:00
draft: false

description: "基本数论，代数计算，初等几何，文字应用题以及比较大小题型。"
upd: "基本数论，代数计算，初等几何，文字应用题以及比较大小题型。"

tags: ["笔记", "GRE"]
categories: ["GRE"]
---

<!--more-->

## 1. 考试介绍

满分：170
Section：2个（或3个）
时间：25min
题目：20个

GRE数学题型分布
• 填空： 1-2个
• 不定项选择：1-2个
• 比较大小： 7-9个
• 普通单选： 其余题⽬

GRE数学注意事项(考试中不要再浪费时间去阅读)

- For each question, **indicate thele best answer**, using the directions given. If you need more detailed directions, click **Help** at any time.

- An on-screen **calculator** is available for each question in this section. To use the calculator, click the calculator icon at the top of the screen.(考试中计算量并不大，用草稿纸手算足够)

- If a question has answer choices with **ovals**, then the correct answer consists of a **single choice**. If a question has answer choices with **square boxes**, then the correct answer consists of **one or more answer choices**. Read the directions for each question carefully.

- All numbers used are real numbers（实数）

- All figures are assumed to lie in a plane unless otherwise indicated.（所有图都默认是平面的）

- **Geometric figures**, such as lines, circles, triangles, and quadrilaterals, are not necessarily drawn to scale. That is, *you should not assume that quantities such as lengths and angle measure are as they appear in a figure*. You should assume, however, that lines shown as straight are actually straight, points on a line are in the order shown, and more generally, all geometric objects are in the relative positions shown. For questions with geometric figures, you should base your answers on geometric reasoning, not on estimating or comparing quantities by sight or by measurement.（长度、角度不能目测图形猜测）

- **Coordinate systems**, such as xy-planes and number lines, are **drawn to scale**; therefore you can read, estimate, or compare quantities in such figures by sight or by measurement.

- **Graphical data presentations**, such as bar graphs, circle graphs,and line graphs, are *drawn to scale*; therefore, you can read, estimate, or compare data values by sight or by measurement.

- Click Continue to go on.

计算不复杂，重点考概念

## 2. 基本数论

本节课教学大纲：

• 奇偶数
• 因数与质因数
• 最大公约数与最小公倍数
• 余数
• 小数、分数与科学计数法
• 比率与比例

### 2.1 奇偶数（Odd and Even Numbers）

- 奇数 + 奇数 = 偶数；奇数 × 奇数 = 奇数
- 偶数 + 偶数 = 偶数；奇数 × 偶数 = 偶数
- 奇数 + 偶数 = 奇数；偶数 × 偶数 = 偶数

【Example】If $ x $ is an even integer and $ y $ is an odd integer, which of the following CANNOT be true?
(A) $ x^{y} $ is an even integer.
(B) $ y^{x} $ is an odd integer.
(C) $ x $ is a multiple of $ y $.
(D) $ y $ is a multiple of $ x $.
(E) $ x y $ is an even integer.
正确答案：选D

【**Example**】If $ a^{2}+b^{2}=c^{2} $, where $ a, b, c $ are integers. Which of the following CANNOT be a value of $ a+b+c ? $
(A) 2
(B) 1
(C) $ -2 $
(D) 4
(E) 6

解析：

- 法一：利用 3，4，5，加上正负号去组合，只有b选项不行；

- 法二：或者假设a=0，b和c相等，只有b选项不可能；

- 法三：abc中必然是两个奇数一个偶数，或者全部是偶数，因此求和之后必然是偶数

### 2.2 质数与因数

因数/因子/约数/除数：factor/ divisor

- 在GRE考试中，因数的负数也算是因数

- 1和本身一定是因数

倍数：multiple

质数（prime number）：仅含1和本身的因数（两个正因数）的数

- 2，3，5，7

- 在质数中，2是唯一的偶数，2是最小的质数

合数（composite number）：含有两个以上正因数的数

- 1既不是质数也不是合数（不考）

判断是否包含某个因数：

- **2，5看最后一位是否能被整除即可**
- **4看最后两位是否能被整除两位即可**
- **8看最后三位是否能被整除两位即可**
- 3看所有位数数字之后能否被3整除
- 9看所有位数数字之后能否被9整除

【Example】The sum of the prime numbers that are greater than 60 and less than 70 is
(A) 67
(B) 128
(C) 191
(D) 197
(E) 260

解析：

- 先排除偶数，再排除65，63和69，剩下61，67
- 结合选项，必有67，因此只要判断61即可
- **试因数的时候从质数开始尝试即可**
- 选 B

【Example】If $ x $ is the product of the positive integers from 1 to 8 , inclusive, and if $ i, k, m $, and $ p $ are positive integers such that $ x=2^{i} 3^{k} 5^{m} 7^{p} $, then $ i+k+m+p= $
(A) 4
(B) 7
(C) 8
(D) 11
(E) 12
解析：inclusive表示包括1和8（闭区间），x = 1x2x3x4x5x6x7x8, 选D

【Example】屏幕中出现一个数：$ 690, \triangle 70 $
If $ \triangle $ represents a single digit in the integer above, which of the following CANNOT be a factor of this integer?
(A) 2
(B) 3
(C) 4
(D) 5
(E) 7

解析：选C

- **2，5看最后一位是否能被整除即可**

- **4看最后两位是否能被整除两位即可**，70不能被整除，因此选D

- 判断7的时候做除法去判断，Delta = 2或者9的时候可以被7整除

### 2.3 最大公约数与最小公倍数 (Greatest Common Divisors and Least Common Multiples)

两个数的最大公约数与最小公倍数的求解方法

1. 将两个数分别各自分解质因数

2. 每一个质数，取较小的指数，相乘得到最大公约数;

3. 每一个质数，取较大的指数，相乘得到最小公倍数

常用平方数：11² = 121， 12² = 144 ，13² = 169 ，14² = 196 ，15² = 225， 16² = 256， 17² = 289 ，18² = 324， 19² = 361 

【Example】求45和60的最大公约数与最小公倍数：

- 45 = 3^2 x 5

- 60 = 2^2 x 3^1 x 5

- 最大公约数  = 2^0 x 3^1 x 5^1 = 15

- 最小公倍数 = 2^2 x 3^2 x 5^1 = 180 

【Example】If M is the least common multiple of 90, 196, and 300, which of the following is NOT a factor of M ?
(A) 600
(B) 700
(C) 900
(D) 2,100
(E) 4,900

解析：选A

- 90 = 2 x 5 x 3^2

- 196 = 2^2 x 7^2

- 300 = 2^2 x 3 x 5^2

- M = 2^2 x 3^2 x 5^2 x 7^2

- 注意选项都是100的倍数，判断的时候直接可以将 2^2 x 5^2约掉

### 2.4 余数（remainder）

【知识点】某数（如3，7，2，8）的n次幂的个位数的循环规律，对于判断余数很有帮助

- 3：3，9，7，1

- 7：7，9，3，1

- 2：2，4，8，6

- 8：8，4，2，6

【练习】What is the sum of the remainders when the first 40 positive integers are divided by 6 ?
(A)96
(B)100
(C)120
(D)132
(E)136

解析：（1+2+3+4+5+0）x 6 + （1+2+3+4）= 100

【练习】If n is a positive integer, what is the remainder when 3^(8n+3) + 2 is divided by 5?
(A)0
(B)1
(C)2
(D)3
(E)4

解析：除以5的余数只需要看个位数即可，个位数找规律

- 3^1 = 3

- 3^2 = 9

- 3^3 = 7

- 3^4 = 1

- 3^5 = 3

- 四个一循环，因此3^(8n+3)的个位数是7

- 选E

### 2.5 小数、分数与科学计数法

 识别各位数字名称”7654.321”，其中： 

- “7”: thousands 

- “6”: hundreds 

- “5”: tens 

- “4”: units (or ones) 

- “.” : decimal point 

- “3”: tenths 

- “2”: hundredths

- “1”: thousandths

考试常考的循环小数：

- 1/9 = 0.11111....

- 2/9 = 0.22222....

- 3/9 = 1/3 = 0.33333.....

- 1/6 = 0.16666.....

- 5/6 = 0.83333.....

【错位相减法】**求解特殊循环小数的分数形式**：例0.535353...

- 令x = 0.535353...，则100x - x = 53，因此x = 53/99

- 可以用来求解所谓无限循环小数的分数形式

术语：

- 有限小数(terminating decimal)

- 循环小数(circulating decimal)

- 十进制计数法base decimal notation

- 科学计数法scientific notation

【Example】On a recent trip, Cindy drove her car 380 miles, rounded to the nearest 10 miles, and used $ 16.3 $ gallons of gasoline, rounded to the nearest tenths gallon. The actual number of miles per gallon that Cindy's car got on this trip must have been between
(A) $ \frac{380}{16.35} $ and $ \frac{380}{16.25} $
(B) $ \frac{380}{16.3} $ and $ \frac{375}{16.25} $
(C) $ \frac{375}{16.3} $ and $ \frac{385}{16.3} $
(D) $ \frac{375}{16.35} $ and $ \frac{385}{16.25} $
(E) $ \frac{385}{16.35} $ and $ \frac{375}{16.25} $

解析：选D

- 里程在区间[375, 385)，注意可以无限接近385，但不能取等

- 汽油在区间[16.25,16.35)

【Example】If the tens digit $ \mathrm{x} $ and the units digit $ \mathrm{y} $ of a positive integer $ \mathrm{n} $ are reversed, the resulting integer is 9 more than $ n $. What is $ y $ in terms of $ x $ ?
(A) $ 10-x $
(B) $ 9-x $
(C) $ x+9 $
(D) $ x-1 $
(E) $ x+1 $

解析：选E

- xy = 10x + y

- yx = 10y + x

- 10y + x - (10x + y)  = 9

- 也可以直接找一个数试试，例如12，56

【Example】Of the following which best approximates the fraction $ \frac{(0.1667)(0.8333)(0.3333)}{(0.2222)(0.6667)(0.1250)} $
(A) $ 2.00 $
(B) $ 2.40 $
(C) $ 2.43 $
(D) $ 2.50 $
(E) $ 3.43 $

解析：fraction（分数），这一题直接用计算器算即可，选 D。
【Example】If $ 10^{50}-74 $ is written as an integer in **base decimal notation**, what is the sum of the digits in that integer?

(A)424
(B)431
(C)440
(D)449
(E)456

解析：最后形如9999....9926,求和（50-2）x 9 + 2 + 6 = 440

### 2.6 比率与比例

- the ratio of $ A $ to $ B $ 表示为 $ A: B $ 或者 $ \frac{A}{B} $.
- There is twice as much $ A $ as $ B $ 表示为 $ A=2 B $ 或者 $ \frac{A}{B}=2 $.

【Example】A certain fraction is equivalent to $ 2 / 5 $. If the numerator of the fraction is increased by 4 and the denominator is doubled, the new fraction is equivalent to $ 1 / 3 . $ What is the sum of the numerator and denominator of the original fraction?
  (A) 21
  (B) 26
  (C) 28
  (D) 35
  (E) 49

解析：设原分数为2a/5a，则(2a+4)/(10a) = 1/3，可得a = 3，7a = 21, 选A。

【Example】A merchant purchased a jacket for \$ 60 and then determined a selling price that equaled the purchase price of the jacket plus a markup that was 25 percent of the selling price. During a sale, the merchant discounted the selling price by 20 percent and sold the jacket. What was the merchant's gross profit on this sale?
  (A) \$ 0
  (B) \$ 3
  (C) \$ 4
  (D) \$ 12
  (E) \$ 15

解析：

- 售价为S，则S = 60 + 25%S，得S = 80，打折后得价格为(1-20%)S = 64, 利润为4，选C

- 错误解法：售价为60 x 1.25 x (1-20%) = 60, 因此利润为0。

术语：

- revenue 收入

- cost 成本

- profit = 利润

- revenue = cost + profit

【Example】In a certain formula, $ p $ is **directly proportional**(正比) to $ s $ and **inversely proportional**(反比) to $ r $. If $ p=1 $ when $ r=0.5 $ and $ s=2 $, what is the value of $ p $ in terms of $ r $ and $ s $ ?
(A) $ \mathrm{s} / \mathrm{r} $
(B) $ \mathrm{r} / \mathrm{4s} $
(C) $ s / 4 r $
(D) $ \mathrm{r} / \mathrm{s} $
(E) $ 4 \mathrm{r} / \mathrm{s} $

解析：s在分子，r在分母，带入后选C。

## 3. 代数计算

本节课教学大纲：

• 指数运算 

• 解方程 

• 不等式 

• 数列

### 3.1 指数运算 (Rules of Exponents)

术语：

- 底数: base

- 指数: exponent

- 3 to the 5th power: $3^{5}$

- 口语化表达：3 power 5

$$
\begin{array}{l}
a^{m} \times a^{n}=a^{m+n} \\
a^{m} \div a^{n}=a^{m-n} \\
\left(a^{m}\right)^{n}=a^{m n} \\
a^{m} \times b^{m}=(a \times b)^{m} \\
a^{m} \div b^{m}=(a \div b)^{m}
\end{array}
$$

【Example】

$$
\left(10^{100}\right)^{\left(10^{100}\right)}=10^{\left(10^{k}\right)},
 \mathrm{k}=\text {？}
$$

解析：k = 102

【Example】Of the following values of $ n $, the value of $ \left(-\frac{1}{5}\right)^{-n}$ will be greatest for $ n= $
(A) $ -3 $
(B) $ -2 $
(C) 0
(D) 2
(E) 3

解析：$\left(-\frac{1}{5}\right)^{-n} = (-5)^{n}$，因此选择偶数且绝对值越大越好。

### 3.2 解方程 (Equations)

一元二次方程 $ a x^{2}+b x+c=0 $

- 标准根的公式为: $ x_{1,2}=\frac{-b \pm \sqrt{b^{2}-4 a c}}{2 a} $

韦达定理：

- $x_1 + x_2 = -b/a$

- $x_1  x_2 = c/a$

常用公式：

- 平方差公式：$a^2-b^2 = (a-b)(a+b)$

- 完全平方公式：$a^2 ± 2ab +b^2 = (a+b)^2$

术语：

- 加：plus，add，increase，and(口语)，sum(两数的和)，addition(加法)

- 减：minus(也表示负号)，**subtract**，difference(两数的差)，subtraction(减法)
  
  - 5 subtracted from 3 = 3 - 5 = -2

- 乘：multiply，multiple(倍数)，times(口语)，product(两数的积)，multiplication(乘法)

- 除：**divide**，over(口语)，quotient(两数的商) = ratio of a to b，division(除法)
  
  - 一般用被动语态：A is divided by B
  
  - B divides A
  
  - 均表示A/B

【Example】If $ \left(x^{2}+6 x+9\right)+6(x+3)+9=0 $, then $ x= $

(A) -6
(B) -3
(C) 0
(D) 3
(E) 6

解析：可以直接利用完全平方公式，得到(x+6)^2 = 0。

【Example】If the sum of two positive integers is 24 and the difference of their squares is 48, what is the product of the two integers?
(A) 108
(B) 119
(C) 128
(D) 135
(E) 143

解析：利用平方差公式易得两个数分别是11和13，选E。

### 3.3 不等式

对已有的不等式两边取倒数或负数，不等号要改变方向。

对 $ \sqrt[4]{x}, \sqrt[3]{x}, \sqrt{x}, x, x^{2}, x^{3}, x^{4} $ 等函数的性质有一定的认识。
在 $ x, x^{2}, x^{3} $ 几个函数的比较大小中, 对 $ x $ 的取值范围要有清醒的分段意识：$ x<-1, \quad-1<x<0, \quad 0<x<1, \quad x>1 $
绝对值(absolute value)： $ |x| $ 恒非负

【Example】If $ X>0.9 $, which of the following could be the value of $ x $ ?
(A) $ \sqrt{0.81} $
(B) $ \sqrt{0.9} $
(C) $ (0.9)^{2} $
(D) $ (0.9)(0.99) $
(E) $ 1- \sqrt{0.01} $

解析：选B

【Example】If $ y+|y|=0 $, which of the following must be true?
(A) $ y>0 $
(B) $ y \geq 0 $
(C) $ y<0 $
(D) $ y \leq 0 $
(E) $ y=0 $

解析：这题是方框不定项选择，应该选择充分条件，即CDE均正确。

【Example】Which of the following inequalities has a solution set that, when graphed in the number line, is a single line segment of finite length?

(A) $ x^{4} \geq 16 $
(B) $ x^{3} \leq 27 $
(C) $ x^{2} \geq 16 $
(D) $ 2 \leq|x| \leq 5 $
(E) $ 2 \leq 3 x+4 \leq 6 $

解析：区间在数轴上表示为单个的线段，选择E。

### 3.4 数列

等差数列 (Arithmetic Sequence)

- 求和公式：$\frac{n\times(a_1+a_n)}{2}$

等比数列 (Geometric Sequence)

【Example】If the sum of 7 consecutive integers is 434 , then the greatest of the 7 integers is
(A) 62
(B) 65
(C) 67
(D) 69
(E) 71

解析：

- consecutive表示连续的，设最大的是x，则7x - 21 = 434。

- **另法**：434是中间数的7倍，因此中间数是62，从而最大的是65

【Example】In the sequence $ R_{n+1}-R_{n}=\frac{(-1)^{n}}{n} $, what is the relationship of $ R_{1}, R_{2} $, and $ R_{3} $ ?
(A) $ R_{1}<R_{2}<R_{3} $
(B) $ R_{1}<R_{3}<R_{2} $
(C) $ R_{2}<R_{1}<R_{3} $
(D) $ R_{2}<R_{3}<R_{1} $
(E) $ R_{3}<R_{1}<R_{2} $
解析：分别取n = 1, 2，得到两个关系式即可得到三者的大小关系，选D。

【Example】In a certain sequence, the first term is 1 , and each successive term is 1 more than the **reciprocal** of the term that immediately precedes it. What is the fifth term of the sequence?

(A) $ \frac{3}{5} $
(B) $ \frac{5}{8} $
(C) $ \frac{8}{5} $
(D) $ \frac{5}{3} $
(E) $ \frac{9}{2} $

解析：reciprocal表示倒数，因此数列为$a_{n+1} = 1+ 1/a_n$，根据这一关系递推下去即可，选C。

## 4. 初等几何

本节课教学大纲： 

• 三角形与四边形 

• 圆 

• 立体几何 

• 直角坐标系

### 4.1 三角形与四边形 (Triangles and Quadrilaterals)

三角形的某些性质：

- 三角形内角和为 $ 180^{\circ} $(n-2个180度)
- 三角形两边之和大于第三边, 两边之差小于第三边.
- 三角形中, 较大角的对边也较大.
- 勾股定理：$(\text { 直角边 } \mathrm{a})^{2}+(\text { 直角边 } \mathrm{b})^{2}=(\text { 斜边 } \mathrm{c})^{2} $

要对以下形状的直角三角形要特别熟悉：

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/2021/20211209103358.png)

- 5，12，13

- 7，24，25

三角形： 面积 = 底 × 高 / 2

矩形 (Rectangles) ： 面积(area) = 长 × 宽；周长(perimeter) = 2 × (长 + 宽)

正方形 (Squares) ： 面积 = 边长^2；周长 = 4 × 边长

术语：

- equilateral triangle 等边三角形

- isosceles triangle 等腰三角形

- quadrilateral  四边形
  
  - double triple quadruple
  
  - 菱形：diamond(口语)，rhombus(书面)
  
  - 梯形：trapezoid

- **pentagon 五边形**，五角大楼

- **hexagon 六边形**

- heptagon 七边形

- **octagon 八边形**

- nonagon 九边形

- decagon 十边形

- circumference特指圆形的周长

- regular 表示正.....形

- right angle 直角

- acute angle 锐角

- obtuse angle 钝角

- 直角三角形：短直角边arm，长直角边leg，斜边hypotenuse

- parallelogram 平行四边形

【Example】If each side of △ACD above has length 3 and if AB has length 1, what is the area of region BCDE ?

(A) $ \frac{9}{4} $
(B) $ \frac{7}{4} \sqrt{3} $
(C) $ \frac{9}{4} \sqrt{3} $
(D) $ \frac{7}{2} \sqrt{3} $
(E) $ 6+\sqrt{3} $

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/2021/20211209103647.png)

解析：等边三角形的面积 = $3 \times 3\sqrt{3}/2 \times 1/2$，小三角形的面积为$\sqrt{3}/2$，做差后选B。

【Example】A ladder 25 feet long is leaning against a wall that is perpendicular to level ground. The bottom of the ladder is 7 feet from the base of the wall. If the top of the ladder slips down 4 feet, how many feet will the bottom of the ladder slip?
(A) 4
(B) 5
(C) 8
(D) 9
(E) 15

解析：perpendicular表示垂直的，梯子底端距离墙7 feet，原来的三角形为25，24，7，新的三角形为25，20，15，因此15 - 7 = 8，选C。

### 4.2 圆 (Circles)

半径为r的圆：面积 = $\pi r^2$，周长 = $2 \pi r$

角度为 $ x^{\circ} $ 的圆弧: 弧长 $ =2 \pi r \frac{x}{360}$

角度为 $x^{\circ}$ 的扇形(sector)：面积 = $=\pi r^2 \frac{x}{360}$

定理：同一段圆弧所对圆心角是圆周角的两倍

术语：

- radius 半径

- diameter 直径

- minor arc 劣弧

- major arc 优弧

【Example】If the number of square units in the area of circle $ C $ is twice the number of linear units in the circumference of $ C $, what is the number of square units in the area?
(A) 4
(B) 8
(C) $ 4 \pi $
(D) $ 8 \pi $
(E) $ 16 \pi $

解析：题意为，圆C的面积是周长的两倍，求得半径为4，因此选E。

【Example】In the circle above, $ \mathrm{PQ} $ is parallel to diameter $ O R $, and $ O R $ has length 18 . What is the length of minor arc PQ?

(A) $ 2 \pi $
(B) $ \frac{9 \pi}{4} $
(C) $ \frac{7 \pi}{2} $
(D) $ \frac{9 \pi}{2} $
(E) $ 3 \pi $

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/2021/20211209112506.png)

解析：PQ对应的圆心角应该是(180 - 70 - 70 = 40)度，通过公式求对应的弧长即可，选A。

### 4.3 立体几何

- 长方体 (Rectangular Solids) : 体积 $ = $ 长 $ \times $ 宽 $ \times $ 高
  - 6个面(face)
  - 12条棱(edge)
  - 8个顶点(vertex, 复数vertices)
- 正方体 (Cubes) : 体积 $ = $ 边长 $ ^{3} $
- 圆柱 (Cylinders) ：体积 = π × 底面半径^2 × 高
  - cylindrical 圆柱体的
- 圆锥(cone)，圆锥形的conic
- 球(sphere)，球形的spherical

【Example】In a certain rectangular solid, the three sides shown have areas 12, 15, and 20, respectively. What is the volume of the solid?
(A) 60
(B) 120
(C) 450
(D) 1,800
(E) 3,600
解析：ab = 12, ba = 15, ac = 20, 求得abc = 60

【Example】A grocer is storing small cereal boxes in large cartons that measure 25 inches by 42 inches by 60 inches. If the measurement of each small cereal box is 7 inches by 6 inches by 5 inches, then what is the maximum number of small cereal boxes that can be placed in each large carton?
(A) 25
(B) 210
(C) 252
(D) 300
(E) 420

解析：大箱子最多可以放多少个小箱子

- 原则：尽量让可以整除的边对着放，可以保证利用率最大化

- 25对应5，42对应7，60对应6

- 可以放5 x 6 x 10共300个

### 4.4 直角坐标系

平面直角坐标几何 (Plane Rectangular Coordinate Geometry)

平面直角坐标上两点间距离为: $ \sqrt{\left(x_{1}-x_{2}\right)+\left(y_{1}-y_{2}\right)^{2}} $

斜截式: $ y=k x+b $

- 其中, $ k $ 为斜率 (Slope)

- b为y轴截距 (Intercept)

$$
k=\frac{y_{2}-y_{1}}{x_{2}-x_{1}}
$$

若两直线垂直, 其斜率乘积为 $ -1 $
术语：

- 对称(symmetric)

- 象限(quadrant)

【Example】In the rectangular coordinate system above, the line $ y=x $ is perpendicular **bisector** of segment $ A B $ (not shown), and the $ x $-axis is the perpendicular bisector of segment $ B C $ (not shown). If the coordinates of point $ A $ are $ (2,3) $, what are the coordinates of point $ C $ ?
(A) $ (-3,-2) $
(B) $ (-3,2) $
(C) $ (2,-3) $
(D) $ (3,-2) $
(E) $ (2,3) $

解析：perpendicular bisector表示垂直平分线，因此A与B关于y = x 对称，B与C关于x轴对称，因此选D。

【Example】In the rectangular coordinate system shown above, if the slope of line $ k $ (not shown) is positive, which of the following statements must be true?
$ \ni $ The $ x $-intercept of $ k $ is negative.
$ \ni $ The $ y $-intercept of $ k $ is positive.
$ \ni \quad \mathrm{k} $ intersects the quadrant $ \mathrm{I} $.
$ \ni \quad k $ intersects the quadrant II.
$ \ni \quad k $ intersects the quadrant III.
$ \ni \quad k $ intersects the quadrant IV.

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/2021/20211209160756.png)

解析：选CE。

【Example】In the rectangular coordinate system above, both of two tangent circles are tangent to the $ x- $ axis. If the radii of the two circles are 4 and 6, respectively, what is the slope of the line on which two centers lie?

(A) $ \frac{1}{2 \sqrt{6}} $
(B) $ \frac{1}{3 \sqrt{2}} $
(C) $ \frac{1}{3} $
(D) $ \frac{1}{\sqrt{5}} $
(E) $ \frac{1}{2} $

![](https://cdn.jsdelivr.net/gh/henrywu97/FigBed@master/2021/20211209160659.jpg)

解析：radii是radius的复数形式，选A。

## 5. 文字应用题

本节课教学大纲：
• 利息问题
• 几何问题
• 排列组合问题
• 概率问题
• 概述统计学

### 5.1 利息问题

单利 (Simple Interests)：$ A=P(I+nr) $

- $ A $ 为本利和, $ P $ 为本金, $ r $ 为利率, $ n $ 为期数.

【练习】Mary invested \$ 14,000  for 3 years in a certificate of deposit paying $ 9.25 \% $ simple annual interest. How many more interest would Mary have received if the interest rate on this certificate had been $ 9.75 \% $ simple annual interest?
(A) \$ 21
(B) \$ 210
(C) \$ 420
(D) \$ 2,100
(E) \$ 4,200

解析：deposit表示存款，certificate of deposit表示存折，多出来的利息为14,000 x (9.75% - 9.25%) x 3 = 210, 选B。

复利 (Compound Interests)：$ A=P(1+r)^{n} $

- $ A $ 为本利和, $ P $ 为本金, $ r $ 为利率, $ n $ 为期数.

付息频率：annually 每年地，semiannually 半年地，monthly 按月地

- 注意付息频率越高，利息越多

【练习】A 2 -year certificate of deposit is purchased for $ k $ dollars. If the certificate earns interest at an annual rate of 6 percent compounded **quarterly**, which of the following represents the value, in dollars, of the certificate at the end of the 2 years?
(A) $ (1.06)^{2} \mathrm{k} $
(B) $ (1.06)^{8} \mathrm{k} $
(C) $ (1.015)^{2} \mathrm{k} $
(D) $ (1.015)^{8} \mathrm{k} $
(E) $ (1.03)^{4} \mathrm{k} $
解析：注意是按照季度进行复利，因此选D。

### 5.2 集合问题

术语：set 集合，intersection 交集，union 并集

【练习】According to a survey, 93 percent of teenagers have used a computer to play games, 89 percent have used a computer to write reports, and 5 percent have not used a computer for either of these purposes. What percent of the teenagers in the survey have used a computer both to play games and to write reports?
(A) $ 82 \% $
(B) $ 87 \% $
(C) $ 89 \% $
(D) $ 92 \% $
(E) $ 95 \% $

解析：画出韦恩图有助于解题，93% + 89% - x + 5% = 1，x = 87%，选B。

【练习】A shipment of banners contains banners of two different shapes, triangular and square, and two different colors, red and green. In a particular shipment $ 26 \% $ of the banners are square and $ 35 \% $ of the banners are red. If $ 60 \% $ of the red banners in the shipment are square, what is the ratio of red triangular banners to green triangular banners?
(A) $ \frac{7}{50} $
(B) $ \frac{3}{13} $
(C) $ \frac{7}{30} $

(D) $ \frac{13}{37} $
(E) $ \frac{35}{26} $
解析：banners表示旗帜，根据下面的表格选C。

|       | triangular | square | Sum  |
| ----- | ---------- | ------ | ---- |
| red   | 14%        | 21%    | 35%  |
| green | 60%        | 5%     | 65%  |
| Sum   | 74%        | 26%    | 100% |

验算，四空之和为100%。

### 5.3 排列组合问题

组合 (Combination):

- $ C_{m}^{n}=\frac{m !}{n !(m-n) !} $

- $ C_{m}^{n}=C_{m}^{m-n} $

排列 (Permutation) :

- $ P_{n}^{n}=n ! $

- $ P_{m}^{n}=C_{m}^{n} \cdot P_{n}^{n}=\frac{m !}{(m-n) !} $

- $ P_{m}^{1}=C_{m}^{1}=m $

术语：factorial 阶乘

【练习】In a meeting of 3 representatives from each of 6 different companies, each person shook hands with every person not from his or her own company. If the representatives did not shake hands with people from their own company, how many handshakes took place?
(A) 45
(B) 135
(C) 144
(D) 270
(E) 288
解析：选B

- 思路1：每个人要握手15次，共18个人，共握手15 x 18 / 2 = 135

- 思路2：$ C_{6}^{2} \cdot C_{3}^{1} \cdot C_{3}^{1} $

- 思路3：$ C_{18}^{2} - C_{3}^{2} \cdot C_{6}^{1} $

【练习】If a code word is defined to be a sequence of different letters chosen from the 10 letters $ A, B $, $ \mathrm{C}, \mathrm{D}, \mathrm{E}, \mathrm{F}, \mathrm{G}, \mathrm{H}, \mathrm{l} $, and J, what is the ratio of the number of 5 -letter code words to the number of 4 letter code words?
(A) 5 to 4

(B) 3 to 2

(C) 2 to 1

(D) 5 to 1

(E) 6 to 1

解析：选E

$$
\frac{A_{10}^{5}}{A_{10}^{4}}=\frac{10 \times 9 \times 8\times7 \times 6}{10 \times 9 \times 8 \times 7}
$$

### 5.4 概率问题

【练习】Six cards numbered from 1 to 6 are placed in an empty bowl. First one card is drawn and then put back into the bowl; then a second card is drawn. If the cards are drawn at random and if the sum of the numbers on the cards is 8, what is the probability that one of the two cards drawn is numbered 5 ?
(A) $ \frac{1}{6} $
(B) $ \frac{1}{5} $
(C) $ \frac{1}{3} $
(D) $ \frac{2}{5} $
(E) $ \frac{2}{3} $

解析：和为8，有2+6，6+2，4+4，3+5，5+3共计5种，其中有两种包含5，因此选D。

【练习】If a certain coin is flipped, the probability that the coin will land heads is $ 1 / 2 $. If the coin is flipped 5 times, what is the probability that it will land heads up on the first 3 flips and not on the last 2 flips?
(A) $ 3 / 5 $
(B) $ \mathrm{I} / 2 $
(C) $ 1 / 5 $
(D) $ 1 / 8 $
(E) $ 1 / 32 $

解析：选E。

### 5.5 描述统计学

- 算术平均数 (Average or Arithmetic Mean): 所有数据之和除以数据个数.
- 中数 (Median)：将所有数据从小到大排列, 取中间的数或中间两个数的算术平均数.
- 众数 (Mode)：一组数据中出现频率最高的数. 一组数据中可能有不止一个众数.
- 极差 (**Range**)：一组数据中最大数与最小数之差.

【练习】The least and greatest numbers in a list of 7 real numbers are 2 and 20, respectively. The median of the list is 6 , and the number 3 occurs most often in the list. Which of the following could be the average of the numbers in the list?
  (A) 7
  (B) $ 8.5 $
  (C) 10
  (D) 11
  (E) $ 12.5 $

解析：数列为2，3，3，6，，，20，空出来的两个数最小取6（接近但不能等于6），此时均值为46/7，最大取20，此时均值为74/7，选ABC。

注意the number 3 occurs most often in the list比3是众数（可能不唯一）更加严格。

四分位数：

- 四分位数 (Quartile): 将所有数据从小到大排列, 排名 $ 25 \%, 50 \%, 75 \% $的数（不严谨）

- 四分位距 (**Interquartile Range**): 第三四分位数与第一四分位数之差.

【练习】Find the three quartiles and interquartile range of the following numbers.
(1) $ 11,13,15,17,19,21,23,25 $.
(2) $ 11,13,15,17,19,21,23,25,27 . $

解析：**先找中位数，再找中位数的中位数即四分位数**（这一步把中位数排除）。

(1) 中位数是18，第一四分位数是14，第二四分位数是22，四分位距为8

(2) 中位数是19，第一四分位数是14，第二四分位数是24，四分位距是10

- 方差 (Variance)：一组数据中每个数与算术平均数之差的平方和的算术平均数.

- 标准方差 (Standard Deviation)：方差的平方根.

【练习】The standard deviation of four numbers $ a, b, c $, and $ d $ is M, then the standard deviation of which of the following MUST be M?
(A) $ \sqrt{a^{2}}, \sqrt{b^{2}}, \sqrt{c^{2}}, \sqrt{d^{2}} $
(B) $ a^{2}, b^{2}, c^{2}, d^{2} $
(C) $ 2 a, 2 b, 2 c, 2 d $
(D)a+2, b+2, c+2, d+2
(E)a+2, b-2, c+2, d-2

解析：同时加上一个常数，标准差不变。

【练习】

| Test      | Steven's Score | Mean Score | Standard Deviation |
| --------- | -------------- | ---------- | ------------------ |
| Math      | 80             | 88         | 4                  |
| Biology   | 90             | 84         | 2                  |
| Physics   | 96             | 86         | 5                  |
| History   | 89             | 81         | 4                  |
| Chemistry | 88             | 85         | 3                  |

The chart above shows data for five tests that Steven took. On which of the five tests did she score highest relative to the rest of the test takers?
(A) math
(B) biology
(C) physics
(D) history
(E) chemistry

解析：计算与平均数相差的标准方差数，选B。

正态分布 (Normal Distribution)

- 已知：
  ✓平均数
  ✓标准方差
- 记住：
  ✓平均数正负一个标准方差之间——68%
  ✓平均数正负两一个标准方差之间——96%

【练习】Suppose the weights of a population of 1,000 apples from a certain district are approximately normally distributed with a mean of 9 ounces and a standard deviation of 1.5 ounces. Approximately how many of the apples are between 7.5 ounces and 12 ounces weight?

解析：平均数-1个到2个标准差之间，根据以上的结论占总体的82%，大约820个。

## 6. 比较大小题型

【题目形式】Compare Quantity A and Quantity B, using additional information centered above the two quantities if such information is given. Select one of the following four answer choices.

- Quantity A is greater.

- Quantity B is greater.

- The two quantities are equal.

- The relationship cannot be determined from the information given.

【练习】

The number of minutes in 24 hours；The number of seconds in 24 minutes
解析：都等于60x24，相等

Twice as much as 4; 2 subtracted from 10

解析：都等于8

The value of the units digit in 7^52 ；The value of the units digit in 6^52

解析：1 < 6

P is a positive integer.
The remainder when 3p + 5 is divided by 3；The remainder when 7p + 8 is divided by 7

解析：**remainder表示余数**，2>1

The median of 10, 15, x and y is 18.5, and x < y.
x; 22

解析：15和x的平均数为18.5，因此x = 22

The number of integers between 15 and 51 that are square of integers；
The number of integers between 6 and 126 that are cube of integers

解析：16，25，36，49共四个；8，27，64，125，共四个；相等。

1<n<5, n is an integer
The sum of the first n odd integers that are greater than zero；n^2 −1

解析：分类讨论，n = 2时，1+3>3；n = 3时，1+3+5>8；n = 4时，1+3+5+7>15，因此左大右小。

总结：前n个正奇数的和一定等于n的平方。

The number of ¼-inch lengths in a 4-inch length; 1

解析：16>1

Two successive discounts of 20 percent and 40 percent are equivalent to a single discount of x percent.
x; 52

解析：1- x% = 0.8 x 0.6，得到x = 52。

Ms. Smith got an 8 percent cost-of-living raise of \$20 per week. Ms. Smith’s new weekly salary; \$260

解析：注意8%对应的就是20元，因此新的周薪为(20/0.08+20) = 270元>260.
