### 1. 아래 코드의 실행 결과는 무엇인가

~~~javascript
var x = 1;

function foo() {
	var x = 10;
	bar();
}

function bar() {
	console.log(x);
}

foo(); // ?
bar(); // ?
~~~

: var 키워드는 함수레벨 스코프이고 중복선언이 가능하다. 함수는 자신이 선언된 위치에서의 상위스코프를 갖는다. 따라서 1, 1이 각각 출력된다.



<br>

<br>

---

### 2. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
var i = 10;

for(var i = 0; i < 5; i++){
	console.log(i); // ?
}

console.log(i); // ?
~~~

---

: for문의 작동순서를 보면 0부터 4까지는 출력이되고 4가 출력이 된 이후 i++에 의해 5가 된 후 i < 5라는 조건을 보고 false가 되므로 for문을 나가게 된다. 따라서 i는 5가 된다. `0, 1, 2, 3, 4` / `5`



<br>

<br>

---

### 3. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
function foo() {
	x = 10;
}

foo();

console.log(x); // ?
~~~

---

: 선언이 되어 있지 않으면 자바스크립튼 엔진은 암묵적으로 전역변수로 x를 선언하고 할당한다. 따라서 10이 출력된다.



<br>

<br>

---

### 4. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
console.log(+true);
console.log(!"Lee");
~~~

---

: true는 1, false는 0으로 평가된다, 문자열은 무조건 true로 평가되므로 `1` / `false`로 출력된다.



<br>

<br>

---

### 5. 다음 중 에러를 발생시키는 것을 모두 고르세요

~~~javascript
const bird = {
	size:'small'
};

const mouse = {
	name:"Mickey",
	small:true
};
~~~

​	A : mouse.bird.size

​	B : mouse[bird.size]

​	C : mouse[bird["size"]]

---

: A



<br>

<br>

---

### 6. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
let c = {greeting: 'Hey!'};
let d;

d = c;
c.greeting = 'Hello';
console.log(d.greeting);
~~~

​	A: Hello

​	B: Hey

​	C: undefined

​	D: ReferenceError

​	E: TypeError

---

: 객체는 참조값을 갖는다. 따라서 객체 내부의 값이 바뀌어도 참조값은 변하지 않으므로 Hello가 출력된다.



<br>

<br>

---

### 7. 전역 변수의 문제점은 무엇인가요?

: 암묵적인 결합 / 긴 생명주기 / 네임 스페이스 오염 / 스코프체인 내에서 최상위에 위치



<br>

<br>

### 8. Var 키워드로 선언한 변수의 문제점은 무엇인가요?

: 중복선언이 가능 / 함수 레벨 스코프 / 변수 호이스팅



<br>

<br>

---

### 9. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
let greeting;
greetign = {}; // 오타!

console.log(greetign);
~~~

​	A : {}

​	B : ReferenceError: greeting is not defined

​	C : underfined

---

: 선언이 안된 상태에서 할당을 하면 자바스크립트 엔진은 암묵적으로 전역변수로서 선언을 하고 할당을 한다. 따라서 `{}` 를 출력한다.



<br>

<br>

---

### 10. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
function bark() {
	console.log('Woof!');
}

bark.animal = 'dog';
~~~

​	A : 에러없이 성공

​	B : SyntaxError

​	C : underfined

​	D : ReferenceError

---

: 에러없이 성공



<br>

<br>

---

### 11. 프로토타입은 무엇인가요?

: 반복되는 코드를 부모역활을 하는 상위 객체로부터 '상속'받아서 사용하는 프로그래밍

<br><br>

### 12. this 는 언제 어떻게 결정되나요? 함수 호출 방식에 따라 설명해 주세요.

> 일반 함수로 호출시, 전역객체를 가리킨다.
>
> 메소드로 호출시 호출한 식별자를 가리킨다.
>
> 생성자 함수를 호출시 생성자함수가 생성할 인스턴스를 가리킨다.
>
> Function.prototype.apply/call/bind 메소드에 의한 간접 호출시 인자로 전달한 객체를 가리킨다.

 