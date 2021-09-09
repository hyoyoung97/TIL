---

title: algorithm
date: 2021-09-09

---
### > 문제
* 요솟수가 n인 배열 a에서 key와 같으 요소를 선형검색합니다.

---
### > 출력예시 

```
요솟수 : 5
x[0] :1
x[1] :3
x[2] :5
x[3] :6
x[4] :2
검색할 값 : 6
6는 [3]에 있습니다.
```

---
### > code

```java
package chap03;

import java.util.Scanner;

public class P102_SeqSearch {
	
	static int seqSearch(int[] a, int n, int key) {	//검색할 배열, 배열의 길이, 검색할 수 
		
		for(int i = 0; i < n; i++) {
			if(key == a[i]) {
				return i;
			}
		}
		return -1;
	}
	
	static int seqSearchSen(int[] a, int n, int key) {
		a[n] = key;
		int i = 0;
		
		for(i = 0; i <= n; i++) {
			if(key == a[i]) {
				break;
			}
			
		}
		return i == n ? -1 : i;
	}

	public static void main(String[] args) {
		Scanner stdIn = new Scanner(System.in);
	
		System.out.print("요솟수 : ");
		int num = stdIn.nextInt();
		
		int[] x = new int[num + 1];
		
		for(int i = 0; i < num; i++) {
			System.out.print("x[" + i + "] :");
			x[i] = stdIn.nextInt();
			//System.out.println();
		}
		
		System.out.print("검색할 값 : ");
		int ky = stdIn.nextInt();
		
		int idx = seqSearchSen(x, num, ky);
		
		if(idx == -1) {
			System.out.println("검색하신 요소가 없습니다.");
		} else {
			System.out.println(ky + "는 [" + idx + "]에 있습니다.");
		}

	}

}
```
