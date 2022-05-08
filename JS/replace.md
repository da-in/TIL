# replace()

문자열을 치환할 때 사용하는 함수이다.
''으로 치환시에는 제거의 역할을 할 수 있다.

<br/>

문자열 l을 L로 치환하기 예제

```
str = 'hello, world';
str = str.replace('l','L');
// result : 'heLlo, world'
```

위의 코드로는 첫 번째 l만 L로 변환된다.  
문자열 내의 모든 l을 L로 치환하기 위한 코드는 다음과 같이 정규표현식을 이용한다.

```
str = str.replace(/l/g, 'L');
```

정규 표현식 뒤의 옵션  
`/g` (global) 모두 찾아 바꾸기  
`/i` (ignore) 대소문자 무시
