# JAVASE

基础语法	basic

面向对象	oop

高级语法	advanced



## 专业术语



class		 班级；类

static        静态
variable	变量



Java体系三个领域

JavaSE     标准基础开发

JavaME	用于手机（非智能手机的java应用）

JavaEE     企业级开发



## 基础语法

### 初识java 

  1.环境变量: 
	<1>作用：任何路径下可以执行命令 java 和javac
			path

​			C:\Program Files\Java\jdk1.8.0_101\bin

  *****2.程序
		**一组有序的指令集合**

  3.Java之父
		詹姆斯·高斯林（之前就职sun, 由于sun被Oracle收购， 目前就职Oracle）



### JDK  JRE   JVM区别

JDK      **java开发工具包**
JRE       **java运行环境**
JVM     **Java虚拟机**			一次编译（.class），到处运行

###### **JDK包含JRE,  JRE包含JVM**



  4.记事本写程序步骤：
	①**编写** 
	②**编译**	 javac Hello.java
	③**运行** 	 java  Hello



  5.基本结构和规范
     1>纯英文编程;
     2>括号成对出现
     3>单独一行并缩进
     4>大小写区分	如：Hello String System 

  6.JVM和JRE区别
	①JRE java运行环境 包含了jvm以及lib
  	②JVM java虚拟机 *.class 一次编写 到处运行



### IDE

​	集成开发环境

​	 Integrated Development Environment 

  7.eclipse写程序步骤：
	①创建 
	②编写	 
	③编译 
	④运行



快捷键
	ALT+/ 		提示
    CTRl+F11或者 F11



输出语句快捷键使用方法：

System.out.print();

####    **syso+ALT+/**          



控制台打印以下内容：（注意对齐）

	姓名		 年龄		工资
	沈腾		 36		  12000
	刘德华		50		 20000



  8.转义字符
	①\n换行符
	②\t制表符（缩进）



  9.注释 
	作用：
		①说明描述 
		②代码作废
		③整理思路


	单行注释  //		
	段落注释 /*注释内容*/	



	单行加注释:ctrl+/  		取消注释:ctrl+/
	多行加注释:ctrl+shift+/  	取消注释:ctrl+shift+\
	
	代码提示：alt+/
	删除一行： ctr+d
	移动行：  alt+方向键



### 数据类型

  1.变量
	如容器
	三要素
		变量类型
		变量名
		变量值

 2.变量三步骤：

​	①声明 
​	②赋值 (初始化)
​	③使用
​	结论：必须赋值再使用



  3.变量取名规范
     1>只能出现字母 数字 下划线 $，首字母不能是数字
	 2>变量名不能用关键字





   数据类型
	基本数据类型	四类八种
	引用数据类型	<u>String</u>

  4.基本数据类型：四类八种
	布尔型1个		<u>boolean</u> 1字节 	正确true或错误false 
	字符型1个 		<u>char</u>	2字节
	浮点型2个
		单精度浮点型	<u>float</u>	4字节
		双精度浮点型	<u>double</u>	8字节
	整型4个
		字节		<u>byte</u>	1字节
		短整型		<u>short</u>	2字节
		整型		<u>int</u>	4字节
		长整型		<u>long</u>	8字节

	0 1
	10101010
	1个字节=8个位  1个字符=2个字节
	1个byte=8个bit	1byte范围：-128~127  
	char=2byte=-32768~32767整数范围（无符号为正数0~65535 char范围）
	
	1个字母：占1byte
	1个汉字：占2byte


     容量大小比较	
    boolean 1byte
    byte	1byte
    
    char	2byte
    short	2byte
    
    int	4byte
    float	4byte
    
    long	8byte
    double	8byte 





  5.*****ASCII*	
		**美国信息交换标准代码**
		**主要把数字和英语大小写字母，规定了的编码规则，二进制数来表示**
			**0-9	48～57**
			**A-Z	65～90**	
			**a-z	97～122**

​	**A与a之间有32，第32个ascll码为空格；**

```
char c0='0',c00=48;
char c1='A',c01=65;
char c2='a',c02=97;
```

```
 System.out.println((int)c0+"\t"+(int)c1+"\t"+(int)c2);
 System.out.println((char)c00+"\t"+(char)c01+"\t"+(char)c02);
 System.out.println((char)(65));
```

![image-20210302135800347](C:\Users\ASUS\AppData\Roaming\Typora\typora-user-images\image-20210302135800347.png)



 6.数据类型转换	
		①小转大自动
		②大转小强制 有数据丢失



  7.Scanner类 
		扫描类
		阻塞式输入类

		import java.util.Scanner;
		Scanner input = new Scanner(System.in);
		System.out.print("请输入一个数字：");
		int num = input.nextInt();

```
  input.next();  //空格结束
  input.nextLine(); //回车结束
```

​		



### 运算符

  6.运算符：
	赋值运算符 	
			**=**
			①右边赋值给左边
			②覆盖原有的值	  

​	算术运算符	

