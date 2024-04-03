## 常用常量

以下是Python的一些内置常量和在`sys`/`math`模块中的常见常量，以及它们的说明和使用示例：

| 常量名称 | 说明 | 使用示例 |
| ----------- | ----------- | ----------- |
| `None` | 表示一个空值或者是没有值的表示 | `a = None` |
| `True` | 布尔数据类型的真值 | `is_ok = True` |
| `False` | 布尔数据类型的假值 | `is_ok = False` |
| `math.pi` | 圆周率，通常用于计算中的圆的面积和圆周长度等等 | `import math; print(math.pi)` |
| `math.e` | 自然对数的底数，称为欧拉数。 | `import math; print(math.e)` |
| `math.tau` | τ 常量，等于2π。这是一个在数学中代表圆或周期性事物的常数。 | `import math; print(math.tau)` |
| `math.inf` | 正无穷大。 | `import math; print(math.inf)` |
| `math.nan` | “非数字”（Not a Number）的浮点表示。表示未定义的或者不可表示的值。 | `import math; print(math.nan)` |
| `sys.maxsize` | Python中“自然”整数的最大值。**如果要使用最小值，则是-sys.maxsize-1** | `import sys; print(sys.maxsize);print(-sys.maxsize-1)` |
| `sys.int_info` | Python整数的信息 | `import sys; print(sys.int_info)` |
| `sys.float_info` | Python浮点数的信息 | `import sys; print(sys.float_info)` |
| `sys.long_info` | Python长整失败的信息 | `import sys; print(sys.long_info)` |
| `sys.path` | Python的模块查找路径 | `import sys; print(sys.path)` |
| `sys.version_info` | Python解释器的版本信息 | `import sys; print(sys.version_info)` |
| `sys.modules` | Python所有导入的模块 | `import sys; print(sys.modules)` |
| `sys.platform` | Python运行的平台名称 | `import sys; print(sys.platform)` |

## 常用运算符

| 运算符 | 名称 | 说明 | 示例 | 示例结果 |
| :---: | :---: | :---: | :---: | :---: |
| `**` | 幂运算符 | 返回左操作数为基数、右操作数为指数的幂运算结果 | `2 ** 3` | 8 |
| `~` | 按位取反运算符 | 对数字的二进制表示进行按位取反操作 | `~2` | -3 |
| `/` | 除法运算符 | 返回两数相除的结果，结果为浮点数 | `10 / 3` | 3.3333333333333335 |
| `//` | 整除运算符 | 返回两数相除后向下取整的结果 | `10 // 3` | 3 |
| `%` | 取模运算符 | 返回两数相除的余数 | `10 % 3` | 1 |
| `!=` | 不等于运算符 | 比较值：如果两个操作数不相等，返回`True`，否则返回`False` | `2 != 3` | True |
| `is not` | 身份运算符 | 比较地址：用于比较两个对象的身份是否不相同，也就是它们是否不是同一个对象（不是同一块内存空间）。 | `[] is not []` | True |

## 常用数据结构及操作

### 内置数据结构（无需import）

#### list

| 操作 | 名称 | 说明 | 返回值 | 示例 | 示例结果 |
| :---: | :---: | :---: | :---: | :---: | :---: |
| `append()` | 添加元素 | 在列表的末尾添加一个元素 | None（操作修改了原列表） | `my_list = [1, 2, 3]; my_list.append(4); print(my_list)` | `[1, 2, 3, 4]` |
| `+` | 列表连接 | 将两个列表连接在一起形成一个新的列表 | 一个新列表 | `my_list = [1, 2, 3]; my_new_list = my_list + [4, 5]; print(my_new_list)` | `[1, 2, 3, 4, 5]` |
| `extend()` | 扩展列表 | 在一个列表的末尾一次性添加另一个列表中的多个值 | None（操作修改了原列表） | `my_list = [1, 2, 3]; my_list.extend([4, 5]); print(my_list)` | `[1, 2, 3, 4, 5]` |
| `remove()` | 删除元素 | 删除列表中的指定元素 | None（操作修改了原列表） | `my_list = [1, 2, 3]; my_list.remove(2); print(my_list)` | `[1, 3]` |
| `pop()` | 弹出元素 | 删除列表中指定位置的元素并返回该元素，如果没有指定索引，则删除最后一个元素 | 被删除的元素 | `my_list = [1, 2, 3]; popped_value = my_list.pop(1); print(my_list, popped_value)` | `[1, 3], 2` |
| `insert()` | 插入元素 | 在列表的指定位置插入一个元素 | None（操作修改了原列表） | `my_list = [1, 2, 3]; my_list.insert(1, 'a'); print(my_list)` | `[1, 'a', 2, 3]` |
| `count()` | 计数 | 计算列表中特定元素出现的次数 | 特定元素在列表中出现的次数 | `my_list = [1, 1, 2, 2, 2, 3, 3, 3, 3]; num_twos = my_list.count(2); print(num_twos)` | `3` |
| `sort()` | 排序 | 对列表的元素进行排序 | None（操作修改了原列表） | `my_list = [3, 1, 4, 1, 5, 9, 2]; my_list.sort(); print(my_list)` | `[1, 1, 2, 3, 4, 5, 9]` |
| `reverse()` | 反转 | 反转列表的元素的排列顺序 | None（操作修改了原列表） | `my_list = [1, 2, 3, 4, 5]; my_list.reverse(); print(my_list)` | `[5, 4, 3, 2, 1]` |

