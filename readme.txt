    learn git 
 配置当前仓库用户及邮箱
git config user.name "Your Name"
git config user.email "email@xx.com"

1. 建一个空目录
    mkdir 目录名
2.建可以管理的仓库
    cd 到该目录下
    git init 
3.提交文件
    a.查看状态有未提交的会显示
        git status 
    b.提交到暂存区(注意，可反复多次使用，添加多个文件)
        git add +文件名及后缀
    c.提交完成
        git commit -m +"注释，这次做的什么修改"
    两步骤完成文件提交到Git仓库
 a.如果中间有需要修改的文件可以再修
   git diff +文件
    可以查看做了什么修改
4.提交到远程仓库
    i.注册一个github账号
    ii.建ssh密钥
    ssh-keygen -t rsa -C "邮箱名称"
    一路回车，创建成功的话在用户主目录里找到.ssh目录，里面有id_rsa和id_rsa.pub两个文件，
    这两个就是SSH Key的秘钥对，id_rsa是私钥，不能泄露出去，id_rsa.pub是公钥，可以告诉任何人。
    登陆GitHub，打开“Account settings”，“SSH Keys”页面：
    点“Add SSH Key”，填上任意Title，在Key文本框里粘贴id_rsa.pub文件的内容：即可
    a.关联到远程库
        git remote add origin git@github.com:账户名/远程仓库名.git
    b.把本地库的所有内容推送到远程库上
        git push -u origin master
    c.提交过之后，只要本地作了提交，就可以通过命令：
        git push origin master
5.用户名的修改
    a.查看远程用户地址
     git remote -v  
    b.修改远程地址
     git remote set-url origin https://github.com/账户名/远程仓库的名字.git
     这样也可以
     git remote set-url origin github.com/账户名/远程仓库的名字.git
    c.修改后再看一下
     git remote -v  
6.从远程克隆文件
    现在远程建个仓库 在本地相应的位置克隆一份
    确定远程有这个仓库
   git clone git@github.com:账户名/远程仓库名.git
7. 创建分支
    git checkout -b 分支名
    git checkout命令加上-b参数表示创建并切换，相当于以下两条命令：
    git branch dev
    git checkout dev
8.文件删除
    a.先删除
        rm test.txt
    b.在git删除
        git rm test.txt
    c. 然后确认
        git commit -m "remove test.txt"

 
  
