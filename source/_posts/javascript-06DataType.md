---
title: 06DataType
date: 2020-08-25 15:13:03
tags:
---

# 데이터 타입

- 데이터 타입은 **값의 종류**이다.
- **모든 값**은 데이터 타입을 갖는다.

## 값의 종류

1. **원시 타입 (primitive type)**

- number
  - **정수 실수 구분 없이** 실수타입 하나만 존재
- string
- boolean
- undefined
- null
- symbol
  - es6 에서 새로 추가

2. **객체 타입(object/reference type)**

- 객체
- 함수
- 배열
- etc...

*타입 마다 생성한 목적, 용도, 메모리 공간 크기, 저장되는 2진수, 해석하는 방식 전부 다르다*



## 1. 숫자 타입(number)

- 하나의 숫자 타입만 존재 (실수)
- 64비트 부동소수점 형식

- 정수, 실수, 2진수, 8진수, 16진수 리터럴이 **모두** **배정밀도 64비트 부동소수점 형식의 2진수**로 저장

  - 예시

    ```
    var binary = 0b01000001; // 2진수
    var octal = 0o101; // 8진수
    var hex = 0x41; // 16진수
    
    console.log(binary);//65
    console.log(octal); // 65
    console.log(hex); // 65
    ```



### 정수로 표시된 수도 실수로 처리한다

- 한가지 저장방식만을 따르기때문에 정수로 표기된 수도 연산시 실수로 나올 수 있다.

```
console.log(3/2); // 1.5
```



### 특이사항

특별한 값 세가지 표현가능

- Infinity : 양의 무한대
- -Infinity : 음의 무한대
- NaN : 산술 연산 불가(not a number)



## 2. 문자열 타입(string)

- 텍스트 데이터를 나타냄
- 0개이상의 16비트 유니코드 문자(UTF-16) 의 집합
- 일반적으로 작은따옴표' ' 사용
  - 따옴표로 감싸지 않으면 엔진이 토큰으로 인식
  - 따옴표 내의 다른 따옴표는 문자열로 인식
- 원시타입이며 생성후 변경 될 수 없다.



### 템플릿 리터럴(template literal)

- es6에 도입된 문자열 표기법
- 백틱 `` 사용
- **멀티라인 문자열/ 표현식 삽입/ 태그드 템플릿** 등 처리 기능 제공



#### 멀티라인 문자열

- 일반 문자열에는 개행 미허용
  - 공백을 표현하려면 이스케이프 시퀀스(escape sequence) 사용해야됨 ( \n )
- 템플릿 리터럴 내에서는 이스케이프 시퀀스를 사용하지 않고도 개행과 공백이 있는 그대로 적용된다.

#### 표현식 삽입

- 문자열을 연결할 때 보통 연결 연산자 + 를 사용한다.
- 템플릿 리터럴 내에서 표현식 삽입 (expression interpolation)을 통해 간단히 문자열 삽입가능

```
var country = 'Korea';
var city = 'Seoul';

console.log(`I live in ${city}, ${country}`);// I live in Seoul, Korea;
```

- ${}으로 표현식을 감싸서 삽입한다.
  - 표현식의 평가값은 문자열로 타입 변환
  - 템플릿 리터럴 내에서만 사용



## 3. 불리언 타입(boolean)

- 논리적 참, 거짓 **true/false** 
- 조건문에서 주로 사용



## 4. undefined 타입

- undefined 로 유일한 값을 가짐

- var 키워도로 변수 선언시 암묵적으로 undefined 로 초기화
  - 변수에 할당 전에 undefined 로 암묵적 할당

#### 개발자가 의도적으로 할당하는 것은 지양

- undefined의 본래 취지와 어긋남
  - 쓰레기값이 할당되지 않도록 자바스크립트 엔진이 암묵적으로 undefined 할당 하는 것이 본래 이유
- 변수에 값이 없다는 것을 개발자 임의로 명시하고 싶을 땐 null 할당

#### 자바스크립트에서는 선언과 정의의 경계가 모호하다

- 다른 언어에서는 보통 선언은 **식별자의 존재만 알리는 것**이고 정의는 **식별자와 메모리 주소를 연결**하는 것이다. 
- 자바스크립트에서는 선언 이후에 자동으로 정의가 이루어진다. 
- ECMAScript 사양에서 변수는 선언으로 표현/ 함수는 정의로 표현
  - 이를 반영하여 변수는 선언, 함수는 정의로 표현하도록 하자

