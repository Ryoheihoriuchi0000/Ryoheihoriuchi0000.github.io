# 隐私政策 (iOS)

**最后更新日期：** 2026年10月23日

SELECT（以下简称「本应用」）尊重用户隐私。本政策说明本应用 iOS 版收集哪些信息以及如何使用。

---

## 1. 我们收集的信息

以下信息**仅保存在您的设备上**，绝不会发送到本应用开发者拥有的任何服务器。

- 登记到各标签页的应用（显示名称、Bundle ID、图标 URL、自定义 URL scheme）
- 自定义项目的设置（标签、图标、快捷指令 URL、网站 URL）
- 显示偏好（标签页图标/文字样式、小组件颜色、「享受」标签页的显示状态）
- 分类和模式的排列顺序
- 语言偏好
- 是否已安装 SELECT Widgets 快捷指令

数据保存在 iOS 的 **SwiftData**（本地存储）和 **App Group** 容器（`group.com.artemis.select.ios`）中。使用 App Group 是为了让主应用和小组件扩展共享同一份数据。

---

## 2. 应用搜索 (iTunes Search API)

当您点按「添加项目」登记应用时，本应用会调用 Apple 公开的 **iTunes Search API**（`https://itunes.apple.com/search`）。

- 发送：**仅您输入的搜索词**（例如「微信」）
- 接收：应用名称、Bundle ID、图标 URL、App Store URL 等
- 搜索词绝不会保存在本应用开发者的服务器上（本应用没有自己的服务器）
- Apple 对该 API 调用的记录受 Apple 自身的隐私政策约束

您登记的应用会保存到本地 SwiftData 存储中，并显示在小组件上。

---

## 3. 应用图标缓存

登记应用时，其图标会从 Apple 的 CDN 下载并缓存在 App Group 容器中。

- 来源：Apple CDN 端点（例如 `is1-ssl.mzstatic.com`）
- 保存位置：App Group 容器内的 `Icons/{bundleId}.png`
- 目的：无需网络往返即可即时渲染小组件
- 与第三方共享：绝不

---

## 4. iCloud 同步

您的数据保存在您本人的 CloudKit 私有数据库（Apple ID 名下的私有区域）中。这适用于所有用户。
开发者及任何第三方均无法访问您的 CloudKit 数据。

---

## 5. 小组件启动

点按小组件中的磁贴时，会将目标应用的 Bundle ID 交给 iOS LaunchServices 来启动该应用。
不会产生网络通信，除目标 Bundle ID 外不会有任何信息离开设备。
此外，可选的「SELECT Widgets」联动功能可让您启动自建的快捷指令。是否安装不影响默认的启动方式。

---

## 6. 网络活动

本应用仅进行以下有限的网络请求。

- `https://itunes.apple.com/search`：查询应用信息（仅在使用「添加项目」时）
- Apple CDN：下载应用图标图片
- Apple CloudKit：iCloud 同步
- Google Firebase Authentication：统计使用人数（见 6-1）
- Google Mobile Ads (AdMob)：在编辑界面底部显示的横幅广告（见 6-2）

我们**不会**做的事：
- 不向本应用开发者拥有的任何服务器发送请求（我们没有自己的服务器）
- 不使用分析 SDK（无 Google Analytics、Firebase Analytics、Crashlytics、Sentry 等）
- 无应用内购买（所有功能免费，完全没有计费）
- 除 Firebase Authentication 和 Google Mobile Ads 外不使用第三方 SDK（其余均为 Apple 框架：CloudKit / WidgetKit / 快捷指令）

### 6-1. 统计使用人数 (Firebase Authentication)

为了大致了解有多少人在使用本应用，本应用使用 Google **Firebase Authentication** 的**匿名认证**。

