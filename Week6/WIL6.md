WIL6.md
=========
2023년 1학기 GDSC OC Web Study 6주차에 학습한 내용을 정리해보고자 한다.

Week6 - 2023. 05. 02. Tue.
=========
> "HTML: Hyper Text Markup Language" </br>
> "CSS: Cascading Style Sheet"

이번 WIL에는 https://flexboxfroggy.com/#ko 의 지정된 문제를 해결한 후 정답의 코드를 정리해 볼 것이다. </br>

```1 ~ 13, 18, 19, 20 스테이지를 해결한 후 솔루션 코드를 정리```

#1: justify-content
====
```css
#pond {
  display: flex;
  justify-content: flex-end;
}
```
#2: justify-content
=====
```css
#pond {
  display: flex;
  justify-content: center;
}
```
#3: justify-content
====
```css
#pond {
  display: flex;
  justify-content: space-around;
}
```
#4: justify-content
====
```css
#pond {
  display: flex;
  justify-content: space-between;
}
```
#5: align-items
====
```css
#pond {
  display: flex;
  align-items: flex-end;
}
```
#6: justify-content, align-items
====
```css
#pond {
  display: flex;
  justify-content: center;
  align-items: center;
}
```
#7: justify-content, align-items
====
```css
#pond {
  display: flex;
  justify-content: space-around;
  align-items: flex-end;
}
```
#8: flex-direction
====
```css
#pond {
  display: flex;
  flex-direction: row-reverse;
}
```
#9: flex-direction
====
```css
#pond {
  display: flex;
  flex-direction: column;
}
```
#10: flex-direction, justify-content
====
```css
#pond {
  display: flex;
  justify-content: flex-end;
  flex-direction: row-reverse;
}
```
#11: flex-direction, justify-content
====
```css
#pond {
  display: flex;
  justify-content: flex-end;
  flex-direction: column;
}
```
#12: flex-direction, justify-content
====
```css
#pond {
  display: flex;
  justify-content: space-between;
  flex-direction: column-reverse;
}
```
#13: justify-content, align-items, flex-direction
===
```css
#pond {
  display: flex;
  justify-content: center;
  align-items: flex-end;
  flex-direction: row-reverse;
}
```
#18: flex-wrap
====
```css
#pond {
  display: flex;
  flex-wrap: wrap;
}
```
#19: flex-direction, flex-wrap
====
```css
#pond {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
}
```
#20: flex-flow
====
```css
#pond {
  display: flex;
  flex-flow: column wrap;
}
```
