# Parameter

> π Reference | Flutter Agency  
> **Difference Between Named and Positional Parameters In Dart?**  
> https://flutteragency.com/named-and-positional-parameters-in-dart/

<br/>

### Parameter

-   Required Parameter(νμ λ§€κ°λ³μ)
-   Optional Parameter(μ ν λ§€κ°λ³μ)
    -   Optional Positional Parameter `[ ]`
    -   Optional Named Parameter `{ }`
    -   Optional Default Parameter `{ }`

<br/>

### Required Parameter(νμ λ§€κ°λ³μ)

νμ λ§€κ°λ³μλ κΈ°μ‘΄μ μ¬μ©νλ μΌλ°μ μΈ λ§€κ°λ³μμ΄λ€.  
νμ λ§€κ°λ³μλ₯Ό μ ν λ§€κ°λ³μμ ν¨κ» μ¬μ©ν  κ²½μ°, νμ λ§€κ°λ³μλ μ μΌ μμ μμΉμν¨λ€.

<br/>

### Optional Parameter(μ ν λ§€κ°λ³μ)

ν¨μ νΈμΆμ λ§€κ°λ³μμ κ°μ μ§μ ν  νμκ° μλ€λ μ μμ μ νμ μΈ λ§€κ°λ³μλ₯Ό λ§νλ€.

<br/>

1.  Optional Positional Parameter  
     μμΉ μ νμ  λ§€κ°λ³μλ `[ ]`λ‘ κ°μΌλ€.  
     μμΉμ μνμ¬ λ§€κ°λ³μλ₯Ό μλ³νλ©° λ―Έμλ ₯μ κΈ°λ³Έκ°μ μ§μ ν  μ μλ€.

    ```
    getHttpUrl(String server, String path, [int port=80, int numRetries=3]) {
        ...
    }
    getHttpUrl('example.com', '/index.html');
    getHttpUrl('example.com', '/index.html', 8080);
    getHttpUrl('example.com', '/index.html', 8080, 5);
    ```

    μμ μμλ₯Ό λ³΄λ©΄ μμΉ μ νμ  λ§€κ°λ³μμΈ `port`μ `numRetries`λ₯Ό λ§€κ°λ³μ μλ ₯ μμμ λ°λΌ κ΅¬λΆνλ€.

    λ°λΌμ `numRetries`λ₯Ό μλ ₯νκΈ° μν΄μλ μμ `port`λ₯Ό μλ΅ν  μ μλ€.

    > π¨ Optional Positional Parameterκ° μ¬λ¬ λ§€κ°λ³μλ₯Ό μ§μ νλ€λ©΄, νΈμΆμ νμμ μμΉ μ νμ  λ§€κ°λ³μ μ¬μ©μ μν΄μλ κ·Έ μμ λ§€κ°λ³μλ₯Ό λͺ¨λ μλ ₯ν΄μΌνλ€.

    μ΄λ¬ν λ¨μ μ λͺλͺλ λ§€κ°λ³μ μ¬μ©μΌλ‘ λ³΄μν  μ μλ€.

    <br/>
    <br/>

2.  Optional Named Parameter

    λͺλͺλ μ νμ  λ§€κ°λ³μλ `{ }`λ‘ κ°μΈκ³ , νΈμΆμ `λ§€κ°λ³μ μ΄λ¦` : `μΈμ` ννλ‘ μ¬μ©νλ€.

    μ νμ  λ§€κ°λ³μμ μ΄λ¦μΌλ‘ μ°Έμ‘°νλ―λ‘ μ μΈ μμμ λ¬΄κ΄νκ² μ¬μ©ν  μ μλ€.

    μλμ κ°μ΄ `port`λ₯Ό μ§μ νμ§ μκ³ λ `numRetries`λ₯Ό μ¬μ©ν  μ μλ€.

    ```
    getHttpUrl(String server, String path, {int port, int numRetries}) {
        ...
    }

    getHttpUrl('example.com', '/index.html', numRetries: 5);
    ```

    <br/>
    <br/>

3.  Optional Default Parameter

    Optional Named Parameterμ λμΌνλ, λ―Έμλ ₯μ dafault κ°μ μ§μ ν΄μ€λ€.

    ```
    getHttpUrl(String server, String path, {int port=80, int numRetries=3}) {
        ...
    }

    getHttpUrl('example.com', '/index.html', numRetries: 5);
    ```

    Optional Named Parameter μμ κ²½μ° μ§μ νμ§ μμ `port`μ κ°μ΄ `null`μ΄ λλ€. νμ§λ§ default κ°μ μ§μ ν Optional Default Parameter μ κ²½μ° `port` κ°μ΄ `80` μ΄ λλ€.

    λ§λΆμ¬ `numRetries`λ default κ°μΌλ‘ `3`μ μ§μ νμμΌλ, ν¨μ νΈμΆμ `5`λΌλ κ°μ μ§μ νμμΌλ―λ‘ `5`κ° λλ€.

<br/>
<br/>

_λ§μΉλ©°, Optional Positional Parameter, Positional Optional Parameter... μ‘°κΈμ© κΈ°μ νλ λ°©μμ κΈλ§λ€ μ°¨μ΄κ° μλ κ² κ°λ€._
