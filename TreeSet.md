## TreeSet

Set子类，TreeSet的本质是一个"**有序的，并且没有重复元素**"的集合，它是通过TreeMap(红黑树)实现的。TreeSet中含有一个"NavigableMap类型的成员变量"m，而m实际上是"TreeMap的实例"。

https://www.jianshu.com/p/b48c47a42916 Set总结

- 它存储唯一的元素
- 它不保留元素的插入顺序
- 它按升序对元素进行排序
- 它不是线程安全的

```xml
TreeSet简介
TreeSet 是一个有序的集合，它的作用是提供有序的Set集合。它继承于AbstractSet抽象类，实现了NavigableSet<E>, Cloneable, java.io.Serializable接口。
TreeSet 继承于AbstractSet，所以它是一个Set集合，具有Set的属性和方法。
TreeSet 实现了NavigableSet接口，意味着它支持一系列的导航方法。比如查找与指定目标最匹配项。
TreeSet 实现了Cloneable接口，意味着它能被克隆。
TreeSet 实现了java.io.Serializable接口，意味着它支持序列化。
TreeSet是基于TreeMap实现的。TreeSet中的元素支持2种排序方式：自然排序 或者 根据创建TreeSet 时提供的 Comparator 进行排序。这取决于使用的构造方法。
TreeSet为基本操作（add、remove 和 contains）提供受保证的 log(n) 时间开销。
另外，TreeSet是非同步的。 它的iterator 方法返回的迭代器是fail-fast的。
 
TreeSet的构造函数

// 默认构造函数。使用该构造函数，TreeSet中的元素按照自然排序进行排列。
TreeSet()

// 创建的TreeSet包含collection
TreeSet(Collection<? extends E> collection)

// 指定TreeSet的比较器
TreeSet(Comparator<? super E> comparator)

// 创建的TreeSet包含set
TreeSet(SortedSet<E> set)

TreeSet的API

boolean                   add(E object)
boolean                   addAll(Collection<? extends E> collection)
void                      clear()
Object                    clone()
boolean                   contains(Object object)
E                         first()
boolean                   isEmpty()
E                         last()
E                         pollFirst()
E                         pollLast()
E                         lower(E e)
E                         floor(E e)
E                         ceiling(E e)
E                         higher(E e)
boolean                   remove(Object object)
int                       size()
Comparator<? super E>     comparator()
Iterator<E>               iterator()
Iterator<E>               descendingIterator()
SortedSet<E>              headSet(E end)
NavigableSet<E>           descendingSet()
NavigableSet<E>           headSet(E end, boolean endInclusive)
SortedSet<E>              subSet(E start, E end)
NavigableSet<E>           subSet(E start, boolean startInclusive, E end, boolean endInclusive)
NavigableSet<E>           tailSet(E start, boolean startInclusive)
SortedSet<E>              tailSet(E start)

```

