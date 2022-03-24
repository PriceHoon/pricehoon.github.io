---
layout: post
title: 코딩테스트Java-5
description: >
    코딩테스트Java 5단계 문자열 뒤집기
sitemap: false
hide_last_modified: false
categories:
  - study
  - java
---

# 코딩테스트 Java - 5

## 코딩테스트 Java 5단계 중복문자열 제거


#### 설명

> 소문자로 된 한개의 문자열이 입력되면 중복된 문자를 제거하고 출력하는 프로그램을 작성하세요.  중복이 제거된 문자열의 각 문자는 원래 문자열의 순서를 유지합니다.


#### 입력
> 첫 줄에 문자열이 입력됩니다. 문자열의 길이는 100을 넘지 않는다.

#### 출력
> 첫 줄에 중복문자가 제거된 문자열을 출력합니다.

#### 출력예시                
> ksekkset      >>>   kset


**작성 코드✏️**
~~~java

import java.util.Scanner;

public class Main {

	public void sol(String an) {

		// indexOf("문자") 찾고자 하는 문자를 순차적으로 탐색하여 몇번째 있는지 알려줌
		// charAt(Int ) int자료형 번째 있는 문자를 찾아줌

		int[] arr = new int[an.length()];
		char[] arrTwo = an.toCharArray();

		for (int i = 0; i < an.length(); i++) {

			arr[i] = an.indexOf(an.charAt(i));
			// System.out.println(arr[i]);
		}

		for (int j = 0; j < arrTwo.length; j++) {

			if (j == arr[j]) {
				System.out.print(arrTwo[j]);
			}
		}
	}

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.print("입력>>");
		String answer = sc.next();

		Main main = new Main();
		main.sol(answer);
	}

}
~~~


**💡배운것과 느낀점💡**

**1. indexOf()**
~~~
> indexOf()를 사용하는 경우는 보통 ()안에 문자가 몇번째 인지 탐색하기 위해서이다.
> indexOf()는 문자를 탐색할 때 앞에서 부터 순차적으로 탐색한다.
~~~

**2. charAt()**
~~~
> charAt()를 사용하는 경우는 보통 ()안에 int자료형이 들어가면, int번째의 문자를 탐색한다.
~~~
**느낀점**
~~~
> 창조적인 사고력이 떨어졌다. indexOf()와 charAt()을 사용하여 할 생각은 못했었고,
  toCharArray를 사용하여 배열화 한 뒤, for을 이용해 비교하려고 했었다.

> 주어진 클레스의 메서드를 활용하자!

> 전 문제부터 느끼는 것은 String class에는 많은 Method가 존재한다는 것!
~~~
