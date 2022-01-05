# 设计模式


### 一、单例模式

> 单例模式: 保证一个类仅有一个实例，并提供一个访问它的全局访问点

#### 惰性单例

> 指的是在需要的时候才创建对象实例。惰性单例是单例模式的重点

应用场景：

创建唯一的浮窗

```js
var getSingle = function( fn ){
   var result;
   return function(){
       return result || ( result = fn .apply(this, arguments ) );
   } 
};
var createLoginLayer = function(){

    var div = document.createElement( 'div' );
    div.innerHTML = '我是登录浮窗';
    div.style.display = 'none';  
    document.body.appendChild( div );

    return div;
};
var createSingleLoginLayer = getSingle( createLoginLayer );
document.getElementById( 'loginBtn' ).onclick = function(){ 
    var loginLayer = createSingleLoginLayer(); 
    loginLayer.style.display = 'block';
};
```



### 二、策略模式
### 三、代理模式
### 四、迭代器模式
### 五、观察者模式
### 六、命令模式
### 七、组合模式
### 八、模板方法模式
### 九、享元模式
### 十、职责链模式
### 十一、中介者模式
### 十二、装饰者模式
### 十三、状态模式
### 十四、适配器模式

## 原则

- 单一职责原则
- 最少知识原则
- 开放-封闭原则