**Tree의 개념**
- 값을 가진 Node와 이를 연결해주는 Edge로 이루어짐
- Root의 노드 번호 = 1
- Node는 0개 이상의 자식 노드를 가지며 이를 부모-자식 관계로 부름

![tree](https://user-images.githubusercontent.com/58163364/189959722-abf6a3aa-3cd3-4ef5-8ae7-449d1925241f.png)


**Tree의 특징**
- 사이클이 존재할 수 X (사이클 O : 그래프 / 사이클 X : 트리)
- 모든 노드는 자료형으로 표현 O
- 루트에서 한 노드로 가는 경로는 유일
- 노드의 개수가 n인 경우, 간선은 n-1

**Tree 순회 방식**
1. 전위 순회 (pre-order) 
- 각 Root를 순차적으로 먼저 방문
- (Root → 왼쪽 자식 → 오른쪽 자식)
- 1 → 2 → 4 → 8 → 9 → 5 → 10 → 11 → 3 → 6 → 13 → 7 → 14

1. 중위 순회 (in-order)
- 왼쪽 하위 트리를 방문 후 Root를 방문
- (왼쪽 자식 → Root → 오른쪽 자식)
- 8 → 4 → 9 → 2 → 10 → 5 → 11 → 1 → 6 → 13 → 3 → 14 → 7

1. 후위 순회 (post-order)
- 왼쪽 하위 트리부터 하위를 모두 방문 후 Root를 방문
- (왼쪽 자식 → 오른쪽 자식 → Root)
- 8 → 9 → 4 → 10 → 11 → 5 → 2 → 13 → 6 → 14 → 7 → 3 → 1

1. 레벨 순회 (level-order)
- Root부터 계층 별로 방문
- 1 → 2 → 3 → 4 → 5 → 6 → 7 → 8 → 9 → 10 → 11 → 13 → 14

사진 출처 : [https://www.geeksforgeeks.org/binary-tree-data-structure/](https://www.geeksforgeeks.org/binary-tree-data-structure/)
