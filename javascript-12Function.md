---
title: javascript 12Function
date: 2020-09-15 22:15:26
category: "javascript"
draft: false
---

# 함수

## 1. 함수란?

함수는 **입력(input) 을 받아 출력(output)**을 내보내는 일련의 과정을 정의한 것이다.

프로그래밍을 처음만든 과학자들 대다수가 수학자였다.

수학적사고를 통해서 프로그래밍을 만들었다. 그렇기 때문에 수학적 사고가 필요하다.

**프로그래밍에서의 함수는?**

프로그래밍 언어의 함수는 일련의 과정을 문(statement)로 구현하고 코드블록으로 감싸서 하나의 실행 단위로 정의한 것이다.

프로그래밍은 함수들의 집합이며, 우리는 함수를 만드는일을한다.

```
function sum(a, b) {
	return a + b;
}
```

**함수를 정의할때**

**function이라는 키워드**를 쓰고 **함수이름**을 준다. **괄호(매개변수 선언부)를 여닫고**, **코드블록(함수 몸체)**을 써준다.

괄호를 매개변수 선언부라고한다. 매개 변수는 **0개이상**으로 여러개쓸 수 있다. 매개 '변수'는 함수 안에서 선언된 변수이다.

**매개변수란?**

**함수 바깥에 있는 값이** 함수 안으로 들어올때 매개를 하는 것이 매개변수이다.

호출할때 인수로 작성하여 사용한다.

인수로 작성하면 매개변수에 할당된다.

함수 외부에 있었던 값을 함수 내부로 받아들이는 역할을 한다.

**함수는 함수정의(function definition)을 통해 생성한다.**

함수를 정의하는 방법은 여러가지가 있다.

function 키워드와 함수이름, 매개변수 선언부() , 함수몸체를 작성해주는 것을 함수 선언문이라고 한다. 함수 몸체안에는 문들의 집합이 온다.

함수는 입력값을 받아서 출력값을 내보내기때문에 return 키워드를 통해 출력값 작성한다.

여기까지 함수 정의이다. 함수정의는 만드는것뿐이다. 사용하기위해선 call,호출해야한다.

**함수는 함수 호출(function call/ invoke) 를 통해 사용한다.**

함수 호출을 하기위해서는 함수 식별자를 주고 괄호를 여닫고 괄호안에 매개변수를 통해 함수 안으로 넣어줄 값인 인수(argument)를 작성한다.

함수를 호출하게되면 인수가 매개변수에 할당이된다.

바깥에 있던 값이 안으로 들어가서 사용할 수 있다.

인수는 함수안에서 행해지는 일련의 과정을 위한 재료이다.

함수는 하나의 기계로 이해하면 편하다.

## 2. 함수를 사용하는 이유

- 코드의 재사용
  - 실행 시점을 개발자가 정하고 재사용이 가능하다
- 코드의 신뢰성을 높인다
  - 중복이 줄어드는 만큼 실수할 가능성도 줄기 때문
- 가독성을 높인다
  - 적절한 함수 식별자 이름을 사용한다면 내부 코드를 몰라도 함수의 역할을 잘 파악할 수 있게 한다.

## 3. 함수 리터럴

리터럴은 사람이 이해할 수 있는 문자 또는 약속된 기호를 사용해 값을 생성하는 표기 방식(notation) 이다. 즉 표기법이다. 함수 리터럴도 평가되어 값을 생성한다.

자바스크립트에서 함수는 **객체 타입의 값**이다.

숫자를 숫자 리터럴로 생성하고 객체를 객체 리터럴로 생성하는 것처럼 함수도 함수 리터럴로 생성할 수 있다.

함수 리터럴은 다음으로 구성된다.

- function 키워드
- 함수 이름
- 매개변수 목록
- 함수 몸체

```
const multiply = function multiply(a, b){
	//var a;
	//var b;
	return a * b;
};
```

**함수 리터럴의 구성요소별 특징**

