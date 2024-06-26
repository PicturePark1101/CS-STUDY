## 🙌 0224 -> 알고리즘 예상 질문 Q&A


### 스택과 큐

1. 스택과 큐의 차이점
   스택은 Fisrt In Last Out 이고 큐는 First In First Out 이다.
2. 스택과 큐의 활용 예시
* 스택 : 감자칩 꺼내 먹는거 생각해라.
*  큐 : 놀이 공원이나 매표소에서 줄서는거
3. LinkedList를 사용하여 자료구조를 만드려 할때, 스택과 큐중 무엇이 더 적합한가?
   스택 또는 큐의 선택은 사용 목적에 따라 다름.
* 스택: LIFO 특성이 필요한 경우
* 큐: FIFO 특성이 필요한 경우

4. 자바 언어를 사용하여 스택과 큐 구현 시 linkedlist와 배열 방법이 있다. 차이점은?
* LinkedList: 동적 크기 조절 가능, 중간 삽입/삭제가 빠름.
* 배열: 고정 크기, 접근 시간이 빠름.
5. 큐로 스택을 구현하는 방법
* 큐에 요소를 계속 enqueue하다가, 가장 최근에 들어온 요소를 제외한 나머지를 계속 dequeue하여 다시 enqueue.
6. 스택으로 큐를 구현하는 방법
* 두 개의 스택을 사용. Enqueue 시에는 하나의 스택에 push, Dequeue 시에는 다른 스택에서 pop.
7. 스택을 단순히 뒤집으면 되는데, 굳이 스택 2개를 사용하는 이유
* 뒤집기 위해 추가적인 공간을 사용하지 않고도 스택의 특성을 유지하기 위함.
8. 스택과 큐의 시간 복잡도
* 스택과 큐 모두 삽입(enqueue), 삭제(dequeue) 연산이 O(1)이며, 탐색이 O(n).
  스택과 큐의 두 가지 특성을 전부 사용하고 싶을 때는 무엇을 사용하면 좋을까요?
* 덱(Deque): 양쪽 끝에서 삽입과 삭제가 모두 가능한 자료구조.
9. 자바 라이브러리에서 덱(Deque) 인터페이스는 LinkedList로 구체화되는데 List 인터페이스가 아닌 덱(Deque)에 의존하는 이유는 무엇인지 설명해주세요.
* 덱은 큐와 스택의 기능을 모두 제공하므로, 큐 또는 스택의 특정 구현과 상관없이 양쪽 끝에서의 조작을 보장하기 위함. List는 순서와 관련이 있지만, 양 끝 조작에 대한 보장은 없음.

### 레드블랙트리

1 . 레드 블랙 트리에 대해 설명해주세요.

* 레드-블랙 트리는 이진 탐색 트리의 일종으로, 각 노드에 레드 또는 블랙의 색을 지닌 트리입니다. 이 트리는 효율적인 검색, 삽입, 삭제 연산을 제공하면서도 트리의 균형을 유지합니다.

2. 레드 블랙 트리의 특징 3가지
* 노드 색깔: 각 노드는 레드 또는 블랙 중 하나의 색을 가짐.
* 루트와 리프 조건: 루트와 리프(끝 노드)는 블랙이며, 리프는 추가적인 특별한 노드로 취급되어 NIL 노드로 표현됨.
* 레드 노드 조건: 레드 노드는 두 개의 연속된 레드 노드가 나타나지 않아야 함.

3. 힙과 레드 블랙 트리의 차이점

* 힙(Heap): 우선순위 큐를 구현하기 위한 자료구조로, 부모 노드의 값이 항상 자식 노드의 값보다 작거나 같음.
  레드-블랙 트리: 이진 탐색 트리의 일종으로, 노드의 색깔에 규칙이 있어 트리의 균형을 유지함.

4. 레드 블랙 트리를 사용하는 이유

* 검색, 삽입, 삭제 등의 연산에서 효율적인 성능을 제공하면서도 트리의 높이를 일정하게 유지하여 최악의 경우에도 O(log n)의 성능을 유지할 수 있음.

5. 레드 블랙트리의 5가지 속성

