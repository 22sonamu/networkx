

### import 

```python
import networkx as nx
import matplotlib.pyplot as plt
```
###### 비주얼 스튜디오 코드에서 draw를 보기 위해선 matplotlib모듈이 필요하다.

### 객체 생성
```python
g1 = nx.Graph()
```

### 노드 추가
```python
g1.add_node("a")
g1.add_node(1)
g1.add_node(2)
g1.add_node(3)
```

### 여러개의 노드를 한번에 추가
```python
g1.add_nodes_from([11, 22])
```

###### 리스트 형태로 추가한다.

### 노드 제거
```python
g1.remove_node(3)
```

### 엣지 추가 
```python
g1.add_edge(1, "a")
g1.add_edge(1, 2)
g1.add_edge(1, 22)
```

### 여러개의 엣지를 한번에 추가
```python
g1.add_edges_from([(1,2),(1,3))
```

### 엣지 제거
```python
g1.remove_edge(1,22)
```

### 그래프 그리기
```python
nx.draw(g1, with_labels = True)
plt.show()
```
###### with_labels 는 폰트 유무에 관한 것이다 False로 작성시 동그란 node만 보인다.


### 실행 

![image](https://user-images.githubusercontent.com/73538957/111279168-c5a6a980-867d-11eb-9022-83aecd0faeb9.png)









