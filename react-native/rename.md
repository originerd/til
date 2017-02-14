# Rename

App의 이름을 변경하고 싶은 마음이 생겨서 일일이 바꾸는 방법을 써볼까 하다가, 새로운 방식을 알게 되었습니다. 다만, 프로젝트 초기에 사용하면 더 좋을 것 같습니다. android 및 ios에 변경을 많이 했다면, 일일이 바꾸는 게 빠를 수도 있습니다(?).

1. `package.json`의 `name` 바꾸기
1. 이름 변경 작업
  - `react-native upgrade`
1. 기존 이름의 android 및 ios 파일들 삭제하기
  - 주의
    - 해당 작업 이전의 커맨드를 실행하면, 새로운 이름으로 android 및 ios 파일들이 생성됩니다.
    - 기존 파일들을 변경했었다면, 새로 생성된 android 및 ios 파일들에 옮겨 적는 작업이 필요합니다.
  - `rm -rf android/app/src/main/java/com/<기존 이름> && rm -rf ios/<기존 이름>*`
1. `index.android.js` 및 `index.ios.js`에서 기존 이름을 새로운 이름으로 변경
1. (필요하다면) 링크
  - `react-native link`
