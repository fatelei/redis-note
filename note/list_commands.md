Redis List commands
===================

在Redis中，List用于存储一个由字符串构成的有序序列。

## 1. Some commonly used List commands
+ RPUSH
```
  命令: RPUSH key-name value [value ...]
  解释: 在列表的右端插入一个或多个值
```

+ LPUSH
```
  命令: LPUSH key-name value [value ...]
  解释: 在列表的左端插入一个或多个值
```

+ RPOP
```
  命令: RPOP key-name
  解释: 移除列表最右端的值，并返回移除的值
```

+ LPOP
```
  命令: LPOP key-name
  解释: 移除列表最左端的值，并返回移除的值
```

+ LINDEX
```
  命令: LINDEX key-name offset
  解释: 返回给定offset对应的值
```

+ LRANGE
```
  命令: LRANGE key-name start end
  解释: 返回指定闭区间列表对应的值
```

+ LTRIM
```
  命令: LTRIM key-name start end
  解释: 对key-name对应的列表执行切片操作，操作区间为闭区间，并将切片之后的值存储到key-name
```

## 2. Some LIST commands for blocking LIST pop and moving items between LISTS
+ RLPOP
```
  命令: BLPOP key-name [key-name ...] timeout
  解释: 将非空列表的最左端元素弹出，或者阻塞等待当列表非空时弹出元素，或者等待一定时间弹出列表最左端元素
```

+ BRPOP
```
  命令: BRPOP key-name [key-name ...] timeout
  解释: 将非空列表的最右端元素弹出，或者阻塞等待当列表非空时弹出最右端元素，或者等待一定时间弹出列表最右端元素
```

+ RPOPLPUSH
```
  命令: RPOPLPUSH source-key dest-key
  解释: 从source-key中右端弹出元素，并从左端插入到dest-key，并返回弹出元素
```

+ BRPOPLPUSH
```
  命令: BRPOPLPUSH source-key dest-key timeout
  解释: 从source-key中右端弹出元素，并从左端插入到dest-key，并返回弹出元素，如果source-key对应列表为空，会等待相应的timeout
```
