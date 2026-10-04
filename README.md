# astrbot_plugin_sakisaki

🎮 一个为 ~~三角初音~~ AstrBot 打造的趣味小游戏插件 —— 香草小祥追击！

---

## ✨ 功能概览

- 🔍 监听关键词 `saki` 或 `小祥`
- 🎯 随机概率判断是否“追上”小祥
- 📊 查询排行榜（含冷却机制）
  - 排行榜数据会记录在以下文件中：
    ```
    /data/plugin_data/astrbot_plugin_sakisaki/sakisaki_data.json
    ```
  - 支持清除排行榜功能（仅限管理员）

- 📷 成功追击后自动发送图片（首次自动联网下载）

---

## 🛠 安装指南

1. 将本插件解压至 AstrBot 插件目录下：
   ```
   data/plugin/astrbot_plugin_sakisaki/
   ```
2. 也可以直接使用 AstrBot 自带的插件市场进行安装。

---

## 🔗 自动下载图片地址

插件首次启动时会自动从以下链接下载图片：

```
https://raw.githubusercontent.com/oyxning/astrbot_plugin_sakisaki/refs/heads/master/sjp.jpg
```

保存到路径：

```
/data/plugin_data/astrbot_plugin_sakisaki/sjp.jpg
```

---

## 🧾 指令示例

| 触发内容              | 功能说明           |
|-----------------------|--------------------|
| saki / 小祥           | 触发小游戏事件     |
| saki排行 / 小祥排行   | 查看追击排行榜     |
| saki清除排行          | 清除排行榜数据 |

---

## 😂 开发备注

能写出这个，家里得请高人了。  

1. 用户可以在 `main.py` 文件中直接修改概率和其他参数：
   - 修改成功概率：`self.success_prob = 0.25`
   - 修改失败概率上限：`self.max_fail_prob = 0.95`
   - 修改游戏触发次数限制：`self.trigger_limit = 3`
   
2. 如遇问题，可在 [GitHub Issues](https://github.com/oyxning/astrbot_plugin_sakisaki/issues) 提交错误报告。

3. 插件会在每次触发时自动检查是否需要下载最新的图片。

4. 只建议一个群内只有一个Bot实例运行此插件，以避免循环触发。

## 📜 许可证

本插件遵循 [MIT 许可证](https://opensource.org/license/mit/)，欢迎自由使用和修改。

## 💡 联系作者

如有紧急问题，请联系邮箱：shy0074@tongujiyu.cn


