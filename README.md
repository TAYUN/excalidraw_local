# excalidraw_local

`excalidraw_local` 是一个基于 Excalidraw 的本地 MCP 服务，用来生成、预览和编辑手绘风格的图表内容。

它适合需要通过 MCP 工具流式渲染 Excalidraw 图形的场景，支持前端视图展示、交互式编辑、检查点恢复以及导出能力。

## 项目结构

- `dist/index.js`：MCP 服务入口
- `dist/mcp-app.html`：MCP App 前端资源
- `manifest.json`：MCP 清单与元数据
- `docs/logo.png`：项目图标资源

## 运行方式

### stdio

```bash
node dist/index.js --stdio
```

### HTTP

```bash
node dist/index.js
```

默认监听地址：

```text
http://localhost:3001/mcp
```

## MCP 配置示例

下面示例表示通过 Node 启动当前项目构建产物；实际使用时，请根据你的安装目录或仓库位置调整脚本路径。

```json
{
  "mcpServers": {
    "excalidraw_local": {
      "command": "node",
      "args": [
        "dist/index.js",
        "--stdio"
      ]
    }
  }
}
```
