> 오준석의 플러터 생존코딩(한빛미디어) | 책을 읽으며 정리한 내용입니다. 책 정보 바로가기 [오준석의 플러터 생존코딩(한빛미디어)](https://www.hanbit.co.kr/store/books/look.php?p_code=B9770627589)

# class

클래스 객체(인스턴트) 생성(인스턴스화)

```
class Person {
    String name;
    int age;
}

var person = new Person();
var person = Person(); //new 생략 가능
```

## static

클래스 메소드에서 static 키워드를 붙이면 최상위 함수처럼 사용할 수 있다.

정확하게는 static을 사용하면 객체를 만들 때 객체의 저장공간을 이용하는 것이 아닌, 별도의 저장공간을 이용하여 공유하는 것이다.

```
class Student {
    static schoolAvg = 70;
    static void printSchoolAvg(){
        print(schoolAvg);
    }
    int math;
    int english;
    int science;
}

print(Student.math); //error
print(Student.schoolAvg);
Student.printSchoolAvg();
```

-   클래스 내 static 변수는 객체를 선언하지 않아도 클래스 명으로 접근할 수 있다.
-   클래스 메소드 또한 객체를 거치지 않아도 외부에서 사용할 수 있다.
