# A-Tutorial-For-Gitlab

> Note：该文档是 AMAS-LAB 实验室成员使用实验室服务器上的Gitlab环境的快速入门文档；本文由[Li Dong](https://github.com/GRF-Sunomikp31)完成，最后更新时间：2022-9-25

目前实验室Gitlab管理员：[Li Dong](https://github.com/GRF-Sunomikp31)。

## 1.Create A Personal Account

首先在浏览器输入实验室服务器的IP：**10.16.18.110**；进入实验室Gitlab的可视化界面上。

![1](C:\Users\LD\Desktop\AMAS-LAB\Server\IMG\1.png)

新使用者需要创建一个账号，用户名命名规范建议采用姓名拼音全拼或其它易看分辨出姓名的命名。

![2](C:\Users\LD\Desktop\AMAS-LAB\Server\IMG\2.png)

创建好之后联系**实验室Gitlab管理员（见文首）**，审批通过后即可登录使用。

![3](C:\Users\LD\Desktop\AMAS-LAB\Server\IMG\3.png)

审批通过登录，这里需要选择一个角色，因为实验室使用不会涉及到CI/CD流程，所以这里可以随意选择。

## 2.Gitlab Usage

#### 图形化界面使用

创建一个项目/仓库

![5](C:\Users\LD\Desktop\AMAS-LAB\Server\IMG\5.png)

![6](C:\Users\LD\Desktop\AMAS-LAB\Server\IMG\6.png)

这里建议将**Visibility Level**设置了 **Internal** 的形式，允许实验室内网的其他成员查看。

创建好之后你可以像Github一样在浏览器可视化界面上修改，增加或者删除文件。

### Git使用

虽然可以直接在浏览器上可视化操作，但是这里建议直接用**git进行版本控制和维护**。

安装Git：[https://git-scm.com/downloads](https://git-scm.com/downloads)   选择对应的版本下载安装即可

Git参考资料：[https://git-scm.com/book/zh/v2](https://git-scm.com/book/zh/v2)

以下操作和github使用中git的相关操作相同。

**（1）拉取项目**

如果是第一次拉项目：安装好之后你，找到合适的地方，然后右键->Git Bash Here，输入：

```bash
#如要拉public_test_project这个仓库，仓库地址.git
git clone  http://10.16.18.110/LiDong/public_test_project.git   
```

如果之前已经拉取过项目了：进入项目目录中然后右键->Git Bash Here，输入：`git pull`这样就将最新的版本拉取到本地。

**（2）推送项目**

当写完代码测试无误后需要将代码推送到远程，操作如下：

- 进入项目目录中然后右键->Git Bash Here，输入：`git pull`（即每次提交之前必须拉取最新的项目）

- `git add .`（最后面是一个点表示将所有更改的文件都添加到上传列表中）

- git commit –m “写你的修改地方”
  - 注意：这句是将你添加的修改文件提交，双引号中一定要写提交说明，建议提交说明采用以下格式：
  - [add]你增加的xxx功能或文件
  - [update]你修改的xxx功能或文件
  - [delete]你删除的xxx功能或文件

- `git push`

Note：以上只是最简单的操作，在拉取项目过程中，如果多人同时对一个文件进行了修改，是会出现冲突的，这个时候就需要先解决冲突，具体的解决方法请参考上述提供的学习资料。

## 3.Other

#### （1）.If You Not In School

> Note：如何你不在学校，即使用的并非是校园网，你可以按照以下教程申请学校VPN进行访问。

Reference：[https://sustech.online/service/network/apply-for-vpn/](https://sustech.online/service/network/apply-for-vpn/)

使用VPN登录、使用实验室Gitlab和校园网相同。

#### （2）.If there is a collaborative project

如果你在和组内的同学进行一个合作的项目，需要项目或者小组的创建者将你添加到项目或小组中。