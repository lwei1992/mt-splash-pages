# MT Splash Pages (GitHub Pages)

白屏开关型启动页（MT 类型）托管仓库。替代 Bunny CDN。

## 在线地址

- 生成器：`https://lwei1992.github.io/mt-splash-pages/`
- 启动页模板：`https://lwei1992.github.io/mt-splash-pages/welcome.html?key=YOUR_BUNDLE_ID`

## App 接入

把 WebView 启动地址设为：

```text
https://lwei1992.github.io/mt-splash-pages/welcome.html?key=com.YourApp
```

原生桥接（与 MT 一致）：

- `webkit.messageHandlers.startAPP`
- `webkit.messageHandlers.scanPrivacyPolicy`

## 本地文件

| 文件 | 说明 |
|------|------|
| `index.html` | URL 生成器（可复制 / 预览 / 下载静态 HTML） |
| `welcome.html` | 参数化白屏启动页 |

## 开关接口

默认：`https://diowen.sbs/api/v1/tro/querySwitch?key=<bundleId>`

可用 `&api=` 覆盖 API 基址。
