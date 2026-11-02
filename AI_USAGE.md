# 让 AI 按需读取上游渠道

本仓库是链接目录。先读取 `README.md` 和 `sources.json`，再选择与任务有关的上游，避免先下载整个案例库。

目录包括 9 个 GitHub 仓库、1 个产品入口，以及原公开影像库中直接采集的 72 位公开作者渠道。作者记录只保留账号和代表原帖出处，均标记为历史链接、本次未重新访问；它们不是完整帖文或线程档案。

## 已有 GitHub 连接器

在支持 GitHub 的 AI 客户端中，直接提供仓库地址：

```text
https://github.com/7yedeng/ai-visual-sources
```

连接器能否读取公开仓库、搜索代码或访问上游文件，取决于当前客户端提供的工具与授权范围。只读研究使用读取与搜索能力即可。本项目不需要为此分发服务器密钥。

可复制的任务：

```text
读取 https://github.com/7yedeng/ai-visual-sources 的 README.md 和 sources.json。
我要找适合「纸雕旅行海报」的生图案例。
先按用途选出最多 3 个相关上游，再按需读取这些上游的 README 或案例文件。
结果给出原始链接、适合的原因及已实际核对的信息。
只有读到原文时才引用提示词；缺失时说明缺失，不补写成作者原话。
不要下载全库，不复制媒体，不执行上游代码或安装 Skill。
```

将用途换成「Seedance 产品短片」「文字海报」「参考图编辑」等即可。来源目录本身不包含全部案例，具体答案仍需要读取相应上游。

## GitHub 官方 MCP

[GitHub 官方 MCP Server](https://github.com/github/github-mcp-server) 提供由 GitHub 托管的远程服务，也提供本地运行选项。使用受支持客户端的远程接入，不需要在本项目的 VPS 上部署 MCP。

按照[官方接入说明](https://docs.github.com/en/copilot/how-tos/copilot-in-your-ide/customize-copilot/extend-copilot-with-tools-and-context/set-up-the-github-mcp-server)选择当前客户端支持的认证与连接方式。客户端支持、账户权限和 GitHub 自身限制以官方说明为准；这里不额外维护一套客户端配置或令牌。

连接后仍先读本仓库的两个目录文件，再读选定上游。旧博客的自建影像库 MCP/API 已退出这一使用流程。GitHub MCP 提供访问 GitHub 的工具，不会把本目录自动变成全量图片向量知识库。

## 程序读取

程序只需要这份 [sources.json](sources.json)，可通过 GitHub 文件页面、原始文件或[官方仓库内容 API](https://docs.github.com/en/rest/repos/contents#get-repository-content)读取，并遵守 GitHub 自身的访问与速率限制。文件包含渠道、分类、出处和核验状态，不包含媒体、完整提示词或私有收藏导出。

运行搜索 API、用户密钥配额、嵌入模型、数据库与定时抓取均不属于这个目录的维护范围。
