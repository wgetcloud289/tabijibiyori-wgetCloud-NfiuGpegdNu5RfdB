[合集 \- Go语言学习(29\)](https://github.com)[1\.Go面经 \| 成都Go面试这么卷？卷王介绍：游戏行业 3年经验 20k\+2023\-08\-10](https://github.com/wangzhongyang/p/17620444.html)[2\.这些负载均衡都解决哪些问题？服务、网关、NGINX2023\-10\-07](https://github.com/wangzhongyang/p/17746631.html)[3\.Golang后端大厂面经！2023\-10\-30](https://github.com/wangzhongyang/p/17798074.html)[4\.Golang面试题从浅入深高频必刷「2023版」2023\-11\-06](https://github.com/wangzhongyang/p/17812372.html)[5\.避免defer陷阱：拆解延迟语句，掌握正确使用方法2023\-11\-16](https://github.com/wangzhongyang/p/17835888.html)[6\.听说90%的人都没搞定手撕协程池这道面试题！2023\-11\-22](https://github.com/wangzhongyang/p/17849157.html)[7\.数据库面试题从浅入深高频必刷「2024版」2023\-12\-01](https://github.com/wangzhongyang/p/17869263.html)[8\.一文搞懂Go GC演进史，讲的太细致了！2023\-12\-29](https://github.com/wangzhongyang/p/17934143.html)[9\.据说这道Go面试题90%的人都搞错了！01\-25](https://github.com/wangzhongyang/p/17987862)[10\.那位拿了多个Offer的大佬分享了最新Go面经03\-26](https://github.com/wangzhongyang/p/18096739)[11\.第一次面字节，一面很简单，二面被疯狂拷打！04\-08](https://github.com/wangzhongyang/p/18121516)[12\.心态崩了，约了半个月，就只有3个面试！04\-09](https://github.com/wangzhongyang/p/18123159)[13\.多高的学历才能轻松找到工作？这个热点有点扯吧\~04\-18](https://github.com/wangzhongyang/p/18143029)[14\.抢先看！美团、京东、360等大厂面试题解析，技术面试必备。04\-24](https://github.com/wangzhongyang/p/18154513):[veee加速器](https://liuyunzhuge.com)[15\.Go\-Zero从0到1实现微服务项目开发（二）04\-29](https://github.com/wangzhongyang/p/18165381)[16\.阿里实习生：面试阿里其实并没有那么难。05\-06](https://github.com/wangzhongyang/p/18174345)[17\.腾讯互娱面经，希望别凉05\-11](https://github.com/wangzhongyang/p/18186035)[18\.腾讯、阿里、B站最新面经汇总，有的妥妥的凉经。05\-13](https://github.com/wangzhongyang/p/18188646)[19\.Go\-Zero定义API实战：探索API语法规范与最佳实践（五）05\-14](https://github.com/wangzhongyang/p/18191472)[20\.工作卷，是主动选择还是迫于无奈？05\-15](https://github.com/wangzhongyang/p/18192763)[21\.腾讯、阿里、B站最新面经汇总，有的妥妥的凉经05\-16](https://github.com/wangzhongyang/p/18195961)[22\.大厂边缘组VS小厂核心组，要怎么选？06\-03](https://github.com/wangzhongyang/p/18228160)[23\.这么简单的问题都不会，那还面试什么！？06\-13](https://github.com/wangzhongyang/p/18246131)[24\.百度的面试，你觉得难度怎么样？07\-03](https://github.com/wangzhongyang/p/18280764)[25\.腾讯特别调薪8%，年底十三薪分摊到月薪：福利升级还是另有深意？07\-16](https://github.com/wangzhongyang/p/18305908)[26\.现在有什么赛道可以干到退休？07\-29](https://github.com/wangzhongyang/p/18329477)[27\.深入解析 Go 语言 GMP 模型：并发编程的核心机制07\-30](https://github.com/wangzhongyang/p/18332142)[28\.什么情况下你能接受 99608\-01](https://github.com/wangzhongyang/p/18336108)29\.Go 必知必会：探索 Go 语言中的数组和切片深入理解顺序集合09\-03收起
**文末有面经共享群**


在 Go 语言的丰富数据类型中，数组和切片是处理有序数据集合的强大工具，它们允许开发者以连续的内存块来存储和管理相同类型的多个元素。无论是在处理大量数据时的性能优化，还是在实现算法时对数据结构的需求，数组和切片都扮演着至关重要的角色。


# Go 语言中的数组


在 Go 语言中，数组是一种基本的数据结构，用于存储具有相同类型元素的集合。数组与切片（slice）不同，数组的长度是固定的，一旦声明就不可改变，并且是数组类型定义的一部分，这意味着数组的类型不仅包括元素的类型，还包括其长度。


## 定义


定义数组时，必须指定元素的类型和数组的长度。例如，`[3]bool` 表示一个布尔类型的数组，长度为 3；`[4]int` 表示一个整型的数组，长度为 4。



```
var a1 [3]bool
var a2 [4]int

fmt.Printf("a1:%T\na2:%T\n", a1, a2)

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=Y2YzZWU5ODZkZTU1MWQyZjljZWE5NmRmNmZmZGY0NmNfcE1vUURHdEhyZ3JkcEN4dzRJRWpQM0R3NDF2OG41R1dfVG9rZW46UXRLQWJHaXVpb2NkVzh4a1c1bmN2QTVzbnBkXzE3MjUzMjg4OTI6MTcyNTMzMjQ5Ml9WNA)


## 数组初始化


### 默认值


定义数组时如果不进行初始化，默认元素就是零值：bool 类型的 false、整型和浮点类型的 0、字符串的空串" "。



```
var a1 [3]bool 
var a2 [4]int

fmt.Println(a1, a2)

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=ZjVjMzU1M2E3NDcyMjcyOWM5Y2I5ZGY5OGNlNjJkOTRfVGVWcm5DTFdRSzBWeXB2SlVOaGZjR1JhdFZxNkpQdzBfVG9rZW46Q3BlZmJYcVVUb3dOdXV4aDM0bWNVZ3g0bmtnXzE3MjUzMjg4OTI6MTcyNTMzMjQ5Ml9WNA)


