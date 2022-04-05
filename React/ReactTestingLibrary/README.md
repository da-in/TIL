> Likelion The Origin | React 강의를 수강하며 정리한 내용입니다.<br/> Tutor John Ahn [Youtube Channel](https://www.youtube.com/channel/UCFyXA9x8lpL3EYWeYhj4C4Q)

<br/>
<br/>

# React Testing Library

DOM Testing Library는 DOM 노드를 테스트하기 위한 매우 가벼운 솔루션이며, 이러한 DOM Testing Library에 React를 위한 API를 추가하여 구축한 것이 React Testing Library 이다.

Create React App으로 생성된 프로젝트는 즉시 React Testing Library를 지원한다.
수동으로 설치하고자 할 경우에는 아래와 같이 명령어를 사용한다.

```
npm install --save-dev @testing-library/react
```

공식문서 [testing-library docs](https://testing-library.com/docs/react-testing-library/intro/)

React Testing Library는 에어비엔비의 Enzyme을 대처하는 솔루션이다.

**Enzyme** : 구현 주도 테스트(Implementation Driven Test)  
**React Testing Library** : 행위 주도 테스트(Behavior Driven Test)

React Testing Library의 경우 사용자의 입장에서 테스트한다. 예를들어 컴포넌트가 구현될 때 글자 출력을 `<p/>` 태그를 사용하건 `<h/>` 를 사용하건 사용자 입장에서는 무관하다. Enzyme에서는 어떠한 태그를 사용하여 구현하였는지 까지 테스트한다.
