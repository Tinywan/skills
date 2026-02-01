# Tinywan Skills - 多语言开发技能集

这是 Tinywan 的 Claude Code Skills 集合，专注于 PHP 及其主流框架的开发技能，未来将扩展到 JavaScript、Python、Java 等多种语言。

## 📦 包含的 Skills

| Skill | 描述 | 状态 |
|-------|------|------|
| [tinywan-php-core](./skills/tinywan-php-core) | 通用 PHP 开发技能，支持 PSR 标准、安全最佳实践 | ✅ 可用 |
| [tinywan-php-laravel](./skills/tinywan-php-laravel) | Laravel 框架专用技能 | ✅ 可用 |
| [tinywan-php-thinkphp](./skills/tinywan-php-thinkphp) | ThinkPHP 6.1 框架专用技能 | ✅ 可用 |
| [tinywan-php-webman](./skills/tinywan-php-webman) | Webman 2.1 高性能框架专用技能 | ✅ 可用 |

## 🚀 快速开始

### 方式一：自动安装（推荐）

在 Claude Code 中使用自然语言安装：

```bash
帮我安装 tinywan-php-core skill，项目地址是：https://github.com/tinywan/skills/tree/master/skills/tinywan-php-core
```

### 方式二：手动安装

1. 下载对应的 skill 文件夹
2. 复制到你的 Claude Code skills 目录：
   - Windows: `%USERPROFILE%\.claude\skills\`
   - macOS/Linux: `~/.claude/skills/`

```bash
# 示例：安装 PHP Core skill
cd ~/.claude/skills
git clone https://github.com/tinywan/skills.git temp
cp -r temp/skills/tinywan-php-core ./
rm -rf temp
```

### 方式三：项目级安装

在你的项目根目录创建 `.claude/skills/` 目录：

```bash
mkdir -p .claude/skills
cd .claude/skills
# 复制需要的 skill 文件夹
```

## 💡 使用方法

安装后，直接在 Claude Code 中提及 skill 名称即可使用：

```bash
# 使用完整名称
用 tinywan-php-core skill 创建一个用户认证类

# 使用简短名称（Claude 会自动识别）
用 webman skill 创建一个 WebSocket 服务

# 自动识别（Claude 会根据上下文自动选择合适的 skill）
帮我写一个 Laravel 中间件来验证 JWT token
```

## 📚 Skill 详细说明

### tinywan-php-core

通用 PHP 开发技能，包含：
- ✅ PSR 标准代码生成（PSR-1, PSR-4, PSR-12）
- ✅ 类型提示和返回类型（PHP 7.4+）
- ✅ 安全最佳实践（防 SQL 注入、XSS、CSRF）
- ✅ 性能优化建议
- ✅ PHPUnit 测试生成
- ✅ Composer 依赖管理
- ✅ 模型命名规范（使用 Model 后缀）

[查看完整文档](./skills/tinywan-php-core/SKILL.md)

### tinywan-php-laravel

Laravel 框架专用技能，包含：
- ✅ 控制器、模型、迁移生成
- ✅ Eloquent ORM 最佳实践
- ✅ 中间件和服务提供者
- ✅ API 资源和表单验证
- ✅ 队列和任务调度
- ✅ 模型命名规范（UserModel、PostModel 等）

[查看完整文档](./skills/tinywan-php-laravel/SKILL.md)

### tinywan-php-thinkphp

ThinkPHP 6.1 框架专用技能，包含：
- ✅ 控制器、模型、验证器生成
- ✅ 路由配置和中间件
- ✅ 数据库查询构造器
- ✅ 命令行工具
- ✅ 事件监听和异常处理
- ✅ 模型命名规范（UserModel、OrderModel 等）

[查看完整文档](./skills/tinywan-php-thinkphp/SKILL.md)

### tinywan-php-webman

Webman 2 高性能框架专用技能，包含：
- ✅ 高性能控制器和路由
- ✅ WebSocket 实时通信
- ✅ 自定义进程和定时任务
- ✅ 异步编程（HTTP、数据库）
- ✅ Redis 操作和连接池
- ✅ 性能优化建议

[查看完整文档](./skills/tinywan-php-webman/SKILL.md)

## 🎯 使用示例

### 示例 1：创建 Laravel 控制器

```bash
用 tinywan-php-laravel skill 创建一个博客文章的 CRUD 控制器
```

### 示例 2：代码安全审查

```bash
用 tinywan-php-core skill 审查 UserController.php 的安全问题
```

### 示例 3：生成测试

```bash
用 tinywan-php-core skill 为 OrderService 类生成 PHPUnit 测试
```

### 示例 4：创建 WebSocket 服务

```bash
用 tinywan-php-webman skill 创建一个聊天室 WebSocket 服务
```

更多示例请查看 [examples](./examples) 目录。

## 🛠️ 命名规范

### Skill 命名格式

```
{author}-{language}-{framework/tool}

示例：
- tinywan-php-core        # 通用 PHP
- tinywan-php-laravel     # Laravel 框架
- tinywan-php-thinkphp    # ThinkPHP 框架
- tinywan-js-react        # React（未来）
- tinywan-python-django   # Django（未来）
```

### 模型命名规范

所有模型类必须使用 `Model` 后缀：

```php
// ✅ 正确
class UserModel extends Model {}
class OrderModel extends Model {}

// ❌ 错误
class User extends Model {}
class Order extends Model {}
```

详见 [MODEL_NAMING_CONVENTION.md](./MODEL_NAMING_CONVENTION.md)

## 🗂️ 项目结构

```
.
├── .claude/
│   └── skills/
│       └── tinywan-php-core/      # 本地开发用
├── skills/                         # 公开分享的 skills
│   ├── tinywan-php-core/
│   ├── tinywan-php-laravel/
│   ├── tinywan-php-thinkphp/
│   └── tinywan-php-webman/
├── examples/                       # 使用示例
├── MODEL_NAMING_CONVENTION.md     # 模型命名规范
└── README.md                      # 本文件
```

## 🌟 未来规划

- [ ] tinywan-js-react - React 开发技能
- [ ] tinywan-js-vue - Vue.js 开发技能
- [ ] tinywan-python-django - Django 框架支持
- [ ] tinywan-python-flask - Flask 框架支持
- [ ] tinywan-java-spring - Spring Boot 支持

## 🤝 贡献指南

欢迎提交 Pull Request！请确保：
1. 遵循 `{author}-{language}-{framework}` 命名规范
2. 在 SKILL.md 中包含完整的 YAML frontmatter（name、description、author、version）
3. 提供清晰的使用示例
4. 遵循模型命名规范（Model 后缀）

### 创建新的 Skill

每个 skill 必须包含一个 `SKILL.md` 文件，格式如下：

```markdown
---
name: tinywan-php-framework
description: 框架的简短描述
author: Tinywan
version: 1.0.0
---

# 框架名称开发技能

详细的 skill 说明和使用指南...
```

## 📝 许可证

MIT License

## 🔗 相关链接

- [Claude Code 官方文档](https://claude.ai/code)
- [Anthropic Skills 仓库](https://github.com/anthropics/skills)
- [Claude Skills 教程](https://mp.weixin.qq.com/s/WJjieivijcLedHTR84zk3g)

## 📮 反馈和支持

如有问题或建议，请提交 Issue 或联系维护者。

---

**作者**: Tinywan
**仓库**: https://github.com/tinywan/skills
**版本**: 1.0.0
