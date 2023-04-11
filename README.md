# Spring1
> Spring1 스터디
--------

## Member
> 조현호 윤혜정 이가영 최서영

---

## Date
> 매주 화요일 오전 10시

---

# Chapter 8
  ## 배열
  - 동일한 자료형(Data Type)의 데이터를 연속된 공간에 저장
  - 자료형[] 변수 = {데이터1, 데이터2, 데이터3, ... };
  - 한 번 생성된 배열은 길이 고정

  ### 배열 선언 1
``` java
  int[] intArr; // int형 배열
  char[] charArr; // char형 배열
  String[] days = { "월", "화", "수", "목", "금", "토", "일" };
```

  ### 배열 선언 2
``` java
  Type[] arr = new Type[length];
```

  ### 반복문에서 활용
``` java
for(int i=0; i < days.length, i++)
  System.out.println(days[i]);

for(int i : days)
  System.out.println(i);
```
---

  ## 리스트
  - 순서 구분하며 중복을 허용한다.
  - Vetor, ArrayList, LinkedList 가 있으며 이 중  ArrayList가 가장 활용성이 좋다.
  - 리스트의 경우 자료를 넣는 만큼 자동적으로 크기 확장

  ### 선언부
  ``` java
  import java.util.ArrayList;
  ArrayList list = new ArrayList(리스트의 길이) //객체이기 때문에 자료형에 관계없이 모두 저장 가능
  ```

  ### 리스트 함수
  ``` java
  list.add(data) // data 삽입
  list.get(data) // 리스트 내의 data를 가져옴
  list.size() // list의 길이 리턴
  list.remove(data) // data 삭제
  ```
  ### 활용
  ``` java
  ArrayList<자료형> list = new ArrayList(list.length) // => 지정한 자료형만 저장 가능
  list.size(); list.get(i)
  for(int i=0;i<list.size();i++{
    System.out.println(list.get(i));
  ```

---

## 맵
- 해싱(Hashing)된 맵(Map)
- 키-값의 쌍을 요소로 가지는 데이터의 집합, 순서를 구분하지 않음
- 키값은 중복불가, 값은 중복 가능
- (key, value)를 묶어 item이라고 말함

### 해쉬맵 선언
``` java
import java.util.HashMap;

HashMap map = new HashMap(); // 
map.put("age",30);
map.put("mbti", "INFP");

System.out.println(map.get("age"));
```

### 해쉬맵 함수
``` java
  map.put(key, value) // data 삽입
  map.get(key) // key에 해당하는 value값
  map.containsKey(key) // key가 있는지 조사 후 참, 거짓 리턴
  map.remove(key) // key값에 해당하는 item 삭제 후 value값 리턴
```

### sorting map
- LinkedHashMap은 입력된 순서대로 데이터를 저장
- TreeMap은 입력된 key의 오름차순 순서로 데이터를 저장

---

# Chapter9
## 함수(메서드)?
> 자바는 다른 언어와 달리 함수라는 것이 따로 존재하지는 않고 클래스내에! 존재한다.
> 이러한 클래스 내의 함수를 메서드라고 부른다.
> 하나의 작업단위를 이루는 코드를 한 묶음으로 만들어서 재사용할 수 있도록 만든 것
> 어떠한 값이 넘겨지거나 아무 값도 넘겨지지 않았을 때 작업을 수행한 후 반환하거나 혹은 반환하지 않고 종료

### 자바 메서드의 구조
```java
리턴자료형 메서드명(입력자료형1 매개변수1, 입력자료형2 매개변수2, …){
	…
	return 리턴값; // 리턴자료형이 void인 경우 return 문이 필요없다.
}
```

1. 입력 O, 출력 O
```java
static int mod (int a, int b){
  int result = a % b;
  return result;
}
```

2. 입력 O, 출력(반환) X
```java
static void printNum(int a){ // 여기서 a는 매개변수!
  System.out.println(a);
}
```

3. 입력 X, 출력(반환) O
```java
static String greeting(){
  return "Hello!";
}
```

4. 입력 X, 출력(반환) X
```java
static void greeting_2(){
  System.out.println("Hello!);
}
```

5. 자료구조 형태 (리스트ver.)
```java
static void printListElements(ArrayList List){
  for (int i = 0; i < List.size(); i++){
    System.out.println(List.get(i));
  }
}
```

- 메인함수
```java
public static void main(String[] args){

  int mod_result = mod(3, 2); // 여기서 3, 2는 인수!
  Sysyem.out.println(mod_result); // 1
  
  printNum(10); // 10
  
  String str = greeting();
  Sysyem.out.println(str); //Hello -> 얘는 str에 반환값이 저장되어있음
  
  greeting_2(); // Hello -> 얘는 저장되지 않고 그냥 출력 중..
  
  ArrayList list_1 = new ArrayList<>();
  list_1.add(10);
  list_1.add(100);
  
  printListElements(list_1); // 10 \n 100

}
```

### 매개변수와 인수
> 매개변수는 ‘Parameter’라고 하며 메서드에 전달된 값을 저장하는 변수를 말한다.
> 인수는 ‘Arguments’라고 하며 메서드에 전달하는 값을 말한다.

---