### 初始化方式 1：在大括号中定义好和长度一致的值


最简单的初始化方式：



```
var a1 [3]bool 
a1 = [3]bool{true,false,false}
fmt.Println(a1)

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=NGM0NmYwNjZhZGM2YWZjYzE4YmZmMTFkZjJhYmU3YmFfbUZPanlDdFFzNHJLY3hOcUxPdUhzMWI3bjQwWkh3SGJfVG9rZW46SFdtNGJBRmRhbzE1cVZ4Q0VjUGM3MzFYblZiXzE3MjUzMjg4OTI6MTcyNTMzMjQ5Ml9WNA)


### 初始化方式 2：根据初始值自动判断数组的长度


在中括号中写明长度，当定义的数值个数比长度小时，会用默认值补齐，比如 0、false、""。



```
a8 := [10]int{0, 1, 2, 3, 4, 5, 6, 7}  //7后面会用0补齐
fmt.Println(a8)

```

打印结果： \[0 1 2 3 4 5 6 7 0 0]。


**\[...]的用法**：\[...]设置数组长度时，会根据初始值自动判断数组的长度。



```
aa := [...]int{0, 1, 2, 3, 4, 5, 6, 7} //[...]根据初始值自动判断数组的长度
fmt.Println(aa)

```

打印结果：\[0 1 2 3 4 5 6 7]。


### 初始化方式 3：根据索引初始化


指定索引对应的值，未指定索引的值会用默认值填充，比如 0、false、""。



```
a3 := [5]int{0: 1, 4: 2} //根据索引初始化
fmt.Println(a3)

```

打印结果：\[1 0 0 0 2]。


## 取值


### 遍历数组


你可以使用一个标准的 `for` 循环来遍历数组的每个元素。这种方法需要你手动管理索引变量，并使用它来访问数组中的元素。


For i 循环遍历数组：



```
citys := [...]string{"北京", "上海", "深圳"} //索引从0到2
// 根据索引遍历
for i := 0; i < len(citys); i++ {
   fmt.Println(citys[i])
}

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=YTBjM2Y2MDIwZDI0YWU4NzJkYTU0ODA3NmIyMjlmZmNfN09aemplaUo2NUJZYk1TZ1JjbVE1V3RZS2Vpb3RXRmhfVG9rZW46TUprWWJJdUwwb2VTS0l4U2NSa2NBNjZwbmtnXzE3MjUzMjg4OTI6MTcyNTMzMjQ5Ml9WNA)


