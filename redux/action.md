# Action

Action은 어떠한 변화를 줄지 정의된 데이터입니다. Action은 `type`을 항상 가지며, 변경에 필요한 데이터를 가지고 있거나 없을 수 있습니다. 일반적으로 `type`은 `string`으로 구성됩니다. 이 `type`은 `string`으로 직접 사용하기도 하지만, [`constant`로 한 번 감싸서 이용](http://redux.js.org/docs/recipes/ReducingBoilerplate.html#actions)하기도 합니다

```
{ type: ADD_TODO, text: 'TIL 쓰기' }
```
