Redis 数据结构
-------------
## Redis数据结构类型

+ String（字符串）
  + 可以存储字符串、整数和浮点数
  + 对于整数和浮点数可以执行自增和自减操作

+ List（链表）
  + 由字符串构成的链表
  + 可以链表的表头和表尾执行push和pop操作，可以根据offset执行trim操作，可以读取单个和多个值，以及根据value进行操作和删除操作

+ Set（集合）
  + 无序的独一无二的字符串集合
  + 可以对单个item执行添加、读取、删除操作，检测membership，进行集合运算

+ Hash（哈希）
  + 无序的key-value键值对
  + 可以对单个item执行添加、读取、删除操作，获取整个hash table

+ ZSet（有序集合）
  + 有序的value-score映射，格局score排序
  + 可以对单个value执行添加、读取、删除操作，以及根据score或者value获取items
