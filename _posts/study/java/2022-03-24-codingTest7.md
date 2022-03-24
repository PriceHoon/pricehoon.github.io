---
layout: post
title: 코딩테스트Java-7
description: >
    코딩테스트Java 7단계 회문 문자열
sitemap: false
hide_last_modified: false
categories:
  - study
  - java
---

# 코딩테스트 Java - 7

## 코딩테스트 Java 7단계 팰린드롬


#### 설명

> 앞에서 읽을 때나 뒤에서 읽을 때나 같은 문자열을 팰린드롬이라고 합니다.
문자열이 입력되면 해당 문자열이 팰린드롬이면 "YES", 아니면 “NO"를 출력하는 프로그램을 작성하세요.
단 회문을 검사할 때 알파벳만 가지고 회문을 검사하며, 대소문자를 구분하지 않습니다.
알파벳 이외의 문자들의 무시합니다.


#### 입력
> 첫 줄에 길이 100을 넘지 않는 공백이 없는 문자열이 주어집니다.

#### 출력
> 첫 번째 줄에 팰린드롬인지의 결과를 YES 또는 NO로 출력합니다.

#### 출력예시                
> found7, time: study; Yduts; emit, 7Dnuof     >>>   YES


**작성 코드✏️**
~~~java
import java.util.Scanner;


public class Main {

	public void sol(String an) {
		an = an.toLowerCase();

		String change = an.replaceAll("[^a-z]","").replace(" ","");
		//System.out.println(change);

		String reChange = new StringBuilder(change).reverse().toString();

		if(change.equals(reChange)) {
			System.out.println("YES");
		}else {
			System.out.println("NO");
		}
	}

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.print("입력>>");
		String answer = sc.nextLine();

		Main main = new Main();
		main.sol(answer);
	}

}
~~~

**💡배운것과 느낀점💡**

**1. replaceAll()**
~~~
> regex(정규식)을 다른 어떠한 지정상황으로 대체할 때 사용한다.
> 본 문제에서는 [^a-z]의 정규식을 사용했다.(a~z이외에는 전부 ""로 바꾸라는 의미)
~~~
**2. replace()**
~~~
> replaceAll()과 다르게 정규식이 들어갈 수 없다.
> 특정문자를 다른 문자로 바꿀 때 주로 사용한다.
~~~

**느낀점**
~~~
> 정규식의 개념을 다시한번 되돌아 볼 수 있는 시간이였다.
> replace()메서드 이외에는 사용해본적이 없었는데, replaceAll()를 통한 정규식 사용을 되돌아 보았다.
~~~