- **함수 이름**

  - 함수 이름은 식별자이므로 식별자 네이밍 규칙을 준수해야 한다.
  - 단, 함수 몸체 내에서만 참조할 수 있는 식별자이다
    - 보통 재귀호출을 위해 사용된다
  - 함수 이름은 생략가능하다
    - 이름이 있는 함수는 기명 함수(named function)
    - 이름이 없는 함수를 무명/익명 함수(anonymous function)

- **매개변수 목록**

  - 0개 이상의 매개변수를 소괄호 () 로 감싸고 쉼표 , 로 구분
  - 각 매겨변수에는 함수를 호출할때 입력한 인수(argument)가 순서대로 할당 된다. 즉 **순서에 의미가 있다**,
  - 함수 몸체 내에서 변수와 동일하게 취급된다.
    - 식별자 네이밍 규칙을 준수해야 한다.

- 함수 몸체
  - 함수 호출 시 실행될 문 들을 정의한 코드 블록이다.
  - 함수 호출에 의해 실행된다.

**함수와 일반객체의 차이**

- 일반 객체는 호출할 수 없지만 함수는 호출할 수 있다.
- 일반 객체에는 없는 함수 객체만의 고유한 프로퍼티를 갖는다.

## 4. 함수 정의

함수 정의란 함수를 호출하기 이전에 인수를 전달받을 매개변수와 실행될 문들, 그리고 반환할 값을 지정하는 것을 말한다. 정의된 함수는 자바스크립트 엔진에 의해 평가되어 함수 객체가 된다.

함수를 정의하는 방법은 여러가지가 있다.

- 함수 선언문 (function declaration / function statement)
- 함수 표현식 (function expression)
- Function 생성자 함수(Function constructor)
- 화살표 함수 (arrow function)

**변수 '선언' 과 함수 '정의'는 어떤 차이가 있을까**

명확하지 않은것들을 명확하게 하는 것을 **정의**

**선언**은 이제부터 ~~할래 라는 뉘앙스

c언어 같은경우 선언과 정의를 명확히 구분했다.

(c언어에서) 변수에 값을 할당하는 것을 정의라고 한다. 값을 할당하는 순간 명확한 값을 가졌기때문이다. 선언은 없었던것을 새롭게 만드는 것이다. 선언하기전에는 메모리공간이 확보가 되어있지 않지만 선언을 하면 메모리공간이 확보된다.

자바스크립트에서는 변수 선언을 하면 자동으로 undefined 로 '정의' 되기때문에 명확하지 않다. ECMAScript에서 정의와 선언을 구분하고 있기때문에 구함수는 정의, 변수는 선언이라고 표현하도록 하자.

### 함수 선언문

함수를 정의하는 방식 중 하나인 함수 선언문이다.

다음과 같은 특징이 있다.

- 표현식이 아닌 문
- 함수 호이스팅
- 함수이름 생략 불가

```
//함수 선언문
function searchWs(sentence){
	var wsNum = 0;
	for(var i = 0; i < sentence.length; i ++){
		if(sentence[i] === ' '){
			wsNum ++;
		}
	}

	return wsNum;
}

//함수 호출
console.log(searchWs('my age is 23')); //3
```

함수 선언문은 함수 리터럴과 형태가 동일하다. 단, 함수 리터럴은 삼수 이름을 생략할 수 있으나 함수 선언문은 함수 이름을 생략할 수 없다.

```
function (x, y) {
	return x + y;
}
// SyntaxError: Function statementws require a function name
```

- 함수 선언문 은 표현식이 아닌 문이다. 즉, 크롬 개발자 도구의 콘솔에서 함수 선언문을 실행하면 완료 값 (completion) undefined 가 출력된다.
- 함수 선언문은 표현식이 아닌 문이기 때문에 변수에 할당할 수 없다.
- 그런데 다음 예제를 보면 함수 선언문이 변수에 할당되는 것처럼 동작한다.

```
var add = function add(x, y) {
	return x + y;
};

//함수 호출
console.log(add(1,3)); // 4
```

