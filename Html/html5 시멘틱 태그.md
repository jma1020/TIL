# HTML5 Sementic Tag

시맨틱(sementic) : '의미가 통하는'이라는 뜻으로 시맨틱태그는 태그만 보고도 페이지 구조를 쉽게 이해할 수 있도록 정의된 태그를 의미


## HTML4 vs HTML5 문서

HTML4는 div태그로 주로 화면 구성을 하였고, 수 많은 태그들을 다시 id 속성으로 구분했다. 하지만 수천 줄이 넘는 코드에서 일일이 헤더, 메뉴, 사이드바를 찾는 것은 쉽지 않았다. 그러한 이유때문에 HTML5에서 시맨틱 태그가 등장했다.

---

시맨틱 태그로 작성한 소스를 보면 태그만 보고도 어느 부분이 제목이고 메뉴이고 실제 내용인지 쉽게 알 수 있다.

### 문서 구조를 위한 HTML5 시맨틱 태그


* `<header>` : 머리말 지정
    - 주로 페이지 맨 위쪽이나 왼쪽에 삽입한다.
    - `<nav>`를 이용해 사이트 메뉴를 넣는다.
    - 그리고 본문 중에 사용해 머리말로 쓸 수도 있다.
    - `<header>` 내부에 `<header>` 혹은 `<footer>`가 올 수 없다.

* `<main>` : 주요 콘텐츠
    - 주요 콘텐츠는 문서의 핵심 주제나 애플리케이션의 핵심 가능성에 대한 부연, 직접적으로 연관된 콘텐츠로 이루어짐
    - IE에서 지원하지 않고 있다.
    - 한 문서에 하나의 요소만 포함 가능

* `<section>` : 주제별 콘텐츠 영역 나타내기 / 문서의 일반적인 영역을 설정 / 문서를 다른 주제로 구분 짓기위해 사용
    - 섹션제목(h1~h6)
    - `<section>`안에 `<section>`을 쓸 수 있다. 
    - 문맥 흐름 중에서 콘텐츠를 주제별로 묶을 때 사용(article내에서도 사용가능)

* `<article>` : 콘텐츠 내용 넣기 / 독립적으로 구분되거나 재사용 가능한 영역을 설정
    - 웹상의 실제 내용을 넣는다.
    - 태그를 적용한 부분을 떼어 독립적으로 배포하거나 재사용해도 완전한 하나의 콘텐츠가 된다면 사용

* `<aside>` : 본문 이외의 내용 표시
    - 사이드바(필수 요소 아님) - 광고, 링크모음 등등

* `<nav>` : 문서를 연결하는 내비게이션 링크(Navigation 약자)
    - 내비게이션 메뉴뿐만 아니라 footer에 사이트 링크 모음에도 많이 사용

* `<iframe>` : 외부 문서 삽입
    - 웹 문서 안에 다른 웹 문서를 가져와 표시하는 것(inline frame)

* `<address>` : 사이트 제작자 정보, 연락처 정보(주소, 이메일, 전화번호)
    - 주로 footer안에 사용
    
* `<div>` : 콘텐츠를 묶어 시각적 효과를 적용할 때 사용(CSS적용)
    - 본질적으로 아무것도 나타내지 않는 콘텐츠 영역을 설정

* `<footer>` : 제작 정보와 저작권 표시
    - header, section, article등 다른 레이아웃 태그들을 모두 사용할 수 있음
    - `<footer>` 내부에 `<header>` 혹은 `<footer>`가 올 수 없다

