# 풀이

## 접근방법

- 다익스트라, 우선순위 큐 이용
- 우선순위 큐에 그래프 정보를 넣음
- 우선순위 큐에서는 가중치를 기준(최소)으로 넣음
- 큐에서 최솟값을 꺼냄
- 목표 정점이 갱신이 되지 않은 상태이면 앞에서 꺼낸 최솟값으로 갱신
- 갱신 후 해당 정점과 연결된 모든 간선의 정보를 갱신
- 목표 정점이 갱신이 되어있으면 큐가 빌 때까지 위의 과정을 반복함

## 어려웠던 부분

- 다익스트라 구현 문제를 많이 풀어보지 않아 실제 코드작성이 어려웠음
- 처음 자기 자신에게 가는 가중치를 0으로 풀었을 때 통과x
- 자기 자신에게 가는 가중치를 1로 설정 후, 출력시 가중치-1을 해주니 통과

## 새로 알게 된 것