이유가 무엇일까? 위와 같이 동작하는 이유는 자바 스크립트가 문맥을 고려하기 때문이다.함수 선언문은 함수 이름을 생략할 수 없다는 점을 제외하면 함수 리터럴과 형태가 동일하다.

즉 동일한 함수 표현을 문맥에 따라 두가지로 해석한다.

- 함수 리터럴
  - 표현식인 문
- 함수 선언문
  - 표현식이 아닌 문

비슷한 사례가 이전에도 있었다. 바로 객체 리터럴과 블록문이다.

{ }은 블록문일 수도 있고 객체 리터럴일 수도 있다. 즉, { }은 중의적 표현이다. 자바스크립트 엔진은 { } 을 문맥에 따라 다르게 해석한다.

만약 {} 이 단독으로 존재하면, 자바스크립트엔진은 { }을 블록문으로 해석한댜ㅏ. 하지만 { } 이 값으로 평가되어야하는 문맥에서는 { } 을 객체 리터럴로 해석한다. 이처럼 동일한 코드도 코드의 문맥에 따라 해석이 달라질 수 있다.

기명 함수 리터럴, 함수 선언문도 마찬가지로 중의적인 코드이다. 코드의 문맥에 따라 해석이 달라질 수 있다.

자바스크립트엔진은 기명 함수 리터럴을 단독으로 사용하면 함수 선언문으로 해석한다. 값으로 평가되어야하는 문맥( 변수 할당 등) 에 사용한다면 함수 리터럴 표현식으로 해석한다.

두 경우 모두 함수가 생성되는 것은 동일 하지만 내부 동작에 차이가 있다. 다음예제를 살펴보자.

```
//기명 함수 리터럴을 단독으로 사용하면 함수 선언문으로 해석된다.
// 함수 선언문에서는 함수 이름을 생략할 수 없다.

function foo() { console.log('foo');}
foo();

// 함수 리터럴을 피연산자로 사용하면 함수 선언문이 아니라 함수 리터럴 표현식으로 해석한다.
// 함수 리터럴에서는 함수 이름을 생략할 수 있다.

(function bar() { console.log('bar');});
bar(); //ReferenceError: bar is not defined
```

위 예제에서 단독으로 사용된 함수 리터럴(foo)은 함수 선언문으로 해석된다. 하지만 그룹연산자 () 내에 있는 함수 리터럴(bar)은 함수 선언문으로 해석되지 않고 함수 리터럴 표현식으로 해석된다. 그룹연산자의 피연산자는 값으로 평가될 수 있는 표현식이어야 한다. 따라서 표현식이 아닌 문인 함수 선언문은 피연산자로 사용할 수 없다.

위 예제에서 함수 선언문을로 생성한 foo는 호출할 수 있으나 함수 리터럴 표현식으로 생성한 bar는 호출할 수 없다. 그이유가 무엇일까?

함수 이름은 함수 몸체 내에서만 참조할 수 있는 식별자이기 때문이다.

함수 몸체 외부에서는 함수 이름으로 함수를 참조할 수 없으므로 함수 외부에서 함수를 함수 이름으로 호출할 수 없다는 것이다. 즉, 함수를 생성하긴 했지만 생성한 함수를 가리키는 식별자가 존재하지 않는다. bar 함수를 호출 시 참조 에러가 발생하는 이유이다.

그런데 함수 선언문으로 정의한 foo 함수는 왜 호출이 가능하였을까?

foo 역시 함수 함수 이름인데 호출이 가능하려면 foo가 식별자이어야 한다. 우리가 명시 적으로 foo 라는 식별자를 생성한 적은 없다. 그러나 자바스크립트 엔진은 foo라는 식별자를 암묵적으로 생성하였다.

자바스크립트 엔진은 함수 선언문을 해석해 함수 객체를 생성한다. 이때 함수 이름은 함수 몸체 내에서만 유효한 식별자이다. 따라서 별도로 생성된 함수 객체를 가리리키는 식별자가 필요하다.

