# WEB1 - HTML & Internet

생활코딩 WEB1 - HTML & Internet을 듣고 기록한 내용입니다.

----
# 1. tag
## 1) tag란 무엇인가?
  - tag는 어떤 정보를 담고 있다.
  - tag의 설명이 부족할 경우 속성(attribute)를 부여한다.
    - 속성부여시 더 많은 의미를 부여할 수 있다.
    - 속성부여시 순서는 상관이 없다.
  - `<parent><child></child></parent>`
      - 부모 자신관계가 수시로 바뀌는 tag도 있고
      - 서로 꼭 붙어있는 tag도 있다.
  - 시각적으로 비슷한 거는 의미가 없다. 그에 맞는 tag를 사용해야 의미가 있다.

## 2) tag의 종류
### * 가장 최상위 tag
  - `<html></html>`
    - `<head>`와 `<body>`를 포함한다.

### * 본문과 관련된 tag
  -  `<body></body>`
    - 본문과 관련된 부분을 묶는데 사용된다.
  -  `<strong></strong>`
    - 글자를 강조한다.
  - `<u></u>`
    - 글자에 밑줄을 긋는다.
  - `<h1></h1>`
    - 글자에 Bold를 취하고, 줄바꿈을 한다.
    - 6까지 있으며 아래로 갈수록 중요성이 떨어진다.
  - `<br>`
    - 줄바꿈을 한다.
    - 원하는 만큼 줄바꿈을 할 수 있다. 3번 하면 3번 줄바꿈을 할 수 있다.
  - `<p></p>`
    - 단락을 나눈다.
    - `<br>`과 다르게 연속해서 줄바꿈을 할 수 없지만, css문법을 통해서 자세히 조정할 수 있다.
  - `<img src="" width="">`
    - 이미지를 삽입한다.
    - src는 폴더의 파일명을 말하며 width는 이미지의 간격을 말한다.
    - width에서 px값으로 설정할 경우 그 px크기만큼 조정되고 %로 설정할 경우 웹페이지의 크기의 비율에 맞춘다.
  - `<li></li>과 <ul></ul>과 <ol></ol>`
    - 목차를 만든다.
    - `<ul></ul>`과 `<ol></ol>`은 `<li></li>`의 부모 tag이고, 서로 부모-자식 관계를 갖는다. 즉, 떨어질 수 없다.
    - `<li></li>`가 만든 목차의 경계를 짓기 위한, 그룹핑을 하기 위한 tag이다.
    - `<ul></ul>`은 Unordered List, <ol></ol>은 Ordered List이다.
  - `<table></table>와 <tr></tr>와 <td></td>와 <th></th>`
      - `<table></table>`은 HTML 표를 만든다.
      - `<tr></tr>`은 표의 행을 말한다.
      - `<th></th>`와 `<td></td>`는 표의 셀을 말한다.
          - `<th>`는 bold체에 가운데 정렬을 한다.
          - `<td>`는 평범체에 왼쪽 정렬을 한다.
      - 위의 3개(혹은 4개)의 tag들은 부모-자식 관계이기에 항상 붙어다닌다.
  - `<a href = "주소" target="_blank" title="html5 specification"></a>`
    - a는 anchor를 뜻한다. 정보의 바다인 곳에 닻을 내린다고 생각하면 된다.
    - <a></a>만 써주면 안되고 어디 링크로 연결할 것인지 써줘야 한다.
    - href(hypertext reference)로 ""에 주소를 적어주면 된다.
    - target에 새 창으로 열어주고 싶우면 위와 같이 해주면 된다.
    - title에 링크 전 마우스를 가져다 댔을 때의 설명(tooltip)을 추가할 수 있다.

### * 본문을 설명하는 tag
  - `<head></head>`
    - 본문을 설명하는 tag를 묶는데 사용된다.
  - `<title></title>`
    - 웹페이지의 제목을 설정한다.
    - 책표지의 제목을 쓰는 것과 같다.
  - `<meta charset="utf-8">`
    - 브라우저에게 utf-8로 html을 읽을 것을 알려준다.

----

# 2. WEB과 Internet
## 1) WEB
Internet 안에 WEB이라는 서비스가 존재하는 것이다. 그 서비스는 WEB에만 국한된게 아니라 FTP(파일 전송), email 등이 있다.
Internet은 1960부터 만들어져 있었다. 이게 WEB과 만나면서 지식인의 소유물이었던 Internet이 대중화가 되면서 지금의 상태가 되었다.

## 2) Internet
Web Browser가 설치된 컴퓨터는 Web Server에게 정보를 요구(request)하고 반대로 Web Server가 설치된 컴퓨터는 그 요구에 응답(response)한다.
그래서 요청하는 컴퓨터를 Client, 요청을 받아 정보를 제공하는 컴퓨터를 Server라고 한다.
Web Server를 사용한다는 것은 내 컴퓨터에 있는 문서를 인터넷이 연결되어 있는 컴퓨터에 Web Browser를 깔 가져다가 볼 수 있도록 하는 것이다.
이 Web Server를 써보려면 내가 직접 Web Server를 설치를 하거나 Web Hosting 업체에 대행을 해야 한다. 하지만, 직접 Web Server를 설치를 하는 것은 어려워서 주로 Web Hosting을 하지만, 서버를 이해하기 위해서는 Web Server를 직접 만들어 보는 것이 좋다.
