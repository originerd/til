# Casting

## float to integer

굉장히 신기하게 실수를 정수로 `casting`하는 방법을 알게 되었습니다. 일반적(개인적)으로는 다음과 같이 할 수 있습니다.

```js
console.log(Math.floor(3.14)); // 3
```

신기한 방식은 다음과 같습니다.

```js
console.log(3.14|0); // 3
```
