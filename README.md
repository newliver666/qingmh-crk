# 青漫 APK (qingmh)

青漫 `com.kunlun.llxq` v2.3.23 的**去广告优化版**安装包，个人自用重新打包，签名与官方版不同。

## 下载

前往 [Releases](https://github.com/newliver666/qingmh-crk/releases) 页面下载：

- **[qingmh_v2.3.23_opt.apk](https://github.com/newliver666/qingmh-crk/releases/download/v2.3.23/qingmh_v2.3.23_opt.apk)**（约 152 MB）

SHA-256：`ff7f0e4bad79bb2a2cdfd160c3148d03e0baf0e806af0f1ce943f497f931fcac`

## 本次优化内容

- 移除开屏广告
- 移除插屏 / Banner / 信息流 / 激励视频等各类广告位
- 移除悬浮「开通会员」按钮
- 移除启动与阅读过程中的营销弹窗（限时福利、深夜专区、免费 VIP 等）
- 移除首页「深夜专区」推广卡片
- 屏蔽应用内自动更新提示，避免被覆盖回官方版本
- 会员状态相关界面正常显示，漫画正文 / 专区内容可正常阅读

## 安装说明

1. 因为签名与官方版不同，**先卸载已安装的官方版本**（否则会提示签名冲突）。
2. 安装下载的 APK，允许「安装未知来源应用」。
3. 首次启动会要求选择性别（应用自身流程，用于推荐内容），选择后即进入主界面。

### 命令行安装（可选）

```bash
adb uninstall com.kunlun.llxq
adb install -r qingmh_v2.3.23_opt.apk
```

包体较大时推荐先推送到设备再安装，速度更稳：

```bash
adb push qingmh_v2.3.23_opt.apk /data/local/tmp/qm.apk
adb shell pm install -r -t /data/local/tmp/qm.apk
```

## 环境要求

| 项 | 说明 |
|---|---|
| Android 版本 | 8.0 及以上（实测 Android 9 正常） |
| CPU 架构 | `arm64-v8a` |
| 包名 | `com.kunlun.llxq` |
| 版本 | 2.3.23 (versionCode 2323) |

## 说明与局限

- 漫画内容、专区内容、宣传图等均由服务端下发，本地不做修改。
- 会员专区中的装扮 / 礼包类权益由服务端按账号资产发放，未做处理，点击后由服务端返回结果。
- 所有 native 库（`.so`）与官方包保持一致，未做改动。
- 本仓库仅存放安装包与说明，供个人自用；请勿用于商业用途。

## 免责声明

本仓库内容仅供个人学习与技术研究使用，请在下载后 24 小时内删除。请支持正版内容与官方渠道。
