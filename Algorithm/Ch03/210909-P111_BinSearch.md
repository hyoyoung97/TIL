---

title: algorithm
date: 2021-09-09

---
### > 문제
* 이진검색 - 요솟수가 n인 배열 a에서 key와 같은 요소를 이진 검색합니다.

---
### > 출력예시 

```
요솟수 : 5
오름차순으로 입력하세요.
x[0] : 1
x[1] : 2
x[2] : 3
x[3] : 4
x[4] : 5
검색할 값을 입력하세요.
4
4는 x[3]에 있습니다.
```

---
### > code

```java
package chap03;

import java.util.Scanner;
//이진검색!
public class. P111_BinSearch {
	//요솟수가 n인 배열 a에서 key와 같은 요소를 이진 검색합니다.
	static int binSearch(int[] a, int n, int key) {
		int pl = 0;
		int pr = n - 1;
		
		do {
		int pc = (pl + pr)/2;
		if(a[pc] == key) {
			return pc;	//검색성공!!
		} else if(a[pc] > key) {
			pr = pc - 1;
		} else {
			pl = pc + 1;
		}
		} while(pl <= pr);
		
		return -1;
	}

	public static void main(String[] args) {
		Scanner stdIn = new Scanner(System.in);
		
		System.out.print("요솟수 : ");
		int num = stdIn.nextInt();
		
		int[] x = new int[num];
		
		System.out.println("오름차순으로 입력하세요.");
	
		System.out.print("x[0] : ");
		x[0] = stdIn.nextInt();
		
		for(int i = 1; i < num; i++) {
			do {
			System.out.print("x[" + i + "] : ");
			x[i] = stdIn.nextInt();
			} while (x[i] < x[i-1]);
		}
		
		System.out.println("검색할 값을 입력하세요.");
		int ky = stdIn.nextInt();
		
		int idx = binSearch(x, num, ky);
		
		if(idx == -1) {
			System.out.println("그 값의 요소가 없습니다.");
		} else {
			System.out.println(ky + "는 x[" + idx + "]에 있습니다.");
		}

		
	}

}
```
