# WEB2 - CSS

생활코딩 WEB2 - CSS를 듣고 기록한 내용입니다.

----

# 1. 더 예쁜 웹 페이지
사람들은 점점 더 예쁜 디자인의 웹페이지를 원하게 된다. 그에 대한 해결책은 두 가지였는데, 하나는 'HTML에 디자인과 관련된 tag를 추가하는 것'이고 다른 하나는 '디자인에 특화된 언어를 만드는 것'이었다. 전자는 비교적 쉬운 방법이었고, 후자는 새로운 언어를 만들내야 했기 때문에 어려웠다.  
그래서 사람들은 HTML에 디자인과 관련된 tag를 추가하게 되는데, 이는 두 가지의 큰 문제점을 가지고 있었다.   
첫 번째 문제점은 '디자인과 관련된 tag는 어떤 중요한 정보도 담고 있지 않다'는 것이었다. 예를 들면, `<h1>`이나 `<a>`와 같은 tag는 글자의 중요도나 링크를 담고 있지만, font와 같은 tag는 글자의 디자인 외에 어떤 중요한 정보도 알려주고 있지 않다.     
두 번째 이유는 '각각의 글자에 디자인과 관련된 tag를 일일이 달아줘야 하기 때문'이다. 예를 들면, 10억개의 디자인 tag가 있다고 생각해보자. 근데 client가 디자인을 바꿔달라고 요구를 했을 때 다시 그 tag를 일일이 바꿔야 한다. 매우 비효율적이고 시간이 오래 걸린다.   
그런 이유로 디자인에 특화된 언어 CSS가 등장하게 되었다. 이로 인해 HTML은 정보에 관한 내용만 전념할 수 있게 되고 CSS를 통해 더 효율적으로 웹 페이지를 디자인할 수 있게 되었다.

----

# 2. CSS문법
## 2.1. 웹 페이지에 CSS를 삽입하는 방법
### 2.1.1. `<style></style>` tag를 사용하는 방법
  - 웹 브라우저에게 여기서부터는 HTML이 아니라 CSS문법으로 해석할 것을 알려주는 tag
  - contents 내용이 아니기에 `<head></head>`에 위치해 있다
  - `<style></style>`안에 관련 tag의 이름을 적고 `{}`을 친 후 CSS효과를 준다.
    - 왜냐하면 CSS효과만 써두면 어떤 것에 그 효과를 적용할 건지 모르기 때문이다.
    - 속성을 부여하기로 한 tag name을 **선택자(selector)** 라고 하며, `{}`안에 있는 것들을 **선언(declaration)** 이라고 한다.
    - **선언(declaration)** 안에 `:`이전에 있는 것을 **속성(property)** 라고 하며, 이후에 속성에 부여되는 것을 **값(value)** 라고 한다.
    - 똑같은 선언을 사용한다면 `,선택자`로 구분하여 중복을 없앨 수 있다.  

### 2.1.2. `style` 속성을 이용하는 방법
  - 어떤 tag에 style속성을 부여하면 CSS 효과를 줄 수 있다.
  - `style=""`은 HTML속성이다. 다만 `style` 속성에 들어오는 값은 CSS로 해석이 된다.
  - 이 경우 따로 어떤 것에 효과를 지정하지 않기 때문에, 선택자가 필요가 없다.
  - 만약 `<style></style>` 태그와 `style`속성 부여를 둘 다 한 경우 후자에 우선순위가 부여된다.
    - 왜냐하면 뒤에 선언되어 있기 때문에 후에 코드에 덮여지기 때문이다.

----

## 2.2. CSS 속성(property)
### 2.2.1. 속성의 종류
#### `color`
  - 색상값이 저장되어 있는 미리 정의된 상수(ex. red, black)
  - #16진수 색상값
#### `text-decoration`
  - none : 글자에 어떤 효과도 주지 않는다.
  - underline : 글자에 밑줄을 그어준다.
#### `font-size`
  - medium : 기본적으로 지정되는 값
  - px값 : 해당 px값으로 크기가 부여된다.
  - xx-small / x-small / small / large / x-large / xx-large
#### `font-size`
  - left / right / center : 왼쪽 정렬 / 오른쪽 정렬 / 가운데 정렬
### 2.2.2. Box Model과 관련된 속성들
#### `border`
  - border와 관련된 속성값을 나열하여 border에 속성을 부여할 수 있다. 순서는 중요하지 않다.
  - `border-bottom`, `border-top`, `border-left`, `border-right`처럼 한 쪽만 `border`를 나타낼 수 있다.
