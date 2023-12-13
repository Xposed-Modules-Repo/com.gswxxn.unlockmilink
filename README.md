# 小米不妙·享

## 主要功能
* 激活模块后，不需要在电脑端配置，即可让所有电脑均支持小米妙享的应用流转
* 替换设备类型，使手机与手机之间可以互联
* 支持在手机端镜像或扩展电脑屏幕
* 解锁 投屏 13.1 之后出现的白名单机型限制

## 使用方法

1. 在Xposed管理器(LSPosed)中激活模块
2. 作用域勾选 投屏(aka 互联互通服务)`(com.milink.service)`、MIUI+ Beta版(aka 跨屏协同服务)`(com.xiaomi.mirror)`、小米通信互联通信服务`(com.xiaomi.mi_connect_service)`
3. 重启三个作用域应用或重启手机

## 下载
[LSPosed 仓库](https://github.com/Xposed-Modules-Repo/com.gswxxn.unlockmilink/releases)

## 注意事项
1. 作用域中勾选 小米互联通信服务 后，在 小米妙享 PC 端手机屏幕镜像将会变大，如看不到屏幕镜像下半部分可以最大化窗口解决；此外，MIUI+ 面板也不会显示。
2. 如果 PC 端没有镜像或扩展屏幕选项，请尝试断开重连。这是因为小米妙享 PC 端似乎有个缓存机制，会读取上一次连接设备的设备类型；如果修改设备类型为手机后，没有出现 MIUI+ 面板，同理。
3. 使用小米妙享 PC 版需要在移动设备中升级以下组件; 如果您对应的应用版本高于提供的版本, 则可以忽略此步
   * MIUI+ Beta版 3.7.26.d 
   * 投屏 13.2.0.13 
   * 小米通信互联服务 2.12.156  
   **需升级的组件下载链接**  
   [查看链接](https://wwp.lanzoub.com/b027lfxdc) 密码:6ca1
4. 如果激活模块后通知栏没有出现小米妙享卡片，那么需要重启一次系统界面

## 无法使用
请先检查模块是否正常激活，并且作用域是否勾选。如果排查后仍有错误，请[提交 Issue](https://github.com/GSWXXN/UnlockMiLink/issues/new)。或联系酷安[@迷璐](http://www.coolapk.com/u/1189245)

## 致谢
使用 [Yuki Hook API](https://github.com/fankes/YukiHookAPI) 构建模块  
使用 [BlockMIUI](https://github.com/Block-Network/blockmiui) 构建UI界面  
使用 [DexKit](https://github.com/LuckyPray/DexKit) 查找被混淆的方法  
使用 [libsu](https://github.com/topjohnwu/libsu) 执行 Shell 命令  
