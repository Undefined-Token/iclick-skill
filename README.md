# iclick-skill

iClick（爱触云）iOS 免越狱自动化技能包（OpenClaw Skill）。

## 功能概览

- 设备列表/状态查询
- 获取屏幕截图
- 点击/滑动/输入/按键等自动化动作

## 使用方式（命令行）

将方法名与 JSON 参数传给入口脚本：

```bash
node server.js <method> '<JSON参数>'
```

- `<method>`：方法名（字母/数字/下划线），例如 `devices`、`getDevice`、`getScreenShot`、`click`、`swipe`、`sendText` 等
- `<JSON参数>`：可选；必须是合法 JSON 字符串，建议用单引号包裹

示例：

```bash
node server.js devices
node server.js getScreenShot '{"deviceId":"xxx"}'
node server.js click '{"deviceId":"xxx","x":100,"y":200}'
```

## 安装依赖

```bash
pnpm i
```

（也可使用 `npm i`）

## 目录结构（约定）

- `server.js`: 命令行入口
- `util/`: iClick 连接与调用封装
- `command/`: 可选的本地命令实现（优先于直连调用）
- `icon/`: 图标资源
- `SKILL.md`: OpenClaw 技能声明与更完整的使用说明
