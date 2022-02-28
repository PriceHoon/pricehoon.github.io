---
layout: post
title: 코딩테스트Java-4
description: >
    코딩테스트Java 4단계 문자열 뒤집기
sitemap: false
hide_last_modified: false
categories:
  - study
  - java
---

# 코딩테스트 Java - 4

## 코딩테스트 Java 4단계 문자열 뒤집기


#### 설명

> N개의 단어가 주어지면 각 단어를 뒤집어 출력하는 프로그램을 작성하세요.

#### 입력
> 첫 줄에 자연수 N(3<=N<=20)이 주어집니다.
> 두 번째 줄부터 N개의 단어가 각 줄에 하나씩 주어집니다. 단어는 영어 알파벳으로만 구성되어 있습니다.

#### 출력
>N개의 단어를 입력된 순서대로 한 줄에 하나씩 뒤집어서 출력합니다.

#### 출력예시
> 3                
> good      >>>   doog
> Time     >>>    emiT
> Big     >>>     giB


**작성 코드✏️**

~~~java
import java.util.ArrayList;
import java.util.Scanner;

public class Main {

	public ArrayList<String> sol(int n ,String[] str) {


		ArrayList<String> an = new ArrayList<>();

		for(String x : str) {
			String tem = new StringBuilder(x).reverse().toString();
			an.add(tem);

		}

		return an;
	}



	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		Main m = new Main();
		System.out.println("입력>>");
		int n = sc.nextInt();
		String[] str = new String[n];

		for(int i=0;i<n;i++) {
			str[i] = sc.next();
		}

		for(String x : m.sol(n,str)) {
			System.out.println(x);
		}
	}
}
~~~


**작성 코드✏️(앞과 끝 뒤집기)**
~~~java
import java.util.ArrayList;
import java.util.Scanner;

public class Main {

	public ArrayList<String> sol(int n ,String[] str) {


		ArrayList<String> an = new ArrayList<>();

		for( String x : str) {
			char[] ans = x.toCharArray();
			int lt = 0;
			int rt = x.length()-1;
			while(lt<rt) {
				char b = ans[lt];
				ans[lt] = ans[rt];
				ans[rt]= b;
				lt++;
				rt--;
			}

			String a = String.valueOf(ans);
			an.add(a);


		}

		return an;
	}


	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		Main m = new Main();
		System.out.println("입력>>");
		int n = sc.nextInt();
		String[] str = new String[n];

		for(int i=0;i<n;i++) {
			str[i] = sc.next();
		}

		for(String x : m.sol(n,str)) {
			System.out.println(x);
		}


	}
}

~~~


**💡배운것과 느낀점💡**

**1. StringBuilder()**
~~~
> String은 객체이다.(명심!!)
> String객체로 선언된 자료형은 바꿀 수 없다.
> 바꾸는 것 처럼 보이는 이유는 계속해서 새로운 객체가 생성되기 때문이다.
> 이러한 무분별한 객체생성을 줄이기 위한 StringBuilder()를 사용하자.
> String 자료형의 데이터를 수정하거나 특정 작업을 할 때 사용하자.
> String tem = new StringBuilder(x).reverse().toString();
( String 객체에 담기 위한 toString()메서드의 사용을 잊지말자! )
~~~

**2. String.valueOf()**
~~~
> char배열로 바꿨던 데이터 자료형을 다시 String으로 변환하기 위한 작업.
> String 자료형으로 바꿔준 후 ArrayList에 add() 해준다.
~~~

**느낀점**
~~~
> java를 처음 배울 때 사용 해보지 못했던 것이 너무 많고, String 자료형을 다룰 때
단순히 문자열 = String 마구 생성! 이라고 생각하지 말자.
> String을 자연스럽게 사용하다 보니 객체가 아닌 int와 같은 자료형이라고 생각되었다.
> 내부for문을 잘 사용하지 못했다.
(숫자를 입력받거나 숫자의 개념이 필요할 땐 기존의 i변수를 활용한 for을 사용했고,
처음부터 끝까지 반복하는 for은 내부 for을 사용하면 될 것 같다.)
~~~
