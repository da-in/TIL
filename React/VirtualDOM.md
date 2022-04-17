> Likelion The Origin | React 강의를 수강하며 정리한 내용입니다. Tutor John Ahn [Youtube Channel](https://www.youtube.com/channel/UCFyXA9x8lpL3EYWeYhj4C4Q)

> 📖 Reference | 쉽게 읽는 프로그래밍  
> **[JavaScript] DOM이란 무엇인가?**  
> https://m.blog.naver.com/magnking/220972680805  
> DOM과 관련한 다양한 개념과 이론적 배경이 잘 정리되어있다.

<br/>

# VirtualDOM

가상돔(Virtual DOM)은 리액트의 큰 특징 중 하나이다.  
가상돔이 무엇인지 그리고 왜 사용하는지 파악한다.

## Critical Rendering Path, CRP

웹 페이지 빌드 과정을 CRP(Critical Rendering Path)라고 하며 브라우저가 서버에서 페이지의 HTML 응답을 받아 문서를 읽고, 스타일을 입히고, 뷰포트에 표시하는 과정을 말한다.

Virtual DOM 사용이유를 설명하기 위하여 CRP의 일부를 기술하면 다음과 같다.

1. DOM tree 생성  
   렌더 엔진이 문서를 읽어들여서 그것들을 파싱하고 어떤 내용을 페이지에 렌더링할지 결정한다.
   _( DOM과 CSSOM도 생성한다. )_

    - DOM(Document Object Model)  
       문서 객체 모델(DOM, Document Object Model)은 문서에 접근하기 위한 인터페이스이며, 계층 구조로 이루어져있다.

    - CSSOM(CSS Object Model)  
      CSS 객체 모델로 문서 객체 모델과 유사하다.

2. Render tree 생성  
   DOM과 CSSOM을 결함하여, 화면에 표시되는 모든 노드의 콘텐츠 및 스타일 정보를 포함한 최종 렌더링 트리를 출력한다.

3. Layout(reflow)  
   브라우저가 페이지에 표시되는 각 요소의 크기와 위치를 계산한다.

4. Paint  
   실제 화면에 그린다.

<br/>

> 🚨 인터렉션 등에 의해 DOM이나 CSSOM 등에 변화가 생기면 Render Tree를 다시생성하게 될 뿐 아니라 Layout, Paint 단계도 다시 실행하게 되는 비효율이 발생한다.

<br/>

## Virtual DOM

`가상 돔(Virtual DOM)`은 실제 돔을 메모리에 복사한 것이다.

1. 데이터가 바뀌면 가상돔에 렌더링된다.

2. `Diffing`, 이전에 생성된 가상돔과 비교해서 바뀐 부분을 찾는다.

3. `Reconciliation(재조정)`, 바뀐 부분만 실제 DOM에 적용시킨다.

> 😉 Virtual DOM을 이용하면 데이터가 변화할 때 마다 전체 DOM을 다시 그리고 처리하는 비효율을 줄일 수 있으며, 이는 React의 큰 특징이다.
