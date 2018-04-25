
# Input Layout

使用 Vertex Buffer 時，我們必須要定義相對應的 Input Layout,
來描述頂點數據的記憶體佈局。 

比如

```cpp
struct Vertex1
{
	XMFLOAT3 Pos;
    XMFLOAT4 Color;
}
```
對應的 Input Layout 就是