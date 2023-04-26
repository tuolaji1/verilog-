# verilog-
运算符：and(&) or(|) xor(^) not(~)  
--
and:用于计算两个数字的按位与。当两个数字的同一位都是1时，运算的结果该位为1，否则为0.  
or：用于计算两个数字的按位或。当两个数字的同一位都是0时，运算的结果该位为0，否则为1.  
xor：用于计算两个数字的按位异或。当两个数字同一位不同时，运算的结果该位为1，否则为0.  
not：用于对单个数字进行按位取反。该运算符将数字的每一位都取反，即0变成1，1变成0. 

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