除了`+`和`pop()`运算符外，其他所有操作都会直接修改列表并不返回任何值。`+`会返回一个新的列表，而`pop()`会返回被删除的元素。

#### Tuple

Python中的元组（Tuple）是一种不可变的数据结构，这意味着一旦创建元组，就无法增加，修改或删除其元素。但是，元组中的可变对象（例如列表）的内容是可以修改的。以下是关于元组的各种操作的表格：

| 操作 | 名称 | 说明 | 返回值 | 示例 | 示例结果 |
| :---: | :---: | :---: | :--- | :---: | :---: |
| `t[1]` | 访问元素 | 通过索引返回元素 | 元组中的元素 | `t = (1, 2, 3); print(t[1])` | `2` |
| `t[1:3]` | 切割元组 | 返回元组的一部分 | 一个新元组 | `t = (1, 2, 3, 4, 5); print(t[1:3])` | `(2, 3)` |
| `t + t2` | 连接元组 | 连接两个元祖来创建一个新元组 | 一个新元组 | `t = (1, 2, 3); t2 = (4, 5, 6); print(t + t2)` | `(1, 2, 3, 4, 5, 6)` |
| `count()` | 计数 | 计算元组中特定元素出现的次数 | 计数值 | `t = (1, 2, 2, 3, 3, 3); print(t.count(2))` | `2` |
| `index()` | 索引 | 返回元组中特定元素首次出现的位置 | 索引值 | `t = (1, 2, 3, 2, 3, 3); print(t.index(2))` | `1` |

以下是关于元组的一些附加信息：

- 元组的元素不能修改，所以没有像`append()`或`extend()`这样的方法。
- 元组是有序的，因此它们支持索引和切割操作。
- 因为元组是不可变的，所以它们可以作为字典的键，反之列表不可以。

#### set

| 操作 | 名称 | 说明 | 返回值 | 示例 | 示例结果 |
| :---: | :---: | :---: | :---: | :---: | :---: |
| `add()` | 添加元素 | 在集合中添加元素 | None（操作修改了原集合） | `s = {1, 2, 3}; s.add(4); print(s)` | `{1, 2, 3, 4}` |
| `remove()` | 删除元素 | 从集合中删除元素，如果元素不存在则会引发KeyError。 | None（操作修改了原集合） | `s = {1, 2, 3}; s.remove(2); print(s)` | `{1, 3}` |
| `discard()` | 删除元素 | 从集合中删除元素，如果元素不存在，则不做任何操作 | None（操作修改了原集合） | `s = {1, 2, 3}; s.discard(2); print(s)` | `{1, 3}` |
| `pop()` | 删除并返回元素 | 删除并返回集合中的一个元素，如果集合为空，则返回KeyError | 被删除的元素 | `s = {1, 2, 3}; ele = s.pop(); print(s, ele)` | `{2, 3}, 1` （结果可能变化，因为set是无序的） |
| `clear()` | 清空集合 | 删除集合中的所有元素 | None（操作修改了原集合） | `s = {1, 2, 3}; s.clear(); print(s)` | `set()` |
| `union()` | 并集 | 返回包含两个集合所有元素的新集合 | 新集合 | `s1 = {1, 2, 3}; s2 = {3, 4, 5}; print(s1.union(s2))` | `{1, 2, 3, 4, 5}` |
| `intersection()` | 交集 | 返回两个集合的交集的新集合 | 新集合 | `s1 = {1, 2, 3}; s2 = {2, 3, 4}; print(s1.intersection(s2))` | `{2, 3}` |
| `difference()` | 差集 | 返回集合的差集的新集合，这就意味着它返回只在第一集合中存在的元素 | 新集合 | `s1 = {1, 2, 3}; s2 = {2, 3, 4}; print(s1.difference(s2))` | `{1}` |
| `symmetric_difference()` | 对称差集 | 返回两个集合的对称差集的新集合，即返回在两个集合中非共有元素集合 | 新集合 | `s1 = {1, 2, 3}; s2 = {2, 3, 4}; print(s1.symmetric_difference(s2))` | `{1, 4}` |

