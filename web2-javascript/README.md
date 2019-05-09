# WEB2 - JavaScript

생활코딩 WEB2 - JavaScript를 듣고 기록한 내용입니다.

----

# 1. JavaScript
기존 HTML로만 구현된 웹페이지는 정보를 표현하는 것 외에는 할 수 없었다. 즉, 정적이었다. 한 번 화면에 출력되면 자기 자신을 바꿀 수 없었다. 하지만, 사람들은 게임처럼 동적으로 사용자와 상호작용할 수 있는 웹페이지를 원하게 되었고, 그래서 태어난 기술이 **JavaScript** 였다.
이제 우리는 HTML을 통해 웹페이지를 생성하고, JavaScript를 이용해 사용자와 상호작용할 수 있는 기능을 추가할 수 있다. 결론적으로 JavaScript는 **HTML을 제어하는 언어** 이고, **HTML 위에서 동작하는 언어** 이다!

----

# 2. HTML과 JavaScript의 만남
## 2.1. ```<script>``` tag
  - HTML에 지금부터 JavaScript 코드가 시작된다는 것을 알리는 tag
  - ```<script>``` tag 안에서는 JavaScript 코드로 해석되기에 1+1이 문자열이 아니라, 연산으로 해석되기 떄문에 화면 출력시 2가 출력된다.
## 2.2. Event
  - JavaScript에서 'on으로 시작하는 속성
  - ```<input type="" value="" onJavaScript속성="">``` tag
    - type - 어떤 형태로 input을 받을 것인가.
      - button : 버튼 생성
      - text : 글자 입력
    - value - input에 글자를 넣을 수 있다.
    - onJavaScript속성 - 속성 값을 웹 브라우저가 기억해 뒀다가, event가 일어나면 속성 값이 JavaScript코드를 실행한다.
      - ```onclick``` : 버튼을 클릭하면, 속성 값에 해당하는 JavaScript 코드를 실행한다.
      - ```onchange``` : 텍스트 상자의 내용이 변경되면, 속성 값에 해당하는 JavaScript 코드를 실행한다.
      - ```onkeydown``` : 키보드의 키를 누르면, 속성 값에 해당하는 JavaScript 코드를 실행한다.
## 2.3. Console
  - 간단한게 JavaScript코드로 데이터를 간단한게 처리하고 싶을 때 사용한다.  ex. 계산기, 사람 추첨
  - Console을 통해 실행되는 JavaScript코드는 열려 있는 웹 페이지를 대상으로 실행된다.

----

# 3. JavaScript 문법
## 3.1. 자료형
  - ```Number```
    - 숫자를 표현하는 자료형
  - ```String```
      - 문자열을 표현하는 자료형  
      - ''나 ""로 감싸면 String 자료형으로 인식된다.
    - ```String``` Properties
      - .length : 문자열의 길이 반환
      - .toUpperCase() : 대문자로 바꾼 문자열 반환
      - .indexOf('문자') : 해당 문자가 있는 index값 반환
      - .indexOf('문자열') : 해당 문자열이 시작되는 index값 반환
      - .trim() : 문자열의 공백을 제거한 문자열 반환
## 3.2. 변수와 대입연산자
  - 변수(Variable) : 바뀔 수 있는 값
  - 상수(Constant) : 바뀌지 않는 값
  - 대입연산자(=) : 오른쪽 항에 있는 값을 왼쪽에 있는 변수에 대입하는 연산자
## 3.3. 제어할 tag 선택하기
  - 내가 어떤 **tag** 의 **속성** 을 제어할 건지 선택을 해야 한다.
  <pre><code>
  document.querySelector(태그).태그의속성 = "속성값";
  </code></pre>