​		*** / +  -**
​		原则：先乘除后加减
​		整除	**/**	结果只取整数部分

​           整数/整数=整数        浮点数/浮点数（整数）=浮点数  

```
可以强制转换   System.out.println(5/2)    =2
             System.out.println((double)5/2)   =2.5
```

​			取余数	**%**

```
可以强制转换   System.out.println((double)5%2)    =1
```



关系运算符 
		比较的意思：
		关系运算符两边必须是数值类型，最终结果是布尔型

​			>  <  >= <= == !=

​	逻辑运算符
​		短路与*  

​			**&&  	并且的意思** 
​			短路与两边都是布尔型，最终结果还是布尔型
​			两边都是true结果才是true,有一个是false则结果为false
​			效率高	
​				结论：左边是假，右边不执行
​	
​		短路或*	
​			**||       或者的意思**
​			短路或两边都是布尔型，最终结果还是布尔型
​			两边有一个是true结果就是true
​			效率高
​				结论：左边是真，右边不执行
​	
​		逻辑非	
​			!true	结果是反面布尔值
​	
​	优先级
​		算术运算符>关系运算符>逻辑运算符>三元运算符>赋值运算符


  7. i++
	
	#### **int a =i++; *先赋值再自加**
	
	**int a =++i; *先自加再赋值**

  8.**+=**
	sum =  sum+ x;
	sum+=x; 同上结果效果



 9.*三元运算 
		双支的简化写法：  符号  ?  :  

	        问号左边放布尔型，冒号左右放任何类型，左边是true结果值
						      右边是false结果值
			String res= c>a? true:false;
	        System.out.println(res);

#### 优先级

##### 		算术运算符>关系运算符>逻辑运算符>三元运算符>赋值运算符



  10.常量
		不变的值可以用常量 
		关键字	**final**

     1>取名全部大写
     2>多个单词之间用下划线
     3>只能被赋值一次
     4>需要final修饰
    
     final double PI_NUM;
     PI_NUM=3.1415926;
     System.out.print(PI_NUM);






### 判断语句

1.选择 if
	①单支
		if(){} 
		小括号里只能是布尔值或布尔型的表达式

	②双支 
		if(){} else{}
		小括号里只能是布尔值或布尔型的表达式
	③多支
		if(){}
		else if(){}
		else{}
		小括号里只能是布尔值或布尔型的表达式
		
		删除大括号的话，只能执行下一行的代码。





#### switch-case 等级

switch 开关,转换

  举例  cj

​	[90,100]  A	

​	[80,90)	B

​	[70,80)	C

​	[0,70)	D

```
switch(cj/10) {
		    case 10:
		    case 9:
		    	System.out.println("A");
		    	break;
		    case 8:
		    	System.out.println("B");
		    	break;
		    case 7:
		    	System.out.println("C");
		    	break;
		    default:
		    	System.out.println("D");
		    	break;
	    }
```

```
结论  
      1.每个case后面都要加break;
      2.一般用char,int,short;			jdk1.7后支持String
    switch-case比if效率高
```




### 循环语句

1.循环:	不停的做同一件事

2.**while**循环			先判断后执行
	基本结构:
		while(){	小括号里只能布尔型或表达式
		}


	组成
		①循环变量	int i = 1;
		②循环条件	 
		③循环操作	 
		④重新赋值	改变i的值 
	执行原理:
		①
		while(②){
			③
			④
		}
	执行顺序：->①->②(true)->③->④->②(true)->③->④->.....->②(false)--结束
  	·


	特点：先判断再执行



3.**do-while**循环  
	基本结构
		do{
		}while();

	组成
		①循环变量	int i = 1;
		②循环条件	
		③循环操作	
		④重新赋值	改变i的值
	原理	
		①
		do{
			③
			④
		}while(②);
	
	执行顺序：->①->③->④->②(true)->③->④->②(true)->③->④->②(true)...->②(fales)->结束
  	特点：先执行一次再判断; 至少执行一次；



4.**for**
	基本结构		先判断后执行
		for(;;){
		}

	组成
		①循环变量	int i = 1;
		②循环条件	
		③循环操作	
		④重新赋值	改变i的值
	原理
		for(①;②;④){
			③
		}
	
	执行顺序：->①->②(true)->③->④->②(true)->③->④->.....->②(false)--结束

​	

#### **String.format 占位符+数据填充 %d数字占位 %s字符串占位**

```
	/* 九九乘法表 */
	for(int i=1;i<=9;i++) {
		System.out.println("");
		for(int j=1;j<=i;j++) {
			if(j*i<10) {
				//String.format 占位符+数据填充 %d数字占位 %s字符串占位
				System.out.print(String.format("%d*%d=0%d\t", i,j,i*j));
//				System.out.print(j+"*"+i+"="+"0"+j*i+" ");
			}else {
				System.out.print(String.format("%d*%d=%d\t", i,j,i*j));
//				System.out.print(j+"*"+i+"="+j*i+" ");
			}
		}
	}
```

**return**;返回





5.**break**;   打破
	break只能用switch-case和循环里 ,跳出循环/杀死循环
	跳出循环
	位置在执行语句前后都可

6.**continue**; 继续
	continue只能用在循环里,杀死某次循环	
	跳过本次循环
	位置在执行语句前面



7.循环方案建议：
	次数确定用for；
	次数不确定while或do-while (和Scanner结合)



8.instanceof：
	判断是否包含

```
if (teacher instanceof ISing) {
			((ISing) teacher).showSing();
		}
```

​	

## 调试 Debug

	操作
		先打断点，再调试运行
		
	F8	跳到下一个断点
	F6	单步操作	  粗粒度
	F5	单步跳入方法  细粒度
	
	作用
		①找逻辑错误 
		②快速熟悉他人代码



	【编程题】
		while- Scanner实现一个菜单跳转的功能。
		内容和动作如下：
	
	  	 1.查看
	 	 2.新增
	 	 3.修改
	 	 4.删除
	 	 5.退出
	
	 请选择菜单编号：



## 本周课后作业

```
1.键盘指法练习、盲打，速度要求达到120个字母/分

2.打印1000以内的水仙花。 所谓水仙花数就是一个三位数,它各位的立方之和加起来的数值等于本身,比如说,153,153 = 1 + 125 + 27。

3.打印1000以内的质数




```


​	



 

​	

 
