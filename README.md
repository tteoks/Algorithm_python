# Algorithm_python 

It is to practice the algorithm using Python.

### 그리디 알고리즘 ###  
***눈 앞에 놓여진 상황 중 가장 최적의 상황만을 찾아서 해결하는 알고리즘*** 

해당 알고리즘은 쉽고 간단하지만, 어느정도 최적의 결과와 근사한 값을 내고,  
특정 상황에서는 최적의 상황을 도출하는 경우도 있다.

하지만 실제로는 최적의 해를 도출하지 못하는 경우가 더 많다.

### 너비 우선 탐색(Breadth First Search, BFS) ###
***탐색할 때 너비를 우선으로 하여 탐색을 수행하는 탐색 알고리즘***

"맹목적인 탐색"을 하고자 할 때 사용하는 탐색 기법으로 "최단 경로"를 찾아준다는 점에서   
최단 길이를 보장해야할 때 많이 사용하고는 한다. (Queue 사용)
1. Queue에 맨 처음의 시작 노드(Start Node)를 삽입하면서 시작, 또한 노드를 방문했다고 "방문 처리"
2. Queue에서 노드를 꺼낸 후, 해당 노드와 인접한 노드 중 방문하지 않은 노드를 탐색한다.
3. 차례대로 큐에 삽입한다.

즉 가장 가까운 순서로 탐색하는 알고리즘이다.

### 깊이 우선 탐색 (Depth First Search, DFS) ###
***탐색할 때 깊은 것을 우선적으로 탐색하는 알고리즘***

DFS도 "맹목적인 탐색"을 할 때 사용하는 탐색기법이다. 
Stack을 사용하여 구현하지만, 굳이 사용하지 않아도 구현은 가능하다.
-> 컴퓨터는 구조적으로 항상 스택의 원리를 사용하기 때문

1. Stack에 시작 노드(Start Node)를 삽입하면서 시작, 또한 노드를 방문했다고 "방문 처리"
2. 최상단 노드에서 방문하지 않은 인접 노드가 있으면 그 노드를 스택에 넣고 방문 처리한다.
3. 인접한 모든 노드에 방문했으면, 스택에서 최상단 노드를 빼고 no.2로 돌아간다.

### 다이나믹 프로그래밍 (Dynamic Programming, DP: 동적 계획) ###
***하나의 문제는 단 한번만 풀도록 하는 알고리즘***

일반적으로 알고리즘은 동일한 문제를 다시 푸는 단점을 가지고 있다. 이러한 비효율성을 없애고자, 전에 풀었던 문제는 저장하고 있다가 다시 호출 했을 때 저장했던 답을 가져와서 사용하는 기법이다.

DP는 다음과 같은 상황에서 사용하면 유용하다.
1. 큰 문제로 작은 문제로 나눌 수 있는 경우
2. 작은 문제에서 구한 정답은 그것을 포함하는 큰 문제에서도 동일한 경우  
-> 피보나치 수열 = D[i] = D[i-1]+D[i-2]

이 과정에서 계산 결과를 배열에 저장하는 데, 이를 Memoization라고 한다.
