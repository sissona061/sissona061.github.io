自 2022 年 11 月推出以来，ChatGPT 风靡全球。它以惊人的速度吸引了用户，仅在发布后 5 天内便获得了 100 万用户，而在几个月内用户数突破 1 亿。随着技术的不断升级和网络能力的增强，ChatGPT 已成为最强大的聊天机器人之一，被广泛应用于客户支持、数据分析、内容生成等领域。

然而，由于区域和账号限制，许多用户仍无法直接体验 ChatGPT 的强大功能。幸运的是，网络上出现了许多基于 ChatGPT 的应用（即套壳应用），让更多人能够享受 AI 技术带来的便利。以下将为你介绍几款工具，帮助你快速搭建自己的 ChatGPT Web 应用。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bit.ly/bewildcard)

## ChatGPT Next Web

> [GitHub 仓库地址](https://bit.ly/bewildcard)

![ChatGPT Next Web 界面](https://developer.qcloudimg.com/http-save/yehe-5851655/24330907f0a28e3afe98a9e062624b4d.png)

![ChatGPT Next Web 特性](https://developer.qcloudimg.com/http-save/yehe-5851655/40c93f084dd28a5007e7e4b9d0807f0c.png)

**ChatGPT Next Web 的主要特性：**

- 提供体积极小（~5MB）的跨平台客户端（Linux/Windows/MacOS）。
- 完整的 Markdown 支持：LaTex 公式、Mermaid 流程图、代码高亮等。
- 精心设计的 UI，响应式设计，支持深色模式和 PWA。
- 极快的首屏加载速度（~100kb），支持流式响应。
- 隐私安全，所有数据保存在用户浏览器本地。
- 预制角色功能（面具），方便创建、分享和调试个性化对话。
- 内置海量 prompt 列表，支持中英文。
- 自动压缩上下文聊天记录，节省 Token 的同时支持超长对话。
- 多语言支持：简体中文、繁体中文、英语、日语等。
- 支持自定义域名绑定，随时随地快速访问。

### 独立部署

ChatGPT Next Web 支持两种部署方式：容器部署和本地部署。以下是具体方法：

#### 容器部署

确保 Docker 版本在 20 及以上，否则可能会提示找不到镜像。

bash
docker pull yidadaa/chatgpt-next-web
docker run -d -p 3000:3000 \
-e OPENAI_API_KEY="sk-xxxx" \
-e CODE="页面访问密码" \
yidadaa/chatgpt-next-web


如需指定代理，可使用以下命令：

bash
docker run -d -p 3000:3000 \
-e OPENAI_API_KEY="sk-xxxx" \
-e CODE="页面访问密码" \
--net=host \
-e PROXY_URL="http://127.0.0.1:7890" \
yidadaa/chatgpt-next-web


#### 本地部署

在控制台运行以下命令：

bash
bash <(curl -s https://raw.githubusercontent.com/Yidadaa/ChatGPT-Next-Web/main/scripts/setup.sh)


⚠️ 如果安装过程中遇到问题，建议优先使用 Docker 部署。

## chatgpt-web

> [GitHub 仓库地址](https://bit.ly/bewildcard)

![chatgpt-web 界面](https://developer.qcloudimg.com/http-save/yehe-5851655/76a5ee76910498d51fa5da7dde6e4f2c.png)

![chatgpt-web 特性](https://developer.qcloudimg.com/http-save/yehe-5851655/f6e9fbb0ed57877b53da18f4ae2d8f5d.png)

**chatgpt-web** 是一款简单易用的 ChatGPT 套壳应用，适合团队内部使用。它还提供了功能更丰富的 Plus 高级版：

> [GitHub Plus 版本地址](https://bit.ly/bewildcard)

通过独立部署，你可以将其变成一个小型组织内部共享的 ChatGPT 应用，在享受 AI 技术的同时，避免受到苛刻的使用限制。

---

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bit.ly/bewildcard)