### 常用的Time代码


```
/**
 * 获取当前时间
 */
function getDate() {
    return new Date();
}

/**
 * 格式化当前时间
 * @param {*} value 
 */
function getFormatDate(value) {
    var date = new Date(value);
    var year = date.getFullYear();
    var month = date.getMonth() + 1;
    month = month < 9 ? '0'+ month : month
    var day = date.getDate();
    day = day < 9 ? '0'+ day : day
    var hours = date.getHours();
    hours = hours < 9 ? '0'+ hours : hours
    var minutes = date.getMinutes();
    minutes = minutes < 9 ? '0'+ minutes : minutes
    var seconds = date.getSeconds();
    seconds = seconds < 9 ? '0'+ seconds : seconds
    return year + '/' + month + '/' + day + ' ' + hours + ':' + minutes + ":" + seconds;
}

/**
 * 获取当月第一天
 */
function getFirstMonthday(){
    var date=new Date();
    var firstmonthday=date.setDate(1);
    return getFormatDate(firstmonthday);
}

/**
 * 日期比较大小(获取天数)
 */
function getDays(fday, tday) {
    var fday = new Date(fday);
    var tday = new Date(tday);
    var times = fday.getTime() - tday.getTime();
    var day = times / (1000 * 60 * 60 * 24);
    return parseInt(day)
}


/**
 * 判断是否为同一年
 */
function isSameYear(s, e) {
    var startyear = "", endyear = "";
    startyear = new Date(s).getFullYear();
    endyear = new Date(e).getFullYear();
    if (endyear != startyear) {
        return true;
    } else {
        return false;
    }
}
```