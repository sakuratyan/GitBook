# javscript syntax highlighting

MarkDown都前缀**小写**,~~JavaScript~~居然识别不出来,GitHub上都能识别!!!

> 1/4 js

```js
class Polygon {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
  get area() {
    return this.height * this.width;
  }
}
```

> 2/4 js

```js
function foo(bar){
  var a = 42,b = 'Prism';
  return a + bar(b);
}
```

> 3/4 JavaScript

```JavaScript
function foo(bar){
  var a = 42,b = 'Prism';
  return a + bar(b);
}
```

> 4/4 javascript

```javascript
function foo(bar){
  var a = 42,b = 'Prism';
  return a + bar(b);
}
```