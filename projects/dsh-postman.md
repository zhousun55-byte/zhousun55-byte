# dsh-postman · DeepSeek Harness 文件投递插件

把文件交给 AI 助手，通常要复制文件、贴路径，再解释该读哪些内容。这个插件在 DeepSeek Harness 的会话输入框里加了 `/upload` 菜单，可以直接选文件或文件夹。

[源码](https://github.com/zhousun55-byte/dsh-postman) · [客户端](https://github.com/zhousun55-byte/dsh-postman/blob/main/lib/client.js) · [服务端](https://github.com/zhousun55-byte/dsh-postman/blob/main/lib/index.js)

2026 年 8 月发布，已被 [awesome-dsh-plugin](https://github.com/awesome-dsh-plugin/awesome-dsh-plugin/pull/1153) 和 [awesome-deepseek-harness](https://github.com/0xsline/awesome-deepseek-harness/pull/308) 两份生态目录收录。

## 文件怎样进入对话

| 输入 | 处理方式 |
| --- | --- |
| 支持类型与大小范围内的图片 | 走宿主原生的图片附件通道 |
| 文本文件 | 上传后提取文本预览，追加到输入框草稿 |
| 其他文件 | 上传到本地，向会话提供文件路径 |
| 文件夹 | 逐个处理所选文件，保留相对目录结构；图片照样走附件通道 |

图片作为消息附件发送，模型能直接看到图片本身。能否理解图片取决于宿主接入的视觉模型。

## 实现

浏览器端通过宿主的扩展接口注册入口、文件选择器和草稿操作；Node.js 服务端接收文件，返回路径、类型和文本预览。上传时限制单个文件大小，写入时不覆盖已有文件，并设置本地文件权限。

插件不声明额外的运行依赖，客户端直接使用宿主提供的 React 和服务。

## 测试

[`client.test.cjs`](https://github.com/zhousun55-byte/dsh-postman/blob/main/client.test.cjs) 用 Node 的 VM 模块和模拟宿主接口跑了 18 个断言，覆盖上传入口、图片与文本分流、文件夹处理和草稿生成。

[返回主页](../README.md)
