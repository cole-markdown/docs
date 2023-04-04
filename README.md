本仓库保存了 [CloudExploer-Lite 项目]() 的 [官方文档](https://fit2cloud.com/cloudexplorer-lite/docs/)，该文档使用 [MkDocs]() 文档框架下的 [Material for MkDocs]() 主题进行构建。

## 本地开发

### 克隆本仓库
```bash
git clone https://github.com/CloudExplorer-Dev/doc.git
```

### 安装依赖
```bash
cd docs
pip install -r requirements/requirements.txt
```

### 修改文档内容
本文档的文档结构定义在 `mkdocs.yml` 文件中，文档的具体内容均在 `docs` 目录中。
```yaml
..........
nav:
    - 项目介绍: index.md
    - 系统架构: system_arch.md
    - 安装部署: 
        - 在线安装: installation/online_installation.md
        - 离线安装: installation/offline_installation.md
    - 用户手册:
        - 管理中心: user_manual/general.md
            - 云账号: user_manual/dataset_configuration.md 
            - 用户管理: user_manual/dataset_configuration.md
            - 日志管理: user_manual/dataset_configuration.md
            - 系统设置: user_manual/dataset_configuration.md
        - 云主机服务: user_manual/datasource_configuration.md
        - 云账单: user_manual/dataset_configuration.md
            - 账单总览: user_manual/dataset_configuration.md
            - 账单明细: user_manual/dataset_configuration.md
            - 自定义账单: user_manual/dataset_configuration.md
            - 分账设置: user_manual/dataset_configuration.md
        - 运营分析: user_manual/view_generation.md
        - 安全合规: user_manual/dashboard_generation.md
    - 关于:
        - 联系我们: about/contact.md

..........
```

文档内容使用 markdown 语法编写，若要添加新的文档，需要先在 `mkdocs.yml` 文件中的 `nav` 部分增加对应章节导航。

### 本地调试文档
```bash
mkdocs serve
```
执行上述命令后，可通过 `http://127.0.0.1:8000` 地址查看生成的文档内容，当修改文档后，页面内容会自动更新。

### 构建文档
```bash
mkdocs build
```

执行上述命令后，会在 `site` 目录下生成文档站点的静态文件，将目录中的内容复制到任意 HTTP 服务器上即可完成文档的部署。

## 帮助完善文档

### Fork 文档仓库
点击仓库右上角的 `fork` 按钮，复制本仓库到自己的 github 账号。

### 克隆 fork 后的仓库
```bash
git clone https://github.com/your-github-account/docs.git
```

### 本地修改并调试

### Push 修改内容到 GitHub 仓库

### 提交 Pull Request 到本仓库