#### dict

| 操作 | 名称 | 说明 | 返回值 | 示例 | 示例结果 |
| :---: | :---: | :---: | :---: | :---: | :---: |
| `d[key]` | 访问元素 | 通过键获取值 | 键对应的值 | `d = {'a': 1, 'b': 2}; print(d['a'])` | `1` |
| `d.get(key)` | 获取元素 | 通过键获取值，如果键不存在则返回 None | 键对应的值或None | `d = {'a': 1, 'b': 2}; print(d.get('c'))` | `None` |
| `d[key] = value` | 修改/添加元素 | 通过键为字典添加或修改一个元素 | None（操作修改了原字典） | `d = {'a': 1, 'b': 2}; d['c'] = 3; print(d)` | `{'a': 1, 'b': 2, 'c': 3}` |
| `del d[key]` | 删除元素 | 删除字典中的一个元素 | None（操作修改了原字典） | `d = {'a': 1, 'b': 2}; del d['a']; print(d)` | `{'b': 2}` |
| `d.keys()` | 获取所有键 | 返回一个包含字典所有键的视图对象 | 视图对象 | `d = {'a': 1, 'b': 2}; print(d.keys())` | `dict_keys(['a', 'b'])` |
| `d.values()` | 获取所有值 | 返回一个包含字典所有值的视图对象 | 视图对象 | `d = {'a': 1, 'b': 2}; print(d.values())` | `dict_values([1, 2])` |
| `d.items()` | 获取所有键值对 | 返回一个包含所有 (键, 值) 元组的视图对象 | 视图对象 | `d = {'a': 1, 'b': 2}; print(d.items())` | `dict_items([('a', 1), ('b', 2)])` |
| `d.pop(key)` | 移除元素 | 删除并返回指定键的值，若键不存在则引发 KeyError | 被删除的键对应的值 | `d = {'a': 1, 'b': 2}; print(d.pop('b'))` | `2` |
| `d.clear()` | 清空字典 | 删除字典中的所有元素 | None（操作修改了原字典） | `d = {'a': 1, 'b': 2}; d.clear(); print(d)` | `{}` |

### 非内置数据结构（需要import）

#### collections
Python `collections` 模块提供了多种特殊的容器数据类型，作为Python内建数据类型的替代选项，如 `list, set, dict` 等。以下是几种常用的 `collections` 数据结构的操作：

##### **namedtuple** 
> from collections import namedtuple

| 操作 | 名称 | 说明 | 返回值 | 示例 | 示例结果 |
| :---: | :---: | :---: | :---: | :---: | :---: |
| - | 创建命名元组 | 创建一个包含名称的元组子类 | 新的命名元组 | `from collections import namedtuple;Point = namedtuple('Point', ['x', 'y']); p = Point(11, y=22); print(p)` | `Point(x=11, y=22)`|

##### **deque** 
> from collections import deque
> `collections.deque` 用于创建双端队列。
> **线程安全**

