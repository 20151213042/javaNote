#java学习笔记 2016-09-05
**String, StringBuilder and StringBuffer**
1.操作少量的的数据用String
2.单线程操作字符串缓冲区 下操作大量的数据用 StringBuilder
3.多线程操作字符串缓冲区 下操作大量数据用 StringBuffer
****
String是"字符串"常量，是不可改变的对象，StringBuilder和StringBuffer是字串变量，是可改变的对象；
****
当我们在字符串缓冲去被多个线程使用是，JVM不能保证StringBuilder的操作是安全的，虽然他的速度最快；
****
但是可以保证StringBuffer是可以正确操作的。当然大多数情况下就是我们是在单线程下进行的操作，所以大多数情况下是建议用StringBuilder而不用StringBuffer的，就是速度的原因。