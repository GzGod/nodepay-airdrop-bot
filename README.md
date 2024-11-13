好的，让我们将这个README文件翻译成中文。

---

# nodepay-airdrop-bot

一个用于自动化Nodepay空投交互的机器人，包括会话管理和具有灵活连接选项（代理或直接）的ping操作。

## 需求

1. **Node.js** (版本 14 或更高)
2. **npm** (Node 包管理器)

## 安装

要开始使用Nodepay Airdrop Bot：

1. 克隆仓库：

    ```bash
    git clone https://github.com/Gzgod/nodepay-airdrop-bot.git
    cd nodepay-airdrop-bot
    ```

2. 安装依赖项：

    ```bash
    npm install
    ```

## 配置

在运行机器人之前，你需要进行配置：

### 1. `token.txt` (必需)

获取你的Bearer令牌：

1. **注册一个Nodepay帐户**：
   - 前往[Nodepay注册页面](https://app.nodepay.ai/register?ref=Pf4yQYI8sYwLNT5)并注册一个帐户。

2. **获取你的令牌**：
   - 在浏览器中打开**开发者工具**（右键 > 检查 或按 `Ctrl+Shift+I`）。
   - 在开发者工具中转到**控制台**选项卡。
   - 输入以下命令以获取你的令牌：

     ```javascript
     localStorage.getItem('np_webapp_token')
     ```

   - 这将返回Bearer令牌。**复制令牌**（不包括`Bearer`前缀，只是字母数字字符串）。

3. **将令牌粘贴到 `token.txt` 中**：
   - 在项目根目录中创建一个`token.txt`文件，并将你的令牌粘贴到文件中（每行一个令牌）。

示例 `token.txt`：

```text
ey...
ey...
ey...
```

### 2. `proxy.txt` (可选)

仅在你选择使用代理运行机器人时需要。

- 在 `proxy.txt` 中添加你的代理详细信息。每行应具有以下格式：

  ```text
  host:port:username:password
  ```

- 示例：

  ```text
  123.45.67.89:8080:username:password
  123.45.67.89:8080:username:password
  123.45.67.89:8080:username:password
  ```

## 运行机器人

要启动机器人，运行以下命令：

```bash
npm start
```

启动机器人后，你将被提示：

1. 选择使用代理还是直接连接
2. 选择单账户模式还是多账户模式

### 连接模式

1. **代理模式**
   - 需要有效的 `proxy.txt` 文件
   - 使用不同的IP地址进行连接
   - 更适合运行多个账户
   - 操作更匿名

2. **直接模式**
   - 不需要代理配置
   - 使用你设备的IP地址
   - 设置更简单
   - 适合单账户使用

## 日志

机器人将记录所有活动，包括：

- 每个会话（UID）的连接状态
- 每个会话的ping状态
- 使用的连接类型（代理/直接）
- IP地址信息（使用代理时）

日志存储在 `bot.log` 中，也可以在控制台中查看。

## 捐赠

如果你想支持这个项目的发展，可以使用以下地址进行捐赠：

- **Solana**: `GLQMG8j23ookY8Af1uLUg4CQzuQYhXcx56rkpZkyiJvP`
- **EVM**: `0x960EDa0D16f4D70df60629117ad6e5F1E13B8F44`
- **BTC**: `bc1p9za9ctgwwvc7amdng8gvrjpwhnhnwaxzj3nfv07szqwrsrudfh6qvvxrj8`

## 许可证

此项目根据MIT许可证授权 - 详情请参阅 [LICENSE](LICENSE) 文件。

---

希望这个翻译对你有帮助！如果你有其他问题，请随时告诉我。
