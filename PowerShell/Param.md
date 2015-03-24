
## PowerShell 處理參數的方式

假如你想給 PowerShell script 檔案傳入參數，例如 script.ps1 -server "http://1.2.3.4"

那可以在檔案開頭放 param() 來處理：

~~~powershell
param (
  [string]$server = "http://defaultserver",
  [string]$username = $(throw "-username is required."),
  [string]$password = $( Read-Host "Input password, please" )
)
~~~

也可已給定預設值
