> 오준석의 플러터 생존코딩(한빛미디어) | 책을 읽으며 정리한 내용입니다. 책 정보 바로가기 [오준석의 플러터 생존코딩(한빛미디어)](https://www.hanbit.co.kr/store/books/look.php?p_code=B9770627589)

<br/>
<br/>

# Syntax

Dart 문법은 다른 프로그래밍 언어들과 매우 유사하여 직관적이다.  
차이점을 정리한다.

<br/>

## DataType

> Dart는 자동 형변환을 지원하지 않는다.
> int와 double의 super type로 num을 사용한다. 😮

```
int a = 10;
double b = 20.0;

b = a; //error

num c = a; //ok
c = b; //ok
```

`num` : int와 double을 포함하는 자료형  
`int` : 정수  
`double` : 실수  
`String` : 문자열  
`bool` : 참 거짓

<br/>

> Dart는 변수의 값 재할당이 언제든지 가능하다.

```
String s = 'hello';
s = 'world';
```

<br/>

> 타입을 직접 명시하지 않고 var로 대체할 수 있는 `타입추론`을 지원한다. 타입추론에 의해 함수 정의시에도 `반환타입` 지정을 생략할 수 있다.

```
var i = 10; //int

void func(String hello){
    print('$hello world');
}

func(String hello){
    print('$hello world');
} //위 코드와 동일하다
```

<br/>

> final 키워드를 통해 값을 수정되지 않는 상수로 사용할 수 있다.

```
final String name = 'dain';
final name = 'dain';
```

<br/>

## function

Dart는 일반적인 형태의 함수 이외에도 익명함수와 람다표현식 등을 사용할 수 있다.

> 익명 함수(anonymous function)

```
([argument]){[expression]}
(number){number % 2 == 0;}
```

> 람다식(lambda)

```
([argument]) => [expression]
(number) => {number % 2 == 0;}
```
