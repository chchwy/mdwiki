## Item 1 類型推斷 type deduction

在原本的 C++98 中只有一種類型推斷，叫做 template type deduction，向這樣：

```cpp
template<typename T>
void func(T param) {}

template<typename T>
void func(T& param) {}

template<typename T>
void func(T* param) {}

template<typename T>
void func(const T& param) {}
```

即使有時候我們會加上指標、參考、const 修飾字，但是大多數時候類型推斷都相當直覺。

需要注意的點:
1. 當 T 是 universal reference 的時候 (還沒研究到 rvalue ref 所以暫時先不寫)
2. 當 T 是 array 的時候 (這時候是不是T&就有差別了)
3. 當 T 是 function 的時候 (同上，T 跟 T& 會推斷出不同的型別)
