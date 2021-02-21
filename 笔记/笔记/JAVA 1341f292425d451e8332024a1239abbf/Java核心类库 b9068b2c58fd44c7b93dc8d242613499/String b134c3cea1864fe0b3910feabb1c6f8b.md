# String

## Final修饰

1.String类由final修饰

2.String类的对象所指向的字符串由final修饰    —>     final 修饰 数组，数组中每个元素的指向不可变—>  String类型所描述的字符串内容不可变

“String对象一旦被创建就是固定不变的了，对String对象的任何改变都不影响到原对象，相关的任何change操作都会生成新的对象”

```java
/** The value is used for character storage. */
    private final char value[];
```

## 常量池概念

由于String类型描述的字符串内容是常量不可改变，因此Java虚拟机将首次出现的字符串放入常量池中，若后续代码中出现了相同字符串内容则直接使用池中已有的字符串对象而无需申请内存及创建对象，从而提高了性能。

![String%20b134c3cea1864fe0b3910feabb1c6f8b/Untitled.png](String%20b134c3cea1864fe0b3910feabb1c6f8b/Untitled.png)

String(String original)  根据参数指定的字符串内容来构造对象，新创建对象为参数对象的副本

new创建字符串时首先查看池中是否有相同值的字符串，如果有，则拷贝一份到堆中，然后返回堆中的地址；如果池中没有，则在堆中创建一份，然后返回堆中的地址（注意，此时不需要从堆中复制到池中，否则，将使得堆中的字符串永远是池中的子集，导致浪费池的空间）！

![String%20b134c3cea1864fe0b3910feabb1c6f8b/Untitled%201.png](String%20b134c3cea1864fe0b3910feabb1c6f8b/Untitled%201.png)

## String 类的字符串比较——str.compareTo" "

```java
public int compareTo(String anotherString) {
        int len1 = value.length;
        int len2 = anotherString.value.length;
        int lim = Math.min(len1, len2);
        char v1[] = value;
        char v2[] = anotherString.value;

        int k = 0;
        while (k < lim) {
            char c1 = v1[k];
            char c2 = v2[k];
            if (c1 != c2) {
                return c1 - c2;
            }
            k++;
        }
        return len1 - len2;
    }
```

## String API

[https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/String.html](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/String.html)

[String一些常用的方法](String%20b134c3cea1864fe0b3910feabb1c6f8b/String%E4%B8%80%E4%BA%9B%E5%B8%B8%E7%94%A8%E7%9A%84%E6%96%B9%E6%B3%95%204155a7d6be5c44c8b132c00f0dff4f74.csv)

[String 查找相关的API](String%20b134c3cea1864fe0b3910feabb1c6f8b/String%20%E6%9F%A5%E6%89%BE%E7%9B%B8%E5%85%B3%E7%9A%84API%20e88d01cc8b684cf4b3310417ce307230.csv)

## 正则表达式编程

[String 正则表达式API](String%20b134c3cea1864fe0b3910feabb1c6f8b/String%20%E6%AD%A3%E5%88%99%E8%A1%A8%E8%BE%BE%E5%BC%8FAPI%20d792a536579a4445b1b29995b1b9c8c1.csv)

[正则表达式的规则](String%20b134c3cea1864fe0b3910feabb1c6f8b/%E6%AD%A3%E5%88%99%E8%A1%A8%E8%BE%BE%E5%BC%8F%E7%9A%84%E8%A7%84%E5%88%99%201c487ac790af412db4be814b6817d08d.csv)

[正则表达式的规则](String%20b134c3cea1864fe0b3910feabb1c6f8b/%E6%AD%A3%E5%88%99%E8%A1%A8%E8%BE%BE%E5%BC%8F%E7%9A%84%E8%A7%84%E5%88%99%2012ea203d47424b6782c622bcf343d4a6.csv)

[正则表达式的规则](String%20b134c3cea1864fe0b3910feabb1c6f8b/%E6%AD%A3%E5%88%99%E8%A1%A8%E8%BE%BE%E5%BC%8F%E7%9A%84%E8%A7%84%E5%88%99%204de8f745ed2e4bbbad2899a50d87e5a9.csv)