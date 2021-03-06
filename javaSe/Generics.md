#泛型 2016-09-06
1. **什么是泛型**
   泛型（*Generic type or generic*）是对Java语言的类型系统的一种扩展，以支持创建可以按类型进行参数化的类。可以把类型参数看作是使用参数化类型时指定的类型的一个占位符。
***
在集合框架（Collection framework）中看到泛型的动机，例如在代码
'''
	Map m = new HashMap();
	m.put("key","blarg");
	String s = (string)m.get("key");
'''
Map.get()定义返回的类型为Object，所以一般要将Map.get()的结果强制转换为期望的类型，代码段中就是将get()的结果强制转为String。**泛型的目的是为了消除代码中的强制类型转换，同时获得一个附加的类型检查层，该检查层防止有人将错误的键或值保存在集合中。**

2. 泛型的好处   
   **类型安全**。泛型的主要目标是提高java程序的类型安全，通过知道使用泛型定义的变量的类型限制，编译器可以在一个高的多的程度上验证类型假设。   
   **消除强制转换**。消除源代码中许多的强制类型转换。  
   **潜在得到性能收益**。泛型为较大的优化带来可能。泛型的初始化实现中，编译器将强制类型转换插入生成的字节码中。 
使用泛型的代码段：
'''
	List<Integer>li = new ArrayList<Integer>();
	li.put(new Integer(3));
	Integer i = li.get();
'''



   

   

	

