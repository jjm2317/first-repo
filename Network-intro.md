---
title: Network intro
date: 2021-03-30 21:01:58
tags:
---

# 네트워크

**네트워크란**

컴퓨터나 태블릿 스마트폰이 연결

분산되어 있는 컴퓨터들이 통신망으로 연결된것

### 중요성

**www**

**youtube**

통신망의 대역폭이 커지면서 유튜브등의 cdn 이 활성화

**email**

**4차 산업혁명**

3차산업혁명에서 정보들이 연결된다.

4차산업혁명에서 떠오르는 기술은 네트워크 기반으로 동작한다.

네트워크로 연결된 여러 컴퓨터들이 연산작업을 수행

**블록체인**

블록체인 기술은 신뢰 가능한 인터넷

FAANG 기업들은 네트워크 연결에서 동작하는 서비스를 제공

삼성의 경우, 5g 모바일 서비스를 상용화

자율주행에도 중요한 개념

### 네트워크역사

1. 계산기에 명령어 전달
2. 컴퓨터에 전신기 연결
3. 시분할 시스템 개발, 전화연결및 제어
4. 패킷스위칭, 네트워크 시스템 제안
5. 아파넷 발족, 4개 대학으로 망구성

**국내**

1. 서울대와 구미 연구소에서 패킷 스위칭 연결
2. lg u+ pc 통신
3. kt 인터넷 상용서비스
4. sk브로드밴드 초고속 인터넷 도입
5. 인터넷 보급률 95%

### 네트워크 형태

LAN 근거리 통신망

- 사무실 또는 학교 등의 가까운 지역을 묶은 네트워크

WAN 장거리 통신망

- 각각 떨어진 LAN망을 연결, 규모가 큰 네트워크, ISP 로 연결

  ISP 는 인터넷 제공자이다. lg, kt sk 를 말한다.

VPN 가상 사설망

- 공중망을 사설망처럼 사용, 암호화

### 네트워크 표준

네트워크 표준 기구 / iso 국제 표준화 기구 / ieee 미국전기 전자 협회

ITU 국제 전기 통신 연합 통신 표준본부

인터넷 표준기구

- ietf 인터넷 엔지니어 테스크포스 / rfc 프로토콜 정의 문서

이더넷 - ieee 802.3

tcp/ip -> rfc 1122 & 1123, http/1.1 -> rfc 2616

## 네트워크 구조

- 네트워크 구조
- 홈 네트워크
- 기업네트워크
- 클라우드 네트워크

**규모**

학교나 회사 등의 집단 크기에 따라 구분- 사용자, 대역폭

**업종**

공공기관, 제조, 금융, 게임 등의 업종에 따른 서비스 중요도

**통신 방식과 경로**

server & client, peer to peer

**토폴로지**

start, ring, mesh, bus, tree, redundancy

**Star**

컴퓨터와 컴퓨터가 가운데 를 기준으로 2depth로 연결 별모양

**ring**

컴퓨터가 상호간으로 1depth 멀어질수록 1depth 추가

**mesh**

개체수가 늘어나면 문제

**bus**

큰라인 버스를 통해 통신

**tree**

물리적인 네트워크 구성시 가장 많이 사용

**redundancy**

한쪽이 문제시 다른쪽으로 통신 (이중화)

### 홈네트워크

인터넷 - isp - 모뎀 - 공유기 - 컴퓨터

인터넷 접속을 위해 isp 필요

isp 업체에 신청 시 모뎀 설치, 모뎀이 연결된 컴퓨터는 인터넷 사용가능

모뎀과 공유기를 연결시켜 여러 기기를 사용할 수 있게 한다.

### 기업용 네트워크

ISP - 전용선 - 라우터 - 방화벽 - l3 백본 - l2 스위치 -서버, 컴퓨터 - l4 로드 밸런서- dmz

안정성이 중요

회사는 서버유지를 위해 여러 ip를 할당받아 사용

데이터는 라우터를 통과, 방화벽으로 보안 강화

각 스위치가 컴퓨터로 연결, dmz는 외부에 공개

로드밸런서로 서비스를 분산시켜준다.

### 클라우드 네트워크 (aws)

인터넷 - route53 - igw - vpc - elb - auto scaling - security group - ec2

