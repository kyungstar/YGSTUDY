# Http 그리고 Http 2.0
- First created By KYG at 2023-01-03

# 저장 방식
- Array 의 element 들은, 인접한 memory 위치에 저장됩니다.
- LinkedList 의 element 들은, memory 어딘가에 저장됩니다.
  - 새로운 element 의 memory 위치 주소는, linked list 의 이전 node 에 저장됩니다.

# 종류
- Array 는 single dimensional, two dimensional, multidimensional 가 있습니다.
- Linked List 는 Linear(Singly), Doubly, Circular linked list 가 있습니다.

# 크기
- Array 의 size는 반드시 array 선언 시점에 지정되어있어야 합니다.
- LinkedList 의 size는 다양할 수 있습니다.
  - node 들이 추가될 때 runtime 시점에서 LinkedList size 는 커질 수 있기 때문입니다.

# 메모리 할당
- Array 에서, Memory 는 Array 가 선언되자 마자 Compile time 에 할당되어집니다.
 이것을 Static Memory Allocation 이라고 부릅니다.
- Stack section 에 memory 할당이 이루어집니다.
- LinkedList 에서, Memory 는 새로운 node 가 추가될 때 runtime 에 할당되어집니다.
- 이것을 Dynamic Memory Allocation 이라고 부릅니다.
- Heap section 에 memory 할당이 이루어집니다.


# 요소 접근
- Array 는 Random Access 를 지원합니다.
- element 들을 index 를 통해 직접적으로 접근할 수 있습니다.
ex) arr[0], arr[1]
- 따라서, 특정 element 에 접근하는 시간 복잡도는 O(1) 입니다.
- LinkedList 는 Sequential Access 를 지원합니다.
- 어떤 element 에 접근할 때, 처음 부터 순차적으로 접근하면서 찾아야 합니다.
- 따라서, 특정 element 에 접근할 때의 시간 복잡도는 O(N) 입니다.

# 삽입 및 삭제
Array
- 인덱스로 접근 후 삽입 및 삭제 O(1) + 전체 배열 요소를 1씩 Shift O(N)

LinkedList
- 삽입하려는 위치 접근 후 삽입 및 삭제 O(N)
- 만약, 맨 앞과 뒤에 삽입 및 삭제한다면 O(1)

# 결론
- 데이터 접근이 주 업무일 경우 → Array
- 데이터 수정이 주 업무일 경우 → Linked List
- 전반적인 내용을 보면, Array 보다 Linked List 의 사용이 훨씬 좋아보이지만,
- 일반적인 알고리즘 문제를 풀 때는 Linked List 보다 Array 가 훨씬 빠르고 편리합니다.
- 대부분의 알고리즘 문제는 메모리 공간의 범위를 파악할 수 있도록, N 의 크기가 주어지기 때문입니다.
- 따라서, 배열의 크기를 MAX 로 초반에 잡는다면, Array 가 훨씬 더 편리하고 빠릅니다.
- Linked List는 요소를 삽입, 삭제할 때마다 메모리의 할당,해제가 일어납니다.
- 이런 작업은 시간복잡도에 포함되지는 않지만, 시스템 콜(System Call)을 사용하는 구문은 시간 소요가 꽤 걸립니다.

참고
- https://medium.com/@audrl1010/linked-list-와-array-차이점-4ba873c2e5f5
- https://woovictory.github.io/2018/12/27/DataStructure-Diff-of-Array-LinkedList/
- https://wooono.tistory.com/281
