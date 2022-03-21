> Likelion The Origin | React 강의를 수강하며 정리한 내용입니다. Tutor John Ahn [Youtube Channel](https://www.youtube.com/channel/UCFyXA9x8lpL3EYWeYhj4C4Q)

### Axios

- Axios는 브라우저, Node.js를 위한 Promise API를 활용하는 HTTP 비동기 통신 라이브러리이다.
- 백엔드와 프론트의 통신을 쉽게 하기 위해 Ajax와 더불어 사용한다.

### Axios 사용 방법

- axios 모듈 설치

```
  npm install axios --save
```

```
axios.get('https://api.themoviedb.org/3/trending/all/week')
```

### Axios 인스턴스화 하는 이유

- 중복된 부분을 계속 입력하지 않아도 되기 때문이다.

### Axios 인스턴스 만드는 순서

1. src 폴더 내에 인스턴스를 생성할 폴더와 파일 생성

- api
  - axios.js : 반복되는 BaseURL과 API 사용자 Key 등을 인스턴스화
  - requests.js : 하위 다양한 경로들을 입력해두어 사용