#### `border-width`
  - px : 테두리의 두께
#### `border-color`
  - `color`와 속성값 동일
#### `border-style`
  - solid : 얇은 실선
  - dotted : 동그란 점으로 된 점선
  - dashed : 두꺼운 실선으로 된 점선
  - double : 굵은 실선
#### `display`
  - inline : 자신의 contents크기만큼을 테두리로 잡는다.
  - block : 화면 전체를 테두리로 잡는다.
  - none : tag를 보이지 않게 한다.
#### `padding`
  - border와 contents 사이의 간격 즉, border에서 안 쪽 간격을 의미한다.
#### `margin`
  - border에서 바깥 쪽 간격을 의미한다.
#### `width`, `height`
  - contents의 너비와 높이를 의미한다.
    - px값 : px값을 받아서 원하는 크기만큼 조정할 수 있다.
    - %값 : 전체 화면에서 차지하는 비율만큼 조정할 수 있다.

----

## 2.3. CSS 선택자(selector)
### 2.3.1. 선택자의 종류
#### 2.3.1.1.`id`
  - html tag 속성이다.
  - `id`의 의미를 생각해 본다면, 그 tag에 부여된 **고유한 속성** 이라고 볼 수 있다. 그러므로, **절대 중복 되서는 안** 된다.
  - `<style></style>` 혹은 css코드에 `#id이름`을 써줘야 id선택자로 인식한다.
#### 2.3.1.2. `class`
  - html tag의 속성이며, 값은 여러개가 올 수 있으며, 띄어쓰기로 구분을 한다.
  - `class`의 의미를 생각해 본다면, 글자를 grouping을 할 수 있다.
  - 그래서 유지/보수 때 class 선택자 내 declaration만 수정하면 일괄 수정이 가능하다.
  - `<style></style>`혹은 css코드에 `.class이름`을 써줘야 class선택자로 인식한다.
#### 2.3.1.3. `tag`
  - 우리가 아는 html tag이다.
### 2.3.2. 선택자의 우선순위
  - `id > class > tag`순이다. 만약 똑같은 형태의 선택자라면 **맨 마지막에 등장하는 선택자** 가 우선순위가 더 높다.
  - 그래서 코드를 짤 때 처음에 tag에 부여해야 하는 property를 먼저 생각하고, 점점 좁혀가면서 세세하게 꾸미면 된다.
### 2.3.3. 최대한 자세하게 하라!
  - 우리가 tag를 쓰는 데 있어서 분명 자주 쓰는 tag들은 몇 번이고 계속 쓰일 게 분명하다.
  - 근데, 속성을 부여하게 될 때 특정 `id` 혹은 `class` 안의 tag만 적용하고 싶을 떄가 있다.
  - 그런 경우, 그 `id`와 `class` 선택자를 써준 뒤 그 tag를 써주면 특정 `id`와 `class`안의 tag에만 속성을 적용할 수 있다.
### 2.3.4. 언제 class를 쓰고, 언제 id를 쓸까?
  - `class`는 item의 형태이다. 내가 현재 혹은 미래에 같은 스타일을 공유하는 한 개 이상의 element가 있을 경우 `class`를 쓰는 게 좋다.
    ex. tag, comment, toolbar-button, warning-message, email
  - `id`는 item의 고유한 이름이다. 즉, 한 번 쓰고 그 element 혼자 가질 스타일일 경우 `id`를 쓰는 게 좋다.
    ex. main-content, header, footer, left-sidebar

----

# 3. Box Model
## 3.1. 각각의 tag는 테두리를 가지고 있다!
### 3.1.1. block-level element
  - 화면 전체를 쓰는 tag들이 갖는 테두리
  - `<h1>`과 같은 tag들이 이러한 테두리를 갖고 있다.
  - 줄바꿈이 된다.
### 3.1.2. inline-level element
  - 자신의 contents 크기만큼을 쓰는 tag들이 갖는 테두리
  - `<a></a>`와 같은 tag들이 이러한 테두리를 갖는다.
## 3.2. Box Model의 구성
우리는 Box Model을 **개발자 도구** 를 이용하여 바로바로 조정할 수 있다. 즉, 결과를 바로 앎으로써 빠르게 수정을 할 수 있다.
<img src="./img/box_model.jpg" width="550" height="426"></img>

