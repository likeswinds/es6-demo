# es6-demo
## 函数
### 箭头函数
#### 
``` javascripe
var reflect = value => value;

// 有效等价于：

var reflect = function(value) {
    return value;
};
```

``` javascripe
var sum = (num1, num2) => num1 + num2;

// 有效等价于：

var sum = function(num1, num2) {
    return num1 + num2;
};
```

``` javascripe
var getName = () => "Nicholas";

// 有效等价于：

var getName = function() {
    return "Nicholas";
};
```

``` javascripe
 var person = (name => {
        return {
          getName: () => name
        }
      })('zhangsan')
      console.log(person.getName())
 //等价于：
 let person = function(name) {

    return {
        getName: function() {
            return name;
        }
    };

}("Nicholas");

console.log(person.getName());      // "Nicholas"
```
