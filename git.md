# Git 全面命令和操作总结

---

## 一、Git 基本配置
```bash
git config --global user.name "你的名字"           # 设置用户名
git config --global user.email "你的邮箱"          # 设置邮箱
git config --global core.editor "vim"              # 设置默认编辑器
```

---

## 二、仓库操作
```bash
git init                 # 初始化本地仓库
git clone 仓库地址       # 克隆远程仓库
```

---

## 三、状态查看
```bash
git status               # 查看当前工作区状态
git log                  # 查看提交历史
git log --oneline        # 简洁模式查看提交历史
git diff                 # 查看文件改动
```

---

## 四、文件操作
```bash
git add 文件名           # 暂存指定文件
git add .                # 暂存所有更改
git commit -m "备注"     # 提交更改
git rm 文件名            # 删除文件
git mv 旧名 新名         # 重命名文件
```

---

## 五、分支管理
```bash
git branch               # 查看所有本地分支
git branch -r            # 查看所有远程分支
git branch -a            # 查看所有分支
git branch 分支名         # 创建新分支
git checkout 分支名       # 切换分支
git checkout -b 分支名    # 创建并切换分支
git merge 分支名          # 合并分支
git branch -d 分支名      # 删除分支
```

---

## 六、远程仓库
```bash
git remote -v                         # 查看远程仓库地址
git remote add origin 仓库地址        # 添加远程仓库
git remote set-url origin 新地址           # 更换远程仓库
git remote remove origin              # 删除远程仓库

git push -u origin main               # 初次推送并建立跟踪关系
git push                              # 推送更改
git pull                              # 拉取最新代码
git fetch                             # 获取远程代码（不合并）
```

---

## 七、标签操作
```bash
git tag                               # 查看所有标签
git tag 标签名                         # 创建标签
git tag -d 标签名                      # 删除标签
git push origin 标签名                 # 推送标签
git push origin --tags                 # 推送所有标签
```

---

## 八、撤销与回退
```bash
git checkout -- 文件名                 # 撤销对某文件的未提交修改
git reset HEAD 文件名                  # 撤销已暂存的文件
git reset --hard 提交ID                # 强制回退到指定提交
git revert 提交ID                      # 生成新的撤销提交
```

---

## 九、日志简化查看
```bash
git log --graph --oneline --all --decorate  # 图形化简洁日志
```

---

## 十、其他常用命令
```bash
git stash               # 临时保存当前修改
git stash pop           # 取出临时保存修改
git clean -fd           # 清理未被 Git 跟踪的文件（慎用）
```

---

## 合计
| 功能 | 命令 |
|-------|------------------|
| 查看本地分支 | `git branch` |
| 查看远程分支 | `git branch -r` |
| 查看全部分支 | `git branch -a` |
| 更换远程仓库 | `git remote set-url origin 新地址` |
| 创建并切换分支 | `git checkout -b 分支名` |
| 合并分支 | `git merge 分支名` |
| 推送并建立跟踪 | `git push -u origin main` |

---

如果需要更详细操作图或性能测试流程，可随时请求我提供进阶版本。

