#数组
### chhuang at live.cn
##数组初始化的方法：
1. `String[] name = new String[] {"Aidan", "Grant"};`
2. `var name = new String[] {"Aidan", "Grant"};` (隐式类型的局部变量）
3. `var name = new [] {"Aidan", "Grant"};`（让编译器推倒数组元素的类型）
4. *`var name = new [] {"Aidan", "Grant", 123};`* (不能通过编译，**error CS0826: 找不到隐式类型数组的最佳类型**，创建`Object`数组的装箱操作代价太高，所以选择编译器报错）
5. `String[] name =  {"Aidan", "Grant"};`
6. *`var name =  {"Aidan", "Grant"};`* (不能通过编译，编译器需要做的事情太多，所以选择编译器错误）

##接口
**所有数组都隐式派生自System.Array**，因此所有System.Array定义的方法和属性都可用。

**所有数组都隐式实现`IEnumerable`，`ICollection`，`IList`接口**，如果是一个*一维0基数组*，CLR还会自动为数组类型的所有**基类型**实现`IEnumerable<T>`, `ICollection<T>`, `IList<T>`接口。

