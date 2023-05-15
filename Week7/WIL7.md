WIL7.md
=========
2023년 1학기 GDSC OC Web Study 7주차에 학습한 내용을 정리해보고자 한다.

Week7 - 2023. 05. 09. Tue.
=========
> "HTML: Hyper Text Markup Language" </br>
> "CSS: Cascading Style Sheet"

이번 WIL에는 YouTube 사이트를 클론코딩한 수업의 예제에서, 과제로 주어진 aside 부분을 내가 직접 만들면서 찾아본 부분만 가볍게 정리하겠다. </br>

```aside-container 부분을 구현하면서 찾아봤던 것```

#1: container의 구성
====
강사님이 제공해주신 pdf에 의하면, 수업시간에 진행한 것과 같이 </br>
```video-container```, ```video-info-container```, ```comment-container```의 3가지 요소가 ```main-container```로 묶여 있고, </br>
```main-container```에 ```aside-container```까지 더해 ```container```로 크게 묶어내는 구획을 구성했었다. </br>
그러나 실제 수업 시간에는 ```video-container```, ```video-info-container```, ```comment-container```의 3가지 요소를 </br>
따로 크게 묶어내는 작업이 없었고, 그래서 처음에 ```aside-container```를 작성해서 추가했을 때 댓글 창 아래에 추천 동영상 목록이 떴었다. </br>

#2: index.html의 수정
====
그래서 수업시간에 작성했었던 ```video-container```, ```video-info-container```, ```comment-container```의 3가지 요소를 </br>
```<div id="main-container"></div>```를 이용해 하나의 블럭으로 묶어주었고, </br>
그 아래에 ```<div id="aside-container"></div>```를 추가해주었다. </br>
물론 이 다음에는 이 큰 2개의 ```main-container```와 ```aside-container``` 블럭을 </br>
```<div id="container"></div>```로 묶어내는 것 또한 잊지 않았다. </br>

#3: style.css에도 추가 내용 작성
====
```index.html```에만 내용을 추가한다고 끝나는 것이 아니다. </br>
```css
#aside-container {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;
    margin: 50px;
}
```
위와 같은 코드를 style.css에 작성해 줘야 멀쩡하게 돌아간다. </br>

#4: <div id="aside-container"></div>의 내용물
====
2번만 달랑 완성해놓으면 과제가 끝나지 않는다. 우리는 ```aside-container```의 내용물도 채워줘야 한다. </br>
내용물은 수업시간에 작성했던 댓글 창의 형식을 적절히 변형하여 추가해 보았다. </br>
```html
<div class="recommend-box">
        <img class="video-thumbnail"
          src="https://img.youtube.com/vi/kqbu1h6adio/default.jpg" />
        <div class="recommend-text-area">
            <div style="font-weight: bold; "> T1 vs. 젠지 | 결승전 매치 하이라이트 | 04.09 | 2023 LCK 스프링 스플릿 결승 </div>
          <div>LCK</div>
          <div>조회수 200만회 </t> 1개월 전</div>
        </div>
      </div>
```
comment-box의 이름을 recommend-box로 바꿔보았다. 또한 profile-thumbnail의 이름을 video-thumbnail로 바꿔 가독성을 좋게 했다. </br>
추천 동영상은 최근에 있었던 LCK 스프링의 결승 영상을 이용했다. </br>
최대한 비슷하게 해보고자 동영상 제목 아래에 표시되는 조회수와 업로드 날짜를 표현해보고자 한줄 더 추가해 보았다. </br>

#5: 아쉬운 점
====
html 파일을 실제로 열어봤을 때 나름 괜찮은 결과물이 나와서 만족스러웠지만, 아쉬운 점도 있었다. </br>
동영상의 제목이 동영상 썸네일의 오른쪽에 붙어 나오는 것이 아니라 썸네일 아래에서 표시된다는 것이었다. </br>
썸네일과 영상 제목의 구역을 추가적으로 row 방향으로 나눌 수 있는 방법에 대해 생각해봤는데 답이 잘 나오지 않아서 일단 마무리했다. </br>
근시일내에 해결할 방법을 찾을 수 있도록 노력해야겠다고 생각했다. </br>
