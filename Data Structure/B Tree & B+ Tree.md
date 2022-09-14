**이진 트리는** 하나의 부모가 두 개의 자식밖에 가질 수 없고 균형이 맞지 않으면 검색 효율이 선형검색 급으로 떨어진다. 하지만 균형이 맞다면 검색, 삽입, 삭제 모두 O(logN)으로 처리할 수 있다.

****B Tree**** 

![BTree](https://user-images.githubusercontent.com/58163364/190071249-7a7d9ecb-57ae-4d1d-a3cf-c3a9dcc691a1.png)

- 데이터베이스, 파일 시스템에서 주로 사용되는 트리 자료구조
    - 대량의 데이터를 처리할 때 하나의 노드에 많은 데이터를 가질 수 있음.
    - 데이터베이스 시스템의 인덱스 저장 방법으로 사용됨
- 이진 트리를 확장해 더 많은 수의 자식을 가실 수 있도록 일반화 시킨 것
- 트리의 균형을 자동으로 맞춤

****B Tree 규칙****

- N = 노드의 자료수, N+1 = 노드의 자식 수
- 각 노드의 자료는 정렬된 상태여야 함
- root 노드는 적어도 2개 이상의 자식을 가져야 함
- root 노드를 제외한 모든 노드는 적어도 M/2개의 자료를 가져야 함
- 외부 노드로 가는 경로의 길이는 모두 같음
- 입력 자료는 중복 X

****B+ Tree**** 

![B+Tree](https://user-images.githubusercontent.com/58163364/190071296-c506d737-9ec9-440b-8a88-f99addc2743e.jpg)


- B Tree + 데이터의 빠른 접근을 위한 인덱스 역할만 하는 비단말 노드
- index + leaf노드로 구성된 순차 데이터
- index의 key값은 leaf에 있는 key값을 직접 찾는데 사용
- 장점
    - 블럭 사이즈를 더 많이 이용 할 수 있음
    - leaf 노드끼리 연결 리스트로 되어 있어 범위 탐색에 유리
- 단점
    - B Tree는 최상 케이스의 경우 Root에서 끝날 수 있지만, B+ Tree는 무조건 leaf 노드까지 내려가봐야 한다.

**B Tree & B+ Tree**

- **B Tree**
    - 각 노드에 데이터가 저장
    - 각 노드에 key data 모두 들어갈 수 O
    - data는 disk block으로 포인터가 될 수 O
- **B+ Tree**
    - index 노드와 leaf 노드로 분리되어 저장
    - 각 노드에 key만 들어감
    - data는 모두 leaf 노드에만 존재
    - add, delete가 모두 leaf 노드에서만 이루어짐

사진 출처 : [https://www.geeksforgeeks.org/difference-between-b-tree-and-b-tree/](https://www.geeksforgeeks.org/difference-between-b-tree-and-b-tree/)
