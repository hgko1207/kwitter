# React And Firebase

## 설정

### Firebase

[Firebase 페이지](https://firebase.google.com/) 에서 콘솔로 이동을 클릭하고 프로젝트를 추가합니다.
그리고 앱에서 Web 을 선택 후 이름을 입력하고 등록을 합니다.

```bash
npm install --save firebase
```

앱을 생성하였을 때 나오는 설정 파일을 복사한 후 src 폴더에 firebase.js 파일을 생성하고 붙여넣기 한 후 아래와 같이 수정합니다.

```js
import firebase from "firebase/app";

const firebaseConfig = {
    apiKey: "AIzaSyAGCluvE0Dhdctb2XReMzFc1hft2lW8xGA",
    authDomain: "kwitter-a5106.firebaseapp.com",
    projectId: "kwitter-a5106",
    storageBucket: "kwitter-a5106.appspot.com",
    messagingSenderId: "168715018538",
    appId: "1:168715018538:web:5e022cb2a98bc7ecfb7e53"
};

export default firebase.initializeApp(firebaseConfig);
```

## 참고

- https://firebase.google.com/docs/web/setup?authuser=0;