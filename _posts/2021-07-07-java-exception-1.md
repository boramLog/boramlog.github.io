---

title:  "[java] 예외처리 Quiz"
excerpt: "예외처리를 해서 숫자가 아닌 값을 입력했을 때는 다시 입력을  받도록 보완하라. "

categories:
  - JavaQuiz
tags:
  - [Java, Quiz]

toc: true
toc_sticky: true

date: 2021-07-08
last_modified_at: 2021-07-08

---


1~100 사이의 숫자를 맞추는 게임을 실행하던 도중에 숫자가 아닌 영문자를  넣어서 발생한 예외이다.
예외처리를 해서 숫자가 아닌 값을 입력했을 때는 다시 입력을  받도록 보완하라. 

```java
import java.util.Scanner;

public class Exception_quiz {

	public static void main(String[] args) {
		// Scanner sc = new Scanner(System.in);

		
		int answer = (int)(Math.random()*100)+1;
		int input = 0;
		int count = 0;
		
		do {
			count++;
			System.out.println("1과 100사이의 값을 입력하시오 >> ");
			
			try {
			// input = sc.nextInt();
			input = new Scanner(System.in).nextInt();
			
			if(answer > input) {
				System.out.println("더 큰 수 입력하시오");
			} else if (answer < input) {
				System.out.println("더 작은 수 입력하시오");
			} else {
				System.out.println("맞힘");
				System.out.println("시도 횟수는? " + count );
				break;
			}
			
			} catch (Exception e) {
				System.out.println("숫자를 입력하시오");
				System.out.println("================");
				continue;
			}
		}while(true);
	
	}

}

```

숫자가 아닌 문자를 입력하였을 경우 예외가 발생해야하므로 `try-catch문`을 사용하여  예외를 처리해준다.

입력을 받는 부분에서 예외가 발생 할 수 있으므로 입력받는 부분을 `try`를 이용해 감싸주는데 이 때 `Scanner`객체 생성을 새로 해주지 않으면 `input`에는 이미 전에 입력받은 객체의 주소가 들어가 있기 때문에 바로 예외 처리가 되어서 `catch문`에 걸리므로 계속해서 반복하게 된다.

`catch문`에는 모든 예외를 처리해주는 `Exception e`을 사용했다.



