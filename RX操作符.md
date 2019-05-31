### RX操作符

-------------------------

> `io.reactivex.Flowable` : 事件源(0..N个元素), 支持 Reactive-Streams and 背压

> `io.reactivex.Observable`:事件源(0..N个元素), 不支持背压

> `io.reactivex.Single`: 仅发射一个元素或产生error的事件源，

> `io.reactivex.Completable`: 不发射任何元素，只产生completion或error的事件源

> `io.reactivex.Maybe`: 不发射任何元素，或只发射一个元素，或产生error的事件源

> `Subject`: 既是事件源，也是事件接受者

![img](https://upload-images.jianshu.io/upload_images/1460006-33372e44a2d58fdc.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/700) 

##### 1.创建操作符 

* create

  创建单一observable

* from

  从数组,list中创建多个observable

* just

  创建多个obervable

##### 2.转换操作符 

* map

  通过一个函数将一个Observable发射的item逐个进行某种转换

* flatMap

  flatMap()处理集合、数组等，map()处理单一对象数据 

* buffer

  ①**时间**:Buffer操作符定期收集Observable的数据放进一个数据包裹，然后发射这些数据包裹，而不是一次发射一个值 

  ②**个数**:将原发射出来的数据已count为单元打包之后在分别发射出来 

* groupBy

  将observable分组后发送

##### 3.过滤操作符 

* filter

  Filter返回满足过滤条件的数据 

* first

  返回第一条数据或者满足条件的第一条数据

* last

  返回最后一条数据或者满足条件的最后一条数据

* skip

  Skip操作符将源Observable发射的数据过滤掉前n项 

* take

  Take操作符只取前n项 

* ofType

  过滤指定类型的数据

* distinct

  去除重复数据

* debounce

  发射数据时，如果两次数据的发射间隔小于指定时间，就会丢弃前一次的数据,直到指定时间内都没有新数据发射时 

* sample

  定期发射Observable最近的数据 

* timeout

  如果原始Observable过了指定的一段时长没有发射任何数据，就发射一个异常或者使用备用的Observable 

##### 4.组合操作符 

* zip

  zip操作符的作用是把多个源`Observable`发射的item通过特定函数组合在一起，然后发射组合后的item。从图中还可以看到一个重要的信息是，最终发射的item是对上面的两个源`Observable`发射的item按照发射顺序逐个组合的结果，而且最终发射的`1A`等item的发射时间是由组合它的`1`和`A`等item中发射时间较晚的那个item决定的，也正是如此，`zip`操作符经常可以用在需要同时组合处理多个网络请求的结果的业务场景中

* concat

  按顺序连接多个Observables 

* startWith

  在数据序列的开头增加一项数据。`startWith`的内部也是调用了`concat` 

* 

##### 5.错误处理符 

##### 6.辅助操作符 

##### 7.条件和布尔操作符 

* all

  判断所有的数据项是否满足某个条件 


##### 8.算数和聚合操作符 

##### 9.连接操作符 

##### 10.转变操作符

