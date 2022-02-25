---
layout: post
title: 코딩테스트Java-3
description: >
    코딩테스트Java 3단계 문자열 탐색
sitemap: false
hide_last_modified: false
categories:
  - study
  - java
---

# 코딩테스트 Java - 3

## 코딩테스트 Java 3단계 문자열 탐색

#### 설명

>한 개의 문장이 주어지면 그 문장 속에서 가장 긴 단어를 출력하는 프로그램을 작성하세요.
> 문장속의 각 단어는 공백으로 구분됩니다.

#### 입력
>첫 줄에 길이가 100을 넘지 않는 한 개의 문장이 주어집니다. 문장은 영어 알파벳으로만 구성되어 있습니다.

#### 출력
>첫 줄에 가장 긴 단어를 출력한다. 가장 길이가 긴 단어가 여러개일 경우 문장속에서 가장 앞쪽에 위치한단어를 답으로 합니다.

#### 출력예시
> it is time to study >>>>>>>study

**작성 코드✏️**
~~~java
public class Main {

	public String change(String answer) {


		String[] an = answer.split(" ");
		String create = "";
		int maxLength = 0;


		for(String x : an) {
			if(x.length()>maxLength) {
				maxLength=x.length();
				create = x;
			}
		}

			return create;
	}
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		System.out.println("입력>>");
		String answer = sc.nextLine();
		Main main = new Main();
		System.out.println(main.change(answer));


	}
}
~~~

**💡배운것과 느낀점💡**

**1. next(), nextLine()**
~~~
> next()로 만 문자열을 입력 받았을 때 공백까지 이후로 담지 못했다.
> enter값을 입력하기 전까지 모든 입력 문자열을 담고 싶다면 nextLine()사용.
~~~

**2. spilit()**
~~~
> 코틀린에서 써봐서 익숙한 메서드로 공백" "을 기준으로 문자열을 잘라 배열로 보관.
> 따라서 초기화하는 자료형도 String[]이 되겠다.
~~~

**3. indexOf()**
~~~
> 공백으로 구별할 때 indexOf(' ')!=-1로 사용할 수 있다는 사실!
~~~
**4. 생각의 한계**
~~~
> 간단하게 가장 큰 길이를 가진 문자열을 찾아 그 길이를 저장하고 비교하면 된다.
> 필자는 이중포문을 사용하여 전부 비교하는 코드를 작성했는데, 로직상의 오류도 있었고,코드도 더러웠다.
~~~

**느낀점**
~~~
> 생각을 복잡하게 하면 보일 것도 안보인다.
~~~