각 노드는 레드 또는 블랙이다.
루트 노드는 블랙이다.
각 리프(NIL) 노드는 블랙이다.
레드 노드의 두 자식은 항상 블랙이다.
어떤 노드에서 그 자손 리프 노드까지의 모든 경로에는 리프 노드를 제외하면 모두 같은 개수의 블랙 노드가 있다.

6. 삭제되는 색이 무엇인지, 그리고 그 경우 두가지

삭제되는 색: 삭제되는 노드의 색이 블랙이다.
삭제 경우 두 가지:
삭제된 노드의 위치에 있는 블랙 노드가 하나 감소하는 경우.
삭제된 노드의 위치에 있는 레드 노드거나, 대체된 노드(삭제된 노드의 후계자)가 레드인 경우.

7. 응용 사례, 사용처:

데이터베이스의 인덱스 구현
파일 시스템의 파일 할당
C++ STL(map, set) 등의 구현
자바의 TreeMap, TreeSet 등의 자료구조에 사용됨.


### 힙

1. 큐와 우선순위 큐 비교

* 큐(Queue): 선입선출(FIFO)의 구조를 가지며, 일반적으로 삽입과 삭제가 O(1) 시간복잡도를 갖음.
  우선순위 큐(Priority Queue): 각 요소는 우선순위를 가지며, 높은 우선순위를 가진 요소가 낮은 우선순위를 가진 요소보다 먼저 처리됨. 일반적으로 힙(heap)을 기반으로 구현되며, 삽입과 삭제 연산에 O(log n)의 시간복잡도를 가짐.

2. 우선순위 큐와 비슷한 자료구조는 어떤게 있을까요?

* 이진 힙(Binary Heap): 우선순위 큐를 구현하는 자료구조로, 최소 힙 또는 최대 힙으로 구현될 수 있음.

3. 힙 활용예시 설명해주세요.

* Task Scheduling: 우선순위가 높은 작업이 먼저 처리되어야 하는 상황에서 사용됨.
* Dijkstra's Algorithm: 최소 비용으로 경로를 찾는 알고리즘에서 우선순위 큐를 활용.

4. 힙 구조에 대해서 설명해주세요.

* 힙은 완전 이진 트리(Complete Binary Tree) 구조를 가짐.
* 최소 힙(Min Heap): 부모 노드의 값이 자식 노드의 값보다 작거나 같음.
* 최대 힙(Max Heap): 부모 노드의 값이 자식 노드의 값보다 크거나 같음.

5. 힙에 대해서 간단하게 설명해주세요.

* 삽입: 새로운 요소를 힙의 맨 끝에 추가하고, 적절한 위치로 옮겨가며 힙 속성을 만족시킴.
* 시간복잡도: O(log n), 트리의 높이에 비례.

6. 힙에 대해서 삽입에 대한 설명과 시간복잡도

* 삽입: 새로운 요소를 힙의 맨 끝에 추가하고, 적절한 위치로 옮겨가며 힙 속성을 만족시킴.
  시간복잡도: O(log n), 트리의 높이에 비례.

7. 힙의 삭제 과정에 대해서 간단하게 설명해주세요.

* 삭제(Extract Min/Max): 최소 힙에서는 루트(최솟값)를 삭제하며, 최대 힙에서는 루트(최댓값)를 삭제.
  삭제 후에는 힙의 끝 노드를 루트로 이동시키고, 적절한 위치로 옮겨가며 힙 속성을 만족시킴.
  시간복잡도: O(log n), 트리의 높이에 비례.

8. 힙과 레드블랙트리를 비교했을 때 장단점

힙:
장점: 삽입과 삭제가 빠르며, 최솟값 또는 최댓값을 빠르게 찾을 수 있음.

단점: 정렬된 순서가 아니기 때문에 중간값을 빠르게 찾을 수 없음.

레드-블랙 트리:

장점: 정렬된 순서를 유지하며, 범위 검색이 빠름.

단점: 삽입과 삭제에 대해 힙보다는 느림.

### 정렬

1. 퀵정렬

* 퀵정렬은 분할 정복(Divide and Conquer) 방법을 사용한 정렬 알고리즘 중 하나.
  주어진 배열을 기준 원소(pivot)를 선택하고, 기준보다 작은 요소는 왼쪽, 큰 요소는 오른쪽으로 분할하여 재귀적으로 정렬 진행.

