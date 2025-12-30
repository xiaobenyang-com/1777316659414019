# HTTP代理服务器 Public Promo

一个轻量级的无数据库、无需配置的HTTP代理服务器，内置数据源，适用于快速开发和测试。
A lightweight, database-free, configuration-free HTTP proxy server with built-in data sources, suitable for rapid development and testing.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| jutuike.public_promo_list | GET /api/mcp/jutuike/public_promo_list with optional query params. |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659414019](https://mcp.xiaobenyang.com/inspector/1777316659414019)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659414019](https://mcp.xiaobenyang.com/inspector/1777316659414019)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "HTTP代理服务器": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659414019/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "HTTP代理服务器": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659414019/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "HTTP代理服务器": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659414019",
          },
          "transport": "stdio"
        }
      }
}

```
