> Likelion The Origin | React 강의를 수강하며 정리한 내용입니다.<br/> Tutor John Ahn [Youtube Channel](https://www.youtube.com/channel/UCFyXA9x8lpL3EYWeYhj4C4Q)

<br/>

# render

-   DOM에 컴포넌트를 렌더링하는 함수이다.
-   인자로 렌더링할 React 컴포넌트가 들어간다.
-   리턴은 RTL(React Testing Library)에서 제공하는 쿼리 함수와 기타 유틸리티 함수를 담고 있는 객체를 리턴한다.

<br/>

### render 함수를 이용한 test.js 작성 예시

```
test('renders learn react link', () ==>{
    render(<App />);
    const linkElement = screen.getByText(/learn react/i);
    expect(linkElement).toBeInTheDocument();
});
```
