WIL5.md
=========
2023년 1학기 GDSC OC Web Study 5주차에 학습한 내용을 정리해보고자 한다.

Week5 - 2023. 04. 11. Tue.
=========
> "HTML: Hyper Text Markup Language" </br>
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
  
    Attribute | Description
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

8. CSS 셀렉터: style을 적용하고자 하는 HTML 요소를 셀렉터로 특정하고 선택된 요소에 스타일을 정의하는 것이다. </br>
복수개의 셀렉터를 연속하여 지정할 수 있으며 쉼표( , )로 구분한다. </br>

패턴 | Description
--- | ---
```* (전체 셀렉터/Unibersal Selector)``` | HTML 문서 내의 모든 요소를 선택한다. html 요소를 포함한 모든 요소가 선택된다. (head 요소도 포함된다)
```태그명 (태그 셀렉터/Type Selector)``` | 지정된 태그명을 가지는 요소를 선택한다.
```#id 어트리뷰트 값 (ID 셀렉터/ID Selector)``` | id 어트리뷰트 값을 지정하여 일치하는 요소를 선택한다. id 어트리뷰트 값은 중복될 수 없는 유일한 값이다.
```.class 어트리뷰트 값 (클래스 셀렉터/Class Selector)``` | class 어트리뷰트 값을 지정하여 일치하는 요소를 선택한다. class 어트리뷰트 값은 중복될 수 있다.
```셀렉터[어트리뷰트] (어트리뷰트 셀렉터/Attribute Selector)``` | 지정된 어트리뷰트를 갖는 모든 요소를 선택한다.
```셀렉터[어트리뷰트=”값”]``` | 지정된 어트리뷰트를 가지며 지정된 값과 어트리뷰트의 값이 일치하는 모든 요소를 선택한다.
```셀렉터[어트리뷰트~=”값”]```	| 지정된 어트리뷰트의 값이 지정된 값을 (공백으로 분리된) 단어로 포함하는 요소를 선택한다.
```셀렉터[어트리뷰트/=”값”](슬래쉬가 아니라 버티컬바이다)```	| 지정된 어트리뷰트의 값과 일치하거나 지정 어트리뷰트 값 뒤 연이은 하이픈(“값-“)으로 시작하는 요소를 선택한다.
```셀렉터[어트리뷰트^=”값”]```	| 지정된 어트리뷰트 값으로 시작하는 요소를 선택한다.
```셀렉터[어트리뷰트$=”값”]```	| 지정된 어트리뷰트 값으로 끝나는 요소를 선택한다.
```셀렉터[어트리뷰트*=”값”]```	| 지정된 어트리뷰트 값을 포함하는 요소를 선택한다.

이 외에도 복합 셀렉터(Combinator), 가상 클래스 셀렉터(Pseudo-Class Selector), 가상 요소 셀렉터(Pseudo-Element Selector)가 있으며 </br>
이 친구들은 위 웹페이지에 자세히 설명되어있다. </br>

9. CSS 프로퍼티 값의 단위 </br>
    1. 크기 단위: px은 절대값이고 em, %는 상대값이다.
        1. px: 1px은 화소 1개 크기, 대부분의 브라우저는 1px을 1/96 인치의 절대단위로 인식한다.
        2. %: %는 백분율 단위의 상대 단위이다. 요소에 지정된 사이즈(상속된 사이즈나 디폴트 사이즈)에 상대적인 사이즈를 설정한다.
        3. em: em은 배수(倍數) 단위로 상대 단위이다. 요소에 지정된 사이즈(상속된 사이즈나 디폴트 사이즈)에 상대적인 사이즈를 설정한다. </br>
        예를 들어 1em은 요소에 지정된 사이즈와 같고 2em은 요소에 지정된 사이즈의 2배이다. </br>
        폰트 사이즈 설정이나 콘텐츠를 포함하는 컨테이너의 크기 설정에 사용하면 상대적인 설정이 가능하여 편리하다.</br>
        중첩된 자식 요소에 em을 지정하면 모든 자식 요소의 사이즈에 영향을 미치기 때문에 주의하여야 한다.</br>
        4. rem: em의 기준은 상속의 영향으로 바뀔 수 있다. 즉, 상황에 따라 1.2em은 각기 다른 값을 가질 수 있다. </br>
        rem은 최상위 요소(html)의 사이즈를 기준으로 삼는다. rem의 r은 root를 의미한다. </br>
        폰트 사이즈 뿐만이 아니라 콘텐츠의 크기에 따라 가변적으로 대응하여야 하는 wrapper 요소(container) 등에 적합하다. </br>
        Reset CSS를 사용하여 사전에 html 요소의 font-size 지정이 필요하다. font-size 미지정 시에는 16px가 적용된다. </br>
            
        5. Viewport 단위(vh, vw, vmin, vmax) </br>
            
            단위 | Description
            --- | ---
            vw | viewport 너비의 1/100
            vh | viewport 높이의 1/100
            vmin | viewport 너비 또는 높이 중 작은 쪽의 1/100
            vmax | viewport 너비 또는 높이 중 큰 쪽의 1/100
            
    2. 색상 표현 단위: red, blue와 같은 키워드 이외에도 사용할 수 있는 단위가 많다. </br>
  
        단위 | 사용예
        --- | ---
        HEX 코드 단위 (Hexadecimal Colors) | #000000
        RGB (Red, Green, Blue) | rgb(255, 255, 0)
        RGBA (Red, Green, Blue, Alpha/투명도) | rgba(255, 255, 0, 1)
        HSL (Hue/색상, Saturation/채도, Lightness/명도) | hsl(0, 100%, 25%)
        HSLA (Hue, Saturation, Lightness, Alpha) | hsla(60, 100%, 50%, 1)
        