자바스크립트 엔진은 생성된 함수를 호출하기 위해 함수 이름과 동일한 이름의 식별자를 암묵적으로 생성하과, 거기에 생성된 함수 객체를 할당한다.

즉 위에서 선언한 함수 foo는 내부적으로 다음과 같이 동작한다.

```
var foo = function foo() {console.log('foo');};
```

함수는 함수 이름으로 호출하는 것이 아니라 함수 객체를 가리키는 식별자로 호출한다. 즉, 함수 선언문으로 생성한 함수를 호출한 것은 함수 이름 foo 가 아닌, 암묵적으로 생성된 식별자 foo 이다.

위 의사 코드(pseudo code) 가 바로 다으에 살펴볼 함수 표현식이다. 결론적으로 자바스크립트 엔진은 함수 선언문을 함수 표현식으로 변환해 함수 객체를 생성한다고 생각할 수 있다. 단, 함수 선언문과 함수 표현식이 정확히 동일하게 동작하는 것은 아니다.

### 함수 표현식

함수는 객체 타입의 값이다. 함수는 값처럼 변수에 할당할 수 도있고 프로퍼티 값이 될수도 있으며, 배열의 요소가 될 수도 있다. 이러하 값의 성질을 갖는 객체를 일급 객체(first class object)라 한다. 자바스크립트의 함수는 일급 객체이다. 함수가 일급 객체라는 것은 함수를 값처럼 자유롭게 사용할 수 있다는 의미다.

함수는 일급 객체이므로 함수리터럴로 생성한 함수 객체를 변수에 할당할 수 있다. 이러한 정의방식을 함수 표현식(function expression) 이라고 한다. 함수 선언문으로 정의한 foo 함수를 함수 표현식으로 바꿔서 정의하면 다음과 같다.

```
//함수 표현식
var foo = function (){
	console.log('foo');
};

foo(); // foo
```

- 함수 리터럴의 함수 이름은 생략 가능하다. 이러한 함수를 익명함수(anonymous function)이라 한다.
- 함수 리터럴은 함수 이름을 생략하는 것이 일반적이다.

함수를 호출할 때는 함수 이름이 아니라 **함수 객체를 가리키는 식별자**를 사용해야한다. 함수 이름은 함수 몸체 내부에서만 유효한 식별자이므로, 함수 외부에서 함수 이름으로 함수를 호출할 수 없다.

```
var foo = function bar () {
	console.log('foo');
}

//함수 객체를 가리키는 식별자로 호출
foo(); // foo

//함수 이름으로 호출하면 ReferenceError 이 발생한다.
bar(); // ReferenceError: bar is not defined
```

자바스크립트 엔진은 함수 선언문의 함수 이름으로 식별자를 암묵적 생성하고 생성된 함수 객체를 할당하므로 함수 표현식과 유사하게 동작하는 것처럼 보인다. 하지만 함수 선언문과 함수 표현식이 정확히 동작하지는 않는다

함수 선언문은 표현식이 아닌문이고 함수 표현식은 표현식인 문이다.

### 함수 생성 시점과 함수 호이스팅

```
//함수 참조
console.dir(foo); // f foo()
console.dir(bar); // undefined

// 함수 호출
foo(); // foo
bar(); // TypeError: bar is not a function

//함수 선언문
function foo () {
	console.log('foo');
}

//함수 표현식
var bar = function () {
	console.log('bar');
};
```

함수 선언문으로 정의한 함수는 함수 선언문 이전에 호출할 수 있다.그러나 함수 표현식으로 정의한 함수는 함수 표현식 이전에 호출할 수 없다.

함수 선언문으로 정의한 함수 표현식으로 정의한 함수의 생성 시점이 다르기 때문이다.

**함수 선언문은 런타임(runtime) 이전에 실행된다**

