# 当前 stable：Google 文档功能更新（2026-10-22）

- 孵化师：**0.9.11**。[完整安装与保留资料升级](https://github.com/wenmin20212-dotcom/UAH-incubator/releases/tag/v0.9.11)（原仓库私有，需访问权限）。
- 秘书：**0.1.7**。[完整安装与保留资料升级](https://github.com/wenmin20212-dotcom/UAH-secretary-4120.1/releases/tag/v0.1.7)（公开下载）。
- 签名清单：[stable-google-docs-20261022-1](https://github.com/wenmin20212-dotcom/UAH-agent-updates/releases/tag/stable-google-docs-20261022-1)，序列2026102201。公共host继续为0.9.9。

新增Google Drive/Docs可选接口，支持Word导入原生Google文档；用户需单独完成Google授权。默认只访问本应用文件，没有全盘写、分享或删除权限。

接入在线更新且启用product更新的兼容实例可以检查、下载并重启安装。职业资料或程序有本地修改时自动更新会拒绝覆盖；请使用匹配版本的程序增量升级包，保留资料并先备份。账号令牌、模型、聊天、工作区不进入分发包。手机接口版本仍为0.1.5，无需为本功能另外升级。

以下为更新协议及历史发布说明；当前版本以上述清单为准。

# Agent 统一升级中心

公开地址：https://github.com/wenmin20212-dotcom/UAH-agent-updates

为兼容的孵化师及独立子 Agent 提供签名程序更新。下载公开更新不需要 GitHub 账号或访问令牌，模型账号与模型设置继续保留在各自电脑上。

- `host`：相同 Windows x64 / host ABI 的公共运行程序及更新引擎。
- `product`：严格匹配产品 ID 的内置职业程序与资源；旧实例默认不自动更新职业内容。
- `preview`：开发验证通道，发布 `update-feed-preview.json`。
- `stable`：正式通道，发布 `update-feed-stable.json`；当前投放孵化师 0.9.10（2026-10-21）。

客户端验证预置公钥签名、版本、适配范围、归档及逐文件 SHA256。当前交互更新器自动检查，提示后由用户选择下载并重启，或稍后手动启动；启动失败自动回退。更新不覆盖模型设置、用户技能、原始知识、聊天、任务与实例身份。现阶段拒绝自动数据迁移。

公钥见 `public-keys.json`。公开公钥只能验证更新，不能签发更新；签名私钥不在本仓库或程序包内。

本中心同时提供 preview 和 stable；目前 stable 的职业产品包仅针对 uah-incubator 0.9.10，公共host为0.9.9。旧程序仍需一次接入固定启动器，新版孵化师源码已接入该地址；本中心上线不表示现有秘书、医生或孵化师已经更新。预览包的真实窗口升级测试使用隔离合成资料，没有调用模型。公开下载验证报告与签名清单附在对应 Release。

## 当前 stable：孵化师 0.9.10

[投放范围、升级步骤及验证记录](incubator-0.9.10-stable.md)。已接入更新器的旧版可从“程序更新 → 检查新版本…”触发；0.9.9可直接升级到0.9.10。公共host适用于匹配ABI的Agent，职业product仅匹配孵化师；手机服务独立更新。历史0.9.7与0.9.9投放记录仍保留。
