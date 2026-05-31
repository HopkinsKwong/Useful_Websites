# 有用的网站

## Claude Code 安装

* 实验室Linux服务器配置Claude Code
  * https://zhuanlan.zhihu.com/p/1974858513684657231

* Claude Code 安装报错 “不兼容 Windows 版本“ 完整修复记录（WinGet安装）
  * https://deepseek.csdn.net/6a05ae8c10ee7a33f2728d49.html
* 五分钟国内配置Claude Code+DeepSeek模型，完全操作指南
  * https://zhuanlan.zhihu.com/p/2010102236194296717
* 别让 Claude Code 一直问你"能不能执行"：权限配置完全指南
  * https://zhuanlan.zhihu.com/p/2020783664926061754

## Huggingface连接不上

* 跑代码连接不上huggingface怎么办？
  * https://zhuanlan.zhihu.com/p/689290456

## Github

* 登陆
  * sudo apt install gh -y # Ubuntu/Debian
  * gh auth login
  * gh auth setup-git # 绑定git凭据，后续git自动用gh登录
  * git clone https://github.com/合作者用户名/私有仓库名.git
* fork
  ```bash
  # 1. 克隆【你自己的 Fork 仓库】到本地
  git clone git@github.com:你的用户名/仓库名.git
  
  # 2. 进入仓库目录
  cd 仓库名
  
  # 3. 绑定【合作者原库】为上游 upstream（只需要执行一次）
  git remote add upstream git@github.com:合作者用户名/仓库名.git
  git remote add upstream https://github.com/合作者用户名/仓库名.git
  
  # 4. 检查远程配置，确认 origin(你的fork)、upstream(原库)
  git remote -v
  
  # ========== 日常第一步：先同步原库最新代码（保证本地主干是最新） ==========
  # 5. 切换到本地主分支 main
  git checkout main
  
  # 6. 拉取合作者原库的最新代码
  git fetch upstream
  
  # 7. 把原库最新代码合并到本地 main，出现冲突就手动修改文件
  git merge upstream/main
  
  # 8. 将同步后的 main 推送到【你自己的 Fork】
  git push origin main
  
  # ========== 开始自己开发（新建专属开发分支 my-dev） ==========
  # 9. 基于 main 创建并切换到开发分支 my-dev（首次创建执行，后续不用再建）
  git checkout -b my-dev
  
  # 10. 修改代码完成后，把改动加入暂存区
  git add .
  
  # 11. 本地提交改动，填写备注
  git commit -m "feat: 增加了xxx功能/修复了xxx问题"
  
  # 12. 将开发分支推送到【你自己的 Fork】
  git push origin my-dev
  ```

## SSH

* VSCode配置 SSH连接远程服务器+免密连接教程
  * https://zhuanlan.zhihu.com/p/667236864
