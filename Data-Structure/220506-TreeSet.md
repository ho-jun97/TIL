# TreeSet
- Set 인터페이스를 구현한 클래스
- 중복해서 저장할 수 없다.
- 저장 순서가 유지되지 않는다.
- 이진 탐색 트리 구조로 이루어져 있다.

## TreeSet 선언, 추가, 삭제, 그 외 메서드
```java
// 선언
TreeSet<Integer> set = new TreeSet<>(); 
```
- Integer 자리에 Long, String과 같은 타입들이 들어갈 수 있음.

## 추가
```java
set.add(1);
set.add(2);
set.add(9);
```

## 삭제
```java
set.remove(1); // 값 1 제거
set.clear(); //  set 초기화(모든 값 제거)
```

## 그 외의 메서드
```java
set.size(); // set의 크기 반환
int value = 1;
set.first(); // 최소값 출력
set.last(); // 최대값 출력
set.higher(value); // value 값보다 큰 데이터중 최소값 반환 없으면 null 반환
set.lower(value); // value 값보다 작은 데이터중 최대값 반환 없으면 null 반

```

