# 基础

```java
//数据类型

//整数类型
int i;     //int[] i;
short s;
long l;
long long ll;
byte b;
//字符串    //char[] c;
char c;
String s;
//浮点数
float f;   //float[] f;
double d;
//布尔类型
boolean b;
//枚举类型
enum e;

//包装类
Integer i;
Short s;
Byte b;
Long l;
//字符串
Character c;
String s;
//浮点数
Float f;
Double d;
//布尔类型
Boolean b;


/*
面向对象编程
类、对象、继承、封装、多态、抽象、接口、方法重载、方法重写
*/
//chong'za
```

集合

```java
		//List接口
        List<Integer> l1 = new ArrayList<>();//数组实现
        List<Integer> l2 = new LinkedList<>();//链表实现
        List<Integer> l3 = new Vector<>();//
        List<Integer> l4 = new Stack<>();

        //Set接口
        Set<Integer> s1 = new HashSet<>();
        Set<Integer> s2 = new LinkedHashSet<>();
        Set<Integer> s3 = new TreeSet<>();

        //Map接口
        Map<Integer, Integer> m1 = new HashMap<>();
        Map<Integer, Integer> m2 = new LinkedHashMap<>();
        Map<Integer, Integer> m3 = new TreeMap<>();
        Map<Integer, Integer> m4 = new Hashtable<>();

        //Queue接口
        Queue<Integer> q1 = new PriorityQueue<>();
        Queue<Integer> q2 = new ArrayDeque<>();
```

泛型

```java
//T和Object的区别

public class Box<T>{
    private T value;

    public T getValue(){
        return value;
    }
}

public class Box{
    private Object value;
    
    public Object getValue(){
        return value;
    }
}

//使用泛型
Box<String> box = new Box<>()
String value = box.getValue();
//使用Obejct
Box box = new Box();
String value = (String) box.getValue();
```



## 常用类

### 1. **基本类型包装类**

这些类用于将基本数据类型（如 `int`、`char`）包装为对象，以便在需要对象的上下文中使用。

- **`Integer`**: 包装 `int` 类型。
- **`Double`**: 包装 `double` 类型。
- **`Boolean`**: 包装 `boolean` 类型。
- **`Character`**: 包装 `char` 类型。

### 2. **集合类（Collection Framework）**

这些类用于存储和操作一组数据。

- **`ArrayList<E>`**: 动态数组，常用于存储元素列表。
- **`LinkedList<E>`**: 双向链表，适合频繁的插入和删除操作。
- **`HashSet<E>`**: 存储不重复的元素，无序。
- **`TreeSet<E>`**: 存储不重复的元素，并按照自然顺序排序。
- **`HashMap<K, V>`**: 基于哈希表的键值对存储，允许 `null` 值和 `null` 键。
- **`TreeMap<K, V>`**: 基于红黑树的键值对存储，键按照自然顺序排序。
- **`Stack<E>`**: 后进先出（LIFO）数据结构。
- **`Queue<E>`**: 先进先出（FIFO）数据结构。

### 3. **字符串处理类**

这些类用于字符串的操作和处理。

- **`String`**: 不可变的字符序列，广泛用于字符串操作。
- **`StringBuilder`**: 可变的字符序列，适合用于频繁的字符串拼接。
- **`StringBuffer`**: 线程安全的可变字符序列，比 `StringBuilder` 慢，但线程安全。

### 4. **输入输出（I/O）类**

这些类用于读写文件、控制台输入输出等。

- **`File`**: 表示文件和目录路径名。
- **`FileInputStream`**: 读取文件的字节流。
- **`FileOutputStream`**: 写入文件的字节流。
- **`BufferedReader`**: 带缓冲的字符输入流，通常用于读取文本文件。
- **`BufferedWriter`**: 带缓冲的字符输出流，通常用于写入文本文件。
- **`ObjectInputStream`**: 反序列化对象的字节流。
- **`ObjectOutputStream`**: 序列化对象的字节流。

### 5. **时间和日期类**

这些类用于处理日期和时间。

- **`Date`**: 表示日期和时间，已过时，建议使用 `java.time` 包中的类。
- **`Calendar`**: 提供对日期字段的操作，如年、月、日等。
- **`LocalDate`**: 处理不带时区的日期（`java.time` 包）。
- **`LocalTime`**: 处理不带时区的时间（`java.time` 包）。
- **`LocalDateTime`**: 处理不带时区的日期和时间（`java.time` 包）。
- **`Instant`**: 时间戳，用于表示瞬间（`java.time` 包）。
- **`Duration`**: 表示时间段（`java.time` 包）。
- **`Period`**: 表示日期间隔，如年、月、日（`java.time` 包）。

**`SimpleDateFormat`**: 适合旧版 Java 的日期格式化，不是线程安全的。

**`DateTimeFormatter`**: 推荐使用的现代日期时间格式化类，线程安全，功能强大。

**`Calendar`**: 旧版 Java 的日期处理类，通常与 `SimpleDateFormat` 一起使用。

**`LocalDate`、`LocalTime`、`LocalDateTime`**: Java 8 引入的处理不同时区日期和时间的类。

**`ZonedDateTime`** 和 **`OffsetDateTime`**: 用于处理带有时区和 UTC 偏移的日期和时间。

### 6. **数学和随机数类**

这些类用于数学计算和生成随机数。

- **`Math`**: 提供数学运算，如 `sqrt`、`abs`、`sin` 等。
- **`Random`**: 生成伪随机数。
- **`BigDecimal`**: 高精度的浮点数运算，常用于金融计算。
- **`BigInteger`**: 任意精度的整数运算。

### 7. **系统和环境类**

这些类用于获取系统属性、运行时信息、环境变量等。

- **`System`**: 提供与系统相关的操作，如标准输入输出、系统属性等。
- **`Runtime`**: 提供与 Java 虚拟机相关的操作，如内存管理、执行命令等。
- **`Thread`**: 表示线程，用于多线程编程。
- **`ThreadLocal<T>`**: 提供线程局部变量，每个线程都有独立的变量副本。

### 8. **异常处理类**

这些类用于处理异常情况。

- **`Exception`**: 所有异常的基类，表示程序中可能出现的问题。
- **`RuntimeException`**: 非受检异常的基类，如 `NullPointerException`、`IndexOutOfBoundsException` 等。
- **`IOException`**: 输入输出异常，如文件未找到、无法读取文件等。
- **`SQLException`**: 数据库操作相关的异常。

### 9. **反射和注解类**

这些类用于在运行时动态访问类和对象的信息。

- **`Class<T>`**: 表示类的字节码对象，可以用于获取类的元信息。
- **`Method`**: 表示类的方法，可以用于调用方法。
- **`Field`**: 表示类的字段，可以用于访问或修改字段的值。
- **`Annotation`**: 注解接口的超类，表示注解。

### 10. **网络编程类**

这些类用于处理网络通信。

- **`Socket`**: 实现客户端和服务器之间的通信。
- **`ServerSocket`**: 实现服务器端的套接字，监听并接受客户端连接。
- **`URL`**: 表示统一资源定位符，用于处理网络资源。
- **`HttpURLConnection`**: 处理 HTTP 请求和响应。









