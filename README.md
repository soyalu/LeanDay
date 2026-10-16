# LeanDay · 轻盈计划

Flutter Android 本地优先减重计划 App，围绕七天家常食谱、每日运动指导、打卡提醒与真实体重趋势设计。

## 功能目标

- 今日：三餐、运动、喝水、体重、便当提醒
- 计划：按星期展示七天家常食谱和低负荷运动计划
- 动作：椅子深蹲、靠墙俯卧撑、臀桥、鸟狗式、站姿提踵
- 趋势：仅根据真实记录展示体重曲线
- 提醒：Android 本地通知，不依赖服务器
- 隐私：身高、体重和目标由用户在手机端设置并保存本地，不上传云端

技术栈：**Flutter / Dart + Material 3 + SharedPreferences + flutter_local_notifications**。

## 仓库状态

- [x] GitHub 项目初始化
- [x] 准备了脱敏的 M1 Flutter 源码压缩包
- [ ] M1 Flutter 源码上传到本仓库
- [ ] 本地 `flutter analyze`、`flutter test` 与 Android 真机验证
- [ ] 动作多帧图解、高保真交互、数据备份恢复

开发追踪：[#1 M1 导入和 Android 真机验证](https://github.com/soyalu/LeanDay/issues/1)。

## 导入脱敏源码

从 ChatGPT 项目会话下载 **LeanDay_M1_GitHub_safe_source.zip**，在 Mac 终端执行：

```bash
git clone https://github.com/soyalu/LeanDay.git
cd LeanDay
unzip /完整路径/LeanDay_M1_GitHub_safe_source.zip -d .
git status
git add .
git commit -m "feat: import privacy-safe Flutter M1"
git push origin main
```

解压后 README、pubspec.yaml、lib/、scripts/、test/ 将位于仓库根目录。进入 Android 调试环境之后可运行：

```bash
bash scripts/bootstrap_android.sh
flutter run
```

该包尚未在有 Flutter / Android SDK 的环境中编译验证，脚本会生成原生 Android 配置并运行静态分析与测试。

## Public 仓库的隐私原则

**请勿提交个人体检结果、真实健康记录或 JSON 备份文件。**
原始原型中曾将个人健康检查结果和初始体重硬编码在源码；请只使用更新后的 **safe_source** 包。用户个人身高、体重及目标在 App 内自行设置，存储在手机端。

本应用用于生活方式记录，不提供医疗诊断或治疗建议。
