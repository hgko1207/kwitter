# React And Firebase

## 설정

### Firebase

[Firebase 페이지](https://firebase.google.com/) 에서 콘솔로 이동을 클릭하고 프로젝트를 추가합니다.
그리고 앱에서 Web 을 선택 후 이름을 입력하고 등록을 합니다.

```bash
npm install --save firebase
```

프로젝트 상단에 .env 파일을 생성합니다.
앱을 생성하였을 때 나오는 Firebas 설정을 아래와 같이 변수를 설정하고 채워넣습니다.

```js
// .env
REACT_APP_API_KEY=
REACT_APP_AUTH_DOMAIN=
REACT_APP_PROJECT_ID=
REACT_APP_STORAGE_BUCKET=
REACT_APP_MESSAGING_SENDERID=
REACT_APP_APP_ID=
```

src 폴더에 firebase.js 파일을 생성합니다. .env 에 입력한 설정들을 불러와서 입력합니다.

```js
import firebase from "firebase/app";

const firebaseConfig = {
    apiKey: process.env.REACT_APP_API_KEY,
    authDomain: process.env.REACT_APP_AUTH_DOMAIN,
    projectId: process.env.REACT_APP_PROJECT_ID,
    storageBucket: process.env.REACT_APP_STORAGE_BUCKET,
    messagingSenderId: process.env.REACT_APP_MESSAGING_SENDERID,
    appId: process.env.REACT_APP_APP_ID
};

export default firebase.initializeApp(firebaseConfig);
```

### React

#### Router 설정

```bash
npm install react-router-dom
```

## 참고

- https://firebase.google.com/docs/web/setup?authuser=0;