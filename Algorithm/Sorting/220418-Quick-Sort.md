# Quick SOrt
- 발안정한 정렬이다.
- 시간복잡도
	- average : O(NlogN)
	- worst : O(N^2)
- pivot 값을 정하고 pivot 값 기준으로 재배치를 한다.
- pivot 값보다 작은 값은 왼쪽에 큰 값은 오른쪽에 배치한다.

## 코드
```java
// pivot 값을 중간 값으로 설정

void quickSort(int[] arr, int low, int high){
	if( low >= high){
		return;
	}
	int pivot = low + ((high-low)/2); // 중간 값
	int pivotValue= arr[pivot];

	int left = low;
	int right = high;
	while(left <= right){
		while(arr[left] < pivotValue){
			left++;
		}
		while(arr[right] > pivotValue){
			right--;
		}
		if( left <= right){
			int temp = arr[right];
			arr[right] = arr[left];
			arr[left] = temp;
			left++;
			right--;
		}
	}
	quickSort(arr, low, right); // 왼쪽
	quickSort(arr, left, high); // 오른쪽
}
```

## 장점
	- 속도가 빠르다. ( 시간복잡도가 O(NlogN)을 가지는 다른 정렬 알고리즘과 비교했을 때도 가장 빠르다.)
	- 추가 메모리 공간을 필요로 하지 않는다.

## 단점
	- 정렬된 리스트에 대해서는 퀵정렬의 불균형 분할에 의해 오히려 수행시간이 더 많이 걸린다.
