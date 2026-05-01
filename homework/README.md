# Git 学习实践记录

## 一、学习资料来源

- [Git 官方文档](https://git-scm.com/doc)
- [Pro Git 中文版](https://git-scm.com/book/zh/v2)
- [GitHub Docs](https://docs.github.com/zh)
- [菜鸟教程 - Git](https://www.runoob.com/git/git-tutorial.html)

## 二、实践流程

### 2.1 安装 Git

1. 访问 https://git-scm.com/ 下载 Windows 版本
2. 运行安装程序，使用默认选项完成安装
3. 右键打开 Git Bash，验证安装：
   ```bash
   git --version

### 2.2 配置 Git
1. 配置用户名和邮箱
    git config --global user.name "Cihper-milro"
    git config --global user.email "你的邮箱"

2. 查看配置
    git config --list

### 2.3 创建仓库并提交

1. 创建项目文件夹
    mkdir homework
    cd homework

2. 初始化 Git 仓库
    git init

3. 创建 Python 文件
    echo "print('Hello, Git!')" > hello.py

4. 第一次提交
    git add hello.py
    git commit -m "第一次提交：添加 hello.py"

### 2.4 关联远程仓库并推送

1. 添加远程仓库
    git remote add origin https://github.com/Cihper-milro/homework.git

2. 推送代码
    git branch -M main
    git push -u origin main

## 三、提交记录说明

|提交序号|主要内容|
|--|--|
|第1次|创建 hello.py，实现简单打印功能|
|第2次|添加 name 变量，优化输出|
|第3次|添加 input 功能，实现交互式问候|
|第4次|添加项目说明文档|

## 四、遇到的问题及解决方法
问题1：Recv failure: Connection was reset
原因：网络问题导致 HTTPS 协议连接 GitHub 不稳定。
解决办法：改用 SSH 协议

问题2：remote origin already exists
原因：之前已经添加过 remote 配置。
解决方法：更新已有的 remote 地址

## 五、Git 学习心得

通过本次实践，我掌握了 Git 的基本使用流程：

### 5.1 核心概念
- **工作区**：电脑中实际看到的目录
- **暂存区**：`git add` 后的临时区域  
- **本地仓库**：`git commit` 后的提交记录
- **远程仓库**：GitHub 上的代码托管

### 5.2 常用命令

| 命令 | 作用 |
|------|------|
| `git init` | 初始化仓库 |
| `git add` | 添加到暂存区 |
| `git commit -m` | 提交到本地仓库 |
| `git push` | 推送到远程仓库 |
| `git status` | 查看状态 |
