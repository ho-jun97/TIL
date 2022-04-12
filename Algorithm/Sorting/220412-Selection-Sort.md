# Selection Sort (선택 정렬)

- 데이터 배열에서 가장 작은 데이터를 선택하여 앞으로 보내는 정렬(오름차순 정렬)
- 시간복잡도 O(N^2)

## 코드
```java
int[] arr = {1, 6, 5, 4, 8, 10, 2};
for(int i=0; i<10; i++){
	int index = 0;
	int min = Integer.MAX_VALUE;
	for(int j=i; j<10; j++){
		if(min>arr[j]){
			min = arr[j];
			index = j;
		}
	}
	int temp = arr[i];
	arr[i] = arr[index];
	arr[index] = temp;
}
```

## 장점
- 직관적이고 구현도 비교적 간단하다.
- 하나씩 비교하기 때문에 정밀한 비교가 가능하다.
- 교환 횟수는 적은편이다.

## 단점
- 비교하는 횟수가 많다.
- 이미 정렬된 상태에서 자료를 추가하게 되면, 재정렬할 때 최악의 처리 속도를 보인다.


