---

title: algorithm
date: 2021-07-19

---
### > 문제
* 양의 정수값의 자릿수를 구하여 나타냄

### > 출력예시
정수값 -> -1
정수값 -> 0
정수값 -> 132

```
양의 정수값의 자릿수를 구합니다.
정수값 : -1
정수값 : 0
정수값 : 132
그 수의 자리는 3입니다.
```
[최종답(1차 + 답지)]
```java
package chap01;
//양의 정수값의 자릿수를 구하여 나타냄
import java.util.Scanner;

//최종답 -> 나의 답 + 답지 

public class DigitsNo_01_11_2 {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);

		System.out.println("양의 정수값의 자릿수를 구합니다.");
		int a;
		
		//a가 양의 자리 정수가 아니면 다시 정수값받기 
		do {
			System.out.print("정수값 : ");
			a = sc.nextInt();
		} while (a <= 0);

		// 숫자를 문자로 형변환 하기
		String b = Integer.toString(a);

		// 문자열의 길이 구하기
		System.out.println("그 수의 자리는 " + b.length() + "입니다.");

	}

}
```

[1차 답안]
```java
package chap01;
//양의 정수값의 자릿수를 구하여 나타냄

import java.util.Scanner;


public class DigitsNo_01_11 {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);

		System.out.println("양의 정수값의 자릿수를 구합니다.");

		while (true) {
			System.out.print("정수값 : ");
			int a = sc.nextInt();

			if (a <= 0) {
			} else {
				// 숫자를 문자로 형변환 하기
				String b = Integer.toString(a);

				// 문자열의 길이 구하기
				System.out.println("그 수의 자리는 " + b.length() + "입니다.");
				break;
			}
			
		}
	}
}
```

[답지]
```java
package chap01;
import java.util.Scanner;
// 양의 정수값의 자릿수를 구하여 나타냄

class DigitsNo_01_11 {
	public static void main(String[] args) {
		Scanner stdIn = new Scanner(System.in);

		System.out.println("양의 정수값의 자릿수를 구합니다.");

		int n;
		do {
			System.out.print("정수값：");
			n = stdIn.nextInt();
		} while (n <= 0);

		int no = 0; 			// 자릿수
		while (n > 0) {
			n /= 10; 			// n을 10으로 나눔
			no++;
		}

		System.out.println("그 수는 " + no + "자리입니다.");
	}
}
```
