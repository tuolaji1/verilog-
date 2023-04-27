# verilog-
运算符：and(&) or(|) xor(^) not(~)  
--
 

第三章
==

3.1端口  
--  
1.模块： module 模块名(口1，口2)  

2.端口：输入端input 输出端output 输入输出端inout  

3.功能定义：(1)assign (2)用实例元件（3）always  

3.2数据
--
3.2.1常量  
1.数字 

（1）整数  
二进制（b或B） 十进制（d或D） 十六进制（h或H） 八进制（o或O）  
<位宽><进制><数字> eg：8'b10101100  //位宽为8的数用二进制表示 

（2）x值：不定值 z值：高阻值  4'b10x0  //低位起第二位为不定数  

（3）负数： 在位宽前加- eg：-8'd5  

（4）下划线：只能用于数字之间，不可以在位宽和进制处使用，用于分隔开数  eg：16'b1010_1111_1010  
2.参数（parameter）型  
parameter msb=7;  
parameter e=25,f=29;  
只能包括数字或先前已定义过的参数 parameter average_delay=(r+f)/2  

3.3.2变量  
1.wire型  
2.reg型 默认初始值是不确定数x  
3.memoty型（较前两个复杂） 

3.3运算符
--
1.各类运算符  
图片![]https://github.com/lulalalulalalulalulahe/verilog-/blob/main/%E8%BF%90%E7%AE%97%E7%AC%A6.jpg  
取余%的结果与第一个操作数的符号位一致  
eg：-10%3 = -1    11%-3 = 2  
算数运算时有一个操作数是不确定x，则结果也为不确定X  
2.位运算符  
and &:用于计算两个数字的按位与。当两个数字的同一位都是1时，运算的结果该位为1，否则为0.  

or |：用于计算两个数字的按位或。当两个数字的同一位都是0时，运算的结果该位为0，否则为1.  

not ~：用于对单个数字进行按位取反。该运算符将数字的每一位都取反，即0变成1，1变成0.  

xor ^：用于计算两个数字的按位异或。当两个数字同一位不同时，运算的结果该位为1，否则为0.  

同或 ^~: 先异或再非  
图表见书p51


第四章
==
4.1逻辑运算符
--
（1）&& 逻辑与 （2）|| 逻辑或 （3）！逻辑非  
（1）（2）是双目运算符，需要两个操作数 eg：（a>b）&&（b>c）  而（3）是单目运算符，只需要一个操作数 eg:!(a>b)  
&&和||的优先级低于关系运算符，！高于算术运算符  

4.2关系运算符
--
< > <= >=  
关系是假则返回值为0，真的为1 操作数的值不定，返回值是不定值  
关系运算符的优先级低于算数运算符  

4.3等式运算符
--
== != === !==  
等式真值图p55  

4.4移位运算符
--
a<<n a>>n  
a表示要进行移位的操作数，n表示要移几位  
 eg: 4'b1001<<1 = 5'b10010   4'b1001>>1 = 4'b0100
  
4.5位拼接运算符
--
{}  
 
4.6缩减运算符
--
对一个操作数进行运算：首先先将操作数的第一位与第二位进行或、与、非运算；再将结果与第三位进行或、与、非运算，依次类推，直到最后一位  
 
4.7优先级表格
--
见书p57  
 
4.8关键词
--                
