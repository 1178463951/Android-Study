#简单计算器（Android）<br>

***

##功能及页面介绍
* **简单计算器**：实现了两位数字间的加减乘除运算以及删除和清除功能<br>
* **程序页面**：在模拟器上的运行页面如下<br>


 
 ![](/imgs/wanjian_Work1_Counter.png)<br>



##内容介绍<br>
* **该计算器主要由主函数MainActivity.java和布局文件activity_main.xml文件构成**<br>
* **布局文件activity_main.xml文件**:  主布局为LinearLayout；显示框的布局为Linearlayout，上下两个textView；键盘区的总布局为LinearLayout，左侧为tablelayout，右侧为LinearLayout；注意使用weight属性控制控件大小比例<br>
* **主函数MainActivity.java文件**: 先定义和实例化所有的buttton以及实例化显示框，再使用setOnClickListener设置按钮的点击事件，最后构建运算的逻辑部分（具体见代码注释）。

##遇到的一些坑···
* **删除问题：**之前在没有输入的情况下点击删除按钮，程序会崩溃自动退出，原因是当显示框为空时，传入的str为空，删除一个使str.length为-1，造成数组越界，使用try···catch捕获异常即可；
* **疏忽问题：**之前碰到了使用除号时结果全为int型，之后检查才发现原来是`除号`在主函数和布局文件中打的不一样···小心一点符号和字母大小写千万别打错了···
* **空格问题（未解决）：**主函数中是使用检测空格来捕获运算符的，但是会导致删除的时候要删除一个数字要删除两个空格，而且删除了一个空格后再按一个数字，运算就不能进行了。。。虽然我用了contain（）函数来使检测到了有运算符就删除三个但是不知道为什么运行起来没有效果···
* **其他问题：**同时有两个运算符会出问题；其他更多的功能还有待实现；

##收获
* 总的来说还是比较有成就感的~虽然很简单但是毕竟是自己动手写的第一个计算器app；
* 在写项目的过程中更加清楚的了解和运用LinearLayout布局和tableLayout布局以及textView控件和button控件，主函数计算器的逻辑部分让自己对函数的了解更多了；
* **多写才能学到更多，多问才能减少踩到更多的坑···另外这个项目确实很适合新手练手可以尝试一下**
