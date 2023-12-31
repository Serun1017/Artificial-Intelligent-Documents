
---
Depth-First Search (깊이 우선 탐색, DFS)는 그래프 또는 트리 구조에서 사용되는 탐색 알고리즘 중 하나로, 특히 그래프의 깊이 방향으로 탐색을 수행하는 알고리즘이다.
DFS는 주로 미로 찾기, 그래프 순회, 깊이 방향으로 트리를 탐색하는 등의 문제에 사용된다. 그러나 최단 경로 문제나 최적 경로 문제에는 적합하지 않을 수 있다. DFS는 완전성(Completeness)을 보장하지만, 최단 경로를 찾는 문제에는 다른 알고리즘인 너비 우선 탐색(BFS) 또는 일정량 탐색(UCS)과 같은 알고리즘이 더 적합할 수 있다.

---
# 특징
- 스택(Stack), LIFO 큐(Last-In-First-Out) 사용 또는 재귀 호출
  - DFS는 주로 스택 자료 구조를 사용하여 구현된다. 또는 재귀 호출을 이용해 구현할 수도 있다.
  - 스택을 사용하면 각 상태를 스택에 넣고 꺼내면서 탐색을 수행한다.
- 깊이 방향 탐색
  - DFS는 가능한 한 깊게 들어가서 목표 상태를 찾을 때까지 탐색한다.
  - 시작 상태에서 출발하여 가장 깊은 상태까지 이동한 후 더 이상 진행할 수 없을 때 되돌아가서 다른 경로를 탐색한다.
- 완전성(Completeness)를 보장하지 않음
  - DFS는 완전성을 보장하지 않는다.
  - 무한 깊이의 상태 공간이나 순환(Loop)이 있는 공간에서 실패할 수 있다.
  - 이러한 문제를 피하기 위해 경로 중 반복된 상태를 피하도록 수정할 수 있으며, 이렇게 수정하면 유한한 상태 공간에서 완전성을 보장할 수 있다.
- 평균적인 시간 복잡도(Time Complexity)
  - DFS의 시간 복잡도는 *O(b^m)* 이다.
    - *b = branch, 각 상태에서 이동 가능한 자식 상태의 개수*
    - *m = max depth, 상태 공간의 최대 깊이*
   - 만약 목표 상태가 깊은 곳(depth가 큰 곳)에 있을 경우, *m* 이 *d(최단 경로의 길이)* 보다 훨씬 크다면 시간 복잡도가 상당히 나빠질 수 있다.
   - 그러나 목표 상태가 같은 깊이 상에 밀집해 있는 경우에는 너비 우선 탐색보다 효율적일 수 있다.
- 낮은 공간 복잡도(Space Complexity)
  - DFS의 공간 복잡도는 *O(bm)* 이다. 이는 메모리 사용량이 깊이에 비례한다는 것을 의미한다.
  - 따라서 깊은 상태 공간을 탐색하는 경우 메모리 사용량이 증가할 수 있다.
  - 그러나 메모리 사용량이 너비 우선 탐색보다 작을 수 있다.
- 최적성(Optimality)을 보장하지 않음
  - DFS는 최적성을 보장하지 않는다.
  - 가장 먼저 발견한 목표 상태를 찾는 경로가 최단 경로가 아닐 수 있다.

---
# Example

![[Depth-First Search_Example.png]]
