

# Array

Powershell 裡面自帶的 Array 

最典型的作法: 用 @ 明確的宣告 array

    $myArray = @( 1, 2, 3, 4 ) 

或者透過逗號串接數個值, 隱式的宣告array

    $myArray = 1, 2, 3, 4 

用 (..) 符號可以簡便的創造連續數值

    $myArray = (1..99)

建立空的 array

    $myArray = @()

建立多維的 array

    $myArray = @( (1,2,3), ('Apple','Banana','Cool') )

添加元素

    $myArray += 3

存取元素

    Write-Host $myArray[0]

取得最末端的元素
    
    Write-Host $myArray[-1]

array 的長度

    Write-Host $myArray.length\

使用 foreach 走訪元素

    foreach( $e in $myArray )
    {
        Write-Host $e
    }

