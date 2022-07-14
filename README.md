# react-native-m1-boilerplate

# m1 실행 시 주의사항

## node, watchman
- 둘 다 brew 로 설치했으나 문제 없었습니다.

## Android

### Java Development Kit
- 자바가 설치되지 않은 상태에서 세팅하시기를 추천합니다. 그렇지 않으면 java 버전이 꼬여 원치 않는 버그를 만날 수도 있습니다.
### environemtn variable
- 맥북 세팅 후 zsh 로 변경하셨다면 `code ~/.zshrc` 로 파일을 열어 맨 아래 관련 변수를 넣으시면 됩니다.

## ios
### xCode
- 설치에 시간이 걸립니다. appStore 에서 설치 시작 후 안드로이드 세팅 및 확인을 추천합니다.
### CocoaPods
- 아래 명령어만 입력하고 넘어갑니다. `arch -x86_64 pod install` 은 RN 세팅 시에는 사용하지 않는 명령문입니다.
```bash
sudo gem install cocoapods
sudo arch -x86_64 gem install ffi
```

## npx react-native init <project-name> 이후
- 프로젝트 페이지로 들어가 `yarn echo` 를 실행하면 ios 초기 세팅이 완료됩니다. 안드로이드는 패키지 추가 삭제 시 별도 작업을 요구하지 않으나, ios 는 다릅니다. 그렇기에 패키지에 변경이 있을 경우 `yarn echo` 명령어를 실행해 주시기 바랍니다.
  - `yarn echo`: `cd ios && arch -x86_64 pod install && cd ../` 입니다. 초기 세팅에서 사용하지 않은 `pod install` 는 여기서 쓰여야 합니다.

# 기타
- RN 세팅은 할 때마다 새롭습니다. 거창하게 m1-boilerplate 라 남겨두지만 그정도는 아닐 듯 합니다. RN 세팅하시는 분들께 도움이 되기를 바래봅니다.
