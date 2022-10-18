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

#### 1.创建一个Github仓库

这里默认大家拥有基本的Github使用基础，创建一个项目仓库。

#### 2.个人开发

如果该项目只有你个人开发/维护，你只需正常维护即可；

Github可视化网页上大概流程：本地更新代码/文件——将更新的文件在github网页上传更新

##### （1）Github上更新项目文件，同时添加简短的commit

![2](/home/doongli/Desktop/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/2.png)

如上图所示：

- 第一个框代表上传文件成功，
- 第二个框里可以添加简短的更新注释，简要描述更新内容（个人使用的项目建议大家添加，多人协同的项目必须添加commit！），
- 第三个框可以添加详细的描述，如果更新比较简单一般不使用，
- 第四个框选择将文件上传至那个分支branch，个人使用或者简单的写协作项目都是直接上传到main分支上（branch问题见下文）。

##### （2）查看之前更新的内容

更新完之后你可以在仓库界面上的 `commits` 处查看历史更新内容以及commit

![1](/home/doongli/Desktop/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/1.png)

![1](/home/doongli/Desktop/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/3.png)

这里可以看到我有两次更新记录，这里我其实更新时没加commit，所以显示的是默认的commit  “Add files via upload”/"Inital commit"

![1](/home/doongli/Desktop/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/4.png)

点进某次更新的版本，你可以看到当时更新的细节，主要本次更新和上一个版本代码的对比情况。

##### （3）版本控制

版本控制的需求分两种情况：1.查看当时版本的仓库；3.下载以前某次更新的版本的代码

![5](/home/doongli/Desktop/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/5.png)

![7](/home/doongli/Desktop/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/7.png)

这里可以在上两张图中分别查看历史版本的仓库文件。

![6](/home/doongli/Desktop/Use_Gitlab-Github_To_Maintain_A_Collaborate_Project_In_Visual_Interface/IMG/6.png)

需要下载相关版本的代码，code处下载即可。

#### 2.协同合作方式

多人

#### 3.更新或者合并代码

#### 4.

#### 5.关于不同的分支