`for range` 是一种更简洁的遍历数组或切片的语法。`for range` 循环会自动生成索引和元素值，使得遍历过程更加简单。



```
citys := [...]string{"北京", "上海", "深圳"} //索引从0到2
for i, city := range citys {
   fmt.Printf("key值：%d 城市为：%v\n", i, city)
}

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=ZDRiZjg5MzNmNDE4Mjc2ODcxZjQxYzEzMWRiZTk1YWRfMmlKaXZweG51ZVNMeks1bHhydm9TMjRBa29zdzVhaW5fVG9rZW46U2ZBTGJiYmpob1BqaGR4emUwbWNkcGRWbkVmXzE3MjUzMjg4OTI6MTcyNTMzMjQ5Ml9WNA)


## 多维数组


### 定义


我们以二维数组举例，比如定义 `[[1 2 3][4 5 6]]` 这样的二维数组，要怎么定义呢？


示例如下：


1. 下面代码中的第一个长度单位\[2]，表示二维数组的有几个元素；
2. 第二个长度单位\[3]，表示子集数组中有几个元素；
3. 初始化的时候：变量 \= 数组类型{}。



```
//定义多维数组
var a11 [2][3]int

//初始化多维数组
a11 = [2][3]int{
   [3]int{1, 2, 3},
   [3]int{4, 5, 6}, //注意：最后这个也要加逗号分隔
}

fmt.Println(a11)

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=NmI1OWQxMzAyMDllMDJmYzFjMWU4ODIzODhlMTFlYzZfZ1d1TVRZQWpMcFllMGpTenBlR2xSRFZRNHF0cFh0TzJfVG9rZW46QUMwMmI3MzhUb09Zcmx4cnNLOGNxYm4zblJ5XzE3MjUzMjg4OTI6MTcyNTMzMjQ5Ml9WNA)


### 取值


多维数组的遍历：



```
//定义多维数组
var a11 [2][3]int

//初始化多维数组
a11 = [2][3]int{
   [3]int{1, 2, 3},
   [3]int{4, 5, 6}, //注意：最后这个也要加逗号分隔
}

//双重for range遍历取值
for _, v1 := range a11 {
   fmt.Println(v1)
   for _, v2 := range v1 {
      fmt.Println(v2)
   }
}

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=YjVlZTNlY2E1N2ZkYmU3ZGRlYTFmZDRhMDIwNDBhNDlfRjUyM2ZuS0dyWXJOUVpzYlA0S0ZOWDJjb2toUHZJc1lfVG9rZW46Q0h6WGJYblBNb1JKeFp4bEZhZGMyOUhDblNjXzE3MjUzMjg4OTI6MTcyNTMzMjQ5Ml9WNA)


## 数组特点：值类型不是引用类型


我们发现把 b 1 赋值给 b 2，再修改 b 2 的值，b 1 的值并没有改变，这是数组和切片最大的区别，建议你再对比学习一下切片的知识点。



```
b1 := [3]int{1, 2, 3}
b2 := b1
b2[0] = 100
fmt.Println(b1,b2)

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=ZDBjZWE3MzQxNGNmNjU0NGUyYjFhNGFmMzJhNjgzMmRfZ2I5WHZaUmtCZ0FQWHo4OGRoVXVhUHEzN0xUSnN6Z1pfVG9rZW46WkFITmJwbjlkb0xDZ2R4ZXFrdGNjVWhCbjZiXzE3MjUzMjg4OTI6MTcyNTMzMjQ5Ml9WNA)


总结：说明 Go 的数组是值类型，不是引用类型 `b2:=b1` 的操作，给 b 2 开辟了新的内存空间，而不是引用 b 1 的内存地址。


## 数组实战


求数组 cArray\[1，3，5，7，8]所有元素之和：



