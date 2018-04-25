# Processing 基本結構

- Processing 使用的語言是簡化版的 java
- 不需要寫落落長的 class 和 public static void main() 巴拉巴拉.
- setup() draw() 這兩個函數是 Processing 的程式入口.
- setup() 會在程式啟動時跑一次，通常用來初始化.
- draw() 就是實際畫圖的函數. 把畫圖指令寫在裡面, 就會呈現在畫布上.
- line() 就是畫一條線, 很簡單. 四個參數分別是起始點 (X,Y) 和終止點 (X,Y)
- strokeWeight() 可以改變當前的筆刷寬度, 畫出粗細不同的線.

## code sample

```java
// setup 這個函數會在一開始被呼叫一次 通常用來做初始化
void setup()
{
    size( 600, 480 ); // 設定窗口尺寸
}

// 實際上畫圖的 code
void draw()
{
    strokeWeight( 8 ); // 筆刷寬度
    line( 100, 100, 300, 300 ); // 劃一條線
}
```

[回目錄](index.md)