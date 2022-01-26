---
layout: post
title: 코딩테스트Java-1
description: >
    코딩테스트Java 1단계 문자열
sitemap: false
hide_last_modified: false
categories:
  - study
---

# 코딩테스트 Java

## 코딩테스트 Java 1단계 문자열찾기


#### 설명

>한 개의 문자열을 입력받고, 특정 문자를 입력받아 해당 특정문자가 입력받은 문자열에 몇 개 존재하는지 알아내는 프로그램을 작성하세요.

>대소문자를 구분하지 않습니다.문자열의 길이는 100을 넘지 않습니다.


#### 입력
>첫 줄에 문자열이 주어지고, 두 번째 줄에 문자가 주어진다.

>문자열은 영어 알파벳으로만 구성되어 있습니다.


#### 출력
>첫 줄에 해당 문자의 개수를 출력한다.

**작성 코드✏️**
~~~java
import java.util.Scanner;

public class Main {
public static void main(String[] args) {
int count = 0;
Scanner sc = new Scanner(System.in);
System.out.print("문자열 입력:");
String answer = sc.next().toUpperCase();
System.out.print("찾을 문자 입력:");
char alpa = sc.next().charAt(0);
char t = Character.toUpperCase(alpa);
for (int i = 0; i < answer.length(); i++) {			
  if(answer.charAt(i)==t) {
    count++;
  }//if			
}//for
System.out.printf("%d",count);
 }//main
}//Main
~~~

**모범답 코드✏️**
~~~java
import java.util.*;
class Main{
	public int solution(String str, char t){
		int answer=0;
		str=str.toUpperCase();
		t=Character.toUpperCase(t);
		//System.out.println(str+" "+t);
		/*for(int i=0; i<str.length(); i++){
			if(str.charAt(i)==t) answer++;
		}*/
		for(char x : str.toCharArray()){
			if(x==t) answer++;
		}
		return answer;
	}

	public static void main(String[] args){
		Main T = new Main();
		Scanner kb = new Scanner(System.in);
		String str=kb.next();
		char c=kb.next().charAt(0);
		System.out.print(T.solution(str, c));
	}
}
~~~
 **💡배운것과 느낀점💡**

 **1.클레스를 따로 분리하자**



~~~
메인에 다 짜지말고 기능을 클레스 단위로 묶는 기초를 망각했다.
~~~

  **2.Char자료형 입력받기**







~~~
  char자료형을 입력 받을 때는
~~~
  ~~~java
  char alpa = sc.next().charAt(0);
  ~~~

  **3.대소문자를 구별하자**



   ~~~
   대소문자를 구별하여 입력한 문자를 판별하기 위해서
   ~~~

   ~~~java
   String answer = sc.next().toUpperCase();
   char t = Character.toUpperCase(alpa);
   //대문자 변환 로직
   ~~~
