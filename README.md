# test
# 如何将git与自己的邮箱绑定

STEP1: 安装git
   
    sudo apt install git

STEP2: 获取SSH KEY

    ssh-keygen -t rsa -C "youremail@youremail.com" 

STEP3: 将公钥绑定至Github (执行以下命令打印出公钥)
    
    cat ~/.ssh/id_rsa.pub

STEP4: 绑定

    ssh -T git@github.com
