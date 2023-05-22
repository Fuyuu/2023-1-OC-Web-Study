WIL8.md
=========
2023년 1학기 GDSC OC Web Study 8주차에 학습한 내용을 정리해보고자 한다.

Week7 - 2023. 05. 16. Tue.
=========
> "HTML: Hyper Text Markup Language" </br>
> "CSS: Cascading Style Sheet" </br>
> "JavaScript"

이번 WIL에는 https://poiemaweb.com/coding 에서 JavaScript와 관련한 게시글을 읽고 내가 몰랐던 것만 정리해보는 시간을 가져보도록 하겠다. </br>

#1. 변수, 값
====
1. 변수를 사용할 때 ```var```키워드를 사용한다.
2. 자바스크립트는 7가지 데이터 타입을 제공한다. </br>
  - 원시 타입 (primitive data type) </br>
      ```number```
      ```string```
      ```boolean```
      ```null```
      ```undefined```
      ```symbol (New in ECMAScript 6)```
  - 객체 타입 (Object data type)
      ```object```
3. 변수에 할당된 값의 타입에 의해 동적으로 변수의 타입이 결정된다. 이를 동적 타이핑이라 한다.

#2. 데이터 타입과 변수
====
1. 원시 타입 (Primitive Data Type) </br>
원시 타입의 값은 변경 불가능한 값(immutable value)이며 pass-by-value(값에 의한 전달)이다.
  - ```number```: 자바스크립트는 독특하게 하나의 숫자 타입만 존재한다. </br>
    &nbsp; &nbsp; &nbsp;&nbsp;&nbsp; &nbsp; ECMAScript 표준에 따르면, 숫자 타입의 값은 배정밀도 64비트 부동소수점 형을 따른다. </br> 
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;즉, 모든 수를 실수를 처리하며 정수만을 표현하기 위한 특별한 데이터 타입(integer type)은 없다. </br>
&nbsp;&nbsp;&nbsp;&nbsp;추가적으로 3가지 특별한 값들도 표현할 수 있다. </br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```Infinity``` : 양의 무한대
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```-Infinity``` : 음의 무한대
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```NaN``` : 산술 연산 불가(not-a-number)
  - ```string```: 문자열(String) 타입은 텍스트 데이터를 나타내는데 사용한다. 문자열은 0개 이상의 16bit 유니코드 문자(UTF-16) 들의 집합으로 대부분의 전세계의 문자를 표현할 수 있다. </br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;문자열은 작은 따옴표(‘’) 또는 큰 따옴표(“”) 안에 텍스트를 넣어 생성한다. 가장 일반적인 표기법은 작은 따옴표를 사용하는 것이다. </br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;자바스크립트의 문자열은 원시 타입이며 변경 불가능(immutable)하다. </br>
  - ```boolean```: 불리언(boolean) 타입의 값은 논리적 참, 거짓을 나타내는 true와 false 뿐이다.
  - ```undefined```: undefined 타입의 값은 undefined가 유일하다. 선언 이후 값을 할당하지 않은 변수는 undefined 값을 가진다. 즉, 선언은 되었지만 값을 할당하지 않은 변수에 접근하거나 존재하지 않는 객체 프로퍼티에 접근할 경우 undefined가 반환된다.
  - ```null```: null 타입의 값은 null이 유일하다. 자바스크립트는 대소문자를 구별(case-sensitive)하므로 null은 Null, NULL등과 다르다.
  - ```symbol```: 심볼(symbol)은 ES6에서 새롭게 추가된 7번째 타입으로 변경 불가능한 원시 타입의 값이다. 심볼은 주로 이름의 충돌 위험이 없는 유일한 객체의 프로퍼티 키(property key)를 만들기 위해 사용한다. 심볼은 Symbol 함수를 호출해 생성한다.
