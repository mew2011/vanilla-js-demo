# vanilla-js-demo
vanilla js

## common js
```javascript
// get an Element object
document.getElementById('id');
document.getElementsByClassName('');
document.getElementsByTagName('');
const el = document.querySelector('#myId'); // 返回第一个匹配的element
document.querySelectorAll('selector'); // 返回所有匹配element
```

```javascript
// 解析json
JSON.parse(string)
```

```javascript
// 获取属性值
el.getAttribute('name');
// 设置属性值
el.setAttribute('name', 'abc');
```

```javascript
// hide
el.style.display = 'none';
// show
el.style.display = '';
```

```javascript
// 设置Style
el.style.boarderWidth = '20px';
el.style.color = '#ff0011';
// 添加class
el.classList.add(className);
// remove class
el.classList.remove(className);
```

## input内容赋值
```javascript
// bing search input
document.getElementById('sb_form_q').value = 'JavaScript';
```

## click事件
```javascript
let el = document.getElementById('btn_1');
// eventHandler is a function
el.addEventListener('click', eventHandler);
```

## ES6对象{}内部定义函数
ES6规范指定了对象{}内部的字面量定义可以省略function
```javascript
// 省略 key-value 形式
const Counter = {
    data() {
        return {
            counter: 0
        }
    },
    mounted() {
        setInterval(() => {
            this.counter++
        }, 1000)
    }
}
```
等价于
```
// 传统k-v形式
const Counter = {
    data: function() {
        return {
            counter: data.num
        }
    },
    mounted: function() {
        setInterval(() => {
            this.counter++
        }, 1000)
    }
}
```
