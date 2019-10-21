### 1. 아래 코드의 실행 결과는 무엇인가

~~~javascript
var x =. ;

function foo() {
	var x =. 0;
	bar();
}

function bar() {
	console.log(x);
}

foo(); // ?
bar(); // ?
~~~

<br>

<br>

### 2. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
var i = 10;

for(var i = 0; i < 5; i++){
	console.log(i); // ?
}

console.log(i); // ?
~~~

<br>

<br>

### 3. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
function foo() {
	x = 10;
}

foo();

console.log(x); // ?
~~~

<br>

<br>

### 4. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
console.log(+true);
console.log(!"Lee");
~~~

<br>

<br>

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

<br>

<br>

### 6. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
let c = {greeting: 'Hey!'};
let d;

d = c;
c.greeting = 'Hello';
console.log(d.greeting);
~~~

<br>

<br>

### 7. 전역 변수의 문제점은 무엇인가요?

<br>

<br>

### 8. Var 키워드로 선언한 변수의 문제점은 무엇인가요?

<br>

<br>

### 9. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
let greeting;
greetign = {}; // 오타!

console.log(greetign);
~~~

​	A : {}

​	B : ReferenceError: greeting is not defined

​	C : underfined

<br>

<br>

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

<br>

<br>

### 11. 프로토타입은 무엇인가요?

<br><br>

### 12. this 는 언제 어떻게 결정되나요? 함수 호출 방식에 따라 설명해 주세요.

