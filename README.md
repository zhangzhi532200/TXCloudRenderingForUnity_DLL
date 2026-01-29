# DTCloudRenderingForUnity
适用于Unity的像素流送插件

## 简介

基于Unity的WebRTC库，inveta的peer-stream库适配的适用于Unity的像素流送插件。

## 功能特性

- 实时流媒体传输
- WebRTC技术支持
- 多种输入设备支持（键盘、鼠标、触摸屏、游戏手柄）
- 可配置的视频编码参数
- ICE服务器穿透支持
- 多平台兼容性

## 安装方式

### 1.安装Packages路径下的前置依赖，在线安装或使用离线包安装
- InputSystem-1.7.0 [InputSystem](https://github.com/Unity-Technologies/InputSystem/releases/tag/1.7.0)

- UnityWebSocket-v2.8.6 [UnityWebSocket](https://github.com/psygames/UnityWebSocket)

- com.unity.webrtc-3.0.0-pre.6 [com.unity.webrtc](https://github.com/Unity-Technologies/com.unity.webrtc/releases/tag/3.0.0-pre.6)

2.将Plugins下的dll拷贝至您项目中Plugins路径下

- DTCloudRendering.Editor.dll
- DTCloudRendering.Runtime.dll

## 组件使用

### 1. 添加 WebRTCController 像素流送组件

将 WebRTCController 组件添加到场景中的主相机上，该组件负责处理WebRTC连接、视频流传输等功能。

![1.png](img/1.png)

### 2. 添加 InitializeManager 初始化管理器

将 InitializeManager 组件添加到场景中的主相机上，该组件负责加载配置文件、初始化系统参数等。

![2.png](img/2.png)

### 3. 添加 CameraController 相机控制器

将 CameraController 组件添加到场景中的主相机上，该组件提供了多种控制摄像机的方式，包括键盘、鼠标、手柄等。

![3.png](img/3.png)

### 4. 添加 TaskIconController 最小化渲染控制器(可选)

将 TaskIconController 组件添加到场景中的主相机上，该组件可以让应用程序在Windows平台上最小化到后台运行。

![4.png](img/4.png)

> 请将所有组件统一挂载在主相机(Main Camera)上或创建一个新对象，将所有组件挂载在该对象上。

## 配置说明

系统配置保存在 `StreamingAssets/Global.conf` 文件中，主要配置项包括：

- `ServerUrl`: 信令服务器地址
- `FPS`: 流媒体帧率
- `ExitTime`: 无连接时退出时间
- `streamSourceType`: 流媒体源类型
- `StreamSize`: 流媒体分辨率
- `VideoCodec`: 视频编解码器
- `Bitrate`: 码率设置
- `ICEConfig`: ICE服务器配置

## 待解决遗留问题
- 移动设备多指触控异常
- 支持4k及以上分辨率
- 支持h265视频编码

## 联系作者

QQ：985691579 [>>> 发起会话 <<<](tencent://message/?uin=985691579&Site=&menu=yes)