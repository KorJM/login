# login

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

# AppWrite를 사용한 간단한 로그인 기능 구현

<img width="644" alt="스크린샷 2023-10-28 오전 6 12 51" src="https://github.com/KorJM/ecloe-project/assets/114234223/d56aa7ca-3254-4bce-b090-55f22ceaae68">

<br>
<p>Vue.js + AppWrite를 사용하여 웹 상에서 간단한 로그인과 회원가입 기능을 구현해보았습니다</p>
<p>실제로 직접 로그인 기능을 구현하려면 훨신 복잡한 과정을 거쳐야하는데 appwrite를 사용하니 아주 간단하게 구현 할 수 있었습니다.</p>

<img width="644" alt="스크린샷 2023-10-28 오전 6 13 03" src="https://github.com/KorJM/ecloe-project/assets/114234223/de905b02-b2aa-4512-8992-5e555c74d063">

<br>
<p>조건부 렌더링을 위해 v-if디렉티브를 사용하였습니다</p>

<img width="644" alt="스크린샷 2023-10-28 오전 6 13 13" src="https://github.com/KorJM/ecloe-project/assets/114234223/f6dd59e5-f12d-4e38-9142-00b6e8b64561">

<br>

<img width="1509" alt="스크린샷 2023-10-28 오전 6 21 38" src="https://github.com/KorJM/ecloe-project/assets/114234223/6d8aee66-bc35-4b87-96fa-faacbc8352b4">

<br>

<img width="1512" alt="스크린샷 2023-10-28 오전 6 29 25" src="https://github.com/KorJM/ecloe-project/assets/114234223/98026b28-937d-402b-aa75-48d01643e8d3">

<br>
<p>SignUp버튼을 누르면 가입을 위한 input박스가 렌더링됩니다</p>

<img width="1512" alt="스크린샷 2023-10-28 오전 6 29 42" src="https://github.com/KorJM/ecloe-project/assets/114234223/96070e97-1bf7-4275-ad2f-97bb96f1c12e">

<br>
<p>로그인에 성공하면 메시지가 변경됩니다</p>

<img width="1509" alt="스크린샷 2023-10-28 오전 6 22 13" src="https://github.com/KorJM/ecloe-project/assets/114234223/3be1cfde-6de6-45d6-8b92-bb14ad3447b8">

<br>

<img width="1509" alt="스크린샷 2023-10-28 오전 6 22 31" src="https://github.com/KorJM/ecloe-project/assets/114234223/1f704e84-9788-4847-bf4a-9bfd62002cb6">

<br>

<img width="1509" alt="스크린샷 2023-10-28 오전 6 26 58" src="https://github.com/KorJM/ecloe-project/assets/114234223/c8ed9311-92d3-4fc2-9cc8-8edbd0555c91">

<br>
<p>퍼센트를 사용하여 브라우저 크기에 따른 반응형 요소로 제작하였습니다</p>
<p>미디어 쿼리를 사용하여 모바일 버전과 웹 버전을 나누어 레이아웃을 작성하였습니다.</p>

<img width="409" alt="스크린샷 2023-10-28 오전 6 27 35" src="https://github.com/KorJM/ecloe-project/assets/114234223/e5f0610c-f6a0-47d6-bbc0-62363c106598">




