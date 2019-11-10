### 1. index.html 에서 main.js 를 로드하기 위한 코드를 완성하라. 단 index.html 은 프로젝트 루트에 위치하고 main.js 는 src/js 디렉토리에 위치한다.

~~~html
<script src = './src/js/main.js'>
~~~



<br>

<br>

---

### 2. ECMAScript 와 JavaScript 의 차이점은?

: 

JavaScript의 문법을 정리해 하나의 표준안을 만든것이 ECMAScript이고 ECAMScript와 WEB API을 포함한 것이 JavaScript이다.



<br>

<br>

---

### 3. 변수란 무엇인가?

: 하나의 값을 저장하는 메모리 공강에 붙인 이름 또는 메모리 공간 자체



<br>

<br>

---

### 4. JavaScript 의 데이터 타입을 모두 나열하라.

> 1. Number
>
> 2. String
>
> 3. Boolean
>
> 4. Undefined
>
> 5. Null
>
> 6. Symbol
>
> 7. Object



<br>

<br>

---

### 5. var foo = 42 / -0; console.log(foo); 의 결과를 기술하라.

> -infinity



<br>

<br>

---

### 6. 리터럴이란 무엇인가?

: 소스코드 내에서 우리가 알수 있게 만든 값.



<br>

<br>

---

### 7. 표현식이란 무엇인가?

: 리터럴과 연산자로 이루어진 값으로 평가될 수 있는 식



<br>

<br>

---

### 8. var x = 5; 일 때, console.log(x != '5'); 의 결과는 무엇인가?

: true



<br>

<br>

---

### 9. var foo = false && 'Cat'; 일 때 foo 의 값은 무엇인가?

: false



<br>

<br>

---

### 10. console.log(!!null); 의 결과는 무엇인가?

: false



<br>

<br>

---

### 11. 0 에서 10 미만까지 홀수만을 큰 수 부터 출력하는 코드를 for 문을 사용하여 작성하라.

~~~javascript
for (let i = 0; i < 10; i++) {
	if (i % 2) return console.log(i);
}
~~~



<br>

<br>

---

### 12. 0 에서 10 미만까지 3의 배수를 큰수부터 출력하는 코드를 while 문을 사용하여 작성하라. 단 0은 출력하지 않는다.

~~~javascript
var count = 1;

while(count < 10) {
  if (count % 3 === 0) {
    console.log(count);
    count++
  }
}
~~~



<br>

<br>

---

### 13. 문자열을 값으로 갖는 name 프로퍼티와 name 프로퍼티를 출력하는 sayName 메소드를 갖는 객체 obj 를 생성하라. 단 객체 리터럴 방식을 사용한다.

~~~javascript
const obj = {
	name : '',
	sayName() {
		console.log(this.name);
	} 
}
~~~



<br>

<br>

---

### 14. Var person = { 'my-name': 'Lee' }; 일 때, my-name 프로퍼티의 값을 'Kim' 으로 변경하고 console.log()를 사용하여 출력하는 코드를 작성하라.

~~~javascript
var person = { 'my-name': 'Lee'};

person['my-name'] = 'Kim';

console.log(person);
~~~



<br>

<br>

---

### 15. 참조에 의한 전달(pass-by-reference)과 값에 의한 전달(pass-by-value)의 차이점에 대하여 설명하라.

> 값에 의한 전달은 전달하려는 값을 복사해서 할당한다. 원래 값을 건드릴 수 없고 변수의 값을 재할당하는 방식이다.
>
> 참조에 의 전달은 참조값을 복사하는 방식이다. 객체를 가리키고 있는 참조값을 두개의 식별자가 가리키고 있기 때문에 어느 한쪽에서 객체의 내용을 변경하면 나머지 객체의 내용도 같이 바뀐다.

