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
3、
```
dumpsys activity |grep -i mresume  ==》查看当前页面的activity
```
4、
```
gdb disassemble命令：
disassemble [func] 反汇编func函数
disassemble /m [func]  反汇编func函数显示对应源码
```
5、
```
grep 常用命令
-i    ==忽略大小写
-iw   ==匹配完整的单词，不是子串
-nr   ==递归搜索显示行号
-v    ==取反
-e -e  ==匹配多个

。。。
```
6、
```
显示帧率： adb shell service call SurfaceFlinger 1034 i32 1
```


