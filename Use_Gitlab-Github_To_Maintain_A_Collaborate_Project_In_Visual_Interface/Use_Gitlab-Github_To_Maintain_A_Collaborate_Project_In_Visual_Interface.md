# Use Gitlab/Github To Maintain A Collaborate Project In Visual Interface

> @Brief：该文档将分享，如何在 **可视化界面**（后面会有一篇文章单独分享如何使用git维护） 上使用Gitlab/Github维护一个多人协同的项目。
>
> @Author：[Li Dong](https://github.com/DoongLi)
>
> @Date：2022-10-18

## Introduction

为什么需要Gitlab/Github进行代码版本控制和项目管理：

- 1.在个人项目开发时，代码本地备份可能会因为本地设备发生故障而导致代码丢失，
- 2.本地电脑缺乏良好的版本控制工具，使用者可能在多个版本中发生混淆
- 3.在多人协作项目中，需要共享的 **局域网/公共网** 的项目托管平台，从而避免频繁的项目单向发送以及代码版本问题等。

So，we chooses gitlab or github do it!

## Procedure

Note：以下以 **Github可视化界面操作** 为例分享整个流程，GItlab类似。

### 1.创建一个Github仓库

这里默认大家拥有基本的Github使用基础，创建一个项目仓库。

### 2.个人开发

如果该项目只有你个人开发/维护，你只需正常维护即可；

Github可视化网页上大概流程：本地更新代码/文件——将更新的文件在github网页上传更新

##### （1）Github上更新项目文件，同时添加简短的commit

![2](https://github.com/SUSTech-AMASLAB/Tutorial/blob/main/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/2.png)

如上图所示：

- 第一个框代表上传文件成功，
- 第二个框里可以添加简短的更新注释，简要描述更新内容（个人使用的项目建议大家添加，多人协同的项目必须添加commit！），
- 第三个框可以添加详细的描述，如果更新比较简单一般不使用，
- 第四个框选择将文件上传至那个分支branch，个人使用或者简单的写协作项目都是直接上传到main分支上）。

##### （2）查看之前更新的内容

更新完之后你可以在仓库界面上的 `commits` 处查看历史更新内容以及commit

![1](https://github.com/SUSTech-AMASLAB/Tutorial/blob/main/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/1.png)

![1](https://github.com/SUSTech-AMASLAB/Tutorial/blob/main/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/3.png)

这里可以看到我有两次更新记录，这里我其实更新时没加commit，所以显示的是默认的commit  “Add files via upload”/"Inital commit"

![1](https://github.com/SUSTech-AMASLAB/Tutorial/blob/main/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/4.png)

点进某次更新的版本，你可以看到当时更新的细节，主要本次更新和上一个版本代码的对比情况。

##### （3）版本控制

版本控制的需求分两种情况：1.查看当时版本的仓库；3.下载以前某次更新的版本的代码

![5](https://github.com/SUSTech-AMASLAB/Tutorial/blob/main/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/5.png)

![7](https://github.com/SUSTech-AMASLAB/Tutorial/blob/main/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/7.png)

这里可以在上两张图中分别查看历史版本的仓库文件。

![6](https://github.com/SUSTech-AMASLAB/Tutorial/blob/main/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/6.png)

需要下载相关版本的代码，code处下载即可。

### 2.协同合作方式

Github上多人协同合作方式分为两种：

- （1）.Github仓库中邀请他人为 Collaborator，
- （2）.PR（Pull requests）方式；

##### （1）Github仓库中邀请他人为 Collaborator

![8](https://github.com/SUSTech-AMASLAB/Tutorial/blob/main/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/8.png)

如图所示，直接在setting中添加邀请他人为 Collaborator即可；此时Collaborator和仓库建立者拥有相同的仓库维护权限，具体维护可直接参考 [2.个人开发](https://github.com/SUSTech-AMASLAB/Tutorial/blob/main/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface.md#2%E4%B8%AA%E4%BA%BA%E5%BC%80%E5%8F%91) 。

Note：因为此时 Collaborator和仓库建立者拥有几乎相同的仓库维护权限，此时要求 仓库建立者 对  Collaborator的行为和仓库更新内容（代码质量等等）高度信任，否则请使用下面PR的方式进行合作。

（2）PR（Pull requests）方式

PR是github上做开源贡献最常用的方式，PR的大致流程：协作者fork仓库建立者的仓库（第一次是这样，后面需要更新代码）——修改代码（一般是增加内容或者是修改bug）——提Pull requests将修改后的代码仓库推到仓库建立者的仓库上——仓库建立者查看更新内容，并选择是否合并。

Note：即使已经要求别人为 Collaborator也可以使用PR的方式，我们**强烈建议使用PR的方式维护协同项目**。

### 3.PR（Pull requests）方式具体流程

大致流程：Fork仓库（如果是第一次contributioins）/更新仓库——修改仓库代码——Pull requests——仓库管理者查看相关修改代码选择合并。

#### （1）Fork仓库

如果你是第一次协作Contributiins，你需要先将别人的仓库fork到自己账户下。

![9](/home/doongli/Desktop/Github/Tutorial/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/9.png)

![10](/home/doongli/Desktop/Github/Tutorial/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/10.png)

#### （2）更新仓库

如果你不是第一次协作Contributiins，即之前fork过别人的仓库了，但是你fork之后别人可能又更新了他的仓库，所以你需要将你fork的仓库和别人最新的仓库同步更新，即在你fork的仓库下点击：“Sync fork”即可。

![18](/home/doongli/Desktop/Github/Tutorial/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/18.png)

#### （3）修改仓库代码

此时假设你做了一些修改，可能是增加内容或者修改bug。

![11](/home/doongli/Desktop/Github/Tutorial/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/11.png)

#### （4）Pull requests

这时候你想更修改后的内容更新的别人的仓库中；你需要在你fork的仓库，`New pull request`。

![12](/home/doongli/Desktop/Github/Tutorial/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/12.png)

这里可以看到一些对比，**head repository**是你修改的仓库（即你需要将这个仓库更新到作者的仓库下），**base repository**是作者的仓库。

![13](/home/doongli/Desktop/Github/Tutorial/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/13.png)

这里提交后就可以在作者仓库**Pull requests** 下产生一条推送信息，如下：

![15](/home/doongli/Desktop/Github/Tutorial/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/15.png)

仓库管理员看到这条信息后，检查修改的内容是否有效，有效后统一合并如下图；同时该Pull request被关闭。

![16](/home/doongli/Desktop/Github/Tutorial/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/16.png)

你可以看到修改的信息已经在原仓库中更新。

![17](/home/doongli/Desktop/Github/Tutorial/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/17.png)
