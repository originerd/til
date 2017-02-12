# Reducer

`Reducer`는 현재 `state`와 `action`을 받아서 새로운 `state`를 만들어 주는 함수입니다. 여기서 `새로운`이 핵심입니다. 현재 `state`를 변경시키지 않아야(Immutable) 합니다.

`Reducer`는 여러 개로 나뉠 수 있는데, 해당 `Reducer`에서 처리할 `action.type`일 경우에는 새로운 `state`를, 아닐 때는 현재 `state`를 반환합니다.
