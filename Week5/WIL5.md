WIL5.md
=========
2023년 1학기 GDSC OC Web Study 5주차에 학습한 내용을 정리해보고자 한다.

Week5 - 2023. 04. 11. Tue.
=========
> "HTML: Hyper Text Markup Language"
> "CSS: Cascading Style Sheet"

```이번 과제는 https://poiemaweb.com/의 일부 내용을 읽으며 새로 알게 된 내용들을 정리하는 형식으로 진행될 것이다.```

1. HTML5의 기본 문법
    1. 빈 요소(Empty Element): content를 가질 수 없는 요소를 빈 요소(Empty element or Self-Closing element)라 한다. </br>
    빈 요소는 content가 없으며(필요가 없다) 어트리뷰트(Attribute)만을 가질 수 있다. </br>
    빈 요소 중 대표적인 요소는 아래와 같다. </br>
      - br
      - hr
      - img
      - input
      - link
      - meta
    
    2. 글로벌 어트리뷰트(HTML Global Attribute): 글로벌 어트리뷰트는 모든 HTML 요소가 공통으로 사용할 수 있는 어트리뷰트다. </br>
    몇몇 요소에는 효과가 적용되지 않을 수 있지만, 글로벌 어트리뷰트는 대체로 모든 요소에 사용될 수 있다. </br>
    자주 사용되는 글로벌 어트리뷰트는 아래와 같다. </br>
  
    Attribute	| Description
    --- | ---
    id | 유일한 식별자(id)를 요소에 지정한다. 중복 지정이 불가하다.
    class | 스타일시트에 정의된 class를 요소에 지정한다. 중복 지정이 가능하다.
    hidden | css의 hidden과는 다르게 의미상으로도 브라우저에 노출되지 않게 된다.
    lang | 지정된 요소의 언어를 지정한다. 검색엔진의 크롤링 시 웹페이지의 언어를 인식할 수 있게 한다.
    style | 요소에 인라인 스타일을 지정한다.
    tabindex | 사용자가 키보드로 페이지를 내비게이션 시 이동 순서를 지정한다.
    title | 요소에 관한 제목을 지정한다.
  
2. 시멘틱 웹(Sementic Web): '의미론적인 웹'이라는 뜻으로, 우리가 웹페이지에 탑재한 여러 정보들을 우리 뿐만 아니라 </br>
컴퓨터도 이해할 수 있도록 정리하는 것이다. 즉, 웹에 존재하는 수많은 웹페이지들에 메타데이터(Metadata)를 부여하여, </br>
기존의 잡다한 데이터 집합이었던 웹페이지를 ‘의미’와 ‘관련성’을 가지는 거대한 데이터베이스로 구축하고자 하는 발상이다. </br>
HTML 요소는 non-semantic 요소, semantic 요소로 구분할 수 있다. </br>
```
non-semantic 요소
div, span 등이 있으며 이들 태그는 content에 대하여 어떤 설명도 하지 않는다.
```
```
semantic 요소
form, table, img 등이 있으며 이들 태그는 content의 의미를 명확히 설명한다.
```
다음은 HTML5에서 새롭게 추가된 시맨틱 태그이다.

tag	| Description
--- | ---
header | 헤더를 의미한다
nav	| 내비게이션을 의미한다
aside	| 사이드에 위치하는 공간을 의미한다
section	| 본문의 여러 내용(article)을 포함하는 공간을 의미한다
article | 분문의 주내용이 들어가는 공간을 의미한다
footer | 푸터를 의미한다

3. 웹페이지를 구성하는 기본 태그
    1. head 태그: 메타데이터를 포함하기 위한 요소이며 웹페이지에 단 하나만 존재한다. </br>
    메타데이터는 HTML 문서의 title, style, link, script에 대한 데이터로 화면에 표시되지 않는다. </br>
    head 요소에는 메타데이터 이외의 화면에 표시되는 일체의 요소를 포함시킬 수 없다. </br>
        1. ```<style></style>```: HTML 문서를 위한 style 정보를 정의한다.
        2. ```<link>```: 외부 리소스와의 연계 정보를 정의한다. 주로 HTML과 외부 CSS 파일을 연계하는 데 사용된다. 
        3. ```<script></script>```: client-side JavaScript를 정의한다. src 어트리뷰트를 사용하면 외부 JavaScript 파일을 로드할 수 있다.
    2. meta 태그: charset, description, keywords, author, 기타 메타데이터 정의에 사용된다. 메타데이터는 브라우저, 검색엔진(keywords) 등에 의해 사용된다.

