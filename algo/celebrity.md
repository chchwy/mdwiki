名人問題 Celebrity Problem
=============================

一個會場裡有一位名人，請你找出名人是誰。

- 這個名人不認識任何一個人。
- 但是剩下的所有人都認識那位名人。

我們問Bob他認不認識Alice，如果他回答認識，那麼Bob就一定不是名人。如果回答不認識，那麼Alice就一定不是名人。所以不管怎樣我們都可以踢掉一個人，把問題由n縮小成n-1。

## 名人演算法 ##

Celebrity(know)
Input:  know (nxn Boolean陣列)
Output: celebrity

begin:
	i = 1;
	j = 2;
	next = 3;

	// 第一階段剔除所有不可能的人，只留下一位可能人選。
	while (next <= n-1)
	{
		if (know[i, j] == 1)
			i = next;
		else
			j = next;		
		next = next + 1;
	}
	
	if (i == n-1)
		candidate = j
	else 
	    candidate = i
	    
   // 第二階段，確定這位可能人選真的是名人	
   
end