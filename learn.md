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

### 참고

- tag[속성명: 속성값]으로 속성을 특정할 수 있다.
- 쉼표로 여러 셀렉터에 같은 스타일을 적용할 수 있다.

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

### cover, contain

background-size의 값

- cover: 빈 공간없이 (div 공간만큼) 이미지로 가득 채워라
- contain: 이미지가 잘리지 않도록 한다.

## margin collapse 현상

- div 박스 2개의 위쪽 테두리가 겹쳐 있으면 margin 설정을 공유하는 일종의 버그
- 박스의 위 아래 테두리가 겹칠 때도 적용된다.
- 해결방안은 두 박스를 떨어뜨리는 것
  - 예를 들면 한 쪽 박스에 padding을 둔다.

## position과 좌표 레이아웃 만들기

- position 기준 설정
- float처럼 공중에 뜬다.

### position 종류

- relative: 원래 위치를 기준으로
- absolute: relative를 가진 부모 태그를 기준으로
  - 가운데 정렬: left right=0, margin: auto, width: 있기만 하면 된다.
- fixed: 화면을 기준으로

### z-index

요소의 쌓임 순서를 결정한다. z-index가 높을 수록 앞에 있다.

## 반응형에 참고할 점

- 반응형 페이지를 만들기 위해서 width와 height에 %를 많이 사용하는데
- pc에서는 요소가 너무 커질 수 있다. 이럴 때, max-width와 min-width를 사용하면 좋다.
- width는 content 영역의 너비를 의미한다. 따라서 padding을 넣으면 max-width로 설정한 것보다 요소가 커진다.
  - box-sizing: border-box; 를 설정하면 width가 padding, border를 포함한다.

## vertical-align

- inline이나 inline-block의 세로 정렬에 사용된다.

## 부모 div가 자식 div를 포함하지 못할 때

- overflow: hidden;
  - 요소의 내용이 요소의 경계를 넘어갈 때, 잘리도록 설정

## nth-child

- table에서 n번째 등장하는 요소만 스타일링할 때, 사용하는 셀럭터
  -  예, .table th:nth-child(2)

## pseudo class

요소와 커서의 상호작용으로 트리거, (a, button, 등)

 - hover: 커서를 올려두면
 - focus: 커서로 선택한 후
 - active: 커서로 누르고 있으면
 - a
   - link: 방문 전
   - visited: 방문 후 

참고로 위 hover, focus, active의 순서가 중요하다.

## class 작명할 때

Block__Element--Modifier 룰을 따라보자.

