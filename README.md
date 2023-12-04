# ubuntu20.04，如何将git与自己的邮箱绑定(修改)

STEP1: 安装git

    sudo apt install git

STEP2: 获取SSH KEY

    ssh-keygen -t rsa -C "MyEmail@qq.com" 

STEP3: 将公钥绑定至Github (执行以下命令打印出公钥,并复制)
    
    cat ~/.ssh/id_rsa.pub
STEP4: 执行上述命令，复制公钥，之后进入Github的【settings】->【SSH and GPG keys】->【New SSH key】。
粘贴公钥，并点击【Add SSH key】,完成公钥注册。

STEP5: 绑定

    ssh -T git@github.com
