---
output:
  html_document: 默认
  pdf_document: 默认
---

# 第5单元：开放研究软件和开源

## 目录

- [介绍](#Introduction)
- [什么是开源软件](#What_OSS)
- [开源软件原理](#Principles)
- [开源社区，治理和贡献](#OS_Community)
- [开源软件的现有平台和工具](#Platforms)
- [用于研究的开源软件](#Research)
- [OSS入门 - 常见问题解答](#FAQ)
- [制作好的软件以便重复使用](#Reuse)
- [开源许可](#Licensing)
- [软件引用](#Citation)
- [使用GitHub和Zenodo](#GitHub_Zenodo)
- [通过开源协作](#Collaborating)
- [从这往哪儿走](#Future_OSS)

**请注意** 可以通过 [Soundcloud](https://soundcloud.com/open-science-mooc/module-5-open-source-and-open-research-software) 和 [YouTube](https://www.youtube.com/watch?v=BHrOEmKk5zM)下载音频版本。

## 介绍 <a name="Introduction"></a>

欢迎来到开放科学MOOC的 **模块5** ： **开放研究软件和开源**。

该模块已经开发 [在打开](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source) 通过协作通过的一个国际研究小组 [开源afficianados](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md#development-team-)。 您在此处看到的所有内容都是通过来自更广泛社区的互动反馈和协作开放的。 它包含一系列视频，信息图表，基于文本的阅读和实用任务，让您沉浸其中。

不要忘记你可以参加我们的开放 [**Slack频道**](https://osmooc.herokuapp.com/)。 请在＃module5opensource上自我介绍一下，并告诉我们你是谁，你的背景，以及你如何在这里结束！

### 这个模块是谁的？

该模块主要面向研究生和本科生阶段的计算研究人员，以及新兴数据科学家和使用分析代码或软件的任何其他研究人员。 在现代研究环境中，这几乎涵盖了使用计算机进行工作的任何人。

> “关于计算结果的文章是广告，而不是奖学金。 实际的奖学金是产生结果的完整软件环境，代码和数据。“ - J. Buckheit和DL Donoho，1995。

软件和技术是现代研究的基础，现在几乎不可避免地以某种方式计算 - 搜索引擎，社交网络平台，分析软件和数字出版。 有了这个，对更复杂的开源软件的需求不断增加，相比之下，研究人员越来越愿意公开合作开发新工具。

开源的力量在于它降低了协作和采用的障碍，因此允许思想和技术更快地传播。 本单元将介绍将软件转换为可由其他人公开访问和重用的内容所需的必要工具。

<img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/open_research_software_open_source.png?raw=true" width="800" />

<p align="center"><i>图片来自Patrick Hochstenbach（CC0 1.0 Universal）</i></p>

  


### **本单元**具体学习目标：

1. 了解开放软件的特点;了解 **伦理，法律，经济和研究影响赞成和反对开源软件**，进一步了解开放代码的质量要求。

2. 能够将个人使用的代码转换为其他人可以访问的开放代码。

3. 使用利用开放内容的软件（工具）并鼓励更广泛的协作。

  


## 什么是开源软件 <a name="What_OSS"></a>

事实上，所有现代科学研究工作流程都依赖于一系列软件工具，可以在不同的数据集上运行，使用不同的参数，以各种方式迭代应用（数据科学）或在不同的输入上运行，并使用模型和方法预测某些输出状态（计算科学）。 开源软件（OSS）是一种计算机软件，其中完整的源代码在特定许可下可用，使其他用户可以出于任何目的访问，查看，修改和重新分发该代码。 由于OSS需要此类许可证，因此默认情况下通常保持免费。 这种明确的许可也是OSS与自由软件的区别。 与专有软件相比，重复使用OSS进行分析，模拟和可视化研究通常也更容易，更灵活。 通常，无论我们是否知道，我们已经将OSS作为我们自己的研究工作流程的一部分。

OSS适用于更广泛的开放科学计划，因为它有助于使完整的研究环境，包括产生研究结果的软件，完全可访问和可重用。 因此，它形成用于最佳实践的必要组成部分（[门尼斯等人，2018](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf)）和可重复性和研究再现性（包括个人和其他），连同其它部件，诸如共享数据（[Stodden，2010](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf)）。

在某些情况下，共享源代码甚至可以成为接受相关研究手稿的条件（[Shamir et al。，2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Shamir%20et%20al.%2C%202013.pdf)）。 人们普遍认为它会增加研究影响（[Vandwalle，2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Vandewalle%2C%202012.pdf)）。

开发人员的一些共同优势包括：

- 提高开发人员的忠诚度和授权;

- 降低服务和营销成本;

- 增加服务和产品的品牌;

- 以较低的费用生产高质量的软件;

- 灵活性和快速创新;

- 定制和模块化集成;

- 提高可靠性和独立性;和

- 基于每个人都可以使用的开放标准。

这样，研究人员的主要优点（用户）包括 **降低成本**， **增加透明度**， **增加安全性和稳定性**， **没有厂商“锁定”具有增加的用户控制**和 **的整体更高质量**。 此外，共享OSS允许研究人员为他们的努力获得信誉，例如通过直接软件引用 [（Smith等，2016）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf)。

常用的OSS包括 [Mozilla Firefox](https://www.mozilla.org/en-US/firefox/) 互联网浏览器和 [LibreOffice](https://www.libreoffice.org/) 全办公套件。 LibreOffice类似于流行的Microsoft Office，包括文字处理器，电子表格管理器和幻灯片演示软件，但完全免费且开源。

一些人认为，开放源码软件运动代表了新自由主义和私有化的反向运动，通过蔑视信息的构建和再利用中的规则和规范，以及通过尽可能少地利用软件大量提供软件来实现现代资本主义的潜在转变。 请参阅 [自由/开源软件运动：阻力还是变化？](http://www.redalyc.org/html/742/74212712006/) 由Panayiota Georgopoulou提供有关此主题的更多信息。

  


## 开源软件原理 <a name="Principles"></a>

[开源倡议](https://opensource.org/)，OSS的先驱之一，提供以下 [定义](https://en.wikipedia.org/wiki/The_Open_Source_Definition#Definition)：

*别担心，您不需要记住所有这些，但了解OSS的原理是很好的。*

- **免费再分发**：许可不得限制任何一方销售或赠送软件，作为包含来自多个不同来源的程序的软件分发的组成部分。 许可证不需要特许权使用费或其他费用进行此类销售。
    
    - **源代码**：程序必须包含源代码，并且必须允许在源代码和编译形式中进行分发。 如果某种形式的产品没有与源代码一起分发，则必须有一种广为人知的获取源代码的方法，最好不超过合理的复制成本，通过互联网免费下载。 源代码必须是程序员修改程序的首选形式。 不允许故意混淆源代码。 不允许使用中间形式，例如预处理器或转换器的输出。
    
    - **衍生作品**：许可证必须允许修改和衍生作品，并且必须允许它们以与原始软件许可证相同的条款进行分发。
    
    - **作者源代码的完整性**：只有在许可证允许使用源代码分发“补丁文件”以便在构建时修改程序时，许可证才可以限制源代码以修改形式分发。 许可证必须明确允许分发由修改后的源代码构建的软件。 许可证可能要求派生作品携带与原始软件不同的名称或版本号。
    
    - **不歧视个人或团体**：许可证不得歧视任何人或团体。
    
    - **对奋斗领域的歧视**：许可证不得限制任何人在特定领域努力使用该程序。 例如，它可能不会限制程序在企业中使用，也不会用于基因研究。
    
    - **许可证**分发：程序附带的权利必须适用于程序重新分发的所有人，而无需由这些方执行额外的许可证。
    
    - **许可证不得特定于产品**：程序附带的权利不得取决于程序是特定软件分发的一部分。 如果程序是从该分发中提取并在程序许可条款中使用或分发的，则重新分发程序的所有各方应具有与原始软件分发一起授予的权限相同的权限。
    
    - **许可证不得限制其他软件**：许可证不得对与许可软件一起分发的其他软件加以限制。 例如，许可证不得坚持在同一介质上分发的所有其他程序必须是开源软件。
    
    - **License Must Be Technology-Neutral**: No provision of the license may be predicated on any individual technology or style of interface.

现在，记住这一切可能有点复杂。 但是，它可以概括为 *使软件尽可能可用于未来的工作，同时也可免费获得*。

  


## 开源清单

有许多支持OSS和协作的现有平台和工具。 [开放科学培训手册](https://open-science-training-handbook.gitbook.io/book/) 提供了一个检查表，用于评估现有研究软件的“开放性”，基于上面的开源定义：

- []软件是否可供下载和安装？

- []软件可以轻松安装在不同的平台上吗？

- []软件是否有使用条件？

- []源代码是否可供检查？

- []源代码的完整历史记录是否可通过公开版本历史记录进行检查？

- []软件（硬件和软件）的依赖关系是否正确描述？ 这些依赖关系是否只需要相当少的努力来获取和使用？

检查，检查，检查，完成！ Simples。

  


## 开源社区及其治理 <a name="OS_Community"></a>

自由软件社区中有两个主要阵营： **自由软件运动**和 **OSS运动**。 两者都有不同的意识形态，这些意识形态基于用户自由和软件的实际应用。 通常，“FLOSS”一词用于调和这两个政治阵营，意为“自由/自由和开源软件”; Libre在自由的背景下是“免费”的法语和西班牙语。

重用的核心原则是将OSS与“自由软件”区分开来。 免费和开源软件（FOSS）是一个包容性术语，用于描述可分为免费和开源的软件。 FOSS的一个很好的例子是 [Ubuntu Linux](https://www.ubuntu.com/) 操作系统。

自由软件和OSS之间的最大区别在于，前者必须在与原始版本相同的许可下分发更新版本，而较新版本的OSS可以在不同许可下分发。 FOSS结合了两全其美。

这些定义现在已被国际政府以及一些大型组织广泛采用，如 [Mozilla Foundation](https://www.mozilla.org/en-US/foundation/) 和 [Wikimedia Foundation](https://wikimediafoundation.org/wiki/Home)。 FLOSS领域的主要组织包括英国 [软件可持续发展研究所](https://www.software.ac.uk/)，他们提供宝贵的资源，例如最近的 [研究人员软件存款指南](https://softwaresaved.github.io/software-deposit-guidance/)。

### 对于个别项目

典型的开源项目具有以下类型的正式角色：

- **作者**：创建项目的人
- **所有者**：对组织或存储库具有管理所有权的人员 
- **维护者**：负责推动愿景和管理项目组织方面的贡献者。 （他们也可能是项目的作者或所有者。）
- **贡献者**：已经为项目做出贡献的用户。
- **社区成员**：使用该项目的人员。 他们可能积极参与对话，创建新问题或表达他们对未来项目改进的意见。

通常，角色通过 `README` 文件，Contributors文件或项目的单独团队页面公开。

  


## 开源软件的现有平台和工具 <a name="Platforms"></a>

虚拟环境和机器作为高性能研究工作流程推动者正变得越来越流行，其中许多基于OSS（例如，操作系统，编程语言和数据处理框架）。 流行的服务包括 [Google Cloud](https://cloud.google.com/compute/) 和 [Amazon Web Services](https://aws.amazon.com/)，它们还有助于数据库存储和内容交付以及计算能力。 [InsideDNA](https://insidedna.me/) 是一个可重复研究生物信息学，基因组学和生命科学的计算平台。

如所提及的 [以上](#What_OSS)，LibreOffice的提供了一种开源替代的Microsoft Office。 两者几乎完全兼容，只是使用不同的默认文件格式。 对于引文管理者来说， [Zotero](https://www.zotero.org/) 是最受欢迎的开源替代品，如Mendeley或EndNote等专有平台。

[Zotero](https://www.zotero.org/) 使用BibTeX（发音为'bib-tech'）格式，基于LaTeX（发音为'lay-tech'），并具有浏览器插件，使引文管理变得简单。 通过将其与LibreOffice等其他软件集成，现在可以在许多情况下拥有完全开源的研究工作流程。

### GitHub上 <a name="GitHub"></a>

> 您是否知道整个项目是作为 [GitHub](https://github.com/OpenScienceMOOC/)的开放和协作社区工作而构建的？

[GitHub](https://github.com/) 是软件和非软件内容（通常称为“笔记本”）的流行托管站点，具有版本控制，项目管理和跟踪以及存储服务的附加功能。 GitHub构建于OSS [Git](https://git-scm.com/)之上，使用户能够远程工作以维护，共享和协作研究软件和其他非基于软件的项目。

版本控制本质上是一个过程，它捕获存储库中文件的快照，并跟踪对它们的修改。 它记录了更改的时间，更改的内容以及执行更改的人员。 如果有多个人同时处理一个文件，则会检测到任何重叠的更改，并且必须在继续之前解决。 与项目开发时手动保存和记录更改相比，这提供了更加简化和自动化的过程。 它还避免了不可避免的混淆命名文件版本列表......

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>GitHub帮助我们避免，呃，次优的文件命名约定（来源：XKCD）</i></p>

  


GitHub的一个比较流行和有用的功能是 [问题跟踪器](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues)，用于组织OSS开发。 以上链接将您带到问题跟踪器以开发此模块！ 如果你认为这里有一些可以改进的东西，或者你想评论，任何人都可以在那里添加或贡献一个问题！

其它类似的项目托管服务，包括 [到位桶](https://bitbucket.org/)， [GitLab](https://about.gitlab.com/)和 [的Launchpad](https://launchpad.net/)。 如果微软最近对GitHub的收购对你有点不利，那么这些都是很好的选择。

但是，我们也知道GitHub可以有很高的学习曲线。 这就是为什么这个MOOC的第一个实际任务将教你如何设置你的第一个GitHub项目存储库！

**[转到任务1：构建您的第一个GitHub存储库](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## 用于研究的开源软件 <a name="Research"></a>

特别是在科学研究方面，开源软件的使用和开发已经成为一种常态。 除了适用于消费者，行业或政府等普遍接受OSS的原因之外，还有很多原因。 其中包括：

- 在分析软件中实施的算法越来越多地成为学术出版物中描述的方法的组成部分。 因此，如果这些算法实现对外人关闭，那么它与严格的同行评审完全不一致。

- 科学合作往往跨越多个机构和分布式研究网络，其中保密和命令层次不是以封闭源开发“必要”的方式维护的。

- 许多计算分析在虚拟化环境（例如机构，国家或国际“云”基础架构）中运行，并托管在多用户服务器上。 封闭源，商业软件通常不允许这样的使用。

- OSS的发展往往依赖于志愿者。 在科学研究的预算限制时期，这是一个明显的优势。

由于这些原因和其他原因，开源工具在科学研究中非常常用。 这包括在许多研究人员都是业余开发人员自己的领域中使用，并依赖于 [R](https://www.r-project.org/) 等工具进行统计分析和编写脚本，在过去十年中，这些工具几乎完全取代了用于统计分析的商业软件，如SPSS或JMP。很多领域。 在生物信息学等领域，涉及DNA测序平台输出的大量文件处理，通用脚本语言，如 [Python](https://www.python.org/) 和基于它的常用库（如 [biopython](http://biopython.org)）已成为至关重要的许多研究人员的工具包的一部分。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>蟒蛇</i></p>

  


R和Python等工具本质上是编写软件的软件。 虽然规划是研究人员一个越来越普遍的活动，当然不是 *每* 科学家做到这一点。 离编程只有一步的步骤是将较长工作流程中各种分析工具的输入和输出链接在一起。 作为基因组学的一个例子，一个非常常见的工作流程是从高通量测序读数开始，然后i）进行基本的质量控制检查; ii）将读数映射到参考基因组; iii）确定新数据与参考不一致的点。 这些步骤通常作为工作流执行，其中在Linux命令行环境中为三个步骤中的每个步骤运行不同的开源可执行文件。 虽然这可能不是一个非常开源的软件开发，但它确实涉及开源工件（例如Linux shell脚本）的使用和生产，我们在本模块中讨论的原则适用于这些工件。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>[R</i></p>

  


最后，OSS也用于科学研究，其原因更接近于那些推动OSS在更广泛社会中采用的原因，即它很便宜。 例如，个人或组织可能决定从Microsoft Office切换到LibreOffice进行稿件编写或电子表格处理，因为后者是免费的（如 [**'免费啤酒'**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) 和'言论自由'）。 同样，可以简单地通过成本考虑来选择从ArcGIS切换到 [QGIS](https://www.qgis.org/en/site/) 以分析地理信息。   


## OSS入门 - 常见问题解答 <a name="FAQ"></a>

**我正在使用X [例如Matlab，STATA，Excel]，我希望转换到更开放的东西。 什么是下一个步骤？**

即使您使用的是专有软件，您通常仍可以共享源代码/文档等。 *最好的第一步是尽可能分享*。

**大！ 我可以把它们放在我的新github回购中。**

如果这对你来说已经足够了！ 如果不是大多数专有软件，则有开源等价物。 和一个人一起去看看你的想法。

| 关闭                                                                              | 打开                                                                                                                                             |
| ------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| MATLAB                                                                          | Python，朱莉娅                                                                                                                                     |
| STATA / SPSS                                                                    | [R                                                                                                                                             |
| 微软Office                                                                        | LibreOffice的                                                                                                                                   |
| 数学                                                                              | JupyterLab                                                                                                                                     |
| 测试你的新 [拉请求-PR-](https://help.github.com/articles/about-pull-requests/) 技能...... | ... 在这里添加你自己的例子 [](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**凉！ 但是，如果我进行切换，我将陷入困境：需要多年才能学习新工具/没有支持/使用有缺陷的软件。**

好问题！ 答案取决于它。 最好的办法是找一个以前做过转换的人，并从他们的经验中学习。 或者只是进行谷歌搜索！ 有些OSS比封闭式对应物要好得多，有些则不然，所以值得仔细选择。

## 制作好的软件以便重复使用 <a name="Reuse"></a>

最有可能在将来重新使用您的软件的人是......你！ 因此，虽然共享总是优于不共享，但通过适当的文档，您可以更轻松地创建自己和他人的生活。 文档可以包含几个内容，例如在代码中包含有用的注释和注释，以帮助解释执行特定操作的原因，而不是它要实现的目标。

其中一个最重要的方面是包含一个信息丰富的 `README` 文件，几乎每个OSS项目都有，有时甚至不止一个。 在每个目录中包含一个这样的文件是一个好习惯，其中包括文件列表，目录以及目录的用途。 `README` 文件通常只是纯文本或markdown（再次，例如MOOC的所有文件！），并且可以包含有关如何安装和运行软件的关键信息，以前的依赖关系和要求，以及教程或例子。

> **你知道吗** 术语 `README` 是一些次调皮地归因于刘易斯·卡罗尔的爱丽丝梦游著名的场景在仙境中的爱丽丝面对标有神奇的零食“吃我””和‘喝我’。 有效。

这里的目的是提供足够的信息以最大化计算环境的重用和再现性，使得没有项目经验的人可以轻松访问和重用软件（[Sandve等，2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)）。 通过降低进入壁垒，您可以增加其他人重新使用您工作的机会，这是OSS的最终目标之一（[Ince et al。，2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)）。

这种扩展有助于使未来重复使用更加容易，是“容器”技术。 容器就像一个及时冻结的生态系统，代码，数据和任何其他依赖关系都完美地保存，打包并保存在当前功能版本中。 这意味着将来任何人都可以进入并再次运行分析。 因此，它们通常适合重复使用，但这可能是由于其他人修改或理解而牺牲的，因为通常很多细节都可以隐藏在源代码及其依赖项中。 研究中容器实现的常见示例包括 [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) （R语言的Docker容器）， [Binder](https://mybinder.readthedocs.io/en/latest/)和 [Code Ocean](https://codeocean.com/)。

**可持续软件是很好的软件。**

  


## 可重复计算研究的10条简单规则

根据 [Sandve et al。，（2013）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)，使计算研究更具可重复性的10条简单规则是：

1. 对于每个结果，跟踪它的生成方式。
2. 避免手动数据操作步骤。
3. 存档所有使用的外部程序的确切版本。
4. 版本控制所有自定义脚本。
5. 尽可能以标准格式记录所有中间结果。
6. 对于包含随机性的分析，请注意基础随机种子。
7. 始终将原始数据存储在图表后面。
8. 生成分层分析输出，允许检查增加细节的层。
9. 将文本语句连接到基础结果。
10. 提供对脚本，运行和结果的公共访问。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/simple_rules.png?raw=true" width="800" /></p>

<p align="center"><i>信息图改编自Sandve等，（2013）。 随意下载并打印出来，以便在研究期间保持方便！</i></p>

  


如果您按照这些步骤，以及 [**任务1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) 和 [**任务2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)，您应该没问题！

  


## 开源许可 <a name="Licensing"></a>

开源许可证是一种专门为软件和代码设计的许可证，它明确了共享和重用的法律条件。 如所提及的 [以上](#What_OSS)，加入合适的许可的是什么区别公开从OSS共享软件。 例如，广泛使用的 [MATLAB](https://www.mathworks.com/products/matlab.html) 是专有软件， [Octave](https://www.gnu.org/software/octave/) 是一种公开许可的替代编程语言。

目前有超过1,400个独特的开源许可证，由于难以理解不同许可证之间的法律影响之间的差异而产生的复杂性。

一些更常见的许可证包括：

- [Berkeley Software Distribution（“BSD”）](https://en.wikipedia.org/wiki/BSD_licenses)，
- [Apache](https://www.apache.org/licenses/LICENSE-2.0)，
- [麻省理工学院（麻省理工学院）](https://opensource.org/licenses/MIT)，或
- [GNU通用公共许可证（“GPL”）](https://www.gnu.org/licenses/gpl-3.0.en.html)。

你不需要知道所有这些背后的所有法律因素，但至少知道哪些选项可供你使用是好的。

有两种方式可以对项目的贡献获得许可：

1. *明确*，个人捐款具有明确指示的许可证，独立于主项目;要么
2. *隐含*，其中贡献属于主项目的原始许可代码。

值得庆幸的是，由于用户友好的工具，例如 [选择许可证](https://choosealicense.com/)，选择开源许可证的过程相对简单。 这些许可证中的每一个都允许其他用户使用，复制，分发和构建您的工作，通常同时确保创作者的工作得到适当的认可。 在这里，关键是为您的工作选择合适的许可证，具体取决于您想要或不想要的，其他人使用它。

  


## 软件引用 <a name="Citation"></a>

引文提供了学术研究中最重要的互动之一，形成了我们的参考和指标系统的基础。 通常，这是由于诸如 [数字对象标识符](https://en.wikipedia.org/wiki/Digital_object_identifier) （DOI）之类的永久唯一标识符的帮助而执行的。 DOI是在 [句柄系统](https://en.wikipedia.org/wiki/Handle_System)实现的持久标识符，其根据目的满足共同标准，例如用于识别学术信息。 这种识别对于跟踪研究的系谱和来源，重现性以及为创建软件的人提供适当的信誉至关重要。 重要的是，软件应该被认为是学术研究的合法输出，引用正在成为一种越来越常见的方式来表明这一点。

在2016年， [Smith等人，2016年](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) 撰写了一篇关于软件引用原则的研究论文，作为FORCE11软件引用工作组的一部分。 与您想要引用您作为良好研究实践的一部分使用的软件的方式相同，重要的是使您的研究也很容易引用。 在引用用于您自己研究的任何软件时，您应至少包括：

- 作者姓名，
- 软件名称，
- 版本号，和
- 唯一标识符/定位符（DOI或URL）。

由六个原则软件引证的 [。Smith等人，（2016）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) ，这里提供：

- **重要性**：软件应被视为合法且可引用的研究产品。 软件引用在学术记录中应与其他研究产品（如出版物和数据）的引用一样重要;它们应该包含在引用工作的元数据中，例如在期刊文章的参考列表中，不应该被省略或分开。 软件的引用应与任何其他研究产品（如纸张或书籍）相同，即作者应引用适当的软件产品集，就像它们引用适当的论文集一样。

- **信用和归属**：软件引用应有助于向软件的所有贡献者提供学术信用和规范的法律归属，并认识到单一的归属方式或机制可能不适用于所有软件。

- **唯一标识**：软件引用应包括一种机器可操作的识别方法，全球唯一，可互操作，并且至少由相应领域专家的社区识别，并且最好由一般公众研究人员识别。

- **持久性**：描述软件及其处置的唯一标识符和元数据应该保持不变 - 甚至超出他们描述的软件的生命周期。

- **可访问性**：软件引用应有助于访问软件本身及其相关的元数据，文档，数据以及人员和机器所需的其他材料，以便明智地使用所引用的软件。

- **特异性**：软件引用应有助于识别和访问所使用的特定软件版本。 软件标识应尽可能具体，例如使用版本号，修订号或平台等变体。

注意：有关“如何使您的软件可用”的说明，请参阅下面的 [**使用GitHub和Zenodo**](#GitHub_Zenodo) 以及 [**任务2：链接GitHub和Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)。

  


## 使用GitHub和Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) 是一个用于项目管理，内容存储和版本控制的流行工具。 请注意，GitHub本身不是OSS。 然而，Git，它所基于的工具，是。 Git旨在帮助管理与软件相关的项目的源代码文件及其更新。 但是，它也可以扩展到其他非软件项目;例如，这 [MOOC](https://github.com/OpenScienceMOOC/)！

然而，对GitHub进行研究只是第一步。 使其持久且可重复使用同样重要，这就是为什么拥有与之相关的数字对象标识符（DOI）可能很有用的原因。 最简单的方法是通过名为 [Zenodo](https://zenodo.org/)的服务，这是一个由OpenAIRE和CERN创建的免费开源多学科存储库，可用于为各个GitHub存储库分配DOI。 有一个 [GitHub指南](https://guides.github.com/activities/citable-code/) 解释了详细信息，其中涉及将GitHub存储库直接链接到Zenodo，以便当开发人员为其软件创建正式版本时，Zenodo创建并存档该版本的软件。

使用Zenodo创建DOI并没有什么特别之处，除了 **免费**;也可以使用其他通用存储库，例如 [DataCite DOI Fabrica](https://doi.datacite.org/)，或您自己的机构存储库，例如 [Caltech](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata)。

许多研究人员可能通常害怕共享不完整，错误或不完美的代码。 但是，在OSS社区中，这种共享“原始”代码的做法相当普遍。 公开共享代码使其他人能够重复使用和改进代码，并且可以更深入地参与与之相关的任何研究。 这是同行合作的基本方面之一，也许最好的例子是传统的研究手稿同行评审过程。

任务2将指导您完成将GitHub存储库链接到Zenodo以进行存档的过程。

> **您知道吗......** 为此MOOC制作的所有内容均作为 [Zenodo](https://zenodo.org/communities/open-science-mooc/)社区的一部分提供？

**[转到任务2：链接GitHub和Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## 通过开源合作和贡献 <a name="Collaborating"></a>

通常，OSS是在多个贡献者之间以公共，分散，协作的方式开发的。 其目的是增强项目及其设计的多样性和范围，以便变得更有益和可持续。 这种方法被着名的早期OSS支持者Eric Raymond称为“市集”模型。 其中一个主要的指导原则是 **同伴制作**，它依靠自组织社区来规范内容的发展，协调共同的目标或结果。

OSS项目在很大程度上依赖于志愿者合作，这通常需要不断变化的新移民才能变得富有成效和可持续（[Steinmacher et al。，2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)）。 为项目创造合适的社交氛围和热情的参与环境通常对OSS中成功的合作关系至关重要。

  


## 从这往哪儿走 <a name="Future_OSS"></a>

希望现在你已经看到了软件作为现代科学基石的重要性，以及OSS在这方面的重要性。

这个 **学习成果** 应该是：

1. 您现在可以定义OSS的特征，以及支持和反对它的一些道德，法律，经济和研究影响论点。

2. 根据社区标准，您现在可以描述共享和重用开放代码的质量要求。

3. 您现在可以使用一系列利用OSS的研究工具。

4. 您现在可以将为个人使用而设计的代码转换为其他人可访问和可重用的代码。

5. 软件开发人员将能够使他们的软件变得可信，软件用户将知道如何引用他们使用的软件。

  


**奖金任务**

如果你已经完成了 [任务1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) 和 [任务2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)，我们还有 **奖金任务** ，如果你想进一步提高你的技能。 [任务3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) 将向您介绍如何将Git与R Studio集成，从而更深入地将Git集成到典型的研究工作流程中。 建议您在继续执行此任务之前完成前2个任务。

但是，您的开源之旅并不止于此！ 这只是一个开始，如果你想做或了解更多，那里有一些令人难以置信的资源：

- 如果您对此感到特别鼓舞，您可以认可 [科学代码宣言](http://sciencecodemanifesto.org/)，它基于代码，版权，引用，信用和策展的五项原则。

- 为了启动和开发您自己的项目， [开源指南](https://opensource.guide/) 计划提供了一系列实用指南和技能，以帮助启动和推进您的OSS项目。

- 有关基于OSS的研究工作流程的详细介绍，Pedro L. Fernandes和Rutger A. Vos的 [开放科学，开放数据，开源](https://pfern.github.io/OSODOS/gitbook/) 手工指南是在线的顶级资源之一。

- 基于软件的文章也存在更为正式的期刊场所，包括 [The Journal of Open Research Software](https://openresearchsoftware.metajnl.com/) 和 [The Journal of Open Source Software](https://joss.theoj.org/)。 这些场地的清单也是 [可用](https://www.software.ac.uk/which-journals-should-i-publish-my-software)。

- [PLOS开源工具包](https://channels.plos.org/open-source-toolkit) 为开源硬件和软件研究和应用提供了一个全球论坛。

- [NumFOCUS](http://www.numfocus.org) 是一个非营利组织，支持和推广世界一流的创新开源科学软件。 他们赞助的一些项目包括：
    
    - [IPython](http://ipython.org) 和 [Jupyter Notebook](https://jupyter.org) 计划。
    
    - [rOpenSci](http://ropensci.org)，它促进开源R统计环境，以实现透明和可重复的研究。
    
    - 为了获得更多的OSS经验， [Software Carpentry](https://software-carpentry.org/) 社区定期举办研讨会，以提高基于实验室的计算技能（[Wilson et al。，2017](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf)）。

  


### 进一步阅读 <a name="Reading"></a>

*这里的这些参考仅仅是开始。 它们包括一些对研究中开源领域最有用的概述。 但是，如果您想要找到更适合您自己研究领域的东西，那么您可以在那里探索！*

- 自由/开源软件开发研究的未来 [（Scacchi，2010）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Scacchi%2C%202010.pdf)。

- 实践中的科学方法：计算科学中的再现性 [（Stodden，2010）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf)。

- 开放计算机程序的案例 [（Ince et al。，2012）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)。

- 关于开源软件社区的当前问题和研究趋势 [（Martinez-Torres和Diaz-Fernandez，2013）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Martinez-Torres%20and%20Diaz-Fernandez%2C%202013.pdf)。

- 可重复计算研究的十个简单规则 [（Sandve et al。，2013）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)。

- 关于开源软件项目新人面临的障碍的系统性文献综述 [（Steinmacher等，2014）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)。

- 开源软件社区中的知识共享：动机和管理 [（Iskoujina和Roberts，2015）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Iskoujina%20and%20Roberts%2C%202015.pdf)。

- 软件引用原则 [（Smith等，2016）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf)。

- Rocker介绍：R [Docker容器（Boettiger和Eddelbuettel，2017）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf)。

- 足够好的科学计算实践 [（Wilson et al。，2017）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf)。

- 鼓励研究软件 [最佳实践的四个简单建议（Jiménez等，2017）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf)。

  


### 开发团队 <a name="Development_team"></a>

- [Alex Morley](https://twitter.com/alex__morley)，Open Sourceror，英国牛津大学。
- [Kevin Moerman](https://twitter.com/KMMoerman)，Open Sourceror，麻省理工学院，美国。
- [Tania Allard](https://twitter.com/ixek)，开源，英国利兹大学数据美女。
- [Simon Worthington](https://twitter.com/mrchristian99)，Book Liberationist，TIB，Germany。
- [Paola Masuzzo](https://twitter.com/pcmasuzzo)，开源蝙蝠侠，意大利。
- [Ivo Grigorov](https://twitter.com/OAforClimate)，开源罗宾，丹麦。
- [Rutger Vos](https://twitter.com/rvosa)，Open Sourceror，荷兰Naturalis生物多样性中心。
- [Julien Colomb](https://twitter.com/j_colomb)，Open Ninja，Berlin。
- [Jon Tennant](https://twitter.com/protohedgehog)，Dinosaur Whisperer。

**知道这种内容可以改进的方式吗？**

是时候将新的GitHub技能用于测试运行了！ 所有内容主要发展发生 [这里](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md)。 如果您对内容，布局或其他任何内容有建议的改进，您可以制作它，然后在主持人验证后它将自动成为MOOC内容的一部分！

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)