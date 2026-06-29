# Material for MkDocs + GitHub Pages 发布说明

`Answer` 文件夹已经整理成一个可以直接上传到 GitHub 的 Material for MkDocs 文档站项目。

## 目录结构

| 文件 / 目录 | 作用 |
| --- | --- |
| `README.md` | MVP 前端说明原始 Markdown |
| `小微ServiceOps能力可行性与价值指标分析.md` | 主分析文档原始 Markdown |
| `小微ServiceOps项目选择思考过程总结.md` | 思考过程总结原始 Markdown |
| `assets/` | 原始截图资源 |
| `mkdocs.yml` | MkDocs 配置 |
| `requirements.txt` | GitHub Actions 构建依赖 |
| `docs/` | 文档站使用的 Markdown 副本 |
| `.github/workflows/deploy.yml` | GitHub Pages 自动发布工作流 |

## 发布到 GitHub Pages

1. 在 GitHub 新建一个仓库，例如 `xiaowei-serviceops-docs`。
2. 把 `Answer` 文件夹里的所有内容上传到这个仓库根目录。
3. 进入仓库 `Settings -> Pages`。
4. 在 `Build and deployment` 中选择 `GitHub Actions`。
5. 推送到 `main` 分支后，等待 Actions 跑完。
6. 成功后，GitHub 会给出公开访问链接。对方不需要登录即可查看。

## 本地预览

如果本机 Python 环境可用，可以在 `Answer` 目录运行：

```powershell
pip install -r requirements.txt
mkdocs serve
```

然后打开：

```text
http://127.0.0.1:8000
```

当前这台机器上的 `python` 命令报 Windows 登录会话错误，所以我没有在本地完成构建验证；GitHub Actions 会在云端安装依赖并构建。