```
cArray := [...]int{1, 3, 5, 7, 8}
r := 0
for _, i2 := range cArray {
   r += i2
}
fmt.Printf("相加结果为：%v", r)

```

打印结果：`相加结果为：24`。


求出 cArray 数组中，和为 8 的下标，比如\[0 3]和\[1 2]：



```
for i := 0; i < len(cArray); i++ {
   for j := 0; j < i; j++ {
      if cArray[i]+cArray[j] == 8 {
         fmt.Printf("符合的下标为：%v,%v \n", j, i)
      }
   }
}

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=N2ZlM2VmZmVkNWMxNTM2MTg1ZjU4YTBlOWRlZGI1ODJfcFE1NDc5Zmg3TXQ0RGZHYnZVaXd2TlAwQzdqTGFOOFFfVG9rZW46RVEya2JRYWtkb3FkNG54Vzc0SGMzSEpVbnNnXzE3MjUzMjg4OTI6MTcyNTMzMjQ5Ml9WNA)


# Go 语言中的切片


切片区别于数组，是引用类型，不是值类型。数组是固定长度的，而切片长度是可变的，我的理解是：切片是对数组一个片段的引用。


## 定义


切片（slice）是一种灵活的序列类型，它基于数组；与数组不同，切片的长度是可变的，并且不包含在类型定义中。例如，`[]int` 表示一个存放整数类型元素的切片，`[]string` 表示一个存放字符串类型元素的切片。



```
var s1 []int 
var s2 []string 
fmt.Println(s1, s2)
fmt.Println(s1 == nil) //true  为空  没有开辟内存空间
fmt.Println(s2 == nil) //true

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=MWEwOWEzMGZiY2NmNGY4OGU1NzJmM2U2MDc4YTcyYmNfUW40Y2FNemViUEtXVU9jM2wyVDM5Y3FoM1pYSFhyeFRfVG9rZW46SDFnRWJieXpMb1huSTF4TU5QWWNzeENCbmplXzE3MjUzMjg4OTI6MTcyNTMzMjQ5Ml9WNA)


解析：这意味着 `s1` 和 `s2` 目前不指向任何实际的内存空间，它们是“空”的切片。在 Go 语言中，当切片被声明但未初始化时，它们的默认值就是 `nil`。`nil` 是一个表示“无”或“空”的特殊值，对于切片来说，它表示切片没有底层数组，也没有长度和容量。因此，尝试访问或修改一个 `nil` 切片的元素将会导致运行时错误。


## 声明并初始化


我们可以在声明的同时初始化：



```
var s1 = []int{1, 2, 3}
var s2 = []string{"北苑", "长阳", "望京"}
fmt.Println(s1, s2)
fmt.Println(s1 == nil) //false
fmt.Println(s2 == nil) //false

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=YjE0Y2VlMzBmN2I3ZmJkZWE3YTg0NzIyNDIwZTQ0OGNfc1B6eWNITzdkY0dHSDZoekZyMExLN3hPZnFxd0FycmVfVG9rZW46WDlzV2JxUlhMb2JpMkV4bXIwUGNLa1ZlbmFoXzE3MjUzMjg4OTI6MTcyNTMzMjQ5Ml9WNA)


解析：初始化成功，`s1` 和 `s2` 的值都不等于 `nil`。


## 长度和容量


分别使用 len ()、cap () 获得切片的长度和容量。



```
fmt.Printf("len(s1):%d cap(s1):%d\n", len(s1), cap(s1))
fmt.Printf("len(s2):%d cap(s2):%d\n", len(s2), cap(s2))

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=Mzc4MjllNzA0ZjhmZDYzM2Q3MmYzOGUyOGQzYzFjOGFfZ3VRT1QzVnpMZEhEOFZDcHpZV2xaNjVTT0xBYklDWWVfVG9rZW46QnFBWmJwUFhTbzNQc3h4RnNYU2NETVdUbmpmXzE3MjUzMjg4OTI6MTcyNTMzMjQ5Ml9WNA)


解析：和我们预期的一致，长度和容量都为 3。


## 由数组得到切片


开篇我已经提到数组和切片的关系，这里再进一步讲一下：


