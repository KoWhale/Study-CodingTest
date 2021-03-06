# DFS/BFS

# 그래프

> 그래프는 노드(Node)와 간선(Edge)로 표현되며 이 때 노드를 정점(Vertex)이라고도 말함.
> 

## 그래프 탐색

> 하나의 노드를 시작으로 다수의 노드를 방문하는 것을 말함
> 
- 두 노드가 간선으로 연결되어 있다면 ‘두 노드는 인접하다'라고 표현

### 그래프를 표현하는 2가지 방식

- 인접 행렬(Adjacency Matrix) : 2차원 배열로 그래프의 연결 관계를 표현하는 방식
    - 노드 개수가 많을수록 메모리가 불필요하게 낭비됨
- 인접 리스트(Adjacency List) : 리스트로 그래프의 연결 관계를 표현하는 방식
    - 연결된 정보만을 저장하기 때문에 메모리를 효율적으로 사용
    - 특정한 두 노드가 연결되어 있는지에 대한 정보를 얻는 속도가 느림

```python
INF = 999999999

#인접 행렬 방식
graph = [[0, 7, 5], [7, 0, INF], [5, INF, 0]]

#인접 리스트 방식
graph = [[] for _ in range(3)]
graph[0].append((1,7))
graph[0].append((2,5))

graph[1].append((0,7))

graph[2].append((0,5))
```

# DFS

> Depth-First-Search, 깊이 우선 탐색이라고도 부르며, 그래프에서 깊은 부분을 우선적으로 탐색하는 알고리즘
> 
- 동작 원리
    - 스택
- 구현 방법
    - 재귀 함수 이용

# BFS

> Breath-First-Search, 너비 우선 탐색이라고도 부르며, 가까운 노드부터 탐색하는 알고리즘
> 
- 동작 원리
    - 큐
- 구현 방법
    - 큐 자료구조 이용