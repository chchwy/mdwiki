
## 什麼是 Widget ?

A. a widget is a visual element in a user interface.

--------------

## 怎麼使用 signal/slot ?

通常長這樣

    QObject::connect ( 元件一, signal事件, 元件二, slot事件 );

因為大部分的 Qt class 都繼承自 QObject，所以也可以直接在物件裡呼叫 connect
signal 表示目前物件發生了某些變化，而slot 則是接受到訊息之後的工作。

-----------------

## 如何移除signal/slot的連接?

`QObject::disconnect()`

------------------

## signal/slot 可以自由配對，是多對多的關係。

一個 singal 可以送給很多個slot。
一個 slot 也可以接收很多個signal。
一個singal也可以連接到另一個singal，如果多個 signal 串在一起就是連鎖發出的機制。

-----------------

## Qt 事件

Qt 事件使用冒泡事件機制，也就是裡面的小元件會先收到event，是由子元件開始，一層層由內往外傳，最外層的大元件最後收到事件。
一個元件要收鍵盤事件，必須要先拿到Focus。
this->setFocus();

如果打算就攔截此事件，就調用 `event->accept()`
如果打算讓事件繼續往外傳，就調用 `event->ignore()`

--------------------

## 產生 Visual Studio 專案檔

    qmake -tp vc -r
    
--------------------

## 產生 Xcode 專案檔

    qmake -spec macx-xcode