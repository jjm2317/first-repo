---
title: "javascript ASCII, Unicode"
date: 2020-08-28 18:30:58
category: "javascript"
draft: false
---

# 아스키 코드(ASCII)& 유니코드 (Unicode) 정리

## 문자인코딩이 필요한 이유

### 먼저, 프로그래밍 언어란?

**컴퓨터는 사람의 언어를 이해하지 못한다.** 컴퓨터는 기계어만을 이해할 수 있다.

그렇기 때문에 컴퓨터에게 명령을 내리기 위해서는 인간의 언어인 자연어를 기계어로 바꿔서 명령을 해주어야 한다. 하지만 이진수로 이루어진 기계어를 **직접 입력한다는 것은 복잡하고 어렵다.**

사람과 컴퓨터의 소통을 매개하기 위해 필요한 것이 컴파일러라는 번역기이다. 우리는 이 번역기에 **프로그래밍 언어**로 작성한 프로그램을 보내주면 컴파일러가 프로그래밍 언어를 기계어로 번역해준다.

즉 프로그래밍언어는 **인간과 컴퓨터의 소통을 매개**하기 위해 만들어진 언어이다.

### 문자 인코딩은 문자열을 컴퓨터에 전달하는 것이다.

명령, 즉 우리의 언어를 기계어로 컴퓨터에게 전달하고 컴퓨터로부터 출력값을 전달받기위해서,

프로그래밍 언어에서는 어떤 값을 어떤 기계어로 변환할 것인지,그리고 컴퓨터가 처리한 정보를 어떻게 변환할 지에 대한 체계를 도입하고 있다.

여기서 인코딩과 디코딩이라는 개념을 짚어보자

- 인코딩 : 사용자가 입력한 문자나 기호들을 컴퓨터가 이용할 수 있는 신호로 만드는 것
- 디코딩 : 인코딩된 신호를 다시 인간이 이해할수 있게 해독하는 것

예로 우리가 '영어'로 작성한 프로그램을 기계어로 바꿔야된다. 그것이 **문자 인코딩**이다. 그런데 문자 인코딩을 위해서는 일관된 체계가 필요하다. 문자인코딩에 대한 기준, 체계를 정리한것이 **문자열 세트**이다.

일반적으로 문자 인코딩과 문자열 세트는 **어떤 문자를 사용할 수 있으며 어떤 식으로 표현되는지를 나타내는 데서 동의어로 취급**되기도한다.

### 문자 인코딩은 어떻게 이루어지는가

문자 인코딩 형태(character encoding form) : 문자열 세트 내의 문자들을 컴퓨터 시스템에서 사용할 목적으르 일정한 범위 안의 정수(코드 값) 으로 변환한다.

## 아스키코드와 유니코드

문자열 세트의 표준으로서, 초기에는 **아스키코드**가 활용되었다. 아스키코드는 '**영어**'라는 언어에 대한 인코딩 기준이다. 하지만 프로그래밍이 세계적으로 점차 확대됨에 따라 영어 하나로는 한계점이 있었다.더욱이 7비트만을 활용하는 아스키 특성상 다른 언어를 새로이 집어 넣는 것도 불가 하였다. 그래서 확장판인 **유니코드**가 등장하였다. 최초버전의 용량이 무려 2byte, 즉 16비트 65536개의 문자를 표현할 수 있다. 버전이 확장됨에 따라 현재 100만자 이상을 표현할 수 있다.

## 1. ASCII

아스키 인코딩의 특징을 알아보자

- 7비트 인코딩
- 1비트는 오류검출용으로 사용
- 33개의 제어문자, 95개의 출력 가능 문자
- 출력가능문자 : 52개 알파벳 대소문자 / 10개 숫자 / 32개 특수문자 1개 공백문자

아스키 코드표

![ASCII Table - 아스키 코드표](https://t1.daumcdn.net/cfile/tistory/216CE84C52694FF020)

## 2. 유니코드

유니코드는 기존의 1byte에 문자열 셋을 할당한 방식에서, 더 많은 언어를 표시하고자 국제적으로 만들어진 표준코드이다.

다음과같은특징이 있다.

- 가변 인코딩 방식(글자마다 byte 길이가 다르다.)

![Image for post](https://miro.medium.com/max/1624/1*A6GcpKbbG-u6ps66f_rEjg.png)

(출처 : 위키피디아)

- 아스키코드와 호환된다.
- 확장 가능하다.
