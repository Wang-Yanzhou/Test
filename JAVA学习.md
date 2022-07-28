#  JAVA
## 开发细节
![image-20220630172344328](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220630172344328.png)
## Java组织形式

![image-20220630173857207](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220630173857207.png)

# CMD命令                                              
![2022-06-22 (7)](C:\Users\WangYanzhou\OneDrive\图片\屏幕快照\2022-06-22 (7).png)
# IDEA
## 快捷键
![image-20220628160409394](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220628160409394.png)

![image-20220711091120931](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220711091120931.png)

![image-20220711093738544](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220711093738544.png)

图3 .

1.  Ctrl + H 社区版没有
2.  第10点直接 Ctrl 加左键定位
3.  第11点 用 Alt+ Enter 也可以

## 模板快捷键

![image-20220711095724215](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220711095724215.png)



**模板查询**：

![image-20220711095429615](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220711095429615.png)


## 项目结构
![image-20220628160750751](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220628160750751.png)

1. 包的本质就是创建不同的文件夹来保存类文件
## 注释
```
1.  // 单行注释
2.  /* */多行注释
3.  /** */ 文档注释
```
# 堆，栈，方法区，常量池

![img](https://img2018.cnblogs.com/blog/1460902/201902/1460902-20190213164222485-2067634141.png)

内存区域类型

1. 寄存器：最快的存储区, 由编译器根据需求进行分配,我们在程序中无法控制；

2. 堆：存放所有new出来的对象；

3. 栈：存放基本类型的变量数据和对象的引用，但对象本身不存放在栈中，而是存放在堆（new 出来的对象）或者常量池中(对象可能在常量池里)（字符串常量对象存放在常量池中。）；

4. 静态域：存放静态成员（static定义的）；

5. 常量池：存放字符串常量和基本类型常量（public static final）。有时，在嵌入式系统中，常量本身会和其他部分分割离开(由于版权等其他原因)，所以在这种情况下，可以选择将其放在ROM中 ；

6. 非RAM存储：硬盘等永久存储空间

# 进制转化
```c
二进制转八进制 例 97：01100001  拆分：01 100 001=》从后往前三个一组按二进制读141
二进制转十六进制 例 97：10110001 拆分：0110 0001=》从后往前四个一组按二进制读出61 
二进制 ，八进制  ，十六进制的数据以0B，0，0X或X0可大写也可小写
二进制 逢二进一  除二取余法
```
```c
由n进制转十进制：从最低位欸开始（及0位），将每个位上的数提取出来，乘以n的位数次方后求和
```
```c
由十进制转n进制：将该数不断除以n，直到商为零将每步的余数倒过来为对应的n进制
除n取余法
```
```c
八进制转二进制：将八进制的每一位数，转成对应一个3位的二进制数
十六进制转二进制：将十六进制的每一位数，转成对应一个4位的二进制数
```
# 数据类型

![image-20220630094734048](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220630094734048.png)


## 引用数据类型


类，接口，数组 ，String

1、**boolean**：数据值只有true或false，适用于逻辑计算。
2、**char**：char型（字符型）数据在内存中占用2个字节。char型数据用来表示通常意义上的字符，每个字符占2个字节，Java字符采用Unicode编码，它的前128字节编码与ASCII兼容字符的存储范围在\u0000~\uFFFF，在定义字符型的数据时候要注意加' '，比如 '1'表示字符'1'而不是数值1， 
3、**byte**：byte型（字节型）数据在内存中占用1个字节，表示的存储数据范围为：-128~127。
4、**short**：short型（短整型）数据在内存中占用2个字节。
5、**int**：int型（整型）数据在内存中占用4个字节。
6、**long**：long型（长整型）数据在内存中占用8个字节。
7、**float**：float型（单精度浮点型）数据在内存中占用4个字节。（float精度为7-8位）
8、**double**：double型（双精度浮点型）数据在内存中占用8个字节。

**除了上述八种基础数据类型，其他都是引用类型**



# 类型转化

## 自动类型转化  

由有范围小的可直接赋给范围大的变量

![image-20220630100539924](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220630100539924.png)



## 表达式中的自动类型提升

1. 表达式的最终结果有表达类型的最高类型决定
2. **在表达式中 byte , short , char , 是直接转换成int类型进行运算**

3. char 在内存中储存的就是整数，对应的 ASCII 表，例：char c1='A'；等效于 char c1= 65；

## 强制类型转化



大范围赋给小范围的



![image-20220630102737425](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220630102737425.png)

强制类型转化可能导致数据的（丢失）溢出

强制类型转换只对最近的操作数有作用

Boolean 无法强转

![image-20220630105509072](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220630105509072.png)



# 运算符



## ++说明

```java
1.  ++:作为独立语句使用前++和后++是一样的; 
    a++；//a=a+1；

2.  int c=2;
    int d=++c;//前++为先自增后赋值  等价于 c=c-1; d=c;
    int d=c++;//后++为先赋值后自增  等价于 d=c; c=c+1;
```



## 逻辑运算符

```
&&和&  &&更高效 // &&在判断第一个为假后，不再判断，直接判为假
||和|  ||更高效 // ||在判断第一个为真后，不再判断，直接判为真
a^b只有在a和b不相同的时候为true 
```

![image-20220703170101098](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220703170101098.png)

![image-20220703170120111](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220703170120111.png)



## 赋值运算符

```c
a+=b;等价a=a+b;
a-=b;等价a=a-b;
复合赋值运算符如：++，--，-=，+=
会进行类型转化
```


## 三元运算符

```c
三元运算符  =___？___:___; 
//若条件为ture运行表达式1;若条件为false运行表达式2
```


## 位运算符

**先导**：原码，反码，补码

符号位是从左向右的第一位，正数为0，负数为1

![image-20220704164544100](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220704164544100.png)



**位运算**：

![image-20220705092106423](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220705092106423.png)

![image-20220705105317651](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220705105317651.png)



# 键盘输入

```c
 //2. 创建 Scanner 对象，new 创建一个对象
 //myScanner就是Scanner类的对象
 Scanner myScanner = new Scanner(System.in);
```
```c
//进行键盘的输入
        int a=myScanner.nextInt();
        double b=myScanner.nextDouble();
        float c =myScanner.nextFloat();
        String d=myScanner.next();
        byte e=myScanner.nextByte();
        long f=myScanner.nextLong();
        short g=myScanner.nextShort();
        boolean h =myScanner.nextBoolean();
```


## 输出提示

println是输出一个就换行
print不会换行



# 类与对象

类可以类比于结构体
对象是类的具体表现，对象的属性是其中的元素；

![image-20220708112812251](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220708112812251.png)



![image-20220719162653906](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220719162653906.png)

```java
class 类名
{

}
```



## **重点：** 对象数组

```java
类名 对象名[] = new 类名[分配的大小]//这一步是创建对象数组
for()
{
	对象名[] = new 类名();//这一步是new对象给数组的元素，循环创建对象
}
```

```java
A a =new A();

//a就是引用变量，它指向了一个A对象，也可以说它引用了一个A对象。我们通过操纵这个a来操作A对象。 此时，变量a的值为它所引用对象的地址
 
//1）右边的“new A()”，是以A类为模板，在堆空间里创建一个A对象。// 分配内存空间
      
//2）左边的“A a”创建了一个A类引用变量，它存放在栈空间中。也就是用来指向a对象的对象引用。 
      
//3）“=”操作符使对象引用指向刚创建的那个A对象。

```

# 方法



## 定义

方法也叫（成员方法）

方法要放在类中。（作为其中的成员）
```java
  class Method //设置一个方法类
{
		public 返回数据类型 方法名 （形参列表..)//public(访问修饰符的一种)
   		{
			//方法体语句;
			return 返回值;//（可以没有返回值）
  	 	}
    
    
    .....//可以写多个方法
}
```

![image-20220708133943168](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220708133943168.png)



## 方法细节

**1.**

![image-20220708134625821](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220708134625821.png)

1. 如何返回多个结果？——————返回数组
2. 驼峰命名法 ————即混合大小写进行命名

**2.** 

![image-20220708145433024](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220708145433024.png)

**3.**
1. 在同一个类中的方法可以直接调用同类中的方法
2. 跨类调用方法，先要创建对象 ，在调用方法。
3. 方法中不能再定义方法



## 方法调用

**值传递**（pass by value）是指在调用函数时将实际参数复制一份传递到函数中，这样在函数中如果对参数进行修改，将不会影响到实际参数。

**引用传递**（pass by reference）是指在调用函数时将实际参数的地址直接传递到函数中，那么在函数中对参数所进行的修改，将影响到实际参数。



## 方法递归

**递归调用**：
简单来说就是方法自己调用自己，每次调用传入不用的变量，解决复杂问题使得代码变得简洁



## 方法重载

Java允许在同一个类中方法名一致但形参列表不一致。
```java
class Method //设置一个方法类
{
		public 返回数据类型 方法名 （形参列表..)//这里不一致，public(访问修饰符的一种)
   		{
			//方法体语句;
			return 返回值;//（可以没有返回值）
  	 	}
    
    
    .....//可以写多个方法
}
```
**例：** 
方法名一样

形参列表，个数不一样，类型不一样

构成重载

> 返回类型不一致并不构成重载

```java
        System.out.println(666);
        System.out.println(99.5);
        System.out.println('a');
        System.out.println("中国");//字符串
        System.out.println("\t台湾");//四个空格
        System.out.println(true);//布尔数
        System.out.println(false);
		//out.println()输出多样的数据却不报错
		//多个同名方法的存在但是要求形参列表不一致
		//666，99.5，'a',.....数据类型不一样，个数也可以不一样
```



## 方法重载细节

![image-20220709092855589](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220709092855589.png)



## 可变参数

![image-20220709103858388](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220709103858388.png)

```java
//对于这同名同功能的方法，这么写过于冗长
//使用可变参数
    public int sum(int... nums)
      	//int...表示接受的是可变参数，类型是int
      	//1. 几时可以接收多个int（0-多）
      	//2. nums 可直接当作数组使用
    {
        int sum=0;
        for(int i=0;i>nums.length;i++)
        {
            sum+=nums[i];
        }
        return sum;
    }
```



## 可变参数细节

![image-20220709110402183](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220709110402183.png)



## 构造方法/构造器

构造器是一种特殊的方法

作用是完成对象初始化

1. 方法名与类名相同
2. 没有返回值
3. 在创建对象时，系统会自动调用该类的构造器完成对象的初始化

![image-20220709150022198](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220709150022198.png)

```java
class Person
{
    String name;
    int age;
    //第一个构造器
    //1. 构造器无返回值，也不能写void
    //2. 构造器名称和构造器名相同
    //3. 构造器的形参列表规则和成员方法一样
    public Person(String pName,int pAge)
    {
        System.out.println("构造器被调用~~完成对象的属性初始化");
        name=pName;
        age=pAge;
    }
    //第二个与第一个形成了重载
    public Person(String pName)
    {
        System.out.println("构造器被调用~~完成对象的属性初始化");
        name=pName;
    }
}
```



## 构造器细节

![image-20220709150557218](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220709150557218.png)



**5.在创建对象时，系统自动的调用该类的构造方法**

![image-20220709150742801](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220709150742801.png)



## this 关键字

this 能解决一些变量名名问题
**例**:
```java
class Person1
{
    String name;
    int age;
    public Person1(String name, int age)//构造器名与类名一致
    {//要是构造器的形参能直接写成属性名就好了
        this.name=name;
        //this.name 就是当前对象的属性name
        //创建好对象以后，谁在调用构造这this就指向那个对象
        this.age=age;
        //this.name 就是当前对象的属性age
        System.out.println("含 this 的构造器被使用");
    }
    public void print()//无形参，下面直接使用对象属性
    {
        System.out.println(name + " " + age);
        //打印对象的属性
    }
}
```
**小结：简单来说，哪个对象调用，this就代表的那个对象**



## this的使用细节

 ![image-20220710095614143](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220710095614143.png)

单用 this 直接指向当前对象


# 包

## 包的本质
就是创建不同的文件夹来保存类文件。



## 包的命名规范

![image-20220712091510200](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220712091510200.png)



## 常用包

![image-20220712095903636](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220712095903636.png)

# 访问修饰符



## 基本介绍

![image-20220712100234567](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220712100234567.png)


## 访问范围图示
![image-20220712100342236](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220712100342236.png)



## 注意事项

![image-20220712123812097](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220712123812097.png)

# 封装



## 封装介绍

![image-20220712162838474](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220712162838474.png)

![image-20220712162918209](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220712162918209.png)

​    

​     封装，即隐藏对象的属性和实现细节，仅对外公开接口，控制在程序中属性的读和修改的访问级别；将抽象得到的数据和行为（或功能）相结合，形成一个有机的整体，也就是将[数据](https://baike.baidu.com/item/数据/5947370)与操作数据的[源代码](https://baike.baidu.com/item/源代码/3814213)进行有机的结合，形成“类”，其中数据和函数都是类的成员。



## 封装步骤

![image-20220712162811001](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220712162811001.png)

```java
package com.fengzhuang.encap;

import java.util.Scanner;

public class Encapsulation1
{
    public static void main(String[] args)
    {

        Person person = new Person( "sdfs",18,5000);
        //此处直接调用了 Perton 类
        //并同时自动使用了其中的构造器
        //person 可以调用其中的方法

//        person.setName("jakesfs");
//        person.setAge(36);
//        person.setSalary(30000);
          System.out.println(person.putout());
//
    }
}

//需求是年龄，薪资不能随意查看，名字长度为 2-6 个字符，年龄范围是18-35

class Person
{
    public String name;//名字公开
    private int age;//年龄隐私
    private double salary;//

    //手写set太慢 我们使用快捷键 Alt + Ins 使用 setter 和 getter
    //插入一个构造器 Alt + Ins

    public Person(String name, int age, double salary) 
    {
//        this.name = name;
//        this.age = age;
//        this.salary = salary;

        //我们直接在构造中使用 setter
        setName(name);
        setAge(age);
        setSalary(salary);
    }


    public String getName()
    {
        return name;
    }

    public void setName(String name)
    {
        //在这里面设置限制，相当于写业务逻辑
        if(name.length()>=2&&name.length()<=6)
        {
            this.name = name;
        }
        else
        {
            System.out.println("名字长度不对（2-6）个字符，请重新输入。。。" +
                    "系统默认为：无名氏");
            this.name = "无名氏";
        }
    }

    public int getAge()
    
    {
        return age;
    }
    public void setAge(int age)
    {
        if(age>=18&&age<=35)
        {
            this.age = age;
        }
        else {
            System.out.println("年龄输入不正确，请重新输入。。。" +
                    "系统默认为：18");
            this.age = 18;
        }
    }


    public double getSalary()
    {
        //这里咱么输入密码才能查看
        Scanner scanner = new Scanner(System.in);
        System.out.println("请输入密码...(200314)");
        int password = scanner.nextInt();
        if(password==200314)
        {
            return salary;
        }
        else
        {
            System.out.println("无法查看薪资,默认为：0");
            return 0;
        }
    }

    public void setSalary(double salary)
    {
        this.salary = salary;
    }

    //写一个方法，返回属性信息
     public String putout()
    {
        return getName()+"\t"+getAge()+"\t"+getSalary();
    }
}
```

## 封装与构造器

简而言之就是将构造器于 setXxx 结合起来，将 setXxx 方法调入进构造器当中。

在构造器中赋值仍然会得到防护



# 继承

## 继承的基本介绍

![image-20220713143657158](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220713143657158.png)



## 继承图示

![image-20220713144804984](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220713144804984.png)



## 继承的语法

![image-20220713144848721](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220713144848721.png)



```java
public class  Graduate extends Parent_class{
    //         子类名              父类名
    public void testing()//特殊的方法，属性写在子类里面
    {
        System.out.println("大学生 "+name+" 正在考试中");
    }
}
```



## 继承的细节
1. 子类继承了父类所有的属和方法，非私有的属性和方法可以在子类直接访问， 但是私有属性和方法不能在子类直接访问，要通过父类提供的公共的方法去访问。



2. 子类必须调用父类的构造器，完成完成父类的初始化




3. 当创建子类对象时，**不管使用子类的哪个构造器**，默认情况都会去调用父类的无参构造器，如果父类**没有提供无参构造器**,则必须**在子类的构造器**中去 super() 去指定使用父类的哪个构造器完成对父类的初始化工作，否则，编译不会通过。

   -----**重要**



4. 如果希望指定调用父类的某个构造器，则显示调用一下：super (参数列表)



5. super（）在使用时，必须放在构造器的第一行（super 只能在构造器中使用）



6. super（） 和 this（）都只能放在构造器的第一行，因此这两种方法不能共存于同一个构造器。



7. Java 的所有类都是 Object类  的子类，Object 是所有类的基类（父类）



8. 父类构造器的调用不限于直接父类，将一直往上追溯到 Object类



9. Java 是单继承机制 ，即一个子类只能继承一个父类



10. 不能滥用继承，子类和父类要满足 is-a 的关系，即 **子类**是**父类**，例：**狗**是**动物**



此处我们分析一道例题：

![image-20220715090911148](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220715090911148.png)

在 class B 中 this 与 super 不共存使用 this 调用同类含参，B（String）中第一句默认 super 调用 class A 中无参构造器，第一个输出a，然后是 b name ，最后是 b。



# super关键字

## 基本介绍
super 代表父类的引用 ，用于访问父类的属性，方法，构造器



## 基本语法

1. 访问父类的属性，但是不能访问父类的隐私 private 属性
   super.属性名；
2. 访问父类的方法，但不能访问父类的 private 方法
   super.方法名（参数列表）
3. 访问父类的构造器
   super（参数列表）；只能放在构造器的第一句，只能出现一句。

4. **super 和 this 只能有一个**



## 使用细节

![image-20220715113940371](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220715113940371.png)



![image-20220715114307397](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220715114307397.png)

先查找到谁就是谁，就近原则。

## super与this的比较

![image-20220715114219380](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220715114219380.png)



# 方法重写


## 方法重写介绍

![image-20220715143824178](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220715143824178.png)



## 方法重写的细节

![image-20220715150205815](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220715150205815.png)

子类方法可以与父类方法的访问权险相同和扩大



## 方法重写和重载的比较

![image-20220715151536323](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220715151536323.png)


# 多态
## 多态介绍
多态指的是方法或对象具有多种形态。是面向对象的第三大特征，多态是建立在继承和封装之上的

1. 方法的多态： 
    重写和重载体现多态
2. 对象的多态

3. 多态的前提是，两个对象（类）存在继承关系

- 一个对象的编译类型和运行类型可以不一致
- 编译类型在定义对象时，就已经确定了，不能改变
- 运行类型是可以改变的
- 编译类型看 = 的左边，运行类型看 = 的右边
- 父类的引用可以指向子类的对象（向上转型）

![image-20220718174118623](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220718174118623.png)

![image-20220718174133891](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220718174133891.png)

编译类型是羊，运行类型是狼。



## 多态细节：向上转型

![image-20220719113428550](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220719113428550.png)

​    **向上转型：子类引用的对象转换为父类类型称为向上转型。通俗地说就是是将子类对象转为父类对象。此处父类对象可以是接口**。向上转型就是把子类对象直接赋给父类引用，不用强制转换。使用向上转型可以调用父类类型中的所有成员，不能调用子类类型中特有成员，最终运行效果看子类的具体实现。

```java
//向上转型：父类的引用指向了子类的对象

//语法：父类类型 引用名 = new 子类类型

//这里可以调用父类中的所有成员（须遵守访问权限）

//但是不能调用子类的特有成员

//因为在编译阶段，能调用那些成员，是由编译类型决定的

//编译的什么，就只能调用那里面的类

//最终的运行效果要看子类的具体实现，在调用方法时从子类本类开始向上查询

//编译是从上往下的
```



## 多态细节：向下转型

![image-20220719150018977](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220719150018977.png)

​    **向下转型：父类引用的对象转换为子类类型称为向下转型。**向下转型可以调用子类类型中所有的成员，不过需要注意的是如果父类引用对象指向的是子类对象，那么在向下转型的过程中是安全的，也就是编译是不会出错误。但是如果父类引用对象是父类本身，那么在向下转型的过程中是不安全的，编译不会出错，但是运行时会出现我们开始提到的 Java 强制类型转换异常，一般使用 instanceof 运算符来避免出此类错误。



```java
//其实就是必须先向上转型，再向下转型
```

```Java
 Animal animal = new Cat("jerry");//向上,在此处刚好 animal 指向 Cat
 Cat cat = (Cat) animal;//向下
//要求父类的引用必须指向当前目标类型的对象
//    -------            -------
//    animal               Cat
//其实就是必须先向上转型，再向下转型
//cat 能调用子类中的所有成员
```



## 多态细节：属性

![image-20220719165742406](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220719165742406.png)

**在访问属性时看编译类型，在访问方法时看运行类型**

**= 号左边看编译，右边看运行**



## 多态：动态绑定

Java的动态绑定机制：

1. 当调用对象方法时**，该方法会和该对象的内存地址/运行类型**绑定
2.   当调用对象属性时，**没有动态绑定机制**，哪里声明，哪里使用



## 多态数组

数组的定义类型为父类类型，里面保存的实际元素类型为[子类](https://so.csdn.net/so/search?q=子类&spm=1001.2101.3001.7020)类型

![image-20220720152947956](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220720152947956.png)

```java
// 多态数组, 这里是向上转型
 Person[] person = new Person[5];//创建对象数组
 person[0] = new Person("jack",20);//以下都是对象数组实例化
 person[1] = new Student(" asdf",19,100);
 person[2] = new Student("hjff",24,60);
 person[3] = new Teacher("jsghdfghg",26,3000);
 person[4] = new Teacher("hjfhfgh",22,2000);



 for (int i = 0; i < person.length; i++)
        {
            if(person[i] instanceof Student)//对类型进行判断
            {
//               Student student = (Student)person[i];
//               student.test();
               //这两步可以合为一步
                ((Student)person[i]).test();//向下转型，可使用子类中方法
            }
          else if(person[i] instanceof Teacher)//对类型进行判断
            {
                ((Teacher)person[i]).teach();//向下转型，可使用子类中方法
            }
           else {
                System.out.println("类型有误，请自行检查");
            }
```





## 多态参数

 指的是方法定义的形参是父类类型，实参类型允许为子类类型



# Object 类详解



## == 运算符作用

![image-20220721093539804](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220721093539804.png)



## equals方法

![image-20220721093423391](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220721093423391.png)

  这里的 equals 可能因为引用类型传入的是 String  ，Integer 而重写子类方法，转为判断内容相同。而 == 不会。



##  hashCode方法

![image-20220721135650272](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220721135650272.png)

返回哈希码值



## toString方法

![image-20220721153838106](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220721153838106.png)



## finalize方法

![image-20220721153800627](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220721153800627.png)



## instanceof 运算符

  instanceof  是Java中的二元运算符，左边是对象，右边是类；当对象**是右边类或子类所创建对象时**，返回true；否则，返回false。（**比的是运行类型**）



  instanceof左边显式声明的类型与右边操作元必须是同种类或存在继承关系，也就是说需要位于同一个继承树，否则会编译错误



# 断点调试

![image-20220721160908369](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220721160908369.png)



![image-20220721160933971](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220721160933971.png)



![image-20220721160948009](C:\Users\WangYanzhou\AppData\Roaming\Typora\typora-user-images\image-20220721160948009.png)

断点可以在 debug 时下断点

调试中光标放在变量上可查看值