# Component

Redux에서(혹은, Dan Abramov)는 `Component`를 두 가지로 구분합니다.

- Presentational component
- Container component

사실 이 둘은, Dumb component 및 Smart component로 불렸었지만, 현재는 [좀 더 세련된 이름을 갖게 되었죠](https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0#).

## Presentational component

- 데이터를 직접적으로 불러오거나 변경하지 않는 컴포넌트입니다.
- 주로 state를 갖지 않습니다.
- store에 직접적인 연관을 갖지 않습니다.
- state 혹은 lifecycle hooks, 성능 최적화를 제외하고는 일반적으로, functional component로 작성합니다.

## Container component

- 다른 컴포넌트들에게 데이터를 전달합니다.
- store를 통해 데이터를 불러오거나 변경합니다.