string을 ip로 변경해주는 것을 dns -> route53

vpc 다양한 네트워크 설계를 하나의 망으로 구성

auto saling : 자동으로 서버 대역폭등을 조절

## OSI 7 layer

- 정의
- 모델
- 기능

### 정의

네트워크 프로토콜과 통신을 7 계층으로 표현

**왜?**

프로토콜을 기능별로 나누고 계층별로 구분

벤더간 호환성을 위한 표준 필요 -> 쉬운 접근성으로 기술의 발전

**역사**

정부나 특정 벤더에서 독점 개발하다 공개형 모델이 필요하게 됨

iso 에 의해 관리

### 모델

application presentation session transport network datalink physical

physical : 네트워크 하드웨어 전송 기술

data link : 이더넷, 랜카드, mac 통신, 에러검충/ 재전송

network: ip 통신 , 라우팅

transport : tcp / udp

session : tcp / ip 통신 연결을 수립 / 유지 / 중단

presentation : 인코딩 암호화 압충

application : 응용서비스 http, smtp

#### 1계층 physical

**기능**

장치와 통신 매체 사이의 비정형 데이터의 전송

디지털을 전기 무선 또는 광신호로 변환

전송되는 방법 제어신호, 기계적 속성 등을 정의

케이블, 인터페이스 ,허브 리피터 등이 이에 속한다.

인터페이스 : 통신을 위해선 규격이 맞아야됨

#### 2계층 Data link

**기능**

동일 네트워크 내에서 데이터 전송, 링크를 통해서 연결을 설정하고 관리

물리 계층에서 발생할 수 있는 오류를 감지하구 수정

모뎀, 스위치

#### 3계층 Network

**기능**

다른네트워크로 데이터 전송, IP 주소로 통신

출발지 ip에서 목적지 ip로 데이터 통신 시 중간에서 라우팅 처리

데이터가 큰 경우 분할 및 전송후 목적지에서 재 조립하여 메시지 구현

ip통신과 라우팅

l3 스위치, 라우터

#### 4계층 Transport

**기능**

호스트 간의 데이터 전송

오류 복구 및 흐름 제어, 완벽한 데이터 전송을 보장

tcp / udp

l4 계층을 특정 하드웨어로 구분하기 모호

port 를 제어한다는 의미로 l4 로드 밸런서가 있다.

#### 5계층 Session

**기능**

로컬 및 원격 애플리케이션 간의 ip / port 연결을 관리

session table :

#### 6계층 Presentation

**기능**

사용자 프로그램과 네트워크 형식간에 데이터를 변환하여 표현과 독립성을 제공

인코딩, 디코딩, 암호화, 압축

ascii, jpg , mpeg

#### 7계층 Application

**기능**

사용자와 가장 밀접한 소프트웨어

이메일 서비스 smtp, 파일전송 ftp

## TCP/IP 모델 비교와 캡슐화

- tcp ip란
- tcp ip 모델
- tcp ip osi7 layer 비교
- 캡슐화

### 정의 tcp ip

네트워크 프로토콜의 모음으로 패킷 통신 방식의 ip와 전송조절 프로토콜인 tcp 로 이루어져 있다.

### tcp/ip 모델

application / transport / network / network interface

### tcp/ip osi 7layer

네트워크 인터페이스와 datalink, physical은 이더넷으로 연결되어 있다.

네트워크는 ip icmp ospf가 존재

transport는 tcp 와 udp 가존재

application http, smtp, dns

### 캡슐화

**인캡슐레이션**

컴퓨터에 접속시 데이터를 상대 컴퓨터에 송신시

세션에서 정형화된 데이터,

tcp 헤더에서 세그먼트가 어떤 포트를 사용하는 지 결정

네트워크 레이어에서 데이터(패킷) ip 헤더에 인캡슐레이션

데이터링크 프레임은 네트워크의 시리얼 장비를 붙인다.

피지컬에서 비트는 신호로 구성된다.

**디캡슐레이션**

피지컬링크에서 비트, 시그널이 보내짐

데이터 링크에서 맥헤더를 보고 하드로 연결

네트워크에서 ip정보를 보고 transport를 찾아감

tcp헤더를 보고 포트를 찾는다.

세션에서 데이터가 사용자영역으로 간다.
