Redis String commands
=====================

在Redis中，String用于存储以下三种类型的值；
+ Byte string values
+ Interger values
+ Floating-point values

Interger和floats，可以自增和自减任意的值。Interger的取值范围由所运行的平台确定，比如运行在32位系统，
则范围是有符号的32位整数，同理64位。而float的取值范围遵守IEEE 754。


## １. Increment and decrement commands in Redis
+ INCR
```
  命令: INCR key-name
  解释: 使key-name对应的value自增１
```

+ DECR
```
  命令: DECR key-name
  解释: 使key-name对应的value自减１
```

+ INCRBY
```
  命令: INCRBY key-name amount
  解释: 使key-name对应的value，执行value = value + amount
```

+ DECRBY
```
  命令: DECRBY key-name amount
  解释: 使key-name对应的value，执行value = value - amount
```

+ INCRBYFLOAT
```
  命令: INCRBYFLOAT key-name float-value
  解释: 使key-name对应的value，执行value = value + float-value
```

## 2. Substring manlpulation commands in Redis
+ APPEND
```
  命令: APPEND key-name value
  解释: 对key-name对应的value，执行字符串拼接操作
```

+ GETRANGE
```
  命令: GETRANGE key-name start end
  解释: 根据start和end，获取key-name对应value指定区间的值，该区间是闭区间
```

+ SETRANGE
```
  命令: SETRANGE key-name offset value
  解释: 从key-name对应的值的offset开始，替换字串的值为value
```

+ GETBIT
```
  命令: GETBIT key-name offset
  解释: 获取key-name对应的value，在offset对应的二进制值
```

+ SETBIT
```
  命令: SETBIT key-name offset value
  解释: 根据提供的value，设置在指定的bit offset，key-name对应的value
```

+ BITCOUNT
```
  命令: BITCOUNT key-name [start end]
  解释: 计算key-name对应的value，其对应二进制数据中1的个数
```

+ BITOP
```
  命令: BITOP operation dest-key key-name [key-name ...]
  解释: 对提供的strings，执行and, or, xor, not中的一种逻辑运算，并把运算结果存入到dest-key
```