변수 선언문과 마찬가지로, 함수 선언문 역시 런타임 이전에 먼저 실행 된다. 즉, 함수 객체가 런타임이전에 생성된다는 뜻이다. 함수 선언문이 실행되면 자바스크립트 엔진은 **함수 이름과 동일한 이름의 식별자를 암묵적으로 생성**하고 생성된 함수 객체를 가리키게 한다.

코드상에서, 함수 선언문 이전에 함수를 참조하고, 호출할 수 있는 이유이다. 함수 선언문이 코드의 선두로 끌어 올려진 것처럼 동작하는 자바스크립트 고유의 특징을 함수 호이스팅(function hoisting)이라고 한다.

**함수 호이스팅과 변수 호이스팅의 차이**

var 키워드를 사용한 변수 선언문과, 함수 선언문은 런타임 이전에 자바스크립트 엔진에 의해 먼저 실행 되어 식별자를 생성한다는 점은 동일하다. 단 변수 호이스팅은 식별자가 암묵적으로 undefined을 할당하는 반면, 함수 선언문의 식별자는 명시한 함수객체를 생성해서 가리킨다는 점에서 차이가 있다. 그렇기 때문에 함수선언문으로 정의한 함수를 선언문 이전에 호출이 가능한 것이다.

**함수 표현식은 런타임(runtime)에 함수 객체를 만들어낸다**

함수 표현식은 변수 선언 및 할당문의 축약표현과 동일하게 동작한다. 런타임 이전에는 변수 선언만 실행이되어 undefined로 초기화 되고 함수 리터럴은 런타임에 평가되어 함수 객체를 생성한다.

따라서 함수 표현식은 함수 호이스팅이 아닌, 변수 호이스팅을 발생시키는 특징이 있다. 함수 표현식 이전에 함수식별자를 참조하면 함수가 아닌 undefined로 평가된다. 함수 호출 역시 불가하다. undefined를 호출하는 것과 마찬가지이므로 타입 에러가 발생한다.

함수 표현식으로 정의한 함수는 함수 표현식 이후에 참조, 호출하자.

### Function 생성자 함수

**생성자 함수(constructor function)란?**

생성자 함수는 객체를 생성하는 함수를 말한다. 객체를 생서하는 방식은 객체 리터럴 이외에도 다양한 방법이 있다. 그 중 하나가 생성자함수를 통한 객체 생성이다.

**Function 생성자 함수를 통해 함수 객체를 생성하는 방법**

Function 생성자 함수는 자바스크립트가 기본 제공하는 빌트인 함수이다. 이 Function 생성자 함수에 매개변수 목록과 함수 몸체를 문자열로 전달하고, new 연산자와 함께 호출하면 함수 객체를 생성해서 반환한다. new 연산자 없이 호출해도 결과는 동일하다.

Function 생성자 함수를 통한 함수 생성 예시

```
var multiply = new Function ('a', 'b', 'return a*b');

console.log(multiply(3,4)); // 12
```

Function 생성자 함수로 함수를 생성하는 것은 보통 바람직하지 않다.

다음과 같은 이유 때문이다.

- 클로저(closure)를 생성하지 않는다.
- 함수 선언문이나 함수 표현식으로 생성한 함수와 다르게 움직인다.

### 화살표 함수(arrow function)

**화살표 함수는 다음과 같은 특징이 있다.**

- 좀 더 간략한 방법으로 함수를 생성
- 익명함수로 정의한다.
- 생성자 함수로 사용할 수 없다.
- this 바인딩 방식이 다르다.
- prototype 프로퍼티가 없다.
- arguments 객체를 생성하지 않는다.

화살표 함수 사용 예시

```
const add = (x, y) => x + y;
console.log(add ( 1,6))// 7
```

## 5. 함수 호출

**함수 호출이란?**

함수 호출은 함수를 참조해서 함수 몸체 내의 문들을 실행하는 것이다.

함수를 가리키는 식별자와 한쌍의 소괄호인 함수 호출 연산자로 호출한다. 함수 호출 연산자 () 내에는 0개 이상의 인수를 쉼표로 구분해서 나열한다.

