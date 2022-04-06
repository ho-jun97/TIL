# HashMap
- Map 인터페이스를 구현한 Map 컬렉션이다.
- Map의 성질을 가지고 있다.(Map = Key와 Value으로 구성된 Entry 객체)
- 많은 양의 데이터를 검색하는 데 있어서 뛰어나다.

## HashMap 선언, 값 추가, 값 삭제, 값 출력
- **선언**
	- HashMap<Key, Value> 이름 = new HashMap<>();
	- ex) HashMap<Integer, String> map = new HashMap<>();

- **추가**
	- map.put(1, "apple");
	- map.put(2, "strawberry");
	- map.put(3, "watermelon");

- **삭제**
	- map.remove(1); -> key값 1 제거
	- map.clear(); -> 모든 값 제거

- **출력**
	- map.get(HashMap이름) -> hashmap 전체 출력
	- map.get(key이름) -> key에 해당하는 value 출력
	- entrySet()
		- for (Entry<keyType,valueType> entry : map.entrySet())
			- entry.getKey(), entry.getValue() 가능
	- keySet()
		- for(Integer i : map.keySet())
			- map의 key 값을 i로 표현, map key 크기만큼 반복

## 그외 함수
- containsKey("Key이름") 
	- 해당하는 key이름이 포함되어 있는 확인하는 함수(있으면 true, 없으면 false)


