---
output:
  html_document: 默认
  pdf_document: 默认
---

# 任务3：如何将Git与R Studio集成

此任务专为希望在标准的基于R的工作流程中实施版本控制系统的学生和研究人员而设计。 这可以应用于一系列软件开发，数据分析和项目管理任务。 您未来的研究自我将感谢您的方便。

不要忘记你可以参加我们的开放 [**Slack频道**](https://osmooc.herokuapp.com/)。 请在＃module5opensource上自我介绍一下，并告诉我们你是谁，你的背景，以及你如何在这里结束！

预计完成时间：30分钟

估计完成后的时间节省：几乎无限

**注** 此任务的视频指南版现已在 [YouTube](https://www.youtube.com/watch?v=Q-6jfjSAspA)。

## 目录

* [入门](#Getting_started) 
  * [混帐](#Git)
  * [R Studio](#Rstudio)
* [第一步：下载所有内容](#one)
* [第二步：在RStudio中配置Git](#two)
* [第三步：为什么我这样做？](#three)
* [第四步：Git和R之间的完美结合](#four)
* [第五步：获取内容内容](#five)
* [第六步：勇敢的承诺](#six)
* [第七步：推！](#seven)

## 入门 <a name="Getting_started"></a>

恭喜你做到这一点！ 如果你正在阅读这篇文章，你就可以幸免于拉请求，网络钩子，甚至可以告诉我们FOSS中的F代表什么（*不是* 挫折...）希望你已经克服了任何怀疑或不情愿为了GitHub和开源软件的好处，并准备采取下一步措施。

在开始此任务之前，请确保您已完成 [任务1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) 和 [任务2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)，以便您更熟悉GitHub和一些标准的开源实践。

此任务将教您如何将版本控制软件Git与流行的编码环境RStudio集成。 是的，Git就像GIF或上帝一样，而不是Jit就像发出错误的方式一样。

如果您是那些认为代码分布在等待破解的多个硬盘驱动器，Dropbox，Google Drive或任何其他非专业软件的研究人员之一，则此任务仅适合您。 如果您曾经历过让不同的共同作者之间有多个“最终”版本的纸张反复的令人头疼的过程，这也适合您。

我们所有人偶尔会对这些事情感到内疚，但有一些方法可以做到这对你，未来的你和那些可能从你的工作中受益的人更好。

  


### 得到Git <a name="Git"></a>

那么，什么是Git，它与GitHub有何不同？ Git是一个版本控制系统，它使您能够在整个开发过程中保存和跟踪工作时间戳的副本。 它也适用于非代码项，例如MOOC，其中大部分是用RStudio中的markdown编写的，并与Git / GitHub工作流集成。

这很重要，因为所有研究都经历了变化，有时我们想知道这些是什么。 您是否删除了一些您认为重要的文字？ 版本控制将为您保存。 您的代码在过去是否完美运行，但现在已经超出了信念范围？ 版本控制。 这是避免混乱状态的好方法，在这种情况下，您拥有相同文件的多个副本，但没有愚蠢和烦人的文件命名约定。 `FINAL_Revised_2.2_supervisor_edits_ver1.7_scream.txt` 将成为过去。

GitHub是一个平台，允许您从工作区（例如，笔记本电脑）无缝共享代码，以便在线空间中托管。 所以，有点像GitHub的公共接口。 Git / GitHub的优点是：

1. 你可以随时随地保留所有作品的副本;
2. 您可以通过时间比较不同副本的工作，这有助于发现错误或错误;
3. 其他人可以公开与您的工作合作;
4. 您的工作本地和在线副本都保持同步;
5. 关于谁做出贡献，为什么做出贡献以及何时做出贡献，这是完全透明的。和
6. 您可以让多个人同时在同一个项目上工作。

虽然这主要是为源代码而设计的，但它应该立即变得如此成为几乎所有研究工作流程的强大工具。

  


### RStudio <a name="Rstudio"></a>

对于使用统计编程语言R的研究人员来说，RStudio是一个流行的编码环境。它带有一个文本编辑器，因此您不必安装另一个并在它们之间切换。 它还包括Git和GitHub的图形用户界面（GUI），我们将在这里使用它。

当辉煌的开源工具无缝集成时，这不是很好。 这应该有助于使您日常使用Git更简单。

如果您在任何时候需要为R安装新软件包，只需使用以下命令：

`install.packages（“PACKAGE NAME”，依赖项= TRUE）`

用呃包名替换 `PACKAGE NAME`。 可能出现的一些例子，你可以与发挥有益包括 `knitr`， `devtools` 或 `GGPLOT2`。

  


## 第一步：下载所有内容 <a name="one"></a>

1. 如果您已经执行了之前的任务，那么您现在应该已经拥有一个GitHub帐户。 如果没有， [标志在这里](https://github.com/)。 为所有人免费提供无限量的存储库！
2. 下载并安装最新版本的 [R](https://www.r-project.org/)。 也适用于 [Mac](https://cloud.r-project.org/) 和 [Linux](https://cloud.r-project.org/bin/linux/)。
3. 下载并安装最新版本的 [Rstudio](https://www.rstudio.com/products/rstudio/#Desktop)。 哦，嘿，看起来是开源！ 沙沙。
4. 下载并安装最新版本的 [Git](https://gitforwindows.org/)。 **确保在安装过程中选择“从Windows命令提示符使用Git”。**

> **专业提示**：要将所有R软件包更新为一个，只需执行以下代码 `update.packages（ask = FALSE，checkBuilt = TRUE）`

现在，只需为每个安装选择所有常用的默认选项。 根据哪个操作系统（例如，Mac，Windows，Linux），每个人可能会有所不同。 就目前而言，对于此任务的其余部分，我们将坚持使用简单的Windows方式（但也提供使用命令行的一些说明）。

对于Linux或Debian用户，只需使用以下命令安装Git：

`sudo apt-get install git-core`

对于Mac用户， [此链接](http://git-scm.com/download/mac)，或购买具有不同操作系统的新笔记本电脑。

如果需要，您还可以下载 [本地版本的GitHub](https://desktop.github.com/) 并通过简单的GUI使用它。 它可以在Windows，Mac和Linux上使用，并且可以让您的生活更轻松，特别是如果您想使用不同的平台来访问RStudio。

> **专业提示：** 您在安装Git时会看到'使用Git Bash作为Git项目的shell？'在这里您可以使用命令行从RStudio外部访问Git。 这是一个强大的野兽。 尝试以下两个命令开始：

`混帐配置--global user.name '您的用户名'`   
`混帐配置--global user.email '您的email'`   


## 第二步：在RStudio中配置Git <a name="two"></a>

是的，这很容易做到。 接下来，进入RStudio，在顶部的选项卡中转到 **工具>全局选项> Git / SVN**。 SVN只是像Git这样的另一个版本控制系统，我们不需要在此担心。

在其中显示 *Git可执行文件*，将此路径添加到您刚刚在上一步中下载的git.exe文件中。 确保此处的框显示 **启用RStudio项目** 版本控制界面。 现在，它已将版本控制与RStudio中的未来项目联系起来，为协作或独奏工作提供了一个非常强大的附加维度。

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git_svn.png?raw=true" width="400px"/>
</p>

<p align="center"><i>RStudio中的全局选项窗口</i></p>

  


接下来，点击此窗口中的按钮，该按钮显示 *创建RSA密钥*，这是一个用于在不同系统之间进行身份验证的私钥，使您无需反复输入密码。 在这里，它将弹出一个带有公钥的新窗口，您希望将其复制到剪贴板。

转到GitHub，转到您的配置文件设置，以及 *SSH和GPG键* 选项卡。 单击 *新SSH密钥*。 在这里，粘贴来自RStudio的密钥，称之为'RStudio'之类的富有想象力的东西。

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/ssh_key.png?raw=true" width="800px"/>
</p>

<p align="center"><i>在GitHub里面，您需要输入刚才在RStudio中生成的密钥</i></p>

  


好的，现在抓住你的屁股，我们进入命令行。 如果您以前从未使用过shell，请不要担心，因为它与使用R或任何其他编码系统非常相似。 这里的主要区别在于，不是调用R中的函数，而是调用命令。

回到RStudio，转到 **工具> Shell**，它将打开一个命令提示符窗口。 如果你已经玩过上面的Git Bash，你应该已经完成了这一步。 输入以下两个命令：

`混帐配置--global user.name '您的用户名'`   
`混帐配置--global user.email '您的email'`   


希望不必说在您自己的GitHub用户名和电子邮件中替换。 您可以通过在Windows中找到“Shell”来随时访问它。 或者，如果您右键单击桌面上链接到GitHub存储库的任何文件夹，您可以立即打开Shell并将其打开。

这个阶段所做的是将Git（在桌面上运行的软件）配置到GitHub，这是一个存储库网站。

重启R Studio。 哇，那太难了。 下一个。

  


## 第三步：为什么我这样做？ <a name="three"></a>

好吧，保持呼吸，我们将暂停这里只是为了学习一些基本的Git命令。 您可以通过学习做的一些关键因素是：

* **添加**：这是您在提交之前将文件提交到临时区域的位置。

* **提交** 这就像通过创建新版本或副本来“保存”您的工作。

* **推送**：这是您将文件从本地项目发送到在线存储库的方式。

* **拉**：这是您从在线存储库获取文件到本地项目的方式。

回到RStudio，在 *终端*中输入以下内容，或者打开一个新的Shell：

`git add。`

现在它实际上并不会做任何事情，但在未来将增加在当前工作目录下的所有文件（这是什么 `。` 那样），以分期准备好提交。

  


## 第四步：Git和R之间的完美结合 <a name="four"></a>

现在，在任务1中，您应该已经学会了如何构建第一个GitHub存储库。 如果你还没有这样做，我们可以在你去的时候在这里等待。 如果您已经拥有或拥有现有的GitHub存储库，我们可以继续前进。

所以，你应该在GitHub上有一个存储库，包含一个 `README` 文件，一个 `LICENSE` 文件和一些其他位和bob。

我们现在要做的是将该存储库与Git集成。 现在稳定。

1. 首先，转到 **Project> Create Project> Version Control> Git**。
2. 回到GitHub，您应该看到有一个https：// URL。 这是指向您的存储库的链接，它为您提供了在桌面上克隆它的选项。 现在，只需复制该链接，切换回RStudio，然后按照指示将其粘贴到“存储库URL”中。
3. 为项目提供目录名称，例如test，Jim或任何您想要的名称。
4. 接下来，浏览桌面上您希望此项目生效的位置，即其子目录。
5. 点击“创建项目”，让魔术完成！

你刚刚做的是告诉RStudio将R中的新项目与GitHub上的特定存储库相关联。

## **第四步：替代方案**

如果你还没有在GitHub上构建你的第一个存储库，我们可以在这里做一些稍微不同的事情。 在RStudio中，单击 *New project* ，然后单击 *New Directory*。 调用它你想要的并根据需要更改目录，确保勾选 *创建一个git存储库*，然后单击 *创建项目*。 这产生了 `.Rproj` 文件，它可以在通常的方式通过RStudio管理，包括添加 `README.md`和 `LICENSE.md` 文件作为在任务1讨论。

## 第五步：获取内容内容 <a name="five"></a>

还记得我们创建的 `README` 文件吗？ 好吧，是时候写了。 回想一下任务1，我们说有一些特定的东西是一个很好的 `README` 文件。 你还记得他们中的任何一个吗？ 为了更新你的记忆，这些是：

* 这个项目是关于什么的，它做了什么。
* 人们为什么要关心，为什么它有用。
* 如何有人开始为项目做贡献。
* 如果有人需要帮助，可以联系谁。
* 许可证，贡献指南和行为准则的链接。
* 项目结构的描述。
* 谁参与，他们的角色是什么。
* 项目的当前状态。

因此，在RStudio中，打开该文件尝试为您的项目添加一些有关此信息的信息。 如果您正在为实际项目执行此操作，请尝试使其有用。 如果你现在只是修修补补，你可以添加你想要的东西。

请记住，您的 `README` 文件采用markdown（.md）格式。 有关一些简单的语法降价用法的复习，请查看这个 [方便的备忘单](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)。

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/markdown.png?raw=true" width="600px"/>
</p>

<p align="center"><i>在开发期间，此模块在markdown中查看的内容的屏幕截图。 元。</i></p>

  


## 第六步：勇敢的承诺 <a name="six"></a>

好的，现在你应该有一个编辑得很好的 `README` 文件。 现在我们将使用Git将其“提交”到项目中。 这基本上相当于保存了这个版本的项目，并记录了所做的更改。 连续提交产生的历史可以在以后检查，让您自信地工作。

有几种方法可以做到这一点。

1. 转到 **工具>版本控制>提交**
2. 在RStudio的环境窗格中，应该有一个新的“Git”选项卡。 便利。
3. 在您的控制台窗格中，现在应该有一个新的“终端”，您可以通过它运行Git命令行。

让我们暂时坚持第二种选择。 这个Git窗格显示了哪些文件已被更改，并包含我们之前看到的最重要的Git命令的按钮。

在Git窗口中选择 `README` 文件，如果您对其进行了任何编辑，该文件应自动显示。 这会将该文件添加到“临时”区域，这有点像您工作的预先节省空间。 单击“提交”，将弹出一个新窗口。

在这里，您有机会查看您的更改，并编写一个很好的提交消息。 输入简短的内容，但提供有关您在此版本或工作快照中所做更改的信息。 您希望这是足够的信息，以便如果您或其他人回顾它，您就会知道为什么要进行此提交以及与之相关的更改。 这些就像您的项目的安全网，以防您因某些原因需要退回。

> **专业提示**：在这里，您将看到自上次提交以来所做的所有更改的列表。 较旧的删除行为红色，新添加的行为绿色。 仔细检查这些以确保您所做的编辑是您打算进行的编辑。 这对于发现拼写错误，杂散编辑以及您可能偶然引入的任何其他小错误非常有用。 安全第一。

**注意** 如果您是色盲并且无法看到添加或删除了哪些行，则可以使用窗口左侧两列中的行号作为指导。 此处，第一列中的数字标识旧版本，第二列中的数字标识新版本。

现在，当您单击“提交”时，将弹出另一个窗口，告诉您已更改的文件数以及该文件中已更改的行数。 关闭那个小窗口。

  


## 第七步：推！ <a name="seven"></a>

单击新窗口右上角的 *Push* 按钮。 现在会弹出一个新窗口。 这样做是将本地存储库中更改的文件与 `README` 文件同步到GitHub上项目的在线版本。

要从命令行管理器执行此操作，请使用以下命令：

`git push -u origin master`

有时在这里会提示您从GitHub添加您的用户名和密码，如果被问到，您应该这样做。

关闭那个窗口，然后关闭下一个窗口。 转到GitHub上的项目，刷新并检查 `README` 文件是否仍然存在于其所有新编辑的荣耀中。 您应该看到您在文件旁边创建的提交消息。

  


**可选的高级/令人敬畏的步骤**

好吧，所以你只是把一些内容推到你的第一个回购中，太棒了！ 现在让我们为实际项目付诸实践。 就像，你现在参与的那个。 我们来试试吧：

1. 在 [GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source)上转到此项目的存储库

2. 将存储库分成您自己的GitHub帐户。 这个URL应该是： `https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source.git`

3. 进入RStudio，转到 **File> New Project**，选择 *Version Control*，选择 *Git*，然后粘贴在您的存储库副本中找到的分叉存储库URL。 您现在拥有自己的整个模块的版本副本。 整齐。 将其保存在本地计算机上。

4. 现在，您需要告诉Git该项目的不同版本存在。 打开 *Shell*，然后输入命令： `git remote add upstream https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source`

5. 你刚刚做了什么就把原来的分支命名为 `上游`，只是为了让事情变得简单。 现在，创建一个新的 **分支** ，以独立于主分支记录您对此的更改。 输入命令： `git checkout -b proposed-changes master`

6. 您刚刚创建了一个名为 `proposed-changes` 的新分支，您现在可以编辑所有内容和文件，让您心满意足。 希望这个项目的结构足够简单，您可以浏览。 可以在 `content_development` 文件夹中找到MOOC的所有原始文件，这是 `Task_3.md`。

7. 如果您滚动到 `Task_3.md`的底部，您应该会看到一个可以在您的姓名和所属关系中进行编辑的地方。 添加这些，然后完成上面提到的提交过程。 如果您还看到其他需要编辑的内容，请随意添加！

8. 现在，您希望将更改推送回原始分支。 在 *Shell*： `git push origin proposed-changes`使用以下命令

9. 回到GitHub，在这里找到你的叉子。 单击绿色小按钮，然后创建拉取请求。 这本质上是一个综述，将对MOOC项目的原始分支所做的更改进行整合。

10.     负责MOOC项目的业主现在将收到通知，审核，并确认是否一切按计划进行！ 我们将对其进行审核，如果一切顺利，您的名字现在将永远显示为完成此高级任务的人。
      

11.     喝一杯茶，咖啡或葡萄酒来庆祝！
      

**恭喜**

您刚刚将Git与R Studio集成，并首次更改为版本控制项目。 您的生活现在将永远不变，您的研究工作流程可能比以往更加快速，灵活和协作。 祝你好运回到Word。

最棒的是，这不必仅用于代码。 您可以将它用于纯文本，markdown，html以及R代码。 可能性是无限的 - 您刚学到的是一种新形式的公开协作项目管理，适用于各种各样的任务。

从现在开始，这完全取决于你！ 一些建议是：

* 经常提交。 像你的小狗一样对待Git，因为它需要不断和特别的关注。 只是轻轻拍打头部就足以让它满意，但是持续服务会很开心。

* 执行此操作的最佳方法是在每次处理特定问题时进行提交。 例如，编写段落，运行分析或修复错误。

* 经常推。 不要让这些提交累积起来，否则会冒更大的风险进入合并冲突。 看到这些可能是噩梦的事情，只要确保经常推动。

* 经常拉。 如果其他人在同一个项目上远程工作，您将需要及时了解他们的更改。 确保经常从GitHub中提取更改，以确保您完全同步。

* 实验和探索！ 这项任务实际上只是触及表面，并且有许多不同的功能，工具和方法可以使用。 实际上，您需要了解如何使用这些信息来改进您的研究工作流程，并最终在更好，更开放和可靠的研究上进行合作！

* 要了解有关问题，分支，合并冲突，拉取请求以及使用Git和RStudio的其他高级方面的更多信息，请查看Hadley Wickham撰写的这篇 [真棒指南](http://r-pkgs.had.co.nz/git.html)。

  


**知道这种内容可以改进的方式吗？**

是时候将新的GitHub技能用于测试运行了！ 所有内容主要发展发生 [这里](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md)。 如果您对内容，布局或其他任何内容有建议的改进，您可以制作它，然后在主持人验证后它将自动成为MOOC内容的一部分！

## 完成此任务的ADVANCED版本的参与者列表

* 科恩大学CRF-C的Brendan Palmer
* Lisa Matthias，柏林自由大学
* 莱斯特大学的Hollie Marshall 
* Eric D. Wilkey，加拿大西部大学
* José-RaúlCanay-Pazos，西班牙圣地亚哥德孔波斯特拉大学
* EncarnaciónMartínezÁlvarez，西班牙
* Alberto Albz Marocchino，意大利
* Iratxe Rubio，巴斯克气候变化中心BC3
* Gabriele Orlandi，法国巴黎社会科学高级研究学院（EHESS）
* HandeSodacı，土耳其
* Luke W. Johnston，丹麦奥胡斯大学
* Philippe Joly，WZB和HU-Berlin
* Paul Griffiths，NCAS和U. Cambridge
* Harin Lee，伦敦大学金史密斯学院
* 秘鲁天主教大学路易斯卡马乔
* 汤姆克里德福德，伦敦帝国理工学院
* 斯塔万格大学Nithiya Streethran 

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)