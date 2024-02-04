# html, css

## html

 markup language: 자료구조를 표현하는 언어. 브라우저를 통해 화면에 보여줄 자료의 구조를 표현한다.

## tag

대부분의 태그는 style 속성을 갖는다.

- img
- a
  - href="#"
- button
- p
- ol, ul
- span
- div, nav, section, footer

## 중간 정렬

```
style="
display: block;
margin-left: auto;
margin-right: auto
"
```

## 폰트

- font-size
- font-family
- letter-spacing
- font-weight
  
## selector

이름을 짓고 style을 지정할 수 있다.

- class
- id
- tag

### 자식 태그

- .content li
  - 위 처럼 class 이름과 태그명과 공백을 두면, content 클래스의 모든 li 자식에게 style을 부여한다.
- .content>li
  - 위 처럼 오른쪽 화살표로 지정하면, 직계 자손 li에만 적용된다.
  
## div

- 기본적으로 상, 하의 길이를 갖지 않는다.
- display: block을 내재한다.

## 레이아웃 만들기

- wrappe div로 감싸면서 순차적으로 만든다.
- float, inline-block으로 정렬할 수 있다.
  - float 사용 후에는 이후의 객체가 margin이나 정렬하면서 예상대로 처리가 되지 않으면 `clear: both`

### text

- 텍스트에는 baseline이 존재한다.
- inline-block으로 정렬하면 baseline 위에 객체가 정렬될 수 있으므로 주의한다.
- vertical-align: top으로 해결할 수 있다.

## p, h 등 텍스트

- 기본적으로 margin을 가지고 있어서 div 박스 안의 p, h 태그가 예상했던 부피보다 커질 수 있다.
- text-decoration: none 으로 a tag의 밑줄을 지울 수 있다.

## 백그라운드를 이미지로

- background-image: url();
  - 참고로 위 background-image와 같은 것을 css의 property(속성), img의 src, alt와 같은 것을 attribute(속성)이라고 한다.
- 이 때, 상대경로는 css 파일을 중심으로
