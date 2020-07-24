### vue-router query和params传参区别

- query方式传参和接收方式

```
    //跳转传参
    this.$router.push({
        path:'',
        query:{
            id:id
        }
    })

    //跳转后的页面的接收
    this.$route.query.id
```

 this.$router 为vue-router实例
 $route 为当前router跳转对象
 另外：query相当于get请求，页面跳转的时候，可以在地址栏看到请求参数

- params方式传参和接收方式

```
    //传参
    this.$router.push({
        name:'',
        params:{
            id:id
        }
    })

    //跳转页面的接收
    this.$route.param.id
```
 注意：params传参，push里面只能是 name:'',不能是path:'/xxx'
 而：params相当于post请求，参数不会再地址栏中显示
