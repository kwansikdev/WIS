### 1. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
function Person(firstName, lastName) {
	this.firstName = firstName;
	this.lastName = lastName;
}

const member = new Person('Ungmo', 'Lee');

Person.getFullName = function() {
	return `${this.firstName} ${this.lastName}`;
};

console.log(member.getFullName());
~~~

​	A: TypeError

​	B: SyntaxError

​	C: Ungmo Lee

​	D: undefined undefined

---

: getFullName이라는 메소드는 Person의 정적 메소드 이므로 인스턴스객체인 member의 메소드로 호출을 할 수 가 없다. 인스턴스 member와 Person의 프로토타입객체에 없기 때문에 TypeError가 출력된다.

**TypeError**는 정의되지 않은 객체의 property를 읽어내거나 method를 호출했을 때 발생한다.



<br>

<br>

---

### 2. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
function Person(firstName, lastName) {
	this.firstName = firstName;
	this.lastName = lastName;
}

const member = new Person('Ungmo', 'Lee');

Person.getFullName = function() {
	return `${this.firstName} ${this.lastName}`;
};

console.log(Person.getFullName());
~~~

​	A: TypeError

​	B: SyntaxError

​	C: Ungmo Lee

​	D: undefined undefined

---

: Person의 정적메소드인 getFullName 메소드를 호출은 했지만 Person 함수 내부에 정의된 this.firstName 과this.LastName은 인스턴스 객체인 member의 property 이므로 Person의 정적메소드인 getFullName 메소드의 this.firstName 과this.LastName은 선언이 되어 있지 않기 때문에 undefined가 출력된다.



<br>

<br>

---

### 3. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
function Person(firstName, lastName) {
	this.firstName = firstName;
	this.lastName = lastName;
}

const lee = Person('Ungmo', 'Lee');

console.log(lee);
~~~

​	A: TypeError

​	B: SyntaxError

​	C: Ungmo Lee

​	D: undefined 

---

: new 연산자 없이 생성자 함수를 새로운 변수에 할당하면 생성자함수는 일반함수 호출로 동작하게 된다. Person 함수 내부에 프로퍼티가 선언이 되어 있지만 return 문이 없으므로 undefined가 출력된다.



<br>

<br>

---

### 4. 이벤트 전파의 3단계는 무엇인가요?

​	A: Target > Capturing > Bubbling

​	B: Bubbling > Target > Capturing

​	C: Target > Bubbling > Capturing

​	D: Capturing > Target > Bubbling

---

: 캡쳐링 -> 타겟 -> 버블링



<br>

<br>

---

### 5. 모든 객체는 프로토타입을 갖고 있나요?

​	A: 네

​	B: 아니오

---

: 모든 함수 객체는 Prototype을 가진다. 하지만 Object.create 함수로 null이라는 프로토타입 객체를 갖는 객체를 만들 수 있기 때문에 모든 객체는 Prototype을 갖는다고는 말을 하기 어렵다.



<br>

<br>

---

### 6. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
function sum(a, b) {
	return a + b;
}

consolo.log(sum(1, '2'));
~~~

​	A: NaN

​	B: TypeError

​	C: "12"

​	D: 3

---

: 숫자 타입 + 문자열 타입의 연산은 문자열로 계산이 된다.



<br>

<br>

---

### 7. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
let number = 0;
console.log(number++);
console.log(++number);
console.log(number);
~~~

​	A: 1 1 2

​	B: 1 2 2

​	C: 0 2 2

​	D: 0 1 2

---

: ++ 연산자가 변수 뒤에오면 변수를 먼저 출력하고 그 다음에 1을 더한다. 변수 앞에 오면 1을 더한 뒤에 출력을 한다.



<br>

<br>

---

### 8. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
function checkAge(data) {
	if(data === {age:18}) {
		console.log("You are an adult!");
	}else if(data == {age:18}) {
		console.log("You are still an adult!");
	}else {
		console.log("Hmm... You don't have an age i guess");
	}
}

checkAge({age:18});
~~~

​	A: "You are an adult!"

​	B: "You are still an adult!"

​	C: "Hmm... You don't have an age i guess"

---

: 객체는



<br>

<br>

---

### 9. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
function getAge(...args) {
	console.log(typeof args);
}

getAge(20);
~~~

​	A: "number"

​	B: "array"

​	C: "object"

​	D: "NaN"

---

: ...args 는 유사배열객체이므로 배열로 평가된다. 자바스크립트에서는 데이터타입에 배열이 없고 전부 Object고 평가된다. 하지만 함수만 function으로 따로 출력된다.



<br>

<br>

---

### 10. 아래 코드의 실행 결과는 무엇인가요?

~~~javascript
function getAge() {
	'use strict';
	age = 20;
	console.log(age);
}

getAge();
~~~

​	A: 20

​	B: undefined

​	C: ReferenceError

​	D: TypeError

---

: 함수 내에서 엄격모드로 설정이 된 상태에서 변수 선언 없이 바로 변수에 할당을 한 경우 변수가 선언되어 있지 않다는ReferenceError가 출력된다.