2. 객체 타입 (Object type, Reference type) </br>
객체는 데이터와 그 데이터에 관련한 동작(절차, 방법, 기능)을 모두 포함할 수 있는 개념적 존재이다. 달리 말해, 이름과 값을 가지는 데이터를 의미하는 프로퍼티(property)와 동작을 의미하는 메소드(method)를 포함할 수 있는 독립적 주체이다. </br>
자바스크립트는 객체(object) 기반의 스크립트 언어로서 자바스크립트를 이루고 있는 거의 “모든 것”이 객체이다. 원시 타입(Primitives)을 제외한 나머지 값들(배열, 함수, 정규표현식 등)은 모두 객체이다. 또한 객체는 pass-by-reference(참조에 의한 전달) 방식으로 전달된다.
3. 동적 타이핑 (Dynamic Typing) </br>
자바스크립트는 동적 타입(dynamic/weak type) 언어이다. 이것은 변수의 타입 지정(Type annotation)없이 값이 할당되는 과정에서 값의 타입에 의해 자동으로 타입이 결정(Type Inference)될 것이라는 뜻이다. </br> 
따라서 같은 변수에 여러 타입의 값을 할당할 수 있다. 이를 동적 타이핑(Dynamic Typing)이라 한다.
4. 변수 호이스팅(Variable Hoisting) </br>
호이스팅이란 var 선언문이나 function 선언문 등 모든 선언문이 해당 Scope의 선두로 옮겨진 것처럼 동작하는 특성을 말한다. 즉, 자바스크립트는 모든 선언문(var, let, const, function, function*, class)이 선언되기 이전에 참조 가능하다.
5. var 키워드로 선언된 변수의 문제점 </br>
대부분의 문제는 전역 변수로 인해 발생한다. 전역 변수는 간단한 애플리케이션의 경우, 사용이 편리한 면이 있지만 불가피한 상황을 제외하고 사용을 억제해야 한다. 전역 변수는 유효 범위(scope)가 넓어서 어디에서 어떻게 사용될 지 파악하기 힘들다. </br>
이는 의도치 않은 변수의 변경이 발생할 수 있는 가능성이 증가한다. 또한 여러 함수와 상호 의존하는 등 부수 효과(side effect)가 있을 수 있어서 복잡성이 증가한다. </br>
변수의 유효 범위(scope)는 좁을수록 좋다. ES6는 이러한 var의 단점을 보완하기 위해 let과 const 키워드를 도입하였다. </br>

#3. 연산자
====
1. 비교 연산자 </br>
  - 동등 / 일치 비교 연산자 </br>
      | 비교 연산자 | 의미 | 사례 | 설명 |
      |-----|-----|-----|-----|
      | == | 동등 비교 | x == y | x와 y의 값이 같음 |
      | === | 일치 비교 | x === y	| x와 y의 값과 타입이 같음 |
      | != | 부등 비교 | x != y | x와 y의 값이 다름 |
      | !==	| 불일치 비교 | x !== y | x와 y의 값과 타입이 다름 |
  
2.  typeof 연산자 </br>
  - typeof 연산자는 7가지 문자열 ```string```, ```number```, ```boolean```, ```undefined```, ```symbol```, ```object```, ```function``` 중 하나를 반환한다. </br>
  ```null```을 반환하는 경우는 없으며 함수의 경우 ```function```을 반환한다. </br>
   null 타입을 확인할 때는 typeof 연산자를 사용하지 말고 일치 연산자(===)를 사용하도록 한다.
   
#4. 제어문
====
1. switch문 </br>
  - switch문의 표현식의 평가 결과와 일치하는 case문으로 실행 순서가 이동하여 문을 실행한 것은 맞지만, </br>
  문을 실행한 후 switch 문을 탈출하지 않고 switch 문이 끝날 때까지 모든 case 문과 default 문을 실행하는 경우가 생긴다. 이를 폴스루(fall through)라 한다. </br>
  결과가 이러한 이유는 case 문에 해당하는 문의 마지막에 ```break``` 문을 사용하지 않았기 때문이다. </br>
  
#5. 타입 변환과 단축 평가
====
1. 암묵적 타입 변환(Implicit coercion) / 타입 강제 변환(Type coercion) </br>
  - 동적 타입 언어인 자바스크립트는 개발자의 의도와는 상관없이 자바스크립트 엔진에 의해 암묵적으로 타입이 자동 변환되기도 한다.
  - 불리언 타입으로 변환: 자바스크립트 엔진은 불리언 타입이 아닌 값을 Truthy 값(참으로 인식할 값) 또는 Falsy 값(거짓으로 인식할 값)으로 구분한다. 즉, Truthy 값은 true로, Falsy 값은 false로 변환된다. </br>
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  아래 값들은 제어문의 조건식과 같이 불리언 값으로 평가되어야 할 컨텍스트에서 false로 평가되는 Falsy 값이다.
&nbsp;&nbsp;&nbsp;```false```
&nbsp;&nbsp;&nbsp;```undefined```
&nbsp;&nbsp;&nbsp;```null```
&nbsp;&nbsp;&nbsp;```0, -0```
&nbsp;&nbsp;&nbsp;```NaN```
&nbsp;&nbsp;&nbsp;```’ ’(빈 문자열)```

2. 단축 평가
    | 단축 평가 표현식 | 평가 결과 |
    | ----- | ----- |
    | ```true \|\| anything``` | true |
    | ```false \|\| anything``` | anything | 
    |```true && anything``` | anything |
    | ```false && anything``` | false |
    단축 평가는 아래와 같은 상황에서 유용하게 사용된다.
    - 객체가 null인지 확인하고 프로퍼티를 참조할 때
    - 함수의 인수(argument)를 초기화할 때

#6. 프로토타입
====

#7. 스코프
====

#8. let, const와 블록 레벨 스코프
====
