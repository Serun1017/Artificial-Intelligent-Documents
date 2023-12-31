
---
Best-First Search (최선 우선 탐색)은 Informed Search 알고리즘 중 하나로, 휴리스틱 함수를 사용하여 상태 공간을 탐색하는 방법이다. 이 알고리즘은 각 상태를 평가하고, 가장 유망한 상태를 먼저 확장하는데 사용된다.
Best-First Search는 다양한 문제에 적용될 수 있으며, 주로 최단 경로 탐색, 인공지능 게임 플레이, 로봇 경로 계획, 자연어 처리 및 기타 탐색 문제에 사용된다. 이 알고리즘은 휴리스틱을 통해 추가 정보를 활용하여 가장 가능성 있는 경로를 먼저 탐색함으로써 탐색 효율성을 향상시킨다.

---
# 특징

- 휴리스틱 함수 사용
  - Best-First Search에서는 휴리스틱 함수가 각 상태의 유망도 또는 가치를 측정하는데 사용된다.
  - 휴리스틱 함수는 목표 상태와의 예상 거리, 비용, 가치 등을 계산하여 상태의 우선순위를 결정한다.
- 우선순위 큐(Priority Queue) 활용
  - Best-First Search는 상태를 확장하는 동안 우선순위 큐를 사용하여 상태의 우선순위를 관리한다.
  - 이 큐는 가장 유망한 상태를 먼저 확장하고, 가장 유망하지 않은 상태를 나중에 확장하는 데 도움이 된다.
- 평가 함수
  - Best-First Search는 각 상태를 휴리스틱 함수에 따라 평가한다.
  - 상태의 평가는 목표와의 예상 관련성을 나타내며, 이를 기반으로 상태의 우선순위를 결정한다.
- 경로 선택
  - Best-First Search는 상태 공간에서 목표에 도달하기 위한 경로를 선택한다.
  - 이 경로는 휴리스틱 함수의 평가에 따라 결정되며, 목표에 가장 가까운 경로를 선호한다.
- 최적성(Optimality) 보장 안됨
  - Best-First Search는 가장 유망한 상태를 먼저 확장하지만, 최적 해를 보장하지는 않는다.
  - 휴리스틱 함수의 품질과 상태 공간의 특성에 따라 최적해를 찾을 수도, 찾지 못할 수도 있다.
- 탐색 종료 조건
  - Best-First Search는 종종 목표 상태에 도달하거나 더 이상 확장할 유망한 상태가 없을 때 탐색을 종료한다.