2. 퀵정렬의 시간복잡도에 대해 설명해주세요.

* 평균 시간복잡도: O(n log n)

최악 시간복잡도: O(n^2)

최선 시간복잡도: O(n log n)

3. 최악의 시간복잡도를 가지는 경우 해결방안은 무엇인가요?

* 해결방안: 피벗을 정할 때 랜덤하게 선택하거나, 중앙값을 선택하여 피벗의 위치를 불규칙하게 만듦.

4. 어떤 경우에 최악의 경우를 가지는 경우는 무엇인가요?

* 배열이 이미 정렬되어 있거나, 역으로 정렬되어 있는 경우.

5. 퀵 정렬의 장단점

장점:

평균적으로 빠른 정렬 알고리즘.

추가 메모리 공간이 필요하지 않음(인플레이스 정렬).

단점:

최악의 경우 성능이 나빠질 수 있음.

불안정 정렬.

6. 퀵정렬의 최악의 경우는 O(n^2)인데, 이문제를 해결하는 방법이 있을까요

* 방법: 랜덤한 피벗 선택이나 중앙값을 피벗으로 선택하여 최악의 경우를 방지.

7. 그 방법은 어떻게 구현되나요?

* 피벗을 랜덤하게 선택하는 방법은 간단히 배열에서 무작위로 원소를 선택하면 됨.

8. 퀵정렬의 시간복잡도가 O(n^2)가 되는 경우 설명해주세요.

* 피벗을 항상 배열의 최솟값 또는 최댓값으로 선택하는 경우.

* 이미 정렬된 배열에서 첫 번째 원소를 피벗으로 선택하는 경우.

9. 병합정렬에 대해 설명해주세요.

* 분할 정복 방법 사용.
  배열을 반으로 나누고 각각을 정렬한 후, 정렬된 두 배열을 병합함.

### 해시
1. Java : Hash Map과 Hash Set 이있음 Hash Set에 대해서 설명

* 중복된 요소를 허용하지 않음.
* 순서를 보장하지 않음.
* 내부적으로 해시 테이블을 사용하여 구현됨.

2.  해시 알고리즘 소개해주세요.

* 해시 알고리즘은 임의의 크기의 데이터를 고정 크기로 매핑하는 함수.

3. 해시 맵과 해시 테이블의 차이점

* 해시 맵: 자바의 컬렉션 프레임워크에서 제공하는 Map 인터페이스의 구현 중 하나.
* 해시 테이블: 일반적인 용어로 해시 기반의 자료구조를 가리킴. 자바에서는 주로 HashMap이라는 용어를 사용.

4. 해시 테이블에 대한 설명해주세요.

* 해시 테이블은 해시 함수를 사용하여 데이터를 해시 버킷으로 매핑하는 자료구조.
* 효율적인 검색, 삽입, 삭제를 위해 사용됨.

5. 어떤 것이 좋은 해쉬 함수인가요?

* 좋은 해시 함수는 해시 충돌을 최소화하고 데이터를 고르게 분산시키는 함수.
* 높은 성능을 위해서는 해시 충돌이 적고, 계산이 빠르며, 고르게 분포되는 함수가 좋음.

6. 해시 충돌 발생할 수 있다. 충돌 경우 해결 방법 한가지만 설명해주세요.

* Open Addressing (개방 주소법): 충돌이 발생한 경우 다른 빈 버킷을 찾아가며 데이터를 삽입하는 방법.

7. Java의 HashMap에서는 어떤 방법으로 해시충돌을 해결하는지 아시나요.
* Java의 HashMap에서는 기본적으로 Separate Chaining 방식을 사용하여 해시 충돌을 해결.
* Separate Chaining은 충돌이 발생하면 해당 버킷에 연결 리스트로 데이터를 추가하는 방식.

8. Separate Chaining 해결방안중 연결리스트를 이용한 방법과 레드블랙트리를 이용한 방법에 대한 시간복잡도 비교

