# 자바의 기본형 데이터와 참조형 데이터

## 1. 기본형 데이터 (Primitive type)
- 자바에서 가장 단순한 데이터 타입  
- 값 자체를 저장함  
- 스택(stack) 메모리에 직접 값이 들어감  
- 총 8가지:  
  - 정수형: `byte`, `short`, `int`, `long`  
  - 실수형: `float`, `double`  
  - 문자형: `char`  
  - 논리형: `boolean`  

### 예시
```java
public class PrimitiveExample {
    public static void main(String[] args) {
        int a = 10;
        int b = a;   // 값 자체가 복사됨

        a = 20;      // a를 바꿔도 b는 그대로
        System.out.println("a = " + a); // 20
        System.out.println("b = " + b); // 10
    }
}
```
👉 기본형은 **값만 복사**되므로 변수 간에 독립적이다.

---

## 2. 참조형 데이터 (Reference type)
- 기본형을 제외한 모든 타입  
  - 배열, 클래스, 인터페이스, 열거형, 컬렉션 등  
- 변수에는 값 자체가 아니라 **객체가 저장된 위치(주소)**가 들어감  
- 여러 변수가 같은 객체를 참조할 수 있다  

### 예시 (배열)
```java
public class ReferenceExample {
    public static void main(String[] args) {
        int[] arr1 = {1, 2, 3};
        int[] arr2 = arr1;   // arr1의 참조(주소)를 복사 → 얕은 복사

        arr1[0] = 99;        // arr1[0] 수정
        System.out.println(arr2[0]); // 99 (같은 배열을 가리킴)
    }
}
```
👉 참조형은 **주소를 복사**하므로 원본과 복사본이 같은 객체를 공유한다.

---

## 3. 그림 비유
- **기본형**: 변수 = 값  
  - 예: 종이에 숫자 10 적어둔 것  
- **참조형**: 변수 = 화살표  
  - 예: 박스 어디에 있는지 알려주는 주소  
  - 박스 안의 내용물이 바뀌면 같은 박스를 가리키는 다른 화살표에서도 바뀐다  

---

## 4. 요약
- **기본형 (Primitive)**  
  - 값 자체를 저장  
  - 변수끼리 독립적  
- **참조형 (Reference)**  
  - 객체의 주소를 저장  
  - 같은 객체를 여러 변수가 공유할 수 있음  
