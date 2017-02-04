# Function

## arguments

JavaScript function에는 지역변수로 this 및 arguments 객체를 갖습니다. 이는 Arrow function에서는 바인딩되지 않는 항목들입니다. 최근 개발 대부분을 Arrow function을 사용하고 있어서 더욱 알지 못했던 부분입니다.

arguments 객체는 Array-like 객체로, 완전한 Array는 아닙니다. function에 인자가 정의되어있지만, arguments는 정의된 인자의 수보다 작거나 클 수 있습니다. 정의된 인자의 수보다 더 적게 혹은 더 많이 입력할 수 있기 때문이죠.

arguments 객체에는 두 가지 주요 속성이 있습니다.

1. length
  - function에 전달된 인자의 수를 가리킵니다.
1. callee
  - 현재 실행 중인 function을 가리킵니다.
  - *다만 ECMAScript 5의 strict mode에서는 이를 [사용하지 못하도록 한다](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Functions/arguments/callee)고 합니다. tail recursion 등의 최적화를 하기 어렵기 때문이라고 하네요.*

이는 다음과 같이 응용할 수 있습니다.

```js
var countDown = function (n) {
  if (n < 1) {
    return;
  }

  console.log(n);

  arguments.callee(n - 1);
}
```
