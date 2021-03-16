# 무방향성 그래프

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




### edge 갯수 에 따른 node 사이즈 설정

###### 그래프 degree(정도) 정보가 담긴 딕셔너리를 만든다.
```python
d = dict(g1.degree)
````

```python
print(d)
```

```
>>{'a': 1, 1: 3, 2: 1, 11: 1, 22: 0}
```

###### 'a'의 node 에는 1개, 1의 node 에는 3개, 2의 node에는 1개 , 11의 node에는 1개, 22의 node에는 0개의 edge가 존재한다는 뜻이다.

```python
nx.draw(g1, nodelist = d.keys(), node_size = [v*100 for v in d.values()], with_labels = True)
```

###### d에서 key값을 nodelist에 , node 사이즈는 v에 d의 values값을 차례로 받아오면서
###### values값이 클수록 ( edge 가 많을수록 ) node 사이즈를 크게 만든다.
###### a node 는 100, 1 node 는 300,  node 는 100, 11 node 는 100, 22node 는 0 의 사이즈를 가질 것이다.

```python
plt.show()
```
![image](https://user-images.githubusercontent.com/73538957/111281113-ed970c80-867f-11eb-9345-0765c2d34c90.png)





