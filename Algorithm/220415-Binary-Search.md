# 이진 탐색 
- 오름차순 정렬되어 있는 리스트 내에서 특정 값의 인덱스 혹은 값을 찾는 알고리즘
- 시간복잡도 O(logN)
- 정렬된 리스트에서만 사용 가능

## 코드
```java
// binary search로 해당하는 인덱스 값 구하는 코드
public binarySearch(int[] arr, int target){
	int start = 0;
	int end = arr.length - 1;

	int mid;
	while(start <= end){
		mid = start + ((start - end) / 2); 
	
		if(arr[mid] == target){
			return mid;
		}

		if(arr[mid] < target){
			start = mid + 1;
		} else{
			end = mid - 1;
		}
	}
	
}
```
## 코드 설명
> mid = start + ((start-end)/2) 한 이유
- start + end 값이 int 범위를 넘어갈 수도 있기 때문에 (start+end)/2 를 하지 않음.
- int 범위를 넘어가지 않는다는 조건이 있으면 (start+end)/2 가능

- target이 중간값보다 크면 오른쪽에 위치해 있기 때문에 start만 바꾸면 됨
- tratget이 중간값도다 작으면 왼쪽에 위치해 있기 때문에 end만 바꾸면 됨