함수를 호출하면 현재의 실행 흐름을 중단하고 호출된 함수로 실행 흐름을 옮긴다. 이때 매개변수에 인수가 순서대로 할당되고 함수 몸체의 문들이 실행되기 시작한다.

### 매개변수와 인수

**매개변수와 인수의 역할**

함수를 실행하기 위해 필요한 값을 함수 외부에서 함수 내부로 전달할 필요가 있을 때 매개변수(parameter, 인자)를 통해 인수(argument)를 전달한다. 인수는 값으로 평가될 수 있는 표현식이어야 한다. 인수는 함수를 호출할 때 지정하며, 개수와 타입에 제한이 없다.

매개변수와 인수 사용예시

```
// 함수 선언문
function divide(a, b) {
	return a / b;
}

//함수 호출
var result = divide (5, 2);
```

**매개 변수는 함수 몸체 내부에서 변수의 역할을 한다.**

매개변수는 함수를 정의할 때 선언하며 함수 몸체 내부에서 변수와 동일하게 취급된다. 즉, 함수가 호출되면 함수 몸체 내에서 암묵적으로 매개변수가 생성되고 일반 변수와 마찬가지로 undefined로 초기화 된 이후 인수를 입력한 순서대로 할당하게 된다.

**매개변수의 스코프는 함수 내부이다. **

매개 변수는 함수 몸체 내부에서만 참조할 수 있고 함수 몸체 외부에서는 참조할 수 없다. 즉 함수 내부에서만 유효하다.

```
// 함수 선언문
function divide(a, b) {
	return a / b;
}

//함수 호출
var result = divide (5, 2);

//매개 변수 a, b는 전역에서 참조할 수 없다.
console.log(a, b); // ReferenceError: a is not defined
```

**매개변수의 개수와 인수의 개수의 일치여부**

함수는 매개변수의 개수와 인수의 개수가 일치하는지 체크하지 않는다. 일반적으로, 함수를 호출할때 매개변수의 개수만큼 인수를 전달하지만, 만약 개수가 일치하지 않더라도 에러가 발생하지 않는다.

**인수가 매개변수의 개수보다 부족한 경우**, 인수가 할당되지 않은 매개변수의 값은 undefined 이다.

```
// 함수 선언문
function divide(a, b) {
	// var a;
	// var b;
	return a / b;
}

//인수가 할당되지 않은 매개변수의 값은 undefined 이다.
console.log(divide(5)); // NaN b에 undefined 가 할당되었다.
```

위에서 매개변수 a에는 인수 5가 전달되지만, b 에는 전달할 인수가 없으므로 매개 변수 undefined로 초기화된 상태이다. undefined로 산술을 할 수 없으므로 NaN이 출력된다.

**매개변수보다 인수가 더 많은 경우,** 초과된 인수는 무시된다.

```
// 함수 선언문
function divide(a, b) {
	return a / b;
}

// 초과된 인수 4는 무시된다.
console.log(divide(5, 2, 4)); //2.5
```

초과된 인수는 그냥 버려지는 것은 아니다. 모든 인수는 arguments 객체의 프로퍼티로 보관된다.

```
// 함수 선언문
function divide(a, b) {
	console.log(arguments); // [Arguments] { '0': 5, '1': 2, '2': 4 }
	return a / b;
}


console.log(divide(5, 2, 4));
```

arguments 객체는 함수를 정의할 때, 매개변수 개수를 확정할 수 없는 가변 인자 함수를 구현할 때 유용하게 사용된다.

### 인수 확인

**적절한 인수 전달의 필요성**

다음예제를 살펴보자.

```
function sum(a, b) {
	return a + b;
}
```

위 함수를 정의한 개발자의 의도는 2개의 숫자 타입 인수를 전달받아 덧셈의 결과를 반환하려는 것이다.

하지만, 불분명한 점이 있다.

- 어떤 타입의 인수를 전달해야하는지
- 어떤 타입의 값을 반환해야하는지

따라서 다음과 같은 문제가 발생할 수 있다.