1. 切片的本质是操作数组，只是数组是固定长度的，而切片的长度可变的；
2. 切片是引用类型，可以理解为引用数组的一个片段；而数组是值类型，把数组 A 赋值给数组 B，会为数组 B 开辟新的内存空间，修改数组 B 的值并不会影响数组 A；
3. 而切片作为引用类型，指向同一个内存地址，是会互相影响的。



```
//定义一个数组
a1 := [...]int{1, 2, 3, 4, 5, 6, 7, 8, 9}
s3 := a1[0:4] //基于一个数组切割  [0:4]左包含 右不包含  即为[1,2,3,4]
fmt.Println(s3)

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=ZDEzYjAyNDc3ZWE4MGU4MGZiMTEyYTE4NWQ4MWMxMmJfRHk3anp1ZHhkY1liOXNyQUtoSnBLTlNteENCV1hLSE5fVG9rZW46U3RjSWJJNHhEb05hbFB4VUZqZWNJYlFZbmlkXzE3MjUzMjg4OTI6MTcyNTMzMjQ5Ml9WNA)



> 注意：`a1[0:4]` 是一个切片表达式，它基于数组 `a1` 创建了一个新的切片，包含了数组中索引从 `0` 到 `3` 的元素，上面示例中就是{1, 2, 3, 4}。


### 更多切割方式举例


切片提供了多种切割方式，这些方式允许你灵活地操作和访问数组或其他切片的部分元素。以下是一些常见的切片切割方式的例子：



```
a1 := [...]int{1, 2, 3, 4, 5, 6, 7, 8, 9}
s4 := a1[2:4] //[3 4]
s5 := a1[:4] //[1 2 3 4]
s6 := a1[2:] //[3 4 5 6 7 8 9]
s7 := a1[:]  //[1 2 3 4 5 6 7 8 9]
fmt.Println(s4)
fmt.Println(s5)
fmt.Println(s6)
fmt.Println(s7)

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=Zjk3MDYzOGIzNDI5MjE1ZGZhNDBhMTUwMDIyZGUyMTdfWGxYWlpYeU1lMk5yT3U3SGNnelJCdThSUkI4RVN2cXpfVG9rZW46VzFxS2JhbjRIb3V0R0l4NTBsamNrUDBybnRlXzE3MjUzMjg4OTI6MTcyNTMzMjQ5Ml9WNA)


解析：切片操作 `s4` 从索引 2 开始到索引 4（左闭右开），`s5` 默认从索引 0 开始截取，`s6` 截取到最后一个元素，而 `s7` 省略了索引，表示获取全部元素，所有这些切片操作都遵循左包含右不包含的原则。


### 切片的长度和容量


切片的长度很好理解，就是元素的个数。


切片的容量我们重点理解一下：**在切片引用的底层数组中从切片的第一个元素到数组最后一个元素的长度就是切片的容量\*\*\*\*。**


我来画个图：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=ZDgzYTU0ZjU4Y2FjZDg0NTU5MzdiOWQ2OGQ0YjliNjRfcmtsc09DaTdQNHlxZlJyMXJqb2dZYzg0QXNxOFRkOU5fVG9rZW46Qzh0WmJxY1Nwb2lxT1F4ZFJnUWMxdk9kbkN0XzE3MjUzMjg4OTI6MTcyNTMzMjQ5Ml9WNA)


我们再看下面这个例子就很好理解了：



