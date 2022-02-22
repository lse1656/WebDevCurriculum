# Quest 01. HTML과 웹의 기초

## Introduction
* HTML은 HyperText Markup Language의 약자로, 웹 브라우저에 내용을 표시하기 위한 가장 기본적인 언어입니다. 이번 퀘스트를 통해 HTML에 관한 기초적인 사항들을 알아볼 예정입니다.

## Topics
* HTML의 역사
  * HTML 4.01, XHTML 1.0, XHTML 1.1
  * XHTML 2.0과 HTML5의 대립
  * HTML5와 현재
* 브라우저의 역사
  * Mosaic와 Netscape
  * Internet Explorer의 독점시대
  * Firefox와 Chrome의 등장
  * iOS Safari와 모바일 환경의 브라우저
  * Edge와 Whale 등의 최근의 Chromium 계열 브라우저
* HTML 문서의 구조
  * `<html>`, `<head>`와 `<body>` 등의 HTML 문서의 기본 구조
  * 시맨틱 엘리먼트
  * 블록 엘리먼트와 인라인 엘리먼트의 차이

## Resources
* [MDN - HTML](https://developer.mozilla.org/ko/docs/Web/HTML)
* [HTML For Beginners](https://html.com/)
* [History of the web browser](https://en.wikipedia.org/wiki/History_of_the_web_browser)
* [History of HTML](https://en.wikipedia.org/wiki/HTML)
* [StatCounter](https://gs.statcounter.com/)

## Checklist
* HTML 표준의 역사는 어떻게 될까요?<br/>
&nbsp;HTML은 웹페이지의 컨텐츠를 다양한 환경에서 열람해도 동일하게 볼 수 있도록 하기 위해 생겨난 것이다. 표준화를 위한 노력 끝에 현재의 HTML5가 완전한 표준으로 정착되었다.<br/><br/>
  * HTML 표준을 지키는 것은 왜 중요할까요?<br/>
  &nbsp;여러 이유가 있지만 웹 표준을 지켜야 다양한 브라우저나 장애인 지원용 프로그램에서도 대응이 가능하므로 접근성이 향상되기 때문이다<br/><br/>
  * XHTML 2.0은 왜 세상에 나오지 못하게 되었을까요?<br/>
  &nbsp;XTHML은 HTML과 동등한 표현능력을 지닌 XML 마크업 언어로 HTML 보다 엄격한 문법을 가지고 있다. XTML 2.0은 하위 호완성에 대한 문제 때문에 이전의 태그들로 작성된 것들이 사용되지 않을 수 있다는 문제점이 있고 문법이 엄격하여 습득에 어려움이 있어 점차 사용자들에게 외면받았다.<br/><br/>
  * HTML5 표준은 어떤 과정을 통해 정해질까요?<br/>
  &nbsp;W3C의 정기적인 컨소시엄을 통해 W3C 권고안을 발표한다. 또한 웹에 관해 토론할 수 있는 열린 포럼 등을 통하여 사용자의 불편함을 이해하고 차기 표준안에 반영할 수 있도록 지속적인 활동을 수행한다.<br/><br/>
* 브라우저의 역사는 어떻게 될까요?<br/>
  * Internet Explorer가 브라우저 시장을 독점하면서 어떤 문제가 일어났고, 이 문제는 어떻게 해결되었을까요?
  * 현재 시점에 브라우저별 점유율은 어떻게 될까요? 이 브라우저별 점유율을 알아보는 것은 왜 중요할까요?<br/>
  &nbsp;2022년 1월 기준 크롬이 63.6%로 가장 많고 사파리 19.8%, 파이어폭스 4.1%, 엣지 4.1%를 차지하며 ie의 경우 0.4%로 가장 적다. 사용자 환경을 파악하고 크로스 브라우징에 대응하기 위해서 브라우저별 점유율을 알아보는 것은 중요하다.<br/><br/>
  * 브라우저 엔진(렌더링 엔진)이란 무엇일까요? 어떤 브라우저들이 어떤 엔진을 쓸까요?<br/>
  &nbsp;브라우저 엔진은 모든 웹 브라우저의 핵심이 되는 소프트웨어 구성 요소이다. 주된 역할은 컨텐츠를 사용자의 화면에 상호작용적인 시각 표현으로 변환시키는 것이다.

      |Browser|Rendering engine|
      |---|---|
      |Internet Explorer|Trident|
      |Firefox|Gecko|
      |Safari|Webkit|
      |Chrome, Opera, Edge|Blink(a fork of Webkit)|

  * 모바일 시대 이후, 최근에 출시된 브라우저들은 어떤 특징을 가지고 있을까요?<br/>
  &nbsp;웹 브라우저를 보다 소형화 하면서 빠른 속도와 적은 데이터 용량을 기반으로 하면서 디바이스별로 반응형 뷰를 제공가능한 브라우저들이 대두되고 있다. 
* HTML 문서는 어떤 구조로 이루어져 있나요?
  * `<head>`에 자주 들어가는 엘리먼트들은 어떤 것이 있고, 어떤 역할을 할까요?
  * 시맨틱 태그는 무엇일까요?<br/>
   &nbsp;semantic은 '의미있는, 의미론적인'이라는 뜻으로 말 그대로 의미가 담긴 태그를 말한다.<br/><br/>
    * 시맨틱 엘리먼트를 사용하면 어떤 점이 좋을까요?<br/>
    &nbsp;시멘틱 태그에 의해 컴퓨터가 HTML 요소의 의미를 보다 명확히 해석하고 기존의 잡다한 데이터 집합이었던 웹페이지에 <strong>의미</strong>와 <strong>관련성</strong>을 부여한다. 또한 검색엔진최적화(SEO)가 보다 효율적이고 잘 되도록 도와준다.<br/><br/>
    * `<section>`과 `<div>`, `<header>`, `<footer>`, `<article>` 엘리먼트의 차이점은 무엇인가요?<br/>
    section - 서로 관계있는 문서를 분리하는 역할<br/>
    article - 내용이 각기 독립적이고 홀로 설 수 있는 내용(블로그글, 포럼글,뉴스기사)<br/>
    div - 아무 의미 없이 단순하게 구분하고 싶을 때 사용<br/><br/>

  * 블록 레벨 엘리먼트와 인라인 엘리먼트는 어떤 차이가 있을까요?<br/>
  인라인 : text 크기만큼만 공간을 점유하고 줄바꿈을 하지 않는다.<br/>
  블록 : 무조건 한 줄을 점유하고 있고, 다음 태그는 무조건 줄바꿈이 적용된다.<br/>

## Quest
* [이 화면](screen.png)의 정보를 HTML 문서로 표현해 보세요. 다만 CSS를 전혀 사용하지 않고, 문서의 구조가 어떻게 되어 있는지를 파악하여 구현해 보세요.
  * [CSS Naked Day](https://css-naked-day.github.io/)는 매년 4월 9일에 CSS 없는 웹 페이지를 공개하여 내용과 마크업에 집중한 HTML 구조의 중요성을 강조하는 행사입니다.
* 폴더에 있는 `skeleton.html` 파일을 바탕으로 작업해 보시면 됩니다.
  * 화면을 구성하는 큰 요소들을 어떻게 처리하면 좋을까요?
  * HTML 문서상에서 같은 층위에 비슷한 요소들이 반복될 때는 어떤 식으로 처리하는 것이 좋을까요?

## Advanced
* XML은 어떤 표준일까요? 어떤 식으로 발전해 왔을까요?
* YML, Markdown 등 다른 마크업 언어들은 어떤 특징을 가지고 있고, 어떤 용도로 쓰일까요?
