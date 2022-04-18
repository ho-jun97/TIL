# Merge Sort
- 분할 정복
- 하나의 문제를 동일한 유형의 작은 문제로 분할을 한 뒤 작은 문제들을 조합하여 큰 문제를 해결하는 알고리즘
- 시간복잡도 : O(NlogN)

## 코드
```java
// 분할
void mergeSort(int[] arr, int low, int high){
	if(low >= high){
		return;
	}
	
	int mid = low + ((high-low)/2);
	mergeSort(arr, low, mid);
	mergeSort(arr, mid+1, high);
	
	merge(arr, low, mid, high)
}

// 합
void merge(int[] arr, int low, int mid, int high){
	int[] temp = new int[high-low+1];
	int idx = 0;

	int left = low; // 분할된 왼쪽 시작 인덱스
	int right = mid + 1; // 분할된 오른쪽 시작 인덱스
	while(left <=mid && right <= high){
		if(arr[left] <= arr[right]){
			temp[idx] = arr[left];
			left++;
		} else{
			temp[idx] = arr[right];
			right++;
		}
		idx++;
	}
	while(left <= mid){ // 왼쪽에 남아 있는 데이터가 있을 수 있는 경우를 대비
		temp[idx] = arr[left];
		idx++;
		left++;
	}
	while(right <= high){ // 오른쪽에 남아 있는 데이터가 있을 수 잇는 경우를 대비
		temp[idx] = arr[right];
		idx++;
		right++;
	}
	for(int i=low; i<=high; i++){
		arr[i] = temp[i - low];
	}
}병

```

## 장점
	- 안정적인 정렬이다.
	- 데이터 분포에 따른 시간 영향을 덜 받는다. 왜냐하면 똑같은 크기로 나누어 정렬되기 때문이다.

## 단점
	- 크기가 큰 경우 많은 이동횟수가 필요하기 때문에 시간 낭비가 될 수 있다.