* 연결리스트를 이용한 방법: 시간복잡도는 O(n), n은 해당 버킷의 연결 리스트 길이.
* 레드블랙트리를 이용한 방법: 시간복잡도는 O(log n), n은 해당 버킷의 레드블랙트리의 높이.

9.  Use case
* 해시 셋은 고유한 값을 유지하고자 할 때 사용.
* 중복된 요소를 허용하지 않으며, 검색과 삽입이 빠른 특성을 가지기 때문에 대량의 데이터 중에서 특정 값을 찾거나 관리할 때 유용.

### 암호화 알고리즘
1. 비대칭키 방식을 구현하는 방식 중 한가지만 선택해서 설명해주세요.

* RSA 알고리즘은 가장 널리 사용되는 비대칭키 알고리즘 중 하나입니다.
  키 쌍(공개키와 비밀키)을 사용하며, 공개키로는 암호화하고, 비밀키로는 복호화합니다.

2. 비대칭 키 암호화와 대칭키 암호화에 대해서 간단히 설명해주세요.

* 비대칭 키 암호화: 두 개의 키(공개키, 비밀키)를 사용하며, 공개키로 암호화하고 비밀키로 복호화합니다. 대표적인 알고리즘으로 RSA가 있습니다.
* 대칭 키 암호화: 암호화와 복호화에 같은 키를 사용합니다. AES, DES 등이 대표적인 대칭 키 알고리즘입니다.

3. 대칭키와 비대칭키의 장단점

* 대칭키:
  장점: 계산이 빠르다.
  단점: 키 교환과 관리의 어려움, 키 배포에 대한 취약성.

* 비대칭키:
  장점: 키 교환에 대한 취약성이 없음, 안전성이 높음.
  단점: 계산이 느리다.

4. 단방향 암호화에 대해서 간단히 설명해주세요.

* 단방향 암호화는 한 방향으로만 암호화가 가능한 알고리즘입니다.
  주로 해시 함수를 사용하여 데이터를 고유한 고정 크기의 문자열로 변환합니다.

5. 단방향 방식을 통해 디지털 디이터를 다룰때. mdc 와 mac를 설명해주세요.

* MDC(Message Digest Code): 메시지 다이제스트 코드는 단방향 해시 함수를 사용하여 메시지의 고유한 요약값을 생성하는 기술입니다.
* MAC(Message Authentication Code): 메시지 인증 코드는 키를 사용하여 메시지에 대한 인증을 수행하는 기술입니다.

6. 암호화적 해쉬함수가 가져야하는 특징

* 고정된 출력 크기: 해시 함수는 항상 고정된 크기의 출력을 생성해야 합니다.
* 겹치지 않는 값: 서로 다른 입력에 대해 겹치지 않는 출력 값을 생성해야 합니다.
* 반전 가능성 없음: 해시 함수의 출력 값을 통해 원래 데이터를 복원할 수 없어야 합니다.
* 빠른 계산: 계산이 빠르게 이루어져야 합니다.
* 충돌 저항성: 서로 다른 입력에 대해 같은 출력이 생성되는 충돌이 발생하지 않아야 합니다.

### 그 외
1. 이진탐색 트리와 이진트리를 설명해주세요.

* 각 노드가 최대 두 개의 자식을 가지는 이진 트리.
* 각 노드의 왼쪽 자식은 현재 노드보다 작은 값이며, 오른쪽 자식은 현재 노드보다 큰 값을 가짐.
* 탐색, 삽입, 삭제 등의 연산이 효율적으로 수행됨.

2. 편향 이진탐색 트리 해결하기 위한 트리 중 한가지 설명
* AVL 트리, 레드-블랙 트리 등.
* 균형을 유지하여 트리의 높이를 최소화하여 탐색 시간을 최적화.

3. 그래프와 트리의 차이점을 설명해주세요.

* 트리(Tree):
  계층적인 구조를 갖는 비순환적인 그래프.
  각 노드는 부모 노드와 자식 노드 간의 관계를 가짐.
  루트 노드에서 어떤 노드로도 가는 경로는 유일.

* 그래프(Graph):
  정점과 간선의 집합으로 이루어진 자료 구조.
  순환이 있을 수 있음.
  방향성을 가질 수도, 가지지 않을 수도 있음.