```
function sum(a, b) {
	return a + b;
}

console.log(sum(4)); // NaN
console.log(sum('x', 'y')); // 'xy'
```

위 코드는 문법상 아무 문제가 없다. 하지만 개발자의 의도와는 다르다.

이런 상황이 발생한 이유는 다음과 같다.

- 자바스크립트는 매개변수와 인수의 개수가 일치하는지 확인하지 않는다
- 자바스크립트는 동적 타입언어이므로 사전에 매개변수 타입을 지정할수없다.

우리는 함수를 정의할 때 적절한 인수가 전달되었는지 추가적인 코드로 확인해야 한다.

**인수의 타입이 부적절한 경우**

매개변수를 통해 전달된 인수의 타입이 부적절한 경우 다음과 같은 방법으로 에러를 발생시킬 수 있다.

```
function sum(a, b) {
	if ( typeof a !== 'number' || typeof b !== 'number'){
		throw new TypeError('인수는 모두 숫자 값이어야 한다.');
	}
	return a + b;
}

console.log(sum(4)); // TypeError: 인수는 모두 숫자 값이어야 한다.
console.log(sum('x', 'y')); // TypeError: 인수는 모두 숫자 값이어야 한다.
```

위와 같이 에러를 통해 잘못된 호출을 방지 할 수 있지만, 사전에 방지할 수 없고 에러가 런타임에 발생한다. 따라서 타입 스크립트(정적 타입을 선언할 수 있는 자바스크립트의 상위 확장)를 도입하여 컴파일 시점에 부적절한 호출을 방지할 수도 있다.

**인수의 개수를 확인하는 법**

앞의 예제는 타입을 확인하지만 인수의 개수는 확인하지 않는다. 인수의 개수를 확인하는 법은 다음과같다.

- arguments 객체를 통해 인수 개수를 확인할 수 있다.
- 인수가 전달되지 않은 경우 단축 평가를 사용해 매개변수에 기본값을 할당할 수 있다.
- ES6의 매개변수 기본값을 사용할 수 있다.

단축 평가를 사용해 매개변수에 기본값을 할당해보자

```
function sum(a, b, c) {
	a = a || 0;
	b = b || 0;
	c = c || 0;
	return a + b + c;
}

console.log(sum(1, 2, 3)); // 6
console.log(sum(1, 2)); // 3
console.log(sum(1)); // 1
console.log(sum); // 0
```

ES6의 매개변수 기본값을 사용해보자. 인수 체크 및 초기화를 간소화할 수 있다. 단, 인수가 부족하게 전달된 경우 즉 인수를 전달하지 않을경우, undefined를 전달한 경우에만 유효하다.

```
function sum(a = 0, b = 0, c = 0) {
	return a + b + c;
}

console.log(sum(1, 2, 3)); // 6
console.log(sum(1, 2)); // 3
console.log(sum(1)); // 1
console.log(sum); // 0
```

### 매개변수의 최대 개수

**매개 변수의 개수는 적을 수록 좋다.**

ECMAScript 사양에서는 매개변수의 최대 개수에 대해 명시적으로 제한하고 있지 않다. 물론 메모리의 제한때문에 매개변수 선언에도 최대 개수는 제한이 있겠지만, 원한다면 충분히 많은 매개변수를 지정할 수 있다. 매개변수는 최대 몇개까지 사용하는 것이 좋을까?

매개변수는 입력 순서에 의미가 있다. 따라서 함수를 호출 시 인수를 전달하는 경우 마찬가지로 순서를 고려해야한다. 매개변수는 함수의 사용법을 이해하기 어렵게 만들고 실수를 유발하는 요소이다. 매개변수의 개수나 순서가 변경될 때 함수의 호출 방법도 바뀌므로 코드 전체를 수정해야 될 수 있다. 매개변수는 유지보수성을 저하시키는 원인이다.

