### Array数组对象


Array.filter、Array.forEach、Array.map、Array.reduce

* 区别
  * forEach没有返回值，重点是function里面处理逻辑
  *  map有返回值，重点是function返回值，组成新数组
  * filter有返回值，重点是function返回值，过滤之后组成新数组
  *  reduce有返回值，重点是计算数组，返回一个值

* 介绍

Array.filter

    语法

    ```
    var new_arr = arr.filter(callback(element, index, array){

    }, this)

    ```
    
    参数

    callback 回调
        element 当前的value
        index   当前的索引值
        array   arr这个数组对象
    this 回调的this指向


    返回值

    Array 类型
    //符合条件的值组成的数组

Array.forEach

    ```
    arr.forEach(callback(element, index, array){

    }, this)

    ```

    参数
    callback 回调
        element 当前的value
        index   当前的索引值
        array   arr这个数组对象
    this 回调的this指向
    返回值
    undefined
    // 这个东西没有返回值



Array.map

    ```
    arr.map(callback(element, index, array){

    }, this)
    ```


    参数
    callback 回调
        element 当前的value
        index   当前的索引值
        array   arr这个数组对象
    this 回调的this指向


    返回值
    array 数组
    // 每个回调的返回值组成的新数组


Array.reduce

    ```
    arr.reduce(callback(accumulator, element, index, array){

    }, initialValue)

    ```

    参数

    callback 回调
        sum     累加器的返回值，也就是上一次回调的返回值
        element 当前的value
        index   当前的索引值
        array   arr这个数组对象
    initialValue 初始传入的值，如果不传回调从下标1开始，下标0作为初始值

    返回值
    //返回最后一次回调的值
    用法
    //累加

    ```
    
    [10,11,12,13].reduce((s,v)=>s+v,0)

    ```
    
    场景
    这个计算整个数组得出一个值的