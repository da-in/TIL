# Parameter

> 📖 Reference | Flutter Agency  
> **Difference Between Named and Positional Parameters In Dart?**  
> https://flutteragency.com/named-and-positional-parameters-in-dart/

<br/>

### Parameter

-   Required Parameter(필수 매개변수)
-   Optional Parameter(선택 매개변수)
    -   Optional Positional Parameter `[ ]`
    -   Optional Named Parameter `{ }`
    -   Optional Default Parameter `{ }`

<br/>

### Required Parameter(필수 매개변수)

필수 매개변수는 기존에 사용하던 일반적인 매개변수이다.  
필수 매개변수를 선택 매개변수와 함께 사용할 경우, 필수 매개변수는 제일 앞에 위치시킨다.

<br/>

### Optional Parameter(선택 매개변수)

함수 호출시 매개변수의 값을 지정할 필요가 없다는 점에서 선택적인 매개변수를 말한다.

<br/>

1.  Optional Positional Parameter  
     위치 선택적 매개변수는 `[ ]`로 감싼다.  
     위치에 의하여 매개변수를 식별하며 미입력시 기본값을 지정할 수 있다.

    ```
    getHttpUrl(String server, String path, [int port=80, int numRetries=3]) {
        ...
    }
    getHttpUrl('example.com', '/index.html');
    getHttpUrl('example.com', '/index.html', 8080);
    getHttpUrl('example.com', '/index.html', 8080, 5);
    ```

    위의 예시를 보면 위치 선택적 매개변수인 `port`와 `numRetries`를 매개변수 입력 순서에 따라 구분한다.

    따라서 `numRetries`를 입력하기 위해서는 앞의 `port`를 생략할 수 없다.

    > 🚨 Optional Positional Parameter가 여러 매개변수를 지정한다면, 호출시 후위의 위치 선택적 매개변수 사용을 위해서는 그 앞의 매개변수를 모두 입력해야한다.

    이러한 단점은 명명된 매개변수 사용으로 보완할 수 있다.

    <br/>
    <br/>

2.  Optional Named Parameter

    명명된 선택적 매개변수는 `{ }`로 감싸고, 호출시 `매개변수 이름` : `인수` 형태로 사용한다.

    선택적 매개변수의 이름으로 참조하므로 선언 순서와 무관하게 사용할 수 있다.

    아래와 같이 `port`를 지정하지 않고도 `numRetries`를 사용할 수 있다.

    ```
    getHttpUrl(String server, String path, {int port, int numRetries}) {
        ...
    }

    getHttpUrl('example.com', '/index.html', numRetries: 5);
    ```

    <br/>
    <br/>

3.  Optional Default Parameter

    Optional Named Parameter와 동일하나, 미입력시 dafault 값을 지정해준다.

    ```
    getHttpUrl(String server, String path, {int port=80, int numRetries=3}) {
        ...
    }

    getHttpUrl('example.com', '/index.html', numRetries: 5);
    ```

    Optional Named Parameter 였을 경우 지정하지 않은 `port`의 값이 `null`이 된다. 하지만 default 값을 지정한 Optional Default Parameter 의 경우 `port` 값이 `80` 이 된다.

    덧붙여 `numRetries`는 default 값으로 `3`을 지정하였으나, 함수 호출시 `5`라는 값을 지정하였으므로 `5`가 된다.

<br/>
<br/>

_마치며, Optional Positional Parameter, Positional Optional Parameter... 조금씩 기술하는 방식에 글마다 차이가 있는 것 같다._
