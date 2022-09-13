**Heap의 개념** 

- 우선순위 큐(데이터가 우선순위를 가지며 순위가 높을수록 먼저 나가는 큐(FIFO)) 를 위해 만들어진 자료구조
    - 우선순위 큐 구현 방법 : 배열, 연결리스트, 힙(가장 효율적인 구현)

**Heap의 특징** 

- 완전 이진 트리 (최대값, 최소값을 빠르게 찾아내도록 만들어진 자료구조)
- 반정렬 상태
- 힙 트리(중복 값 허용) / 이진 탐색 트리(중복 값 허용 X)

**Heap의 종류**

- 최대 힙 (max heap) : 부모 노드의 키 값 ≥ 자식 노드의 키 값. 완전 이진 트리
- 최소 힙 (min heap) : 부모 노드의 키 값 ≤ 자식 노드의 키 값. 완전 이진 트리

**Heap의 구현**

- 배열을 통해 구현
- 쉬운 구현을 위해 0번 index는 사용 X
- 삽입이 있더라도 특정 위치의 노드 번호는 변하지 X (ex. root(1)의 오른쪽 노드 번호는 항상 3)
    - 부모 index = (자식 index) / 2
    - 왼쪽 자식 index = (부모 index) * 2
    - 오른쪽 자식 index = (부모 index) * 2 + 1
    

**Heap의 삽입  O(logn)**

1. 새로운 노드를 힙의 마지막 노드에 삽입
2. Heap의 종류(max, min)에 따라 부모 노드들과 교환
- 반복문을 통해 마지막 노드 ~ root, 현재 노드(자식) vs 부모 노드 비교 후 교환

**Heap의 삭제  O(logn)**

1. 루트 노드 삭제
2. 비어있는 루트를 힙의 마지막 노드로 채움
3. Heap의 종류(max, min)에 따라 자식 노드들과 교환
- 반복문을 통해 root~마지막 부모 노드,  현재 노드(부모) vs 자식 노드(왼 / 오) 비교 후 교환