## 5. null 타입

- null 로 유일한 값을 가짐
- 변수에 값이 없다는것을 개발자 의도적으로 명시/ 이전에 참조하던 값을 더이상 참조 안한다/ 즉 값의 제거를 의미
- 대소문자 구별!

### 언제 사용하는가/ 어떤 의미인가

- 개발자가 의도적으로 변수에 값이 없다는 것을 명시
- 이전에 참조하던 값을 더이상 참조 안한다
- 값을 제거 하였다
- 함수가 유효한 값을 반환할 수 없을때 null을 반환하기도함
  - null 보다 undefined 반환이 타당하다는 의견도 있음



## 6. symbol 타입

- es6 에서 새로 추가된 원시 타입 값
- 다른 값과 중복되지 않는 유일무이한 값

### 사용예시

```
var key = Symbol('key');
console.log(typeof key); // symbol

var obj = {};

obj[key] = 'special value'
console.log(obj[key]); // special value
```



## 7. 객체 타입

- 앞의 6가지 원시타입 (primitive type) 이외에는 전부 객체 타입
- 자바스크립트는 객체 기반의 언어, 즉 거의 모든것이 객체
- 자세한 내용은 추후 학습



## 데이터 타입은 왜 필요한가

크게 세가지로 정리할 수 있다

1. 값을 **저장**할 때 확보해야 하는 메모리 공간의 크기를 결정

- 값의 낭비나 손실없이 저장할 수 있어야 한다
- 데이터 타입에 따라 정해진 크기의 메모리 공간 확보
- ex ) 숫자 타입은 64비트 부동소수점 형식이므로 8바이트의 메모리공간을 확보
- 문자열과 숫자 이외에 데이터 타입의 크기는사양에서 명시하지 않아서 엔진 제조사의 구현에따라 다를 수도 있다.

2. 값을 **참조**할때 한번에 읽어들일 메모리 크기 결정

3. 메모리에서 읽어들인 2진수를 어떻게 해석할 지 결정

## 동적 타이핑

정적을 static, 동적을 dynamic 이라고 한다.  프로그래밍 언어 관점에서는 정적이 더 좋긴 하다. 동적은 변한다, 정적은 변하지 않는다로 받아들이자.

### 동적 타입 언어 & 정적 타입언어

동적 타입은 타입이 변한다는 개념으로 받아들이면된다. 

변수선언은 var 키워드를 선언하고 변수이름을 적으면 선언이 된다. 

var로 선언한 변수에는 모든  타입의 값이 들어갈 수 있다.

대부분의 언어는 정적 타입언어이다. 대표적으로 c 언어 같은 경우 타입별로 변수선언 키워드가 다르다. 즉 변수의 타입마다 할당할 수 있는 값이다르다. 

동적타입언어인 자바스크립트는 숫자의 경우 하나의 타입이 존재한다.



#### 어떤게 좋을까?

동적타입언어가 편하긴하지만 이걸로 인해서 에러가 발생할 수 있는 여지가 있다. 

웹페이지에서 보조적인 기능을 하기 때문에 한사람을 위해서 만들어진 언어였다. 하지만 협업이 많이 일어나고 큰 규모의 프로그래밍을 하고 있다. 지금은 에러발생가능성이 높아졌기 때문에 큰 문제이다. 

즉 한번 정해진타입이 안바뀌는게 개발자에게 좋기 때문에 정적 타입언어가 좋다고 보여진다. 



자바스크에서 변수는 잘써야 한다. 동적 타입언어기 때문이다. 변수 안에 들어가 있는 값을 타입오브로 확인하지 않으면 언제든지 실수가 발생할 수 있다. 예상과 다른 값이 들어갈 수 있다는 말이다. 

변수가 많으면 많을수록 오류의 개수가 많이질 수 있다. 



#### 변수의 개수는 적은게 좋다.

변수가 1000개인 프로그램이 100개인 프로그램이 오류 가능성이 높다. 변수를 줄일 수 없다라고 하면 생명주기를 짧게하여 빨리 죽이는게 좋다.

다음을 지키도록하자 

- 전역변수를 사용하지 않는다.
- 변수보다는 상수를 사용합니다.
- 변수이름은 심사숙고해서 지어야 한다.


