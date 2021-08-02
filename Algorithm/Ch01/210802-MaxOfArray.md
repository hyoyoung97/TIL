---

title: algorithm
date: 2021-08-02

---
### > 문제
* 배열 요소의 최댓값을 나타냅니다.(값을 입력 받음)

### > 출력예시
키의 최댓값을 구합니다.   
사람 수 : -> 5  
height[0] : -> 110   
height[1] : -> 120  
height[2] : -> 130  
height[3] : -> 140  
height[4] : -> 150  
최댓값은 150입니다.

```java
package chap02;
//배열 요소의 최댓값을 나타냅니다.(값을 입력 받음)
import java.util.Scanner;

public class MaxOfArray {
	//매개변수가 배열인 메소드 선언 
	static int maxOf(int[] a) {
		
		//비교해주기 위해 기본값 정해주기 
		int max = a[0];
		for (int i = 1; i < a.length; i++) {
			if (a[i] > max) {
				max = a[i];
			}
		}
		return max;
	}

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		System.out.println("키의 최댓값을 구합니다.");
		System.out.print("사람 수 : ");
		
		//명수 -> 배열의 길이 
		int person = sc.nextInt();
		//배열 만들고 변수에 저장(자료형 - 배열)
		int[] height = new int[person];
		
		
		for(int i = 0; i < person; i++) {
			System.out.print("height[" + i + "] : ");
			
			//배열 0 ~ i 에 하나하나 값 저장 
			height[i] = sc.nextInt();
		}
		//만든 배열의 변수 height를 메소드의 매개변수로 넣어주기
		//이 때 메소드의 매개변수의 자료형과 같은 자료형인 배열을넣어주는 것이다 
		System.out.println("최댓값은 " + maxOf(height) + "입니다.");
	}

}
```
