# MT Splash Pages (GitHub Pages)

白屏开关型启动页（MT 类型）。开关文本来自 `app-gonow`。

## 在线地址

- 生成器：https://lwei1992.github.io/mt-splash-pages/
- 启动页：https://lwei1992.github.io/mt-splash-pages/welcome.html?path=26066919/liziyoupin

## 开关接口格式

默认请求：

```text
https://lwei1992.github.io/app-gonow/<path>/
```

例如：https://lwei1992.github.io/app-gonow/26066919/liziyoupin/

返回纯文本，用 `~` 分割：

| 内容 | 行为 |
|------|------|
| `0~https://…` | 不跳转，调用 `startAPP` |
| `1~https://…` | 调用 `scanPrivacyPolicy`，打开第二个参数 URL |

## App 接入

```text
https://lwei1992.github.io/mt-splash-pages/welcome.html?path=26066919/liziyoupin
```

或直接指定完整开关 URL：

```text
https://lwei1992.github.io/mt-splash-pages/welcome.html?api=https://lwei1992.github.io/app-gonow/26066919/liziyoupin/
```

原生桥接：

- `webkit.messageHandlers.startAPP`
- `webkit.messageHandlers.scanPrivacyPolicy`