10. 박스 모델: 웹디자인은 콘텐츠를 담을 박스 모델을 정의하고 CSS 프로퍼티를 통해 스타일(배경, 폰트와 텍스트 등)과 위치 및 정렬을 지정하는 것이라고 할 수 있다. </br>

    명칭 | 설명
    --- | ---
    Content | 요소의 텍스트나 이미지 등의 실제 내용이 위치하는 영역이다. width, height 프로퍼티를 갖는다.
    Padding | 테두리(Border) 안쪽에 위치하는 요소의 내부 여백 영역이다. padding 프로퍼티 값은 패딩 영역의 두께를 의미하며 기본색은 투명(transparent)이다. 요소에 적용된 배경의 컬러, 이미지는 패딩 영역까지 적용된다.
    Border | 테두리 영역으로 border 프로퍼티 값은 테두리의 두께를 의미한다.
    Margin | 테두리(Border) 바깥에 위치하는 요소의 외부 여백 영역이다. margin 프로퍼티 값은 마진 영역의 두께를 의미한다. 기본적으로 투명(transparent)하며 배경색을 지정할 수 없다.
    
    1. width / height 프로퍼티: width와 height 프로퍼티는 요소의 너비와 높이를 지정하기 위해 사용된다. 이때 지정되는 요소의 너비와 높이는 콘텐츠 영역을 대상으로 한다. </br>
    ```overflow: hidden;```을 지정하면 넘친 콘텐츠를 감출 수 있다.</br>
    2. margin / padding 프로퍼티: content의 4개 방향(top, right, left, bottom)에 대하여 지정이 가능하다.
    3. border 프로퍼티
        1. border-style: 테두리 선의 스타일을 지정한다.
        2. border-width: 테두리의 두께를 지정한다. border-width 프로퍼티는 border-style과 함께 사용하지 않으면 적용되지 않는다.
        3. border-color: 테두리의 색상을 지정한다. border-color 프로퍼티는 border-style과 함께 사용하지 않으면 적용되지 않는다.
        4. border-radius: 테두리 모서리를 둥글게 표현하도록 지정한다. 프로퍼티 값은 길이를 나타내는 단위(px, em 등)와 %를 사용한다. </br>
        각각의 모서리에 border-radius 프로퍼티를 개별적으로 지정할 수도 있고 4개의 모서리를 short-hand로 한번에 지정할 수도 있다. </br>
        하나 혹은 두개의 반지름을 설정하여 각각의 모서리 굴곡을 설정할 수 있기 때문에 원 혹은 타원의 모양으로 정의가 가능하다. </br>
        5. border: border-width, border-style, border-color를 한번에 설정하기 위한 shorthand 프로퍼티이다.
    4. box-sizing 프로퍼티: width, height 프로퍼티의 대상 영역을 변경할 수 있다. </br>
    
    키워드 | 설명
    --- | ---
    content-box | width, height 프로퍼티 값은 content 영역을 의미한다. (기본값)
    border-box | width, height 프로퍼티 값은 content 영역, padding, border가 포함된 값을 의미한다.
    
