---

title: algorithm
date: 2021-07-19

---
### > 문제
* //1, 2, …, n의 합을 구합니다  (식1 + 2 + … + n = 999라고 출력함)

### > 출력예시
```
1부터 n까지의 합을 구합니다.
n의 값:5
1+2+3+4+5=15
```

```java
package chap01;

import java.util.Scanner;

//1, 2, …, n의 합을 구합니다  (식1 + 2 + … + n = 999라고 출력함)

public class SumForEx_01_07 {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);

		System.out.println("1부터 n까지의 합을 구합니다.");

		System.out.print("n의 값:");
		int n = sc.nextInt();

		int sum = 0;

		// i + 출력 -> i가 n이 될 때 만 + 붙여주지 않는다 -> = sum 출력하기
		for (int i = 1; i <= n; i++) {
			if (i < n) {
				System.out.print(i + "+");
			} else {
				System.out.print(i);
			}
			sum += i;
		}
		System.out.print("=" + sum);

	}

}
```
