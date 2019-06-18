---
output:
  html_document: 默认
  pdf_document: 默认
---

# 任务1：如何在GitHub上设置存储库

此任务专为希望在GitHub上创建其第一个开源项目（软件或非软件）的学生和研究人员而设计。 GitHub是一个让您来玩和尝试新的研究工作流程的地方，而且实际上只是帮助您为自己的途径和想法创造舞台的开始。

不要忘记你可以参加我们的开放 [**Slack频道**](https://osmooc.herokuapp.com/)。 请在＃module5opensource上自我介绍一下，并告诉我们你是谁，你的背景，以及你如何在这里结束！

**请注意** 此功能的屏幕录制也可通过 [YouTube](https://www.youtube.com/watch?v=AnftV9HBPSc&)。

预计完成时间：30-45分钟。

估计一旦完成时间节省：难以想象..

## 目录

* [入门](#Getting_started) 
  * [设置GitHub配置文件](#Profile)
  * [GitHub语言](#Language)
  * [创建一个新的存储库](#Create_new)
* [基本步骤](#Foundation) 
  * [选择许可证](#License)
  * [创建README文件](#Readme)
  * [创建贡献指南](#Contributing)
  * [制定行为准则](#Conduct)
  * [使你的代码可以理解](#Citation)
* [让您的问题保持最新](#Issues)
* [启动项目的检查清单](#Check-list)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task1.png?raw=true" alt="任务1工作流程" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
</p>

<p align="center"><i>任务1的工作流程。 在完成任务时保持这个方便！</i></p>

  


## 入门 <a name="Getting_started"></a>

“存储库”实际上只是GitHub上项目的一个奇特名称。 GitHub是一个在线地方，您可以在其中管理项目，存储文件以及与他人公开协作。 这一切都是通过使用版本控制来跟踪项目进展情况来实现的。 因此，GitHub是软件和非软件项目的强大工具。

在这个早期阶段要考虑的最重要的事情之一是考虑您希望更广泛的社区如何与您的项目进行互动。 当您在公开场合工作时，您希望确保其他人在访问，查看和参与您的工作时感到舒适。 以降低进入壁垒的方式建立存储库，并且担心成为“局外人”是维持成功项目的第一步。

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/octocat.png?raw=true" width="150px" height="125px"/>
</p>

<p align="center"><i>Octocat，GitHub的小吉祥物</i></p>

  


### 设置GitHub配置文件 <a name="Profile"></a>

要设置GitHub配置文件，只需转到主页面，然后单击 [注册GitHub](https://github.com/join)。 在这里，您可以使用用户名，电子邮件和密码作为标准创建个人帐户。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/github_signup.png?raw=true" width="800" /></p>

<p align="center"><i>注册GitHub</i></p>

  


下一步是制定个人计划。 目前，只需选择“无限制公共存储库免费”计划，除非您担心隐私，在这种情况下选择私人计划。 如果您打算为组织设置项目，也可以选择该选项。

  


### GitHub语言 <a name="Language"></a>

这可能是GitHub最令人困惑和反感的方面。 以下是一些最常用的术语及其定义：

* **初始化**：创建一个空存储库。
* **Checkout**：创建本地存储库的工作副本。
* **克隆**：将存储库复制到计算机上的本地目录中。
* **分叉**：创建存储库的个人分支以并行处理它。
* **分支**：存储库的独立并行版本。 更改不会影响主分支。
* **Master**：存储库的主分支和默认分支。
* **清洁**：分支上没有待处理的提交。
* **阶段**：添加准备好提交给分支的更新。
* **提交**：对存储库的修订，如版本化的“保存”功能。
* **提交消息**：提交随附的更改的描述。
* **检查**：状态检查。
* **取**：与狗没什么关系。 指的是从在线存储库获取最新更改而不合并它们。
* **索引**：充当临时区域的“树”。
* **工作目录**：保存文件的“树”。
* **头**：表示最后提交的“树”。
* **推送**：将已提交的更改添加到远程存储库的头部。
* **合并**：完成后将一个分支中所做的更改与主分支相结合。
* **拉**：通过获取和合并最新提交来更新存储库。
* **拉请求**：将更新的分支合并到主分支的请求。
* **问题**：与存储库相关的建议改进，任务或问题。

呼！ 不要担心记不住 *所有* 的这些现在。 像任何新技能一样，熟悉程度来自经验。

您可以看到其中一些与保存，复制，粘贴等标准工作流操作非常相似，但适用于软件管理过程。 有一个 [几个](https://mirrors.edge.kernel.org/pub/software/scm/git/docs/gitglossary.html) 太大，但这应该为入门做。

如果您有兴趣，这些术语大多来自底层的 [Git系统](https://git-scm.com)。 Git的构建允许开发人员以分布式方式管理不同版本的源代码，这很好。 它有很多的功能，并做大量的复杂的东西的能力，通过书面 [非常聪明的家伙](https://www.linuxfoundation.org/blog/2015/04/10-years-of-git-an-interview-with-git-creator-linus-torvalds/)。 但是， [用户界面的设计并未考虑到新用户](https://xkcd.com/1597/)，因此很难学习。

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git.png?raw=true" width="150px"/>
</p>

<p align="center"><i>无与伦比的使用Git指南。 （资料来源：XKCD）</i></p>

  


### 创建一个新的存储库 <a name="Create_new"></a>

在GitHub配置文件中，单击“创建新存储库”。 第一步是创建一个名称作为项目的品牌。 理想情况下，它应该是令人难忘的，并给出项目的作用。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/new_repo.png?raw=true" width="800" /></p>

<p align="center"><i>创建一个新的存储库</i></p>

  


确保不要复制名称，侵犯其他商标，或将其命名为可能被认为具有攻击性的任何商标。

  


## 基本步骤 <a name="Foundation"></a>

任何GitHub存储库都需要4个关键元素才能开始并开始开发一个热情的社区：

1. 开源许可证;
2. 一个 `README` 文件;
3. 贡献指南;和
4. 行为准则。

这些是用户了解其合法权利，期望，项目目的以及改善整体用户体验的任何项目的关键方面和最佳实践。

所有这四个文件都应保存在项目存储库的根目录中。 这是约定使用降价的文件格式（`.MD`）大多数这些文件的（尽管许可证文件是最常见的纯文本（`.TXT`）），并利用所有文件名。 而不是文件名中的空格，请确保使用下划线 `_`。

所以你最终应该选择这样的基础文件：

1. `LICENSE.md`
2. `README.md`
3. `CONTRIBUTING.md`
4. `CODE_OF_CONDUCT.md`

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/foundation.png?raw=true" width="800" /></p>

<p align="center"><i>基本的存储库结构</i></p>

  


### 选择许可证 <a name="License"></a>

选择适当的许可证将使您的开源存储库与公开可用的软件区别开来。 虽然您没有义务选择许可证，但这样做可以保证其他人能够在法律框架内修改，共享，重复使用和构建您的项目。

首先，您要检查 [选择许可证](https://choosealicense.com/) 以查找最适合您的存储库意图的许可证。

三个主要可供选择的是：

* **麻省理工学院许可证**：许可许可证，允许人们对您的代码做任何他们想做的事情，只要他们向您提供适当的归属，并且不会让您承担责任。
* **Apache许可证2.0**：对MIT许可证的类似权限，但也向用户的贡献者提供明确的专利权授予。
* **GNU通用公共许可证（GPL）第三版**：一个 [copyleft的](https://en.wikipedia.org/wiki/Copyleft) 许可证需要任何人谁重新分配你的代码，或衍生作品，使源可按照同样的条件与原许可证;还向用户的贡献者提供明确的专利权授予。

值得庆幸的是，当您在GitHub上启动新存储库时，您可以从下拉菜单中选择现有许可证。 您应该始终（极少数例外）使用现有许可证，因为这是潜在用户和贡献者在选择使用或贡献您的软件之前会看到的。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/license.png?raw=true" width="800" /></p>

<p align="center"><i>选择示例许可证</i></p>

  


如果他们没有您想要的，您可以手动添加一个。 要执行此操作，只需单击存储库中的“创建新文件”，然后复制并粘贴现有许可证文本。 将文件命名为 `LICENSE.txt` 或 `LICENSE.md` 以使其清除，并将其保存在主存储库文件夹（即根目录）中。 确保添加一个干净的提交消息，你就完成了！

> **助手**：此MOOC对代码内容和非代码内容使用不同的许可证组合。 在这里，您可以找到我们申请的所有代码和软件的 [MIT许可证](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/LICENSE.md) 的示例，该代码和软件是作为MOOC生产的一部分生成的。

  


### 创建README文件 <a name="Readme"></a>

初始化新存储库时，应该有一个使用 `README` 文件的选项。 就像爱丽丝梦游仙境一样，这些正是他们所说的 - 提供关于项目的关键信息。 这些通常是外部贡献者在访问您的存储库时会看到的第一件事，因此让他们提供信息和欢迎是关键。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/readme.png?raw=true" width="800" /></p>

<p align="center"><i>此模块的README文件的一部分</i></p>

  


该文件最初将采用markdown（`.md`）格式。 这是一种纯文本格式的轻量级标记语言。 要学习一些基本的降价，请参见 [此备忘单](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)。 但就目前而言，我们可以使用纯文本。

您需要在 `README` 文件中包含以下几项内容：

* 这个项目是关于什么的，它做了什么。
* 人们为什么要关心，为什么它有用。
* 如何有人开始为项目做贡献。
* 如果有人需要帮助，可以联系谁。
* 许可证，贡献指南和行为准则的链接。
* 项目结构的描述。
* 谁参与，他们的角色是什么。
* 项目的当前状态。

> **专业提示**：随着项目的发展，您可能希望根据社区反馈添加常见问题解答，或者帮助用户了解项目工作原理的教程。

请记住，并非所有参与您项目的人都是专家，或了解您正在做什么以及为什么。 拥有详细记录的 `README` 文件将增强具有一系列先验知识的人的用户体验。

当 `README` 文件包含在根目录中时，GitHub将自动在存储库的主页上显示该文件。 这意味着这是人们经常看到的第一件事，所以算一算！

> **助手**：在这里，您可以找到用于此 [MOOC模块](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md)的 `README` 文件。 这包括有关状态，基本原理，学习成果，开发团队，关键文档和帮助许可的信息。 您可以根据需要为自己的项目复制和调整此结构。

  


### 创建贡献指南 <a name="Contributing"></a>

贡献指南旨在向潜在的贡献者传达如何与您的项目和社区互动的简短指南。 您希望确保欢迎，并表明您渴望参与者参与您的项目。 每当参与者打开新的拉取请求或创建新问题时，他们都会看到指向您的贡献文件的链接。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/contributing.png?raw=true" width="800" /></p>

<p align="center"><i>该模块的“贡献”指南的一部分</i></p>

  


坚持使用全部大写文件名，下一步是创建一个 `贡献` 文件。 单击“创建新文件”，并确保像以前一样以标记格式保存。 该文件将告诉其他用户他们如何参与和参与您的项目。 这是围绕您的项目建立社区的第一步，因此请使其具有吸引力，简洁和信息。

`CONTRIBUTING` 文件应包含以下信息：

* 您正在寻找什么样的贡献。
* 如何建议更新或新功能。
* 如何使用GitHub的功能（例如拉取请求协议）与项目交互。
* 如何提交错误报告或创建问题。
* 项目的最终目标，愿景或路线图。
* 如何联系项目负责人。
* 指向任何外部文档或网站的链接。

> **专业提示**：考虑让人们花时间考虑贡献，请考虑简短的感谢信 - 他们点击了文件以了解更多信息！ 如果您还有其他识别方法，请务必将它们包含在此处。

在这里，您基本上是在鼓励人们自愿花时间推进您的项目。 确保热情友好，并确保人们如何参与。 在撰写本文时，请务必从用户的角度考虑这一点 - 在提交拉取请求和打开问题以使整个项目更顺畅地运行时，如何让他们的生活更轻松。

> **帮助手**：此MOOC模块的 [贡献指南](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CONTRIBUTING.md) 包括一些非常具体的内容：使用Git和GitHub的介绍，入门提示，联系信息，如何更改内容和报告问题，链接到 `README` 文件，以及有关首选内容和代码样式的信息。 您可以根据需要随意复制和修改此项目。

  


### 制定行为准则 <a name="Conduct"></a>

行为准则对于为项目贡献者设定预期行为和参与的基本规则非常重要，并且是一个易于参考的文档，用于表明您的项目团队认真对待建设性对话。 因此，它是创造和维持一个健康社区的关键因素，在积极的社会氛围中以建设性和富有成效的方式参与其中。

行为准则不仅提供了对行为的期望，而且还描述了这些期望适用于谁，何时适用，如果违反代码会发生什么，以及针对此的行动项目。 因此，需要在行为准则中明确联系点。 通常，这应该是私人方式，例如电子邮件地址。

> **专业提示**：如果需要报告有关收到这些报告的人的违规行为，请确保包含联系辅助方的选项。

要添加行为准则，您可以通过添加新的降价文件从头开始创建自己的行为，或者使用现有模板，例如 [Contributor Covenant](https://contributor-covenant.org/)。 将文件命名为 `CODE_OF_CONDUCT.md`，并确保它在 `README` 文件中可见。

> **助手**：本MOOC还有基于贡献者公约的 [行为准则](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CODE_OF_CONDUCT.md)。 如您所见，它包括有关行为的预期标准，社区中的责任以及CoC执行的信息，包括联系方式。 您可以随意重新使用并根据需要将其调整到您的项目中。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/code_of_conduct.png?raw=true" width="800" /></p>

<p align="center"><i>此模块的CODE OF CONDUCT文件的一部分，基于Contributor Covenant</i></p>

  


确保执行行为准则非常重要，因为它表明您不仅重视代码，还尊重它对您社区的影响。 重要的是要尊重社区中的每个成员，尊重他们应得的尊重，礼貌和重要性。 如果发生违规行为，或重复违规者一致违规，最好参考 [开源指南](https://opensource.guide/code-of-conduct/#enforcing-your-code-of-conduct) ，了解如何执行行为准则。

  


### 使你的代码可以理解 <a name="Citation"></a>

如果你想从一开始就让代码变得可行，你应该通过创建一个 `[codemeta.json]（https://codemeta.github.io)` 文件或 `[CITATION.cff]（https： //citation-file-format.github.io)5` 文件。 两者都将允许当前正在开发的工具自动创建引文信息，而不是要求您稍后在表单中键入它。

如果您有兴趣， [cite.research-software.org](https://cite.research-software.org) 提供了有关学术界软件引用的更多背景信息。

  


## 让您的问题保持最新 <a name="Issues"></a>

问题不一定是项目的问题，而是改进建议，未来发展的事情，以及有关项目的评论和反馈。 他们可以根据需要与贡献者公开分享和讨论，有点像论坛。

如果您是项目负责人，那么维护一系列问题非常重要，这些问题可以使贡献者清楚地了解项目的哪些方面需要注意。 同样重要的是以积极的方式与其他人讨论尽可能多的问题，以表明你认真对待他们的贡献。

问题的关键要素包括：

* 信息标题和描述;
* 用于分类和过滤的Coloud编码标签/标签;
* 将问题与特定功能或项目阶段相关联的里程碑;
* 受让人表明谁负责处理某个问题;
* 提供反馈的评论。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/issues.png?raw=true" width="800" /></p>

<p align="center"><i>开放奖学金战略项目的问题跟踪器</i></p>

  


在问题中，可以使用@ mentions通知其他contirbutors有关该问题，并让合适的人员以有效的方式参与。 GitHub有一个内部通知系统，就像Facebook或Twitter一样，也可以向问题跟踪器中提到的人发送电子邮件。 这些都可以在用户设置中为个人定制。

  


## 启动项目的清单 <a name="Checklist"></a>

所以现在你已准备好启动你的项目，开始做广告，并获得贡献！ 在继续之前，请确保您拥有：

* []项目有一个令人难忘和信息丰富的名称
* [] Project有一个 `LICENSE` 文件，它是开源许可证的精确副本
* []完整的文档包括一个 `自述`， `贡献`，和 `CODE_OF_CONDUCT` 档
* []项目至少有一个明确标注的问题
* []此阶段包含的任何代码都有明确的结构和注释

**恭喜！**

您现在已经启动了一个开源研究项目！ 希望从现在开始，您的工作将有利于更广泛的社区，建立新的合作，并为您创造新的和梦幻般的机会。 尝试并考虑将这些技能应用于未来项目的方式，以及它们在过去如何帮助过一些项目。

从现在开始，这完全取决于你！ 一些建议是：

* 写清洁代码;
* 有一个结构良好的项目;
* 经常提交干净的信息;
* 保持项目记录良好;
* 有明确的贡献准则;
* 利用描述和标签功能;
* 除非你打算对它们进行处理，否则不要分叉别人的存储库;
* 确保也为其他人的项目做出贡献。

**知道这种内容可以改进的方式吗？**

是时候将新的GitHub技能用于测试运行了！ 所有内容主要发展发生 [这里](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)。 如果您对内容，布局或其他任何内容有建议的改进，您可以制作它，然后在主持人验证后它将自动成为MOOC内容的一部分！

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)