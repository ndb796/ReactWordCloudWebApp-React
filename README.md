# ReactWordCloudWebApp-React
* 프로젝트 환경을 구축할 수 있습니다.
```
git clone https://github.com/ndb796/ReactWordCloudWebApp-React.git
```
* Visual Studio Code로 루트 폴더를 엽니다.
* 종속성 모듈을 설치합니다.
```
yarn add --dev webpack webpack-dev-server
yarn add --dev babel-core babel-loader babel-preset-react-app
npm install --save-dev style-loader
npm install --save-dev css-loader
yarn add webpack-cli
```
* Firebase에 새로운 프로젝트를 생성해 테스트 모드로 Realtime DB를 생성합니다.
* 다음과 같이 규칙을 설정합니다.
```
{
  "rules": {
    ".read": true,
    ".write": true,
  	"words": {
      ".indexOn": ["word"]
    }
  }
}
```
* 소스코드에서 databaseURL 경로를 새로운 파이어베이스 경로로 변경합니다.
* 이후에 프로젝트를 시작합니다.
```
yarn start
```
* 프로젝트 정상 동작 확인 이후에는 파이어베이스에 배포합니다.
```
yarn add --dev copy-webpack-plugin
yarn add webpack-cli
npm install -g firebase-tools
firebase init
# 호스팅 서비스 설정: Deploy - Build 폴더 - No Single Page App
yarn build
firebase deploy
```
