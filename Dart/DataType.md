> 오준석의 플러터 생존코딩(한빛미디어) | 책을 읽으며 정리한 내용입니다. 책 정보 바로가기 [오준석의 플러터 생존코딩(한빛미디어)](https://www.hanbit.co.kr/store/books/look.php?p_code=B9770627589)

<br/>
<br/>

# DataType

> Dart는 자동 형변환을 지원하지 않는다.
> int와 double의 super type로 num을 사용한다. 😮

<br/>

`num` : int와 double을 포함하는 자료형  
`int` : 정수  
`double` : 실수  
`String` : 문자열  
`bool` : 참 거짓

```
int a = 10;
double b = 20.0;

b = a; //error

num c = a; //ok
c = b; //ok
```

<br/>

> Dart는 변수의 값 재할당이 언제든지 가능하다.

```
String s = 'hello';
s = 'world';
```
