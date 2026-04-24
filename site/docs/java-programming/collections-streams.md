# ☕ Java编程 - 集合与流处理

Java8引入的流API让数据处理更加优雅和高效。

## 📚 主要内容

### Collections框架
- List、Set、Map接口
- ArrayList、HashMap等实现
- 排序和查找

### Stream API
```java
List<Integer> data = Arrays.asList(1, 2, 3, 4, 5);

// 函数式处理
int sum = data.stream()
    .filter(x -> x % 2 == 0)
    .map(x -> x * 2)
    .reduce(0, Integer::sum);
```

---

**下一步：** 学习[并发编程](concurrent-programming.md)！
