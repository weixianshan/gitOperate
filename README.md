git 操作步骤:
1、linux git与github连接:
  安装git: sudo apt-get install git
  创建github账号
  生成ssh key, 使用命令 "ssh-keygen -t ras -C 'your_email@youemail.com'"
  回到github, 进入Account Settings, 选择SSH Keys, Add SSH Key >>> title随便填, key就是~/.ssh/id_rsa.pub的内容
  测试ssh key 是否成功, 使用命令 "ssh -T git@github.com", 出现You’ve successfully authenticated, but GitHub does not provide shell access.表示已成功连山github
  配置Git的配置文件(username&email): git config --global user.name "your account name" && git config --global user.email "your account email"

2、git提交项目到github远程仓库上:
  切换到要提交的项目目录下
  初始化一个本地库: git init
  添加文件到本地仓库: git add filename
  (本地库内删除: git rm filename)
  提交到本地库并备注(此时变更仍在本地): git commit -m "first commit"
  自动更新变化的文件: git commit -a(a --- auto)
  将本地文件提交到github的 projectname 版本库中,此时才更新了本地变更到github服务上: git push origin master
  (注: 修改文件后 , 从git add 或者 git commit -a重复操作)