```
a1 := [...]int{1, 2, 3, 4, 5, 6, 7, 8, 9}

s5 := a1[:4] //[1 2 3 4]
s6 := a1[2:] //[3 4 5 6 7 8 9]
s7 := a1[:]  //[1 2 3 4 5 6 7 8 9]

fmt.Printf("len(s5):%d cap(s5):%d\n", len(s5), cap(s5)) //4 9
fmt.Printf("len(s6):%d cap(s6):%d\n", len(s6), cap(s6)) //7 7
fmt.Printf("len(s7):%d cap(s7):%d\n", len(s7), cap(s7)) //9 9

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=MDdjMjI1MWI3ZWIwMjE0NTI1MTdmNGY1N2Y5YWViNmRfMWNYTkpLanoxTFJEdlF0b3d1U2UzZk0wRmpYU0ZiUk1fVG9rZW46UmlIRGI4d1RBb2hsZjl4U0o5aGMzZ0s2blpiXzE3MjUzMjg4OTI6MTcyNTMzMjQ5Ml9WNA)


解析：a 1 是数组长度为 9，容量也为 9，值是从 1\~9。


S 5/s 6/s 7 都是切割数组 a 1 得到的切片。


S 5 的长度为 4，因为只有 1 2 3 4 这 4 个元素，容量为 9，因为 s 5 切片是从数组起始位置开始切割的：第一个元素是 1，而 s 5 底层数组 a 1 最后一个元素是 9，1\~9 共 9 个元素，所以 s 5 的容量为 9。


S 6 的长度为 7，因为 s 6 的元素是 3\~9 这 7 个元素；容量也为 7，因为 s 5 的底层数组最后一个元素是 9，3\~9 共 7 个元素，所以 s 6 的容量为 7。


S 7 更好理解了，长度和容量都是 9，小伙伴们自己理解一下。


### 切片再切片


我们可以对切片进行再切片操作，比如，针对上面的数据再次切片进行测试：



```
s8 :=s6[3:]
//s8的值为：6 7 8 9
fmt.Printf("len(s8):%d cap(s8):%d\n", len(s8), cap(s8)) //4 4

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=MjVlNTFmMjU4NmIxN2RjNjJiMGVlMjY0YTMyYjIxMzVfRGs3YXA0a2ZEWTBFcDIyV3FHRG9hN3FsOUZPRnlSMFdfVG9rZW46VVFKMGJJRFJNb3R4d3p4dUVpRmNyWTZpbngxXzE3MjUzMjg4OTM6MTcyNTMzMjQ5M19WNA)


解析：我们知道可以对切片进行再次切片就可以，至于长度和容器大家搞明白上面的例子，这个输出结果就是意料之中的了。


## 切片特点：引用类型不是值类型


我们举个例子来证明切片是引用类型：



```
//定义数组
a1 := [...]int{1, 2, 3, 4, 5, 6, 7, 8, 9}
//由数组切割成切片s6
s6 := a1[2:] //[3 4 5 6 7 8 9]
//切片再次切片，赋值给s8
s8 :=s6[3:] //[6 7 8 9]
//修改原始数组，把下标为2的值由3改为333
a1[2] = 333
//打印s6，发现s6中的3也变成了333
fmt.Println("s6:", s6) //[333 4 5 6 7 8 9]
//因为s8基于s6切片而成，我们测试一下切片再切片的引用传的
fmt.Println("s8:", s8) //[6 7 8 9]
//我们把原始数组下标为5的值由6改为666
a1[5] = 666
//打印s8切片，得到结果6也变成了666
fmt.Println("s8:", s8) //[666 7 8 9]

```

打印结果如下：


![](https://awq7m8b63wy.feishu.cn/space/api/box/stream/download/asynccode/?code=ZjljMWQ4YzYxMjk5MDUwZGQ4ZmJjOWUzNGZhNDJlNGJfOWh3TGdXQWd3eG5EOU1Vb3doQmdLR3ludUFuY2d4VGZfVG9rZW46UnM5VGJrOW9tb25RaWF4WlFLT2NQVlR5bmtlXzE3MjUzMjg4OTM6MTcyNTMzMjQ5M19WNA)


解析：**由此我们可以明确的知道切片是引用类型，当底层数组改变时，不管是切片，还是切片再切片，值都会改变。因为他们使用的是一个内存块，引用的一个内存地址。**


# 总结


Go 语言的数组和切片各有特点：


1. 数组适合于长度固定且已知的场景，而切片则提供了更大的灵活性，特别是在处理动态大小的数据集合时；
2. 数组作为值类型，在赋值和函数传递时会复制数据，保证了数据的独立性；而切片作为引用类型，多个切片变量可能指向同一个底层数组，因此在操作时要特别注意对底层数据的影响。


## 欢迎关注 ❤


我们搞了一个免费的面试真题共享群，互通有无，一起刷题进步。


没准能让你能刷到自己意向公司的最新面试题呢。


感兴趣的朋友们可以加我微信：wangzhongyang1993，备注：【博客园】。


