1、  push 当前目录下的ko到指定目录
```
for /r %%i in (*.ko) do (
adb push  %%i /vendor/lib/modules/
)
```
2、
```
adb shell cmd package bg-dexopt-job com.jingdong.app.mall
adb shell "pm list packages | cut -d ':' -f2 | xargs -n1 pm bg-dexopt-job"
adb shell cmd package compile -m speed-profile -f com.tencent.mm com.ss.android.article.news
全量应用dex2oat优化（常用）
adb shell "pm list packages | cut -d : -f2 | xargs -n1 cmd package compile -m speed-profile -f "
-c命令会在编译优化执行前先清空应用profile
adb shell "pm list packages | cut -d : -f2 | xargs -n1 cmd package compile -c -m speed-profile -f "
```
