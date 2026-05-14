# excalidraw_local

这是基于 `D:\code-open\excalidraw-mcp` 执行 `pnpm build` 后产物整理出来的本地 MCP。

## 目录结构

- `dist/index.js`：MCP 服务入口
- `dist/mcp-app.html`：MCP App 的前端资源
- `manifest.json`：MCP 清单

## 启动方式

### stdio

```bash
node dist/index.js --stdio
```

### HTTP

```bash
node dist/index.js
```

默认会监听：

```text
http://localhost:3001/mcp
```

## MCP 配置示例

```json
{
  "mcpServers": {
    "excalidraw_local": {
      "command": "node",
      "args": [
        "D:\\ai-work\\mcp\\excalidraw_local\\dist\\index.js",
        "--stdio"
      ]
    }
  }
}
```
