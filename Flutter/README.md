> 오준석의 플러터 생존코딩(한빛미디어) | 책을 읽으며 정리한 내용입니다. 책 정보 바로가기 [오준석의 플러터 생존코딩(한빛미디어)](https://www.hanbit.co.kr/store/books/look.php?p_code=B9770627589)

<br/>
<br/>

## Why Flutter

플러터는 IOS와 안드로이드 개발을 동시에 할 수 있는 강력한 장점이 있다. 이에 관하여 네이티브와의 퍼포먼스 차이로 고민을 할 수 있는데 저자는 아래와 같은 의견을 준다.
<br/>
<br/>

> 생산성과 퍼포먼스를 모두 생각했을 때 반드시 네이티브가 정답은 아니었습니다. 개발하려는 서비스에 강력한 성능이 꼭 필요하지 않다면 반드시 네이티브 앱 개발을 고집할 필요는 없습니다. 플러터가 있으니까요. (중략) 초보자도 플러터라면 더 쉽게 앱 개발을 시작할 수 있다... 특히 중소기업에서 플러터에 대한 수요가 늘어날 것으로 보입니다. - 지은이의 말 중

<br/>
<br/>

## 앱 개발 방식

스마트폰 앱 개발 방식은 크게 네이티브, 하이브리드, 크로스 플랫폼 방식으로 개발된다.

플러터는 `크로스 플랫폼` 개발 프레임워크이다.

1. 네이티브  
   플랫폼 자체에서 제공하는 개발 환경으로 개발하는것. 여러 플랫폼에 맞추어 개발을 진행하려면 Cost가 많이 든다.  
   _ex) 안드로이드 - 안드로이드 스튜디오 Kotlin_  
   _iOS - XCode Swift_

2. 하이브리드  
   **웹 기술로 앱 화면을 만든 후 네이티브 기술로 감싼다.** 기존 웹을 이용하므로 빠르게 개발할 수 있지만 네이티브에 비해 성능이 떨어지고, UI적으로도 앱 느낌을 내지 못한다.

3. 크로스 플랫폼  
   한 번 구현하여 안드로이드와 iOS등의 각 플랫폼용 앱을 만든다. 빌드할 때에 네이티브 코드로 변환되므로 결과적으로는 네이티브와 거의 유사한 성능을 보장하며, 따라서 생산성과 품질을 고려했을때 선호된다.
