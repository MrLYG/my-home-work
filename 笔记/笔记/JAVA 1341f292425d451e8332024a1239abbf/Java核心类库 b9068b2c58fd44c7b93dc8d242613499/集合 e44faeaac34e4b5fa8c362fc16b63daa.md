# 集合

[Collection集合](%E9%9B%86%E5%90%88%20e44faeaac34e4b5fa8c362fc16b63daa/Collection%E9%9B%86%E5%90%88%20ce5516d671de4686a9f08a931fd7cf54.md)

[Iterator接口](%E9%9B%86%E5%90%88%20e44faeaac34e4b5fa8c362fc16b63daa/Iterator%E6%8E%A5%E5%8F%A3%207f660789c1904e1096cf225e013ed6b6.md)

- java.util.List集合是Collection集合的子集合，该集合中允许有重复的元素并且有先后放入次序。
- 该集合的主要实现类有：ArrayList类、LinkedList类、Stack类、Vector类。
- 其中ArrayList类的底层是采用动态数组进行数据管理的，支持下标访问，增删元素不方便。
- 其中LinkedList类的底层是采用双向链表进行数据管理的，访问不方便，增删元素方便。
- 可以认为ArrayList和LinkedList的方法在逻辑上完全一样，只是在性能上有一定的差别，ArrayList更适合于随机访问而LinkedList更适合于插入和删除；在性能要求不是特别苛刻的情形下可以忽略这个差别。
- 其中~~Stack~~**（被DEQUE取代）**类的底层是采用动态数组进行数据管理的，该类主要用于描述一种具有后进先出特征的数据结构，叫做栈(last in first out LIFO)。
- 其中**~~Vector~~**类的底层是采用动态数组进行数据管理的，该类与ArrayList类相比属于**线程安全的类**，效率比较低，以后开发中基本不用。

[List](%E9%9B%86%E5%90%88%20e44faeaac34e4b5fa8c362fc16b63daa/List%20cc73819cbaff4911ae9b5960fe49cd99.md)

[LinkedList](%E9%9B%86%E5%90%88%20e44faeaac34e4b5fa8c362fc16b63daa/LinkedList%20d7b1df5735ff4ce896212e1862d83556.md)

[泛型](%E9%9B%86%E5%90%88%20e44faeaac34e4b5fa8c362fc16b63daa/%E6%B3%9B%E5%9E%8B%20c9cd49f8ad8442ec9485c46f35feb3b1.md)

[Map](%E9%9B%86%E5%90%88%20e44faeaac34e4b5fa8c362fc16b63daa/Map%20bcb54f1ce8214214be9d28522da4f2cc.md)

[Copy of List](%E9%9B%86%E5%90%88%20e44faeaac34e4b5fa8c362fc16b63daa/Copy%20of%20List%20a148675b163346f089835474e534a9e7.md)