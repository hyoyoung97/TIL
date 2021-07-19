---

title: algorithm
date: 2021-07-19

---
### > 문제
* 정수a, b를 포함하여 그 사이의 모든 정수의 합을 구합니다. 

### > 출력예시
a -> 3
b -> 5
```
a와 b를 포함하여 그 사이의 모든 정수의 합을 구합니다.
a의 값：3
b의 값：5
정수 a, b 사이의 모든 정수의 합은 12입니다.
```

```java
package chap01;

import java.util.Scanner;

public class SumOf_01_09 {

	//sumOf 함수만들기 
	static int sumOf(int a, int b) {
		int min;
		int max;
		
		//상황에 따라 min, max에 매칭될 a, b 정해주기 
		if(a < b) {
			min = a;
			max = b;
		} else {
			min = b;
			max = a;
		}
		
		int sum = 0;
		//답지 
		/*
		for(int i = min; i <= max; i++) {
			sum += i;
		}
		 */
		//min++ 로 인해 첫번째 조건을 선언해주지 않아도 됨 
		for( ;min <= max; min++) {
			sum += min;
		}
		//합을 리턴 
		return sum;
	}
	
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		System.out.println("a와 b를 포함하여 그 사이의 모든 정수의 합을 구합니다.");
		System.out.print("a의 값：");
		int a = sc.nextInt();
		System.out.print("b의 값：");
		int b = sc.nextInt();	
		
		//스캐너로 입력받은 a, b를 넣은 함수 호출 
		System.out.println("정수 a, b 사이의 모든 정수의 합은 " + sumOf(a, b) + "입니다.");
	}

}
```