| 操作 | 名称 | 说明 | 返回值 | 示例 | 示例结果 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `deque([iterable[, maxlen]])` | 创建deque | 使用可迭代对象创建一个新的deque对象。如果指定了maxlen，则deque的长度固定为maxlen，否则deque长度可变。 | deque 对象 | `from collections import deque; d = deque(maxlen=3); d.extend([1,2,3,4]); print(d)` | `deque([2, 3, 4], maxlen=3)` |
| `d.append(x)` | 右侧添加元素 | 在deque的最右侧添加一个新元素。如果deque已满，将从左侧移除一个元素。 | None (原deque对象被改变) | `d = deque([1, 2, 3], maxlen=3); d.append(4); print(d)` | `deque([2, 3, 4], maxlen=3)` |
| `d.appendleft(x)` | 左侧添加元素 | 在deque的最左侧添加一个新元素。如果deque已满，将从右侧移除一个元素。 | None (原deque对象被改变) | `d = deque([1, 2, 3], maxlen=3); d.appendleft(4); print(d)` | `deque([4, 1, 2], maxlen=3)` |
| `d.pop()` | 右侧弹出元素 | 删除并返回deque的最右侧的元素。如果deque为空，则引发`IndexError`。 | deque的最右侧的元素 | `d = deque([1, 2, 3]); print(d.pop(), d)` | `3, deque([1, 2])` |
| `d.popleft()` | 左侧弹出元素 | 删除并返回deque的最左侧的元素。如果deque为空，则引发`IndexError`。 | deque的最左侧的元素 | `d = deque([1, 2, 3]); print(d.popleft(), d)` | `1, deque([2, 3])` |
| `d.extend(iterable)` | 右侧扩展 | 在deque的右侧添加iterable的元素。如果deque已满，将从左侧移除相应数量的元素。 | None (原deque对象被改变) | `d = deque([1, 2, 3], maxlen=5); d.extend([4, 5]); print(d)` | `deque([1, 2, 3, 4, 5], maxlen=5)` |
| `d.extendleft(iterable)` | 左侧扩展 | 在deque的左侧添加iterable的元素。如果deque已满，将从右侧移除相应数量的元素。注意，左侧扩展时元素会被逆序添加。| None (原deque对象被改变) | `d = deque([1, 2, 3], maxlen=5); d.extendleft([4, 5]); print(d)` | `deque([5, 4, 1, 2, 3], maxlen=5)` |
| `d.rotate(n)` | 旋转 | 向右旋转n步。如果n是负数，则向左旋转。 | None (原deque对象被改变) | `d = deque([1, 2, 3, 4, 5]); d.rotate(2); print(d)` | `deque([4, 5, 1, 2, 3])` |

选择使用deque而非list的理由：
- 高效的插入和删除操作：对于deque，在队列的两端插入或删除元素的操作复杂度是O(1)，而对于list，在列表的起始位置插入或删除元素需要O(n)的时间复杂度。这是因为list是基于数组的，所以在列表的起始位置插入或删除元素需要移动整个列表中的所有元素。
- 线程安全：deque设计为在多线程环境下从两端进行操作的线程安全数据结构，而list没有这样的特性。
支持最大长度：通过设置maxlen参数，deque可以限制队列的最大长度。在达到最大长度后，新的元素会替换掉最旧的元素。这对于实现特定长度的缓存或循环缓存非常有用。
- 更多的队列操作：deque设计为支持从两端添加和移出元素的数据结构，在这个意义上，它比list提供了更完整的队列操作。

##### **Counter**
> from collections import Counter
> `collections.Counter`是Python中的一个**字典子类**，用于计数可哈希的对象。
> **线程安全**

| 操作 | 名称 | 说明 | 返回值 | 示例 | 示例结果 |
| :---: | :---: | :---: | :---: | :---: | :---: |
| `Counter([iterable or mapping])` | 创建Counter对象 | 使用可迭代对象或映射创建一个Counter对象 | Counter 对象 | `from collections import Counter; c = Counter('gallahad'); print(c)` | `Counter({'a': 3, 'l': 2, 'g': 1, 'h': 1, 'd': 1})` |
| `c.elements()` | 返回元素 | 返回包含计数的元素迭代器 | 元素迭代器 | `c = Counter(a=3, b=2); print(list(c.elements()))` | `['a', 'a', 'a', 'b', 'b']` |
| `c.most_common([n])` | 常见元素 | 返回一个列表，其中包含n个最常见的元素及其对应的计数，降序排序。如果未指定n，返回计数器中所有元素的列表 | list | `c = Counter('abracadabra'); print(c.most_common(3))` | `[('a', 5), ('b', 2), ('r', 2)]` |
| `c.subtract([iterable or mapping])` | 剪除 | 从可迭代对象或映射中剔除元素 | None (原Counter对象被改变) | `c = Counter(a=3, b=2); c.subtract(Counter(a=1, b=2)); print(c)` | `Counter({'a': 2, 'b': 0})` |
| `+c` | 正数视图 | 创建一个新的Counter，其中只包含正数计数的元素 | Counter 对象 | `c = Counter(a=3, b=2, c=-1); print(+c)` | `Counter({'a': 3, 'b': 2})` |
| `-c` | 负数视图 | 创建一个新的Counter，其中只包含负数计数的元素 | Counter 对象 | `c = Counter(a=3, b=2, c=-1); print(-c)` | `Counter({'c': 1})` |

