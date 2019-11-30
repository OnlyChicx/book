# MongoDB

</br>

## MongoDB查询语句

```sql
db.name.find()
```

### 判断语句

+ 等于 
  + ```{<key>:<value>}```
+ 小于 
  + ```{<key>:{$lt:<value>}}```
+ 小于或等于 
  + ```{<key>:{$lte:<value>}}```
+ 大于 
  + ```{<key>:{$gt:<value>}}```
+ 大于或等于 
  + ```{<key>:{$gte:<value>}}```
+ 不等于 
  + ```{<key>:{$ne:<value>}}```

### AND条件查询
```sql
db.name.find({key1:value1, key2:value2})
```

### OR条件查询
```sql
db.name.find({$or:[{key1:value1},{key2,value2}]})
```


</br>
</br>
</br>
</br>
## MongoDB Limit与Skip方法

### **Limit()方法**
读取指定数量的数据记录
```sql
db.name.find().limit(number)
```
示例：
> db.col.find({},{"title":1,_id:0}).limit(2)
> //{ "title" : "PHP 教程" }
> //{ "title" : "Java 教程" }

> <small>注：  如果没有指定参数，默认显示集合中所有数据</small>
### **Skip()方法**
跳过指定数量的数据
```sql
db.name.find().skip(number)
```

> <small>注：  如果没有指定参数，默认为0</small>


1.  $set  
2.  $gte
3.  $or
4.  $and
5.  $regx