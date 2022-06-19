# BigDecimal

## BigDecimal初始化方式

right
```java
new BigDecimal("10.20");
```

wrong
```java
new BigDecimal(10.20);
```

## BigDecimal比较方式
right
```java
new BigDecimal("10.20").compareTo(new BigDecimal("10.2") == 0;
```

## 常用的舍入方式

1. 四舍五入
```java
BigDecimal num = new BigDecimal("10.20");
// 四舍五入，保留一位小数
num.setScale(1, RoundingMode.ROUND_HALF_UP);
```

2. 其他模式
```java
java.math.RoundingMode
```

### 常见错误
1. 将BigDecimal存入HashSet

```java
Set<BigDecimal> treeSet = new TreeSet<>();
treeSet.add(new BigDecimal("1.0"));
System.out.println(treeSet.contains(new BigDecimal("1")));//返回true
```