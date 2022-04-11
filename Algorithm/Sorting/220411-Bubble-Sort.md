# Bubble Sort

- 두 인접한 원소를 검사하여 정렬하는 방법
- 시간 복잡도 : O(n^2)

## Bubble Sort Code

>[java] 
```java
int[] list = {10,5,4,6,7};
int len = list.length;
for(int i=len-1; i>0; i--){
	for(int j=0; j<i; j++){
		if(list[j]<list[j+1]){ // 부등호가 < 면 내림차순, >면 오름차순 
			int temp = list[j];
			list[j] = list[j+1];
			list[j+1] = temp;
		}
	}
}
```

## 장점
- 구현이 간단하다.
- 한개씩 비교하기 때문에 정밀한 비교 가능

## 단점
- 비교를 할 때 하나씩 비교해야하기 때문에 시간이 오래 걸린다.

