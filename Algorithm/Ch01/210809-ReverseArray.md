---

title: algorithm
date: 2021-08-09

---
### > 문제
* 베열의 요솟값을 읽어들여 역순으로 정렬합니다. 

---
### > 출력예시 

요솟수 -> 5
```
요솟수 : 5
x[0] : 1
x[1] : 2
x[2] : 3
x[3] : 4
x[4] : 5
요소를 역순으로 정렬했습니다.
x[0] = 5
x[1] = 4
x[2] = 3
x[3] = 2
x[4] = 1
```

### > code

```java
package chap02;

import java.util.Scanner;

//베열의 요솟값을 읽어들여 역순으로 정렬합니다. 
public class ReverseArray {
	//역순으로 정렬하려면,,,? -> 1. 맨 앞과 맨 뒤를 바꾸는 과정을 2. 배열의 길이/2 만큼을 반복 해야한다.
	//두 과정으로 나누어지기 때문에 두개의 메소드로 구성이 된 것이다 
	
	

	//배열 안의 두 요소를 바꾸는 메소드 t를 저장소로 사용한다 
	static void swap(int[] a, int idx1, int idx2 ) {
		int t = a[idx1];
		a[idx1] = a[idx2];
		a[idx2] = t;
	}
	
	//배열을 매개변수로 넣어서 배열의 길이에 따라 swap의 반복횟수를 결정짓는 메소드 
	static void reverse(int[] a) {
		//배열의 길이/2 를 하여 몫만큼 반복한다.(길이가 홀수일시 중간 요소는 바꿔줄 필요가 없음 -> 나머지를 생각하지 않아도 됨) 
		for(int i = 0; i < a.length / 2; i++) {
			//인데스 번호가 늘어가고 줄어들기 때문에 i를 활용함 
			swap(a, i, a.length - 1 - i);
		}
	}
	
	public static void main(String[] args) {
		Scanner std = new Scanner(System.in);
		
		System.out.print("요솟수 : ");
		int num = std.nextInt();
		
		int[] x = new int[num];
		
		for (int i = 0; i < num; i++) {
			System.out.print("x[" + i + "] : ");
			x[i] = std.nextInt();
		}
		
		reverse(x);
		
		System.out.println("요소를 역순으로 정렬했습니다.");
		
		for (int i = 0; i < num; i++) {
			System.out.println("x[" + i + "] = " + x[i]);
		}
		
	}

}
```