4. 텍스트 관련 태그
    1. 글자 형태 (Text Formatting) 태그
        1. ```em```: emphasized(강조, 중요한) text를 지정한다. i tag와 동일하게 Italic체로 표현된다. 의미론적(Semantic) 중요성의 의미를 갖는다.
        2. ```small```: small text를 지정한다.
        3. ```del```: deleted (removed) text를 지정한다.
        4. ```ins```: inserted (added) text를 지정한다.
        5. ```sub / sup```: sub 태그는 subscripted(아래에 쓰인) text를 sup 태그는 superscripted(위에 쓰인) text를 지정한다.
    2. 본문 태그
        1. 연속된 공백을 삽입하는 방법: ```&nbsp;```
        2. ```pre```: 형식화된(preformatted) text를 지정한다. pre 태그 내의 content는 작성된 그대로 브라우저에 표시된다.

5. CSS 기본 문법
    1. 셀렉터(Selector, 선택자): 셀렉터는 스타일을 적용하고자 하는 HTML 요소를 선택하기 위해 CSS에서 제공하는 수단이다.
    2. 프로퍼티(Property / 속성): 셀렉터로 HTML 요소를 선택하고 {} 내에 프로퍼티(속성)와 값을 지정하는 것으로 다양한 style을 정의할 수 있다. </br>
    프로퍼티는 표준 스펙으로 이미 지정되어 있는 것을 사용하여야하며 사용자가 임의로 정의할 수 없다. 여러 개의 프로퍼티를 연속해서 지정할 수 있으며 세미콜론(;)으로 구분한다.</br>
    3. 값(Value / 속성값): 셀렉터로 지정한 HTML 요소에 style을 적용하기 위해 프로퍼티를 사용했다. </br>
    4. 프로퍼티의 값은 해당 프로퍼티에 사용할 수 있는 값을 “키워드”나 “크기 단위” 또는 “색상 표현 단위” 등의 특정 단위로 지정하여야 한다.</br>

6. HTML과 CSS의 연동
    1. Link style: HTML에서 외부에 있는 CSS 파일을 로드하는 방식이다. 가장 일반적으로 사용된다.
    2. Embedding style: HTML 내부에 CSS를 포함시키는 방식이다. 매우 간단한 웹페이지의 경우는 문제될 것이 없겠지만 Link style을 사용하는 편이 좋다. </br>
    HTML과 CSS는 서로 역할이 다르므로 다른 파일로 구분되어 작성하고 관리되는 것이 바람직하다. </br>
    3. Inline style: HTML 요소의 style 프로퍼티에 CSS를 기술하는 방식이다. JavaScript가 동적으로 CSS를 생성할 때 사용하는 경우가 있다.</br>
    하지만 일반적인 경우 Link style을 사용하는 편이 좋다. </br>
    
7. Reset CSS 사용하기</br>
    모든 웹 브라우저는 디폴트 스타일(브라우저가 내장하고 있는 기본 스타일)을 가지고 있어 CSS가 없어도 작동한다. </br>
    그런데 웹브라우저에 따라 디폴트 스타일이 상이하고 지원하는 tag나 style도 제각각이어서 주의가 필요하다. </br>
    Reset CSS는 기본적인 HTML 요소의 CSS를 초기화하는 용도로 사용한다. 즉, 브라우저 별로 제각각인 디폴트 스타일을 하나의 스타일로 통일시켜 주는 역할을 한다. </br>
    자주 사용되는 Reset CSS는 다음과 같다. </br>
    - Eric Meyer’s reset
    - normalize.css
