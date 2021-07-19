---

title: algorithm
date: 2021-07-19

---
### > 문제
* 정수 b에서 정수 a를 뺀 값을 구합니다(b > a가 되도록 입력 받음)

### > 출력예시
a -> 5
b -> 4
b -> 7

```
a의 값：5
b의 값：4
a보다 큰 수를 입력해주세요.
b의 값：7
b - a 는 2입니다.
```

```java
package chap01;

import java.util.Scanner;

public class Difference_01_10 {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);

		System.out.print("a의 값：");
		int a = sc.nextInt();

		int result;
		
		/*
		1. b의 값을 받는다
		2. a와 비교해준다
		3. 조건에 성립하지 않으면 다시입력받고, 성립하면 값을 구한다
		*/
		
		while (true) {
			System.out.print("b의 값：");
			int b = sc.nextInt();
			
			//a 보다 더 큰수를 입력받기 
			if (b <= a) {
				System.out.println("a보다 큰 수를 입력해주세요.");
			} else {
				result = b - a;
				System.out.println("b - a 는 " + result + "입니다.");
				//반복문 멈추기
				break;
			}
		}
	}
}
```
