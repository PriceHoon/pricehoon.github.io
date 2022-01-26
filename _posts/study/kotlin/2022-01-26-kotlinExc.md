---
layout: post
title: 코틀린 기초
description: >
    코틀린 기초 설명
sitemap: false
hide_last_modified: false
categories:
  - study
  - kotlin
---

# 코틀린 기초문법 배우기 - 1

## 코틀린 기초문법 배우기 - 주석,자료형

**1. 주석처리**
~~~
java와 마찬가지로 // or /**/로 부분 주석처리, 전체 주석처리가 가능하다.
~~~


**2. 변수**
~~~
자료형은 java와 마찬가지로 존재한다.
1.숫자: Int, long, double, Float
2.문자: String
3.논리: boolean(true,false)
> 듣는 강의에서 char형은 따로 언급하지 않았다.
~~~
**2-1. 변수 val,var**
~~~
java와 마찬가지로 자료형이 각각 존재하지만 java와는 사용방식이 조금 다르다.
~~~
**Java 예시**
~~~java
String name ="박상훈";
int number = 1234;
~~~

**Kotlin 예시**
~~~
val name1 = "박상훈"
var name2 = "박상훈"

val number1 = 1234
var number2 = 1234
~~~

~~~
val: 한번 초기화 시키면 다시 바꿀 수 없는 변수(java의 final 상수 개념과 비슷)
var: 한번 초기화 시켜도 언제든 다시 바꿀 수 있는 변수
~~~
**Kotlin변수 선언**
~~~
var number : Int = 1234
자료형을 선언하여 주는 것으로 : 다음 나오는 자료형과 초기화 위한 자료형이 다르면 안된다.
~~~
**Null And ""**
~~~
java와 마찬가지로 아예없는 것과 빈 문자열로 서로 다르다는 것을 인지하자.
~~~
**자료형 변환**
~~~
문자열 변환: toString()메서드 사용
숫자 변환: Integer.parseInt()메서드 사용
> java와 똑같다.
~~~
**자료형 출력**
~~~
println(name::class.java.simpleName)
> String, Int ....의 출력
~~~

💡**java와 다른 점 및 요약**💡
~~~
1. 세미클론이 붙지않는다.
2. val, var로 모든 자료형을 담을 수 있다.
3. fun main()의 형태
4. 출력 메서드 사용시 java처럼 System을 Import하지 않는다.
> 거의 java와 유사하다......
~~~
