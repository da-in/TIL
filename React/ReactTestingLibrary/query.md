> Likelion The Origin | React 강의를 수강하며 정리한 내용입니다.<br/> Tutor John Ahn [Youtube Channel](https://www.youtube.com/channel/UCFyXA9x8lpL3EYWeYhj4C4Q)

<br/>

# query

공식 문서 [queries docs](https://testing-library.com/docs/quries/about/)

-   쿼리 함수는 페이지에서 요소를 찾기 위해 테스트 라이브러리가 제공하는 방법이다.
-   `get` `find` `query` 유형의 쿼리가 있다.

<br/>

### get, find, query 의 차이점

1. getBy...
   쿼리에 대해 일치하는 노드를 반환하고 일치하는 요소가 없거나 둘 이상의 일치가 발견되면 설명 오류를 발생시킨다.

2. queryBy...
   쿼리에 대해 일치하는 노드를 반환하고 일치하는 요소가 없으면 `null`을 반환한다. 존재하지 않는 요소를 어설션하는 데 유용하다.둘 이상의 일치 항목이 발견되면 오류를 발생시킨다.

3. findBy...  
   `findBy = getBy + waitfor `  
    **waitfor** : 일정 기간 동알 기다려야 할 때 waitFor를 사용하여 기대가 통과할 때까지 기다린다.

    주어진 쿼리와 일치하는 요소가 발견되면 Promise를 반환한다. 요소가 발견되지 않거나 기본 제한 시간인 1000ms 후에 둘 이상의 요소가 발견되면 거부된다.

<br/>

| Type of Query         | 0 Matches     | 1 Match        | >1 Matches   | Retry(Async/Await) |
| --------------------- | ------------- | -------------- | ------------ | ------------------ |
| **Single Element**    |
| `getBy...`            | Throw error   | Return element | Throw error  | No                 |
| `queryBy...`          | Return `null` | Return element | Throw error  | No                 |
| `findBy...`           | Throw error   | Return element | Throw error  | Yes                |
| **Multiple Elements** |
| `getAllBy...`         | Throw error   | Return array   | Return array | No                 |
| `queryAllBy...`       | Return `[]`   | Return array   | Return array | No                 |
| `findAllBy...`        | Throw error   | Return array   | Return array | YEs                |
