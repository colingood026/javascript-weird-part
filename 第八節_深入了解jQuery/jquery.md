嚴謹模式：

```javascript
"use strict";
```



用一個函數回傳new 函數建構子，簡潔的技巧，不用每次都寫new

jQuery = function( selector, context )

jQuery.fn = jQuery.prototype

jQuery.extend = jQuery.fn.extend

Sizzle

jQuery.fn.init

init.prototype = jQuery.fn;

$('ul.people').addClass('newClass').removeClass('people');

key word:method chaining
obj.method1().method2(), 每個函數都會影響到母物件

jquery的作法是在method1()的最後回傳this，因為這些方法都在物件上，他在原型上，
當我們呼叫物件的方法時，它會往物件上找，如果找不到則會往原型去找。
但當我呼叫方法時，它會在原型鍊上找到this變數指向原本的物件($('ul.people'))，也就是真正的物件。