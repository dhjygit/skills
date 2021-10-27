### 全局配置

```shell
git config --global user.email "liu2211402141@qq.com"
git config --global user.name "dhjygit"
```

### SSH免密登陆

```shell
ssh-keygen -t rsa -C liu2211402141@qq.com
```

一直输入回车键 `cd ~/.ssh `

`id_rsa`是私钥，`id_rsa.pub`是公钥

在github中生成ssh keys时，将公钥复制进去

```shell
ssh -T git@github.com # 验证是否成功
```

```shell
git remove -v # 查看本地仓库与远程仓库的关联详情
git remote rm origin # 解除与现有远程仓库的关联
git remote add origin git@github.com:dhjygit/skills.git
```

### token登录

1. 单击您的个人资料照片，然后单击 **Settings（设置）**。
2. 在左侧边栏中，单击 **Developer settings**。
3. 在左侧边栏中，单击 **Personal access tokens（个人访问令牌）**。
4. 单击 **Generate new token（生成新令牌）**。
5. 选择要授予此令牌的作用域或权限。 要使用令牌从命令行访问仓库，选择 **repo（仓库）**。
6. 单击 **Generate token（生成令牌）**。
7. 单击复制图标将令牌复制到剪贴板。
8. 记住token，把token作为密码使用。

### 初始化和推送仓库

1. 本地初始化

```shell
git init
git add remote origin https://github.com/dhjygit/skills.git
git add .
git commit -m "add"
git push --set-upstream origin master
```

2. git clone方式

```shell
git clone origin https://github.com/dhjygit/skills.git
git add .
git commit -m "add"
git push
```

