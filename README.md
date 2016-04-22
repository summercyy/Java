# Java

阅读JDK文档及源代码并简要回答以下问题。
注：JDKAPI文档（http://docs.oracle.com/javase/8/docs/api/index.html或从http://cf.pku.cn/tds/java下载chm格式的）
 JDK的源代码（一般在 C:\Program Files\Java\jdk1.8.0\src.zip）中

-----java.lang.Object类-----
1.	其equals与==有没有差别？
2.	其hashCode及clone前面有个什么修饰语？
3.	其toString()返回什么？
4.	其构造函数及finalize()做了什么？

-----java.lang.Class类-----
5.	为什么说Class类不能被继承？
6.	为什么说我们不能 new Class()?
7.	forName()中执行了什么流程？
8.	toString()返回什么？
9.	newInstance()中执行了什么？


-----java.lang.String类-----
10.	为什么说String是immutable的？为什么不要多次循环中使用+=？ 其value是加了哪个修饰语？其replace、append、trim等方法返回的值是什么？
11.	hashCode使用了什么公式，试比较一下它与身份证验证码、ISBN（国际标准书号）、银行卡号的验证码的生成算法有何不同？
12.	equals方法是判断内容相等还是引用相等？compareTo是比较什么？
13.	intern()方法的注释表明什么样的字符串一定是放到一个池子中的？
14.	其indexOf使用了什么样的算法流程？
15.	substring函数会抛出什么样的异常，这个异常是不是一定要捕获？
16.	concat函数使用了哪个类的什么方法，这个方法中最终又是调用了什么类的什么方法？
17.	replaceAll中借用了什么类来实现？valueOf及format呢？

-----java.lang.StringBuilder 及 AbstractStringBuilder类-----
18.	StringBuilder的初始内存是多少字符？
19.	expandCapacity()方法是在原来的基础上扩展多少？
20.	insert()、append()、delete()等方法的返回值是什么，这有什么好处？


-----java.lang.Integer类-----
21.	value字段前面加了什么修饰词？为什么说Integer是immutable的？
22.	其常数如MAX_VALUE前面用了什么修饰词？
23.	toString(int i)用了什么办法加快其计算的速度？
24.	parseInt函数会抛出什么样的异常，这个异常是不是一定要捕获？
25.	IntegerCache是起什么作用的？valueOf(int i)表明什么范围内的int在boxing后会缓存？
26.	hashCode是怎样算的？

-----java.lang.Math类-----
27.	举几个方法是native的方法。

-----java.util.Random类-----
28.	构造函数用什么进行了初始化？
29.	随机数的公式是用了什么?

-----java.math.BigInteger类-----
30.	判断一个大数是否可能为素数，有两个passXXX函数，分别是什么？
31.	内部是用什么来表示大整数的
-----java.util.Arrays类-----
32.	sort(int[])是使用什么排序方法？
33.	sort(Object[] a)是使用什么排序方法？
-----java.util.ArrayList类-----
34.	grow()的代码中可以看出每次容量增加多少倍？
-----java.util.Vector类-----
35.	grow()的代码中可以看出每次容量增加多少倍？
-----java.util.Stack类-----
36.	Stack类继承了什么类？
37.	push()与pop()进行了什么操作？
-----java.util.Hashtable类-----
38.	其内部类class Entry含有哪4个字段？
-----java.util.TreeMap类-----
39.	containsKey()的代码中可以看出要找到对象的条件是什么？如果一个Key对象的hashCode是变化的（如随着内容而算出来的），这个Key对象还会找到吗？
-----java.util.TreeSet类-----
40.	TreeSet的底层是用什么对象来实现的？
-----java.util.Timer类-----
41.	Timer的底层是如何实现重复执行的？
-----javax.swing.Timer类-----
42.	Timer的底层是在哪里调用SwingUtilities.invokeLater的？