결론적으로, 매개변수는 코드의 가독성을 떨어뜨리는 요소이므로 이상적으로 0개가 best이며, 적을수록 좋다. 매개변수가 많은 것은 함수가 하나의 기능이 아닌 여러가지 일을 한다는 증거이므로 좋지않다. 이상적인 함수는 한 가지 일만 해야 하며 가급적 작게 만들어야 한다.

매개변수는 최대 3개를 초과하지 않도록 하는 것이 좋다. 그 이상의 매개변수가 필요한 상황이라면 객체를 함수의 인수에 전달함으로서 가독성을 높이고 실수를 줄일 수 있다.

객체를 인수로서 전달하는 예제

```
$.ajax({
	method: 'POST',
	url: '/user',
	data: { id: 1, name: 'Lee'},
	cache: false
});
```

**객체를 인수로 전달할 시의 장점**

객체를 인수로 사용하면 프로퍼티 키만 정확히 지정하면 순서를 고려하지 않아도 되므로 신경쓸 것이 줄어든다. 또한 함수에 인수를 전달할때 프로퍼티 키가 인수의 의미를 설명해주므로, 코드의 가독성이 좋아지고 실수가 줄어드는 효과가 있다.

**주의점**

함수 외부에서 함수 내부로 전달한 객체를 함수 내부에서 변경하면 함수 외부의 객체가 변경되는 부수효과가 발생한다.

### 반환문

**함수의 실행결과 반환(return)**

함수는 return 키워드와 표현식(반환값)으로 이루어진 반환문을 사용해 실행 결과를 함수 외부로 반환(return)할 수 있다.

반환문 사용예시

```
function divide (num1, num2) {
	return num1 / num2;
}

//함수 호출은 반환값으로 평가된다.
var res = divide(2, 8);
console.log(res); // 0.25
```

함수는 return 키워드를 사용해 자바스크립트의 모든 값을 반환할 수 있다. 함수 호출은 표현식이다. 함수 호출 표현식은 return 키워드가 반환한 표현식의 평가 결과인 반환값으로 평가된다.

**반환문은 두 가지 역할을 한다.**

1. 함수의 실행을 중단하고 함수 몸체를 빠져나간다.
2. return 키워드 뒤에 오는 표현식을 평가해 반환한다.

**반환문의 역할 1 : 함수의 종료**

반환문이 실행되면 함수의 실행이 중단되고 함수 몸체 밖으로 실행흐름이 이동한다. 그렇기 때문에 함수 몸체 안에서 반환문 이후에 오는 문들은 실행되지않고 무시된다.

```
function divide (num1, num2) {
	return num1 / num2;

	console.log('실행 안되요');
}

console.log(divide(4/2)); //2

```

**반환문의 역할 2 : 함수의 실행결과 반환**

반환문은 return 키워드 뒤에 위치한 표현식을 평가하여 그 값을 반환한다. return 키워드뒤에 반환결과를 명시하지 않으면 undefined가 암묵적으로 반환된다. 반환문은 생략될 수 있고, 이 경우 함수의 실행 종료시점에 암묵적으로 undefined를 반환한다.

```
// 실행결과 반환

function isOdd(num) {
	return num % 2 === 1 ? true : false;
}
//return 뒤의 표현식 평가 후 반환
console.log(isOdd(5)); //true

// return 뒤에 표현식이 없는 경우
function foo1 (){
	return;
}

//암묵적으로 undefined 반환
console.log(foo1()); //undefined


//return 문이 없는 경우
function foo2(){

}

//함수 몸체의 마지막 문까지 실행후 undefined 반환
console.log(foo2()); //undefined
```

**반환문 사용시 주의점**

1. return 키워드와 반환값 사이에 줄바꿈이 있으면 ASI에 의해 반환값이 무시될 수 있다.
2. 함수 몸체 내부에서만 사용할 수 있다.
   - 전역에서 사용시 문법에러 발생
   - 단, node.js 는 파일별로 독립적인 파일 스코프를 가져서 에러발생하지 않음

## 6. 참조에 의한 전달과 외부 상태의 변경
