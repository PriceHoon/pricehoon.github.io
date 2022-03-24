---
layout: post
title: 코딩테스트Java-6
description: >
    코딩테스트Java 6단계 회문 문자열
sitemap: false
hide_last_modified: false
categories:
  - study
  - java
---

# 코딩테스트 Java - 6

## 코딩테스트 Java 6단계 회문 문자열


#### 설명

> 앞에서 읽을 때나 뒤에서 읽을 때나 같은 문자열을 회문 문자열이라고 합니다.
문자열이 입력되면 해당 문자열이 회문 문자열이면 "YES", 회문 문자열이 아니면 “NO"를 출력하는 프로그램을 작성하세요.
단 회문을 검사할 때 대소문자를 구분하지 않습니다.


#### 입력
> 첫 줄에 길이 100을 넘지 않는 공백이 없는 문자열이 주어집니다.

#### 출력
> 첫 번째 줄에 회문 문자열인지의 결과를 YES 또는 NO로 출력합니다.

#### 출력예시                
> gooG      >>>   YES

**작성 코드✏️**
~~~java
import java.util.Scanner;


public class Main {

	public void sol(String an) {


		String ans = an.toLowerCase();
		String rev = new StringBuilder(ans).reverse().toString();

		if(ans.equals(rev)) {
			System.out.println("YES");
		}else {
			System.out.println("No");
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

**모범답 코드✏️**

~~~java
import java.util.Scanner;


public class Main {

	public void sol(String an) {


		String ans = "YES";
                an = an.toUpperCase();
		int len = an.length();

		for(int i =0 ; i<len/2;i++){

      if(an.charAt(i)!=an.charAt(len-i-1)) return "NO";

    }



	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.print("입력>>");
		String answer = sc.next();

		Main main = new Main();
		System.out.println(main.sol(answer));
	}

}
~~~

**💡배운것과 느낀점💡**
~~~
> String클레스의 변형이나 첨삭등의 과정을 거칠 때 StringBuliser Class를 생각했다.
> 틀린 부분은 없었지만 다양한 풀이방법이 존재한다.
> 조금만 더 생각하고 코딩하자.
~~~
