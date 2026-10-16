# LeanDay · 轻盈计划

一个以**每日执行**为中心的本地优先 Android 减重追踪 App。

## 产品定位

面向希望通过普通家常饮食与适度运动长期管理体重的用户，而不是依赖严格卡路里计算的节食工具。

- **今日**：今天吃什么、做什么运动、完成了什么
- **7 天计划**：普通中式家常食谱，工作日支持前一晚准备次日便当
- **动作指导**：椅子深蹲、靠墙俯卧撑、臀桥、鸟狗式、提踵
- **体重趋势**：仅基于真实记录绘图，显示目标进度
- **本地提醒**：每日三餐与运动提醒、次日带饭提醒
- **数据管理**：本地存储，不依赖服务器和付费 AI API

## 技术栈

Flutter / Dart · Material 3 · SharedPreferences · flutter_local_notifications

Android 优先，后续可扩展至 iOS。

## 当前状态

- [x] GitHub 仓库初始化
- [ ] 将已制作的 Flutter M1 源码完整迁入本仓库
- [ ] 在 Flutter SDK 环境中运行 `flutter analyze` 和 `flutter test`
- [ ] Android 真机测试（数据持久化、通知授权、跨日打卡）
- [ ] 完善运动动作图解和用户界面

**注意：仓库当前尚不包含完整 App 源码；M1 源码包已在项目会话中提供。**

## M1 源码导入方法

在 Mac 上下载并解压此前提供的 `LeanDay_Android_Flutter_M1_source.zip`，然后从解压目录执行：

```bash
git clone https://github.com/soyalu/LeanDay.git
cp -R leanday_flutter/. LeanDay/
cd LeanDay
git status
git add .
git commit -m "feat: import Flutter M1 app source"
git push origin main
```

请检查当前路径，确保解压目录 `leanday_flutter` 与克隆目录 `LeanDay` 处于同一父目录。导入后按源码中的 `scripts/bootstrap_android.sh` 配置 Android 工程。

## 设计约束

普通家常菜、低摩擦打卡、真实记录、无需登录；不对健康检查结果作医学诊断，也不默认采用高强度运动和高蛋白饮食。