以上便是`collections.Counter`提供的主要操作及示例。

##### **OrderedDict** 
> from collections import OrderedDict
> `collections.OrderedDict`是Python中的一个字典子类，它可以记住其元素被添加的顺序。

| 操作 | 名称 | 说明 | 返回值 | 示例 | 示例结果 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `OrderedDict()` | 创建OrderedDict | 创建一个有序字典 | OrderedDict 对象 | `from collections import OrderedDict; od = OrderedDict();od["a"] = 1;od["b"] = 2;od["c"] = 3; print(od)` | `OrderedDict([('a', 1), ('b', 2), ('c', 3)])` |
| `od.popitem(last=True)` | 弹出元素 | 如果 last 为真，则删除并返回有序字典中的最后一个元素，否则删除并返回第一个元素 | pair(k, v) | `od = OrderedDict([('a', 1), ('b', 2), ('c', 3)]);print(od.popitem(last=False), od)` | `('a', 1) OrderedDict([('b', 2), ('c', 3)])` |
| `od.pop(k[,d])` | 弹出元素 | 如果字典中有键 k ，删除并返回 k 对应的值 v 。如果没有这个键，并且没有给出默认值 d ，则引发一个KeyError。 | v(default_value) | `od = OrderedDict([('a', 1), ('b', 2), ('c', 3)]); print(od.pop('b'),od); print(od.pop('d', 'default'),od)` | `2 OrderedDict([('a', 1), ('c', 3)])` <br> `default OrderedDict([('a', 1), ('c', 3)])` |
| `od.move_to_end(k, last=True)` | 移动元素至尾部或头部 | 将键为 k 的元素移动至有序字典的尾部（如果 last 为真），或头部（如果 last 为假）。如果元素不存在则引发 KeyError。 | None(原地操作) | `od = OrderedDict([('a', 1), ('b', 2), ('c', 3)]); od.move_to_end('b', last=False); print(od)` | `OrderedDict([('b', 2), ('a', 1), ('c', 3)])` |


##### **heapq**
> import heapq
> 
> `heapq` 提供了基于堆的（堆是一种特殊的树形数据结构：满足堆属性的二叉树）的排序算法。

| 操作 | 名称 | 说明 | 返回值 | 示例 | 示例结果 |
| :---: | :---: | :---: | :---: | :---: | :---: |
| `heappush()` | 添加元素 | 向堆中添加一个元素并保持堆的性质 | None（堆已被修改） | `from heapq import heappush, heappop; heap = []; heappush(heap, 3); heappush(heap, 2); heappush(heap, 5); print(heap)` | `[2, 3, 5]` |
| `heappop()` | 删除元素 | 从堆中删除并返回**最小**的元素，并保持堆的性质 | 堆中最小的元素 | `heap = [2, 3, 5]; print(heappop(heap), heap)` | `2, [3, 5]` |
| `heappushpop()` | 添加并删除元素 | 先向堆中添加一个新元素，然后删除并返回堆中最小的元素 | 堆中最小的元素 | `heap = [3, 5]; print(heappushpop(heap, 7), heap)` | `3, [5, 7]` |
| `heapify()` | 转换为堆 | 将列表转换为堆 | None（列表已被修改）| `from heapq import heapify; heap = [3, 1, 5, 8, 7]; heapify(heap); print(heap)` | `[1, 3, 5, 8, 7]` |

#### queue
> import queue
> 
> Python中的`Queue`，`PriorityQueue`和`LifoQueue`都属于`queue`模块，

