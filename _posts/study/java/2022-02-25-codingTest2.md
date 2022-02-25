---
layout: post
title: 코딩테스트Java-1
description: >
    코딩테스트Java 1단계 문자열
sitemap: false
hide_last_modified: false
categories:
  - study
  - java
---

# 코딩테스트 Java - 2

## 코딩테스트 Java 2단계 문자열 대 소문자

#### 설명

>대문자와 소문자가 같이 존재하는 문자열을 입력받아 대문자는 소문자로 소문자는 대문자로 변환하여 출력하는 프로그램을 작성하세요.

#### 입력
>첫 줄에 문자열이 입력된다. 문자열의 길이는 100을 넘지 않습니다.

>문자열은 영어 알파벳으로만 구성되어 있습니다.


#### 출력
>첫 줄에 대문자는 소문자로, 소문자는 대문자로 변환된 문자열을 출력합니다.

#### 출력예시
> StuDY >>>>>>>sTUdy


**작성 코드✏️**
~~~java
public class Main {

	public String change(String i) {

		String answer = "";

		for( char x : i.toCharArray()) {
			if(Character.isLowerCase(x)) {
				answer+=Character.toUpperCase(x);
			}else {
				answer+=Character.toLowerCase(x);
			}
		}
		return answer;

	}


	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("입력>>");
		String answer = sc.next();
		Main main = new Main();
		System.out.println(main.change(answer));

	}
}
~~~

**💡배운것과 느낀점💡**

**1. toCharArray()**
~~~
> 저 자리에는 Collection객체만 올 수 있으며, String자료형을 Char배열 형태로 바꿔준다.
~~~

**2. Character.isLowerCase()**
~~~
> Character자료형의 형태가 소문자 인지 판별해주는 것으로, Boolean을 return한다.
~~~
**느낀점**
~~~
> java를 공부할 때 사용해보지 못했던 Method가 많이 존재했으며, 문자열의 for형태를
Character형태의 배열로 변환하여 배소문자를 판별하고 특정 로직을 수행하는 것이 가능했다.
~~~
