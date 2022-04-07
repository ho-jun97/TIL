# HashSet
- Set 인터페이스에서 지원하는 구현 클래스이다.
- 중복을 허용하지 않음
- null 요소 허용됨

## HashSet 변수 선언 및 값 추가, 값 삭제, 출력
	- **선언**
		- HashSet<Integer> set(이름) = new HashSet<>();
		- (Integer 자리에 String, Long 가능)
	
	- **추가**
		- set.add(값)
	
	- **삭제**
		- set.remove(값) : 값에 해당하는 데이터 삭제
		- set.clear() : 데이터 모두 삭제(초기화)
	
	- **출력**
		- System.out.println(set) : [value1, value2, value3, ..] 전체 출력
		 
		```java
			Iterator iter = set.iterator();
			while(iter.hasNext()){
				System.out.println(iter.next());
			}
		```
		> hashNext() -> 다음에 올 수 있는 값이 있는지 확인
		while(iter.hasNext()) -> 다음 데이터가 없을 때까지 반복
		iter.next() -> 다음 데이터를 가르킴
## 그외 메소드
- set.size()
	- set의 크기를 알려주는 메서드

- set.contains(value)
	- set에 value값이 있으면 true, 없으면 false


