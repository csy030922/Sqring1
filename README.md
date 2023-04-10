# Spring1
> Spring1 스터디
--------

## Member
> 조현호 윤혜정 이가영 최서영

---

## Date
> 매주 화요일 오전 10시

# 함수(메서드)?
> 자바는 다른 언어와 달리 함수라는 것이 따로 존재하지는 않고 클래스내에! 존재한다.
> 이러한 클래스 내의 함수를 메서드라고 부른다.
> 하나의 작업단위를 이루는 코드를 한 묶음으로 만들어서 재사용할 수 있도록 만든 것
> 어떠한 값이 넘겨지거나 아무 값도 넘겨지지 않았을 때 작업을 수행한 후 반환하거나 혹은 반환하지 않고 종료

## 자바 메서드의 구조
‘’’java
리턴자료형 메서드명(입력자료형1 매개변수1, 입력자료형2 매개변수2, …){
	…
	return 리턴값; // 리턴자료형이 void인 경우 return 문이 필요없다.
}
‘’’

1. 입력 O, 출력 O
'''java
static int mod (int a, int b){
  int result = a % b;
  return result;
}
'''

2. 입력 O, 출력(반환) X
'''java
static void printNum(int a){ // 여기서 a는 매개변수!
  System.out.println(a);
}
'''

3. 입력 X, 출력(반환) O
'''java
static String greeting(){
  return "Hello!";
}
'''

4. 입력 X, 출력(반환) X
'''java
static void greeting_2(){
  System.out.println("Hello!);
}
'''

5. 자료구조 형태 (리스트ver.)
'''java
static void printListElements(ArrayList List){
  for (int i = 0; i < List.size(); i++){
    System.out.println(List.get(i));
  }
}
'''

- 메인함수
'''java
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
'''

## 매개변수와 인수

> 매개변수는 ‘Parameter’라고 하며 메서드에 전달된 값을 저장하는 변수를 말한다.

> 인수는 ‘Arguments’라고 하며 메서드에 전달하는 값을 말한다.
