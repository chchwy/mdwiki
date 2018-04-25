Bellman-Ford Algorithm
===========================

- Bellman-Ford 是一種單一源頭的最短路徑演算法。
- Bellman-Ford 的優點 (相對於Dijkstra來說) 
	1. 可以有負邊。 
	2. 單純容易實作。


原理: 圖上做 V-1 次鬆弛操作。
假設有向圖 G(V,E), Vs 為起點

找出一個最短路徑樹

- 起點Vs就是這棵樹的root。
- 建立一張表 pred[V] 裡面存的是每一個點的parent。
- 建立一張表 dist[V] 裡面存的是目前已知Vs到其他每個點的距離。

演算法步驟

1. 初始化 
	dist[1~N] = INFINITY
	pred[1~N] = NULL
	dist[Vs] = 0 

2. 對所有的邊進行比較
	foreach i = 1 to N // 對每個點跑
		for each () {
			if ( Weight())
			{
		
		}
	}
	
3. 




