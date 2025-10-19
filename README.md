如果没有创建git源，则：git init

若有改动代码，则保存代码文件后：git add 受变动的文件名
提交暂存区修改，“”里填写一些修改的提示：git commit -m “”
如果github没有建立仓库，就在GitHub repository上新建一个repo，这个直接在GitHub页面里找到手动添加即可，不用命令行
复制以下一段到命令行，将改动上传至仓库：
git remote add origin https://github.com/fengqin1108/test_git.git
git branch -M main      #强制重命名
git push -u origin main #推送并设置上游才能把改名同步，会把本地的 main 分支推送到名为 origin 的远端仓库，并把本地 main 与远端 origin/main 建立“上游（tracking）”关系（以后可只用 git push / git pull）。若远端不存在 origin/main，会在远端创建该分支。-u 等同于 --set-upstream（只需执行一次以建立追踪），后续可以只运行 git push 或 git pull 即可同步该分支。




【# 可选：切到工作分支并同步远端
git branch --show-current
git fetch origin
git pull

# 查看状态
git status

# 编辑并保存文件（确保在编辑器里保存）
# 查看改动（可选）
git diff assighment_1/a1.py

# 暂存并提交
git add assighment_1/a1.py
git commit -m "修正 a1.py: 描述改动"

# 推送（如果已设置上游）
git push
# 若第一次推送或未设置上游：
# git push -u origin main】