11. 폰트와 텍스트: 폰트의 크기, 폰트의 지정, 폰트의 스타일, 텍스트 정렬 등을 정의한다.
    1. font-size: 텍스트의 크기를 정의한다.
    2. font-family: 폰트를 지정한다. 컴퓨터에 해당 폰트가 설치되어 있지 않으면 적용되지 않는다.
    3. font-style / font-weight: font-style 프로퍼티는 이탤릭체의 지정, font-weight 프로퍼티는 폰트 굵기 지정에 사용된다.
    4. font Shorthand: 한번에 설정하기 위한 shorthand 프로퍼티이다. </br>
    ```font : font-style(optional) font-variant(optional) font-weight(optional) font-size(mandatory) line-height(optional) font-family(mandatory)```
    5. line-height: 텍스트의 높이를 지정한다. 텍스트 수직 정렬에도 응용되어 사용된다.
    6. letter-spacing: 글자 사이의 간격을 지정한다.
    7. text-align: 텍스트의 수평 정렬을 정의한다.
    8. text-decoration: 링크 underline을 제거할 수 있다. 또는 텍스트에 underline, overline, line-through를 추가할 수도 있다.
    9. white-space: white space는 공백(space), 들여쓰기(tab), 줄바꿈(line break)을 의미한다. </br>
    html은 기본적으로 연속된 공백(space), 들여쓰기(tab)는 1번만 실행되며 줄바꿈(line break)은 무시된다. </br>
    또한 텍스트는 부모의 가로 영역을 벗어나지 않고 자동 줄바꿈(wrap)된다. </br>
    
    프로퍼티값 | line break | space/tab | wrapping(자동 줄바꿈)
    --- | --- | --- | ---
    normal | 무시 | 1번만 반영 | O
    nowrap | 무시 | 1번만 반영 | X
    pre | 반영 | 그대로 반영 | X
    pre-wrap | 반영 | 그대로 반영 | O
    pre-line | 반영 | 1번만 반영 | O
    
    10. text-overflow: 부모 영역을 벗어난 wrapping(자동줄바꿈)이 되지 않은 텍스트의 처리 방법을 정의한다. 이 프로퍼티를 사용하기 위해서는 아래의 조건이 필요하다. </br>
        - width 프로퍼티가 지정되어 있어야 한다. 이를 위해 필요할 경우 block 레벨 요소로 변경하여야 한다.
        - 자동 줄바꿈을 방지하려면 white-space 프로퍼티를 nowrap으로 설정한다.
        - overflow 프로퍼티에 반드시 “visible” 이외의 값이 지정되어 있어야 한다.
   
        프로퍼티값 | Description | ---
        --- | --- | ---
        clip | 영역을 벗어난 텍스트를 표시하지 않는다. (기본값) |	 
        ellipsis | 영역을 벗어난 텍스트를 잘라내어 보이지 않게 하고 말줄임표(…)를 표시한다. | 	 
        <!– | ```<string>``` | 프로퍼티 값으로 지정한 임의의 문자열을 출력한다. Firefox(9.0~)만 지원하는 기능이다. –>

    11. word-wrap: 한 단어의 길이가 길어서 부모 영역을 벗어난 텍스트의 처리 방법을 정의한다. </br>
    link 등을 표기할 때(e.g. https://poiemaweb.com/css3-font-text) 그 길이가 매우 길어지는데 이 프로퍼티를 사용하지 않으면 부모 영역을 넘어가게 된다. </br>
    12. word-break: 한 단어의 길이가 길어서 부모 영역을 벗어난 텍스트의 처리 방법을 정의한다. </br>
    word-wrap 프로퍼티는 단어를 어느 정도는 고려하여 개행하지만(.,- 등을 고려한다) word-break: break-all;는 단어를 고려하지 않고 부모 영역에 맞추어 강제 개행한다. </br>
    
12. 요소의 위치 정의
    1. position: 요소의 위치를 정의한다. top, bottom, left, right 프로퍼티와 함께 사용하여 위치를 지정한다.
        1. static (기본 위치): position 프로퍼티의 기본값으로 position 프로퍼티를 지정하지 않았을 때와 같다.
        2. relative (상대 위치): 기본 위치(static으로 지정되었을 때의 위치)를 기준으로 좌표 프로퍼티(top, bottom, left, right)를 사용하여 위치를 이동시킨다.
        3. absolute (절대 위치): 부모 요소 또는 가장 가까이 있는 조상 요소(static 제외)를 기준으로 좌표 프로퍼티(top, bottom, left, right)만큼 이동한다.
        4. fixed (고정 위치): 부모 요소와 관계없이 브라우저의 viewport를 기준으로 좌표 프로퍼티(top, bottom, left, right)을 사용하여 위치를 이동시킨다. </br>
        스크롤이 되더라도 화면에서 사라지지 않고 항상 같은 곳에 위치한다. </br>
        fixed 프로퍼티 선언 시, block 요소의 width는 inline 요소와 같이 content에 맞게 변화되므로 적절한 width를 지정하여야 한다. </br>
    2. z-index 프로퍼티: z-index 프로퍼티에 큰 숫자값을 지정할수록 화면 전면에 출력된다. positon 프로퍼티가 static 이외인 요소에만 적용된다.
    3. overflow 프로퍼티: 자식 요소가 부모 요소의 영역를 벗어났을 때 처리 방법을 정의한다.
    
    프로퍼티값 | Description
    --- | ---
    visible | 영역을 벗어난 부분을 표시한다. (기본값)
    hidden | 영역을 벗어난 부분을 잘라내어 보이지 않게 한다.
    scroll | 영역을 벗어난 부분이 없어도 스크롤 표시한다.(현재 대부분 브라우저는 auto과 동일하게 작동한다)
    auto | 영역을 벗어난 부분이 있을때만 스크롤 표시한다.

13. 요소 정렬: float 프로퍼티는 주로 레이아웃을 구성할 때 블록 레벨 요소를 가로 정렬하기 위해 사용되는 중요한 기법이다. </br>
flexbox 레이아웃를 사용한다면 더욱 간단하게 정렬을 구현할 수도 있지만 flexbox 레이아웃을 지원하지 않는 IE를 고려해야 한다면 float 프로퍼티를 사용해야 한다. </br>
float 프로퍼티를 사용할 때 요소의 위치를 고정시키는 position 프로퍼티의 absolute를 사용하면 안된다. </br>

    프로퍼티값 | Description
    --- | ---
    none | 요소를 떠 있게 하지 않는다. (기본값)
    right | 요소를 오른쪽으로 이동시킨다
    left | 요소를 왼쪽으로 이동시킨다.
    1. 정렬: float 프로퍼티를 사용하지 않은 블록 요소들은 수직으로 정렬된다. </br>
    float:left; 프로퍼티를 사용하면 왼쪽부터 가로 정렬되고, float:right; 프로퍼티를 사용하면 오른쪽부터 가로 정렬된다. </br>
    오른쪽 가로 정렬의 경우, 먼저 기술된 요소가 가장 오른쪽에 출력되므로 출력 순서가 역순이 된다. </br>
    float 프로퍼티는 좌측, 우측 가로 정렬만 할 수 있다. 중앙 가로 정렬은 margin 프로퍼티를 사용해야 한다. </br>
    2. width: width 프로퍼티의 기본값은 100%이므로 width 프로퍼티값을 지정하지 않은 block 요소는 부모 요소의 가로폭을 가득 채운다. </br>
    width 프로퍼티를 선언하지 않은 block 레벨 요소에 float 프로퍼티가 선언되면 width가 inline 요소와 같이 content에 맞게 최소화되고 다음 요소 위에 떠 있게(부유하게) 된다. </br>
    3. float 프로퍼티 관련 문제 해결 방법
        1. float 프로퍼티가 선언된 요소와 float 프로퍼티가 선언되지 않은 요소간 margin이 사라지는 문제 </br>
        answer) 두번째 요소에 float 프로퍼티를 선언하지 않았기 때문에 발생하는 박스 모델 상의 문제이다. </br>
        이 문제를 해결하는 가장 쉬운 방법은 float 프로퍼티를 선언하지 않은 요소에 overflow: hidden 프로퍼티를 선언하는 것이다. </br>
        overflow: hidden 프로퍼티는 자식 요소가 부모 요소의 영역보다 클 경우 넘치는 부분을 안보이게 해주는 역할을 하는데 </br>
        여기서는 float 프로퍼티가 없어서 제대로 표현되지 못하는 요소를 제대로 출력해준다. </br>
        2. float 프로퍼티가 선언된 자식 요소를 포함하는 부모 요소의 높이가 정상적으로 반영되지 않는 문제 </br>
        answer) float 프로퍼티가 선언된 자식 요소의 부모 요소에 overflow: hidden 프로퍼티를 선언하는 것이다.
