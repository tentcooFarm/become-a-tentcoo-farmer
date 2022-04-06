# Become A Tentcoo Farmer

[![Build And Deploy](https://github.com/tentcooFarm/become-a-tentcoo-farmer/actions/workflows/ci.deploy.yml/badge.svg)](https://github.com/tentcooFarm/become-a-tentcoo-farmer/actions/workflows/ci.deploy.yml)

来自养鸡农场的师兄师姐杂七杂八的碎碎念

## 本地编译

本项目使用 MkDocs，如需构建，你需要先在本地安装 Python 并执行:

```shell
pip install -r requirements.txt
```

以下是 mkdocs 常用的指令

* `mkdocs serve` - 开启实时更新的预览服务器
* `mkdocs build` - 构建静态网站
* `mkdocs -h` - 搞不定了！我要看文档

## 项目结构

    mkdocs.yml    # 配置文件，不要随便改，除非你知道自己在干啥
    docs/
        index.md  # 文档首页
        ...       # 其他知识库的文件 ...
