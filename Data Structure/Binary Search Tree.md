**Binary Search Tree 목적** 

- 이진 탐색 + 연결 리스트 → 효율적인 탐색 능력 & 자료의 삭제 삽입 가능
    - 이진 탐색 : 탐색 시간복잡도 O(logN), 삽입 삭제 불가능
    - 연결 리스트 : 탐색 시간복잡도 O(N), 삽입 삭제 시간복잡도 O(1)

**Binary Search Tree 특징**

- 각 노드의 자식이 2개 이하
- 왼쪽 자식 < 부모 < 오른쪽 자식
- 중복된 노드가 없어야 함 (검색 목적의 자료구조이므로 중복이 있는 경우 트리에 삽입하여 노드로 인해 속도를 느리게 만드는 것 보다 노드가 count값을 가지게 하여 처리하는 것이 효율적)
- 중위 순회 (in-order) 방식을 사용해 정렬된 순서로 읽음 (원쪽 - root - 오른쪽)

**Binary Search Tree  핵심 연산**

- 검색
- 삽입
- 삭제
- 트리 생성
- 트리 삭제
    - 자식이 없는 노드 → 그냥 삭제
    - 자식이 1개인 노드 → 지워진 노드에 자식을 올리기
    - 자식이 2개인 노드 → 오른쪽 자식 노드에서 가장 작은 값 or 왼쪽 자식 노드에서 가장 큰 값 올리기

**Binary Search Tree 특징 시간 복잡도 (N = 노드 개수)**

- 균등 트리 : O(logN)
- 편향 트리 : O(N) → 트리를 사용할 이유가 없으므로 AVL Tree, RedBlack Tree 사용
