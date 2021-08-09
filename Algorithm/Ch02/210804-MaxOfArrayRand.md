---

title: algorithm
date: 2021-08-04

---
### > 문제
* 배열 요소의 최댓값을 나타냅니다.(값을 난수로 생성)

키의 최댓값을 구합니다.  
사람 수 : -> 5  
heght[0] : 189  
heght[1] : 103  
heght[2] : 113  
heght[3] : 118  
heght[4] : 149  
최댓값은 189입니다.

### > code

```java
package chap02;

import java.util.Random;
import java.util.Scanner;

public class MaxOfArrayRand {
	
	static int max(int[] a) {
		int max = a[0];
		for(int i = 0; i < a.length; i++) {
			if(a[i] > max) {
				max = a[i];
			}
		}
		return max;
	}

	public static void main(String[] args) {
		
		//난수 객체 생성하기 
		Random rand = new Random();
		Scanner stdIn = new Scanner(System.in);
		
		System.out.println("키의 최댓값을 구합니다.");
		
		System.out.println("사람 수 : ");
		int num = stdIn.nextInt();
		
		//입력받은 사람 수만큼의 길이를 가진 배열 선언하기 
		int[] height = new int[num];
		
		for (int i = 0; i < num; i++) {
			//난수로,, 직접 입력하지 않아도 자동으로 입력해주기 때문에
			//배열에 먼저 집어 넣은 후에 
			//nextInt(90) 은 0을 포함 90개의 정수. 즉, 0~89 까지이다 (인덱스와 비슷)
			height[i] = 100 + rand.nextInt(90);
			
			//height[i]은 위에서 이미 입력이 되었고, 입력된 난수를 출력해준다
			System.out.println("heght[" + i + "] : " + height[i]);
		}
		System.out.println("최댓값은 " + max(height) + "입니다.");
 		
	}

}
```