- 首次启动时，会发放一个称为**匿名 ID** 的随机字符串。
- 该 ID **绝不会与您的邮箱地址、姓名、电话号码或任何其他个人信息关联**。没有登录界面，也不需要注册账户。
- 开发者只能看到**汇总数字**：每日活跃用户数、每月活跃用户数以及已发放的 ID 总数。无法识别或追踪个人用户。
- **不会传输任何行为记录**——既不包括您使用了哪些功能，也不包括您登记了哪些应用。
- 匿名 ID 按设备发放，重新安装本应用会产生不同的 ID。不会在设备之间将您关联为同一个人。
- 数据处理遵循 [Google 隐私政策](https://policies.google.com/privacy)。
- 即使没有网络连接，本应用的所有功能也能继续使用。

### 6-2. 广告 (Google Mobile Ads)

本应用会在编辑界面底部显示横幅广告，广告由 Google 的 **Google Mobile Ads SDK (AdMob)** 投放。

- 仅在编辑界面底部显示广告。小组件、设置界面和首次启动时的说明界面不显示广告。
- 为投放广告、衡量广告效果和防止欺诈，Google 会处理设备信息（IP 地址、设备型号、系统版本、广告展示与点按记录等）。
- 仅当您选择「允许跟踪」时才会使用广告标识符 (IDFA)。即使不允许，所有功能也能照常使用。您可以随时在 **iOS 设置 → 隐私与安全性 → 跟踪** 中更改。
- 在本应用收费期间获取本应用的用户不会看到广告。
- 数据处理遵循 [Google 如何使用使用其服务的网站或应用中的信息](https://policies.google.com/technologies/partner-sites) 和 [Google 隐私政策](https://policies.google.com/privacy)。

---

## 7. 向第三方披露

本应用不会与第三方共享收集到的信息。向 Apple 发出的网络请求（iTunes Search API、CloudKit）受 Apple 自身的隐私政策约束。
Firebase Authentication 发放的匿名 ID 仅由 Google 用于统计用户数，绝不会提供给任何第三方。为投放广告，Google 会处理 6-2 中所述的信息。

---

## 8. 儿童个人信息

本应用不会在知情的情况下收集 13 岁以下儿童的个人信息。

---

## 9. 权限与功能

本应用使用以下 iOS 功能。

- `LSApplicationQueriesSchemes`：用于在设备上进行 `canOpenURL` 检查的 URL scheme 列表（不涉及网络通信）
- `App Group`（`group.com.artemis.select.ios`）：主应用与小组件扩展之间的共享数据存储
- `WidgetKit`：渲染主屏幕小组件
- `AppIntents`：定义小组件内的按钮操作
- `CloudKit`：iCloud 同步
- `App Tracking Transparency`：请求跟踪许可，仅用于让广告更符合您的兴趣（不允许也不会限制任何功能）

本应用**绝不会请求**以下权限：
- 相机、麦克风、位置、通讯录、照片、蓝牙、本地网络、通知

---

## 10. 费用

本应用的所有功能均免费。**不含任何应用内购买**——没有订阅，也没有付费功能。本应用的运营费用由编辑界面底部显示的横幅广告支撑（见 6-2）。

---

## 11. 删除您的数据

您可以在设置界面中将所有设置恢复为默认值。如需完全卸载，请前往 **iOS 设置 → 通用 → iPhone 储存空间 → SELECT → 删除 App**。

如果启用了 iCloud 同步，还可以在 **设置 → [您的姓名] → iCloud → 管理储存空间 → SELECT → 删除数据** 中删除云端副本。

删除本应用后，匿名 ID（见 6-1）也会从您的设备上消失，且该 ID 不会再被使用。由于 ID 本身不包含任何可识别个人的信息，无法从任何残留记录中追溯到个人。

---

## 12. 本政策的变更

本政策可能在不事先通知的情况下更新。重大变更将在应用内或商店页面公布。

---

## 13. 联系方式

如对本政策有任何疑问，请通过 App Store 上列出的开发者联系方式与我们联系。

---

日本語版: [プライバシーポリシー (iOS版)](./Select-PRIVACY_POLICY-ios) ・ English: [Privacy Policy (iOS)](./Select-PRIVACY_POLICY-ios-en)
