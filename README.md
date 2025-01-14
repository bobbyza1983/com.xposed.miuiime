# MIUI IME Unlock

解锁 MIUI 全面屏优化限制

## 测试环境

LSPosed v1.2.2(API 93.0)

MUI 12.5

Android 11(R,API 30)

## 使用方法

Xposed API Version >= 93

在作用域勾选需要解除限制的输入法即可，小米定制版也要勾上

## 下载

[app-release.apk](../../release)

## 特别说明

1. 全面屏优化与百度输入法官方版存在兼容问题，这不属于本模块 BUG。
2. 因为本人在用的是 MIUI12.5、Android11，所以对于其他版本的 MIUI 适配并不完整，存在不可用的可能性。
3. ~~托盘按钮设置为小爱语音输入时，按钮失效不可用，目前未发现原因，但通过长按选择启动小爱似乎没有问题。~~
4. 不接受任何为特定输入法适配 xxx 的请求，这不现实不合理。
5. 使用了小白条沉浸模块的系统，可能在部分输入法上无法使用全面屏优化(郑重声明：这事关我屁事)

## 更新日志

v1.08

    删除一个hook函数，解决重复hook
    整理代码

v1.07

    增加检查prop ro.miui.support_miui_ime_bottom
    底部按钮改为反色按钮
    尝试在安卓9使用与安卓10相同的hook方法

v1.06

    更换检查MIUI版本为检查Android版本
    删除旧方法依赖的代码

v1.05

    感谢 @ketal178 帮忙删除无用的代码
    删除一些非必要的Hook
    删除一些过时的代码
    尝试修复小爱语音输入按钮失效问题

v1.04

    对 MIUI12 改回使用旧的hook点

v1.03

    加入对 MIUI 版本的检查
    修复 MIUI12 输入法切换菜单不全的问题
    现在仅对 MIUI12、MIUI12.5 生效

v1.02

    优化执行逻辑
    部分hook方法不会对定制版进行hook
    增加对底视图颜色的修改，颜色完全由输入法控制
