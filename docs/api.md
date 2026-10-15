# API 参考

本页是 API 文档的编写示例，展示常见的接口说明格式。

## 用户接口

### 获取用户信息

获取指定用户的详细信息。

- **URL**：`GET /api/users/{id}`
- **参数**：

| 参数 | 类型 | 必填 | 说明 |
| --- | --- | --- | --- |
| `id` | integer | 是 | 用户 ID |

- **响应示例**：

```json
{
  "code": 0,
  "data": {
    "id": 1,
    "name": "Alice",
    "email": "alice@example.com"
  },
  "message": "success"
}
```

### 创建用户

创建一个新用户。

- **URL**：`POST /api/users`
- **请求体**：

```json
{
  "name": "Bob",
  "email": "bob@example.com"
}
```

- **响应**：返回 `201 Created`， body 中包含新用户的 `id`。

## 错误码

| 错误码 | 含义 |
| --- | --- |
| 0 | 成功 |
| 1001 | 参数错误 |
| 1002 | 用户不存在 |
| 5000 | 服务器内部错误 |
