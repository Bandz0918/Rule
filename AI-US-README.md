# AI-US — Loon iOS 海外 AI 分流

将 AI-US.list 的 Raw 链接添加到 Loon 远程规则，策略选 United States 并启用，放到旧 AI / OpenAI / Claude / Gemini / Google 等远程规则前面。美国策略组须选可用的美国节点。

```ini
https://raw.githubusercontent.com/Bandz0918/Rule/main/AI-US.list, policy=United States, tag=海外AI美国, enabled=true
```

覆盖 ChatGPT、Codex、Sora、Claude、Gemini、AI Studio、NotebookLM、Jules、Flow、Antigravity、Muse、Meta AI、Grok、Perplexity、Microsoft Copilot、GitHub Copilot、Poe、Mistral、Cursor、Windsurf、Manus、Hugging Face、ElevenLabs、Midjourney、Suno、Runway、OpenRouter、Cohere、Devin、Groq、Cerebras、海外版 Coze / Trae。

这是一份应用和服务域名表，不绑定具体模型版本。不包含国内 DeepSeek / 豆包 / 通义等服务，保留国内直连配置。登录与实时通信部分使用共享端点，因此该端点的非 AI 请求也可能使用同一策略。未添加整个 Google、Facebook 或共享云服务的规则，也未添加共享 IP / ASN 规则。

个人配置、节点订阅、密码、MITM 证书均不在本仓库新文件中。普通 raw/main 链接读取当前 main 分支文件：仓库中更新文件后，Loon 刷新远程规则即可拉取。文件不会自行维护或保证第三方域名永远有效。本地规则及插件规则优先于远程规则，仍需检查冲突及请求记录。

## 更新

在 GitHub 打开 AI-US.list → Edit → 修改域名 → Commit changes，然后在 Loon 更新该规则。建议保留可用的本地规则缓存，不要删除当前配置后才尝试下载。

## 来源

- https://github.com/v2fly/domain-list-community/tree/master/data （openai、anthropic、google-deepmind、xai、perplexity、poe、cursor、windsurf、github-copilot、manus、huggingface、elevenlabs、groq、cerebras、category-ai-!cn）
- https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Loon （按服务补充具体依赖端点，未照搬宽泛云服务/IP规则）
- https://about.fb.com/news/2026/09/introducing-muse-personal-ai-agent/amp/
- https://help.mistral.ai/en/articles/682992-le-chat-is-now-vibe
- https://www.suno.com/
- https://runwayml.com/
- https://nsloon.app/en/docs/Rule/

2026-10-01 核对。规则语法已检查，尚未在手机验证每项服务的运行情况。新增服务或登录/文件上传/语音功能仍可能需要补充域名。
