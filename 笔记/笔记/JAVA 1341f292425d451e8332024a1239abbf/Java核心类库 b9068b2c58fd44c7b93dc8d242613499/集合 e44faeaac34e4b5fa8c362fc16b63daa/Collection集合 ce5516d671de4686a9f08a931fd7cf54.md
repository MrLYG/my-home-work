# Collection集合

集合用于取代数组的结构

## 常用方法

[Collection常用方法](Collection%E9%9B%86%E5%90%88%20ce5516d671de4686a9f08a931fd7cf54/Collection%E5%B8%B8%E7%94%A8%E6%96%B9%E6%B3%95%2017d73a11ee6643779ac791b1ac351ba4.md)

## API

- boolean add(E e); 向集合中添加对象
- boolean addAll(Collection<? extends E> c)用于将参数指定集合c中的所有元素添加到当前集合中
- boolean contains(Object o); 判断是否包含指定对象
- boolean containsAll(Collection<?> c) 判断是否包含参数指定的所有对象
- boolean retainAll(Collection<?> c) 保留当前集合中存在且参数集合中存在的所有对
- boolean remove(Object o); 从集合中删除对象
- boolean removeAll(Collection<?> c) 从集合中删除参数指定的所有对象
- void clear(); 清空集合
- int size(); 返回包含对象的个数
- boolean isEmpty(); 判断是否为空
- boolean equals(Object o) 判断是否相等
- int hashCode() 获取当前集合的哈希码值
- Object[] toArray() 将集合转换为数组
- Iterator iterator() 获取当前集合的迭代器

## 个人感悟

- 集合中的所存储的自定义类一定要重写Object的equals()方法，因为Collection涉及的方法中包含一些equals()方法进行判断是否相等（例如contains()方法），如果自定义类不重写Object的equals()方法，默认判断地址！！！