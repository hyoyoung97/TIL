---

title: algorithm
date: 2021-08-09

---
### > 문제
* 베열의 요솟값을 읽어들여 역순으로 정렬합니다. 

---
### > 출력예시 

- 배열이 같을 때
```
배열 a의 요솟수：3
a[0] : 1
a[1] : 2
a[2] : 3
배열 b의 요솟수：3
b[0] : 1
b[1] : 2
b[2] : 3
배열 a와 b는 같습니다.
```

- 배열이 다를 때
```
배열 a의 요솟수：3
a[0] : 1
a[1] : 2
a[2] : 3
배열 b의 요솟수：3
b[0] : 2
b[1] : 1
b[2] : 3
배열 a와 b는 다릅니다.
```

---
### > code

```java
package chap02;

import java.util.Scanner;

//두 배열이 같은가를 판단 
public class ArrayEqual {
	
	//두 배열이 다를 경우 false를 리턴, 같으면 true를 리턴하는 함수 -> boolean 으로 만든어준다 
	static boolean equals(int[]a, int[]b) {
		
		//두 배열의 길이가 다르면 무조건 false라서 하나하나 비교해줄 필요가 없기 때문에 먼저 길이가 같은지 확인해준다 
		if(a.length != b.length) {	
			return false;
		}
		//두 배열의 값을 하나하나 비교 
		for(int i = 0; i < a.length; i++) {
			if(a[i] != b[i]) {
				return false;
			}
		}
		//위의 테스트를 통과하면 같은 배열이기 때문에 true를 리턴 
		return true;
	}

	public static void main(String[] args) {
		Scanner stdIn = new Scanner(System.in);
		
		//배열 a의 값을 받음 
		System.out.print("배열 a의 요솟수：");
		int na = stdIn.nextInt();
		
		int[] a = new int[na];
		
		for(int i = 0; i < na; i++) {
			System.out.print("a[" + i + "] : ");
			a[i] = stdIn.nextInt();
		}
		
		//배열 b의 값을 받음 
		System.out.print("배열 b의 요솟수：");
		int nb = stdIn.nextInt();
		
		int[] b = new int[nb];
		
		for(int i = 0; i < nb; i++) {
			System.out.print("b[" + i + "] : ");
			b[i] = stdIn.nextInt();
		}
		
		//equals메소드가 true / false 를 반환하는 메소드 이므로 삼항연산자를 사용해서 값을 나타내준다.
		//이렇게 삼항연산자를 사용해주면 if(equals(a, b)==false) <- 이러한 식을 추가로 쓰지 않아도 된다.
		System.out.println("배열 a와 b는 " + (equals(a, b) ? "같습니다." : "다릅니다."));
	}

}
```
