# vitepress-docs-site-template [![update website](https://github.com/Otto-J/vitepress-docs-site-template/actions/workflows/main.yml/badge.svg?branch=main&event=push)](https://github.com/Otto-J/vitepress-docs-site-template/actions/workflows/main.yml)

> 以下内容请手动删除，仅供参考。

## 背景

很多人希望利用 vitepress 管理文档，并制作一个文档网站，这里提供一个快捷模板，使用该模板可以很快建立起托管到 github pages 上。

## 目前状态

`alpha` 你需要有看懂代码的能力。

## 使用方式

使用本模板会很容易，请按照下面步骤操作：

1. 选择 "use template" 使用本模板，并建立仓库。

![create repo](/docs/assets/create-repo.png)

2. 准备 token。点击 [https://github.com/settings/tokens/new](https://github.com/settings/tokens/new) 按照截图进行操作，名称 Name 和 过期时间 Expiration 可自定义。

![new token](/docs/assets/new-token.png)

3. 点击创建之后，会看到下图，请务必点击第二个圆框处进行自动复制，并将复制到的 token 保存到妥善位置。

![copy token](/docs/assets/copy-token.png)

4. 设置仓库 street。这一步是把 token 和仓库操作绑定。进入仓库设置 `/settings/secrets/actions`，点击 `New repository secret`。分别创建：

- Name: token，Value 刚才复制的 token
- Name: email，Value 输入你的邮箱

5. 回到仓库仓库 `/actions/workflows/main.yml` ，点击 `Run Workflows` 手动运行一次。

6. 如果运行成功。可以访问。`你的用户名.github.io/仓库名` 页面。就看到结果了。

7. 克隆仓库，执行依赖安装，请任意选择 `pnpm/yarn/npm` ，个人推荐 `pnpm` 理由是更轻更快。
8. 修改 `package.json` 中的相关字段，比如 `name` `author` `repository` `homepage` 等
9. 观察并维护 `docs/` 文件夹内容
10. 后续提交 commit 就可以自动维护了。

## roadmap

- [x] 补充 actions 里创建 secrets 的介绍
- [x] 完善 readme.md
- [x] actions 里尽可能使用变量，减少操作步骤
- [ ] 完善自动生成 `data.json` 的脚本
- [ ] 推广试用
- [ ] gitlab/gitee/coding 支持
