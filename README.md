"# mother_BTC_record" 
# 第一种办法使用token连接库
# 在GitHub上创建新仓库，获取其远程仓库URL
# 例如：https://github.com/username/new-repository.git
 
# 在本地初始化git仓库（如果你还没有的话）
git init
 
# 添加文件到本地git仓库中
git add .
 
# 提交你的改变到本地仓库
git commit -m "Initial commit"
 
# 将本地仓库关联到GitHub仓库
git remote add origin https://github.com/username/new-repository.git
 
# 拉回仓库
git pull -u origin main

# 推送你的代码到GitHub
git push -u origin main

# 第二种办法使用ssh公钥连接
# 在本地初始化git仓库（如果你还没有的话）
git init
 
# 添加文件到本地git仓库中
git add .
 
# 提交你的改变到本地仓库
git commit -m "Initial commit"

# 删除原来的关联remote
git remote remove origin
# 将本地仓库关联到GitHub仓库
git remote add origin git@github.com:qcao2003/mother_BTC_record.git

# 修改仓库的端口为443
vim ~/.ssh/config
# 内容输入
Host github.com
  Hostname ssh.github.com
  Port 443

# 拉回仓库
git pull origin main

# 推送你的代码到GitHub
git push -u origin main

# 在github添加本地计算机公钥
cd ~
rm -r .ssh/
ssh-keygen -t rsa -C 276914192@qq.com
cd .ssh
cat id_rsa.pub
# 复制公钥到github上 Settings->SSH and GPG keys

