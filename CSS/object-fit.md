- `object-fit` 속성은 다양한 이미지나 비디오 형식의 내용이 지정된 너비와 높이에 삽입되는 방식을 정한다. (ex `<img>, <video>, <object>, <svg>` 등)
- 크기각 각기 다른 오브젝트를 넘겨받아 비율을 유지한 채로 일정한 크기로 재가공하는 경우 유용하게 사용된다.(ex 프로필 이미지 등)
- CSS3의 background-size 속성과 매우 유사하다.

속성값

```object-fit : fill
# 비율을 유지하지 않고 꽉채운다.

object-fit : contain
# 비율을 유지한 채로 잘리지 않는 범위 내에서 가능한 최대 사이즈로 채우며 빈 공간이 생길 수 있다.

object-fit : cover
# 비율을 유지한 채로 화면에 여백이 없을 때 까지 채우므로 잘림이 발생할 수 있다.

object-fit : none
# 크기 상관없이 기본 로직에 의해 자동 조정된다.

object-fit : scale-down
# 크기를 아무것도 지정되지 않거나 contain이 지정된 것처럼 조정한다. 원본크기보다 작아지는 결과를 보여준다.
```

> 참고 [WEBDIR BLOG](https://webdir.tistory.com/486)
