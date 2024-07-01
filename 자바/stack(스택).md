## 스택클래스
    Stack<Integer> s = new Stack<Integer>();
    Stack<String> s1 = new Stack<>();
  위에 코드는 정수형 Integer인 정수형 스택, 문자형 String 인 문자형 스택클래스를 만들수 있다.

## 값넣기
    s.push(1);
    s.push(2);
    s.push(3);
    s.push(4);
  push 함수 또는 add 함수을 사용하여 스택에 값을 넣는다.

## 값제거
    s.pop(1);
    s.pop(2);
    s.pop(3);
    s.pop(4);
   pop 함수로 스택에 들어있는 값을 제거한다.
   
## 비어있는지 확인
    public boolean isEmpty() {
       return top == null;
     }
   boolean은 참인 true와 거짓인 false을 판별하고 isEmpty인 empty 함수을 사용하여 값이 비어있는지를 판별하는 코드이다.

## peek 함수
    System.out.println(s.peek());
  peek으로 값에서 가장 위에 있는 값을 출력하라는 코드이다.

# 실행화면 
  ![스크린샷 2024-07-01 124230](https://github.com/asertty/21111/assets/127906148/34613cfa-bee1-4643-a232-2fa6af169a49)