| 操作 | 名称 | 说明 | 返回值 | 示例 | 示例结果 |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `Queue(maxsize)` | 创建Queue | 创建一个“先进先出”的队列。maxsize是队列中能保有的最大元素数。如果maxsize小于或等于零，队列大小是无限大。 | Queue 对象 | `from queue import Queue; q = Queue(); q.put(1); print(q.get())` | `1` |
| `LifoQueue(maxsize)` | 创建LifoQueue | 创建一个“后进先出”的队列。与 Queue 工作方式类似，但最后添加的元素将首先获取。| LifoQueue 对象 | `from queue import LifoQueue; lq = LifoQueue(); lq.put(1); lq.put(2); print(lq.get())` | `2` |
| `PriorityQueue(maxsize)` | 创建PriorityQueue | 创建一个优先级队列。优先级按元素的排序顺序确定。| PriorityQueue 对象 | `from queue import PriorityQueue; pq = PriorityQueue(); pq.put(2); pq.put(1); print(pq.get())` | `1` |
| `q.put(item, block=True, timeout=None)` | 入队 | 将一个元素添加入队列。如果队列已满，参数block设为True会让操作陷入阻塞状态，直到队列有空的位置。超时可以用timeout参数设置。 | None | `q = Queue(maxsize = 2); q.put(1); q.put(2); print(q.full())` | `True` |
| `q.get(block=True, timeout=None)` | 出队 | 从队列中删除并返回一个元素。如果队列为空，参数block设为True会让操作陷入阻塞状态，直到队列不空。超时可以用timeout参数设置。 | 元素 | `q = Queue(); q.put(1); print(q.get()` | `1` |
| `q.full()` | 检查是否满 | 如果队列满了返回True，否则返回False。 | 布尔值 | `q = Queue(maxsize = 2); q.put(1); q.put(2); print(q.full())` | `True` |
| `q.empty()` | 检查是否空 | 如果队列为空返回True，否则返回False。 | 布尔值 | `q = Queue(); print(q.empty())` | `True` |
| `q.qsize()` | 获取大小 | 返回队列的大小。 | 队列的大小 | `q = Queue(); q.put(1); print(q.qsize())` | `1` |

Queue、PriorityQueue 和 LifoQueue 中的`put()` 和 `get()` 方法默认设定为阻塞操作，意味着如果队列为空（满），`get()`（`put()`）就会等待，直到队列不为空（不满）为止。如果不想让它们阻塞，可以把`block`参数设为`False`，但这样在队列为空（满）的情况下，`get()`（`put()`）会抛出`Empty`（`Full`）异常。

## 常用内置方法

| 名称 | 说明 | 返回值 | 示例 | 示例输出 |
| :--- | :--- | :--- | :--- | :--- |
| `map()` | 对可迭代对象中的每个元素应用函数 | 一个迭代器，其元素为应用函数后的结果 | `result = map(lambda x: x**2, [1,2,3,4]); print(list(result))` | `[1, 4, 9, 16]` |
| `zip()` | 构造一个迭代器，聚合来自每个可迭代对象的元素 | 一个迭代器，其元素为元组 | `result = zip(['a', 'b'], [1, 2]); print(list(result))` | `[('a', 1), ('b', 2)]` |
| `any()` | 检查可迭代对象是否有任何元素为True | 布尔值 | `result = any([False, 0, None, [], {}, '']); print(result)` | `False` |
| `enumerate()` | 对一个可迭代对象的元素配对一个索引值 | 一个迭代器，其元素为元组（索引，元素） | `result = enumerate(['a', 'b'], start=1); print(list(result))` | `[(1, 'a'), (2, 'b')]` |
| `filter()` | 使用函数筛选可迭代对象的元素 | 一个迭代器，其元素为函数返回True的元素 | `result = filter(lambda x: x%2==0, [1,2,3,4]); print(list(result))` | `[2, 4]` |
| `ord()` | 返回一个字符的Unicode数值 | 整数 | `result = ord('a'); print(result)` | `97` |
| `chr()` | 返回Unicode数值对应的字符 | 字符串 | `result = chr(97); print(result)` | `a` |
| `sorted()` | 返回一个根据任意指定比较函数进行排序的新列表 | 列表 | `result = sorted([3, 1, 4, 1, 5, 9], reverse=True); print(result)` | `[9, 5, 4, 3, 1, 1]` |
| `round()` | 四舍五入到给定的精度 | 数字 | `result = round(10.6783, 2); print(result)` | `10.68` |
| `all()` | 如果所有的值都为True，返回True | 布尔值 | `result = all([True, 1, 's']); print(result)` | `True` |
| `reversed()` | 返回一个反向的迭代器 | 迭代器 | `result = reversed([1, 2, 3, 4]); print(list(result))` | `[4, 3, 2, 1]` |

以上都是调用时立即执行的函数。`map()`和`filter()`如果在Python3.x中返回迭代器，需要通过`list()`或其他方式转换才能看到所有的结果。虽然`map()`、`zip()`、`filter()`等返回的是迭代器，这些函数仍然是立即执行的，没有实现惰性计算。

## 杂项
1. `assert`可以接收两个参数，第二个参数是失败时提供的错误信息。如`assert self.max_height == 3, "Unexpected max height"`
2. 用`raise`抛出异常时，选择内置的异常类型无需进行额外导入。如`raise(Exception('this is wrong'))`或`raise(ValueError('this is wrong'))
3. 用`help()`和`dir()`列出某个包所包含的全部函数和常量
