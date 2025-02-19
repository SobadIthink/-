1、  push 当前目录下的ko到指定目录
for /r %%i in (*.ko) do (
adb push  %%i /vendor/lib/modules/
)