----

# 4. Grid
## 4.1. 관련 tag
### 4.1.1. `<div></div>`와 `<span></span>`
  - 오직 디자인 용도로 쓰기 위한 아무런 의미,정보가 없는 tag
  - `<div></div>`는 block-level element이고, `<span></span>`은 inline-level element이다.
### 4.1.2. `<div></div>`와 `<span></span>`은 언제 쓸까?
  - `<span></span>`은 그들 주위에 다른 elements로부터 분리되게 해준다. 그리고 줄바꿈을 하지 않는다. 주로 글자를 꾸밀 때 쓰인다.
  - `<div></div>`는 여러 elements들을 담는 container다. 그리고 줄바꿈이 된다. 주로 레이아웃을 만들 때 쓰인다.
## 4.2. Grid를 쓰는 방법
  - Grid로 만들기 위해서 하나로 묶으려는 contents들의 부모가 필요하다. 즉, 다시 `<div></div>`으로 묶어준다.
    - `<span></span>`안에 `<div></div>`가 들어갈 수 없으므로, `<div></div>`로 묶어주어야 한다.
    - 왜냐하면 `<div></div>`는 block-level element이기 때문이다.
    - 정리하자면 block-level element가 inline-level element에 들어갈 수 없다.
  - 부모 tag의 id값을 "grid"로 설정한다.
  - 여기까지가 디자인을 하기 위한 과정이다. 큰 의미가 없다.
  - id의 declaration에 `display: grid;`를 추가한다. 여기까지 하면 아무런 변화가 없다.
  - `grid-template-columns` 속성을 추가한다.
    - `grid-template-columns : 150px 1fr` - 첫 번째 칸은 150px 두번째 칸은 나머지를 차지한다.
    - `grid-template-columns : 1fr 2fr` - 전체를 3으로 봤을 떄, 첫 번째 칸은 1을, 두 번째 칸은 2를 차지한다.

----

# 5. 반응형 디자인
화면 크기에 따라 웹 페이지의 각 요소들이 **반응** 해서 최적화된 모양으로 바뀌는 것을 말한다.
## 5.1. 왜 반응형 디자인이 필요한 것일까?
웹은 운영체제와 상관 없이 PC든 스마트폰이든 모든 정보 시스템에서 동작하기 때문에 이런 여러가지 화면에 대응하기 위해 필요하다. 그리고 반응형 디자인을 구현하기 위해 CSS의 미디어 쿼리를 사용한다.
## 5.2. 미디어 쿼리 사용법
`@media(특정 조건){ 특정 조건 때의 속성 선언들 }`
  - 특정 조건
    - `min-width : 최소값` : width가 최소값보다 클 때 media안에 있는 속성이 적용이 된다.
    - `max-width : 최대값` : width가 최대값보다 작을 떄 media안에 있는 속성이 적용이 된다.

----

# 6. CSS코드의 재사용
지금까지 CSS코드를 삽입할 때 html파일 안에 주었다. 이런걸 'inline code'라고 한다. 하지만, 이런 코드는 유지/보수 시 매우 불편하다. 그래서 우리는 CSS코드를 밖으로 빼서 `.css`파일을 따로 빼고 html파일과 연결한다. 이것을 'external code'라고 한다.
## 6.1. CSS파일
  - css파일을 따로 생성한다.
  - 이 css파일을 적용하고자 하는 html파일의 `<head>`에 `<link rel="stylesheet" href="파일명.css" />`를 추가한다.
    - rel은 relationship의 줄임말로 내가 참조하는 파일이 어떤 유형인지 알려준다.
    - href은 링크로, 내가 연결하고자 하는 파일을 적어준다.
## 6.2. 좋은 점
  - 유지/보수시 매우 편리하고 재사용성이 높아진다.
  - html에 inline으로 코드를 쓰는 것보다 코드의 양이 줄었기 때문에 웹 페이지를 내려받을 때 인터넷 트래픽을 덜 쓸 수 있다.
    - 웹 브라우저는 처음 웹 페이지를 다운로드 할 때 파일을 저장해 놓는다.
    - 그 파일이 변경 사항이 있기 전까지는 기존의 있던 것을 그대로 가져와 사용자에게 보여준다.
    - 그러므로 트래픽을 줄이고 또한 웹 페이지를 빠르게 볼 수 있다.
