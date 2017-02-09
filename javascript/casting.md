# Casting

굉장히 신기하게 실수를 정수로 `casting`하는 방법을 알게 되었습니다. 이를 계기로, `casting`에 대해 정리합니다.

## float to integer

기존 방식

```js
Math.floor(3.14); // 3
```

새로운 방식

```js
3.14 | 0; // 3
```

## string to number

기존 방식

```js
Number('3.14'); // 3.14
```

새로운 방식

```js
+ '3.14'; // 3.14
```
