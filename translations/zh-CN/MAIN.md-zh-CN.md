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
- [The Open Source community and its governance](#OS_Community)
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

一些人认为，开放源码软件运动代表了新自由主义和私有化的反向运动，通过蔑视信息的构建和再利用中的规则和规范，以及通过尽可能少地利用软件大量提供软件来实现现代资本主义的潜在转变。 See [The free/open source software movement: Resistance or change?](https://doi.org/10.15448/1984-7289.2009.1.5569) by Panayiota Georgopoulou for more on this topic.

  


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

There are two main camps within the free/libre and open source software (FLOSS) community: The **free software movement**, and the **open source software movement** (OSS). 两者都有不同的意识形态，这些意识形态基于用户自由和软件的实际应用。 The term 'FLOSS' is used as a overaching neutral term to refer to both; libre being French and Spanish for 'free' in the context of freedom.

In a similar way that people active in the open science movement are heterogeneous in their assumptions and aims, different opinions exist in the FLOSS community as well. Recalling module 1, two of the schools of thought in open science were the *Pragmatic school* and the *Democratic school*. While the former is driven by the assumption that research could be more efficient if scientists worked together, the latter wants to set straight an unequal distribution of knowledge. They probably both end up sharing their research, but each with different intentions.

This is roughly comparable to the OSS and the free software movement: The latter evolved around 1983 to protect what they call the four essential freedoms of a program's user. These include the freedom to run, copy, distribute, study, change and improve a program. Software that respects these freedoms with an appropriate license is considered 'free'. The four freedoms are seen as vital for a society as a whole in the sense that they only enable sharing, cooperation and ultimately freedom in general. In this sense the free software movement is a social movement that creates an ethical imperative.

The open source software movement, which splintered off in 1998, focuses on the practical advantages and does not campaign for principles. It is concerned with developing high-quality software, for which everyone's ability to obtain, modify and contribute back the source code is considered highly beneficial.

Among multiple conclusions they arrive at, access to a program's source code is a shared one. Software thus may be considered *free*, *open source*, or both, according to agreed-on definitions by the Free Software Foundation ([FSF](https://www.gnu.org/philosophy/free-sw.html)) and the Open Source Initiative ([OSI](https://opensource.org/osd)). The FSF argues that free software is a subset of OSS, with only a [fraction](https://www.gnu.org/philosophy/free-open-overlap.html) being open source but nonfree.

Thus, highlighting a particular license status of software in use—open source or free—is mostly about different philosophies, not about software not having the other status as well. Each movement has its share of problems explaining their term: *free* means more than being gratis and *open source* means more than having access to the source code. The [FSF](https://www.gnu.org/philosophy/open-source-misses-the-point.html) and the European counterpart [FSFE](https://fsfe.org/documents/whyfs.html) provide more information on this topic.

### 对于个别项目

A typical open source project has the following types of formal roles:

- **作者**：创建项目的人
- **所有者**：对组织或存储库具有管理所有权的人员 
- **维护者**：负责推动愿景和管理项目组织方面的贡献者。 （他们也可能是项目的作者或所有者。）
- **贡献者**：已经为项目做出贡献的用户。
- **社区成员**：使用该项目的人员。 他们可能积极参与对话，创建新问题或表达他们对未来项目改进的意见。

Typically, roles are made public through either the `README` file, a Contributors file, or a separate team page for the project.

  


## 开源软件的现有平台和工具 <a name="Platforms"></a>

Virtual environments and machines are becoming increasingly popular as high-powered research workflow enablers, and many of these are built upon OSS (e.g., operating systems, programming languages, and data processing frameworks). Popular services include [Google Cloud](https://cloud.google.com/compute/) and [Amazon Web Services](https://aws.amazon.com/), which also assist with database storage and content delivery, as well as computational power. [InsideDNA](https://insidedna.me/) is a computing platform for reproducible research in bioinformatics, genomics and the life sciences.

As mentioned [above](#What_OSS), LibreOffice provides an Open Source alternative to Microsoft Office. The two are almost completely compatible, just with different default file formats. For citation managers, [Zotero](https://www.zotero.org/) is the most popular Open Source alternative to proprietary platforms such as Mendeley or EndNote.

[Zotero](https://www.zotero.org/) uses the BibTeX (pronounced 'bib-tech') format, based on LaTeX (pronounced 'lay-tech'), and has browser plugins to make citation management simple. By integrating this with other software such as LibreOffice, it is now possible to have a fully Open Source research workflow in many cases.

### GitHub上 <a name="GitHub"></a>

> 您是否知道整个项目是作为 [GitHub](https://github.com/OpenScienceMOOC/)的开放和协作社区工作而构建的？

[GitHub](https://github.com/) is a popular hosting site for both software and non-software content (often called 'notebooks'), with added capabilities for version control, project management and tracking, and storage services. GitHub is built on top of the OSS [Git](https://git-scm.com/), which enables users to work remotely to maintain, share, and collaborate on research software and other non-software based projects.

Version control is essentially a process that takes snapshots of the files in a repository, and tracks modifications to them. It records when the changes were made, what they were, and who did them. If several people are working on one file at once, any overlapping changes are detected, and must be resolved prior to continuing. This provides a much more streamlined and automated process than manually saving and recording changes as projects develop. It also avoids the inevitable lists of confusing named file versions...

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>GitHub helps us to avoid, er, sub-optimal file naming conventions (source: XKCD)</i></p>

  


One of the more popular and useful functions of GitHub is the [issue tracker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues), which is used to organise OSS development. The above link takes you to the issue tracker for the development of this module! If you think there is something here that can improved, or you want to comment on, anyone can add or contribute to an issue there!

Other similar project hosting services include [BitBucket](https://bitbucket.org/), [GitLab](https://about.gitlab.com/), and [Launchpad](https://launchpad.net/). If the recent acquisition of GitHub by Microsoft is a bit off-putting to you, these are great alternatives.

However, we also know that GitHub can have quite a high learning curve. Which is why the first practical task for this MOOC will teach you how to set up your first GitHub project repository!

**[GO TO TASK 1: Building your first GitHub repository](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## 用于研究的开源软件 <a name="Research"></a>

Especially in scientific research, Open Source Software usage and development has become practically the norm. There's a number of reasons for this beyond those that apply to the general acceptance of OSS by, for example, consumers, industry, or government. Among these reasons are:

- 在分析软件中实施的算法越来越多地成为学术出版物中描述的方法的组成部分。 因此，如果这些算法实现对外人关闭，那么它与严格的同行评审完全不一致。

- 科学合作往往跨越多个机构和分布式研究网络，其中保密和命令层次不是以封闭源开发“必要”的方式维护的。

- 许多计算分析在虚拟化环境（例如机构，国家或国际“云”基础架构）中运行，并托管在多用户服务器上。 封闭源，商业软件通常不允许这样的使用。

- OSS的发展往往依赖于志愿者。 在科学研究的预算限制时期，这是一个明显的优势。

For these and other reasons, Open Source tools are very commonly used in scientific research. This includes usage in fields where many researchers are amateur developers themselves and rely on tools such as [R](https://www.r-project.org/) for statistical analysis and scripting, which, in the last decade, has almost completely displaced commercial software for statistical analysis such as SPSS or JMP in a lot of fields. In fields such as bioinformatics, that involve a lot of file handling of the outputs of DNA sequencing platforms, general purpose scripting languages such as [Python](https://www.python.org/) and commonly used libraries built on top of it (such as [biopython](http://biopython.org)) have become a vital part of the toolkit of many researchers.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>Python</i></p>

  


Tools such as R and Python are essentially software for writing software. Although programming is an increasingly common activity among researchers, of course not *every* scientist does this. One step away from programming is the chaining together of the inputs and outputs of various analysis tools in longer workflows. As an example from genomics, a very common workflow is to start out with high-throughput sequencing reads and then i) do basic quality control checks; ii) map the reads against a reference genome; iii) identify the points where the new data are at variance with the reference. These steps are routinely executed as a workflow where a different Open Source executable is run in a Linux command-line environment for each of the three steps. Although this is arguably not quite open source software development, it does involve the usage and production of open source artifacts (such as Linux shell scripts) for which the principles that we discuss in this module are applicable.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>R</i></p>

  


Lastly, OSS is also used in scientific research for reasons that more closely mirror those that drive the adoption of OSS in wider society, namely that it is cheap. For example, individuals or organizations might decide to switch from Microsoft Office to LibreOffice for manuscript writing or spreadsheet processing because the latter is free (both as in [**'free beer'**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) and 'free speech'). Likewise, the choice to switch from ArcGIS to [QGIS](https://www.qgis.org/en/site/) for the analysis of geographic information might be prompted simply by cost considerations.   


## OSS入门 - 常见问题解答 <a name="FAQ"></a>

**I'm using X[e.g. Matlab,STATA,Excel] and I want to transition to something more open. What are the next steps?**

Even if you are using proprietary software, you can usually still share your source code/documents etc. *The best first step is sharing whatever you can*.

**Great! I can put them in my new github repo.**

If that's enough for you for now great! If not for most pieces of proprietary software there are Open Source equivalents. Have a go with one and see what you think.

| 关闭                                                                                                      | 打开                                                                                                                                                                |
| ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| MATLAB                                                                                                  | Python，朱莉娅                                                                                                                                                        |
| STATA / SPSS                                                                                            | [R                                                                                                                                                                |
| 微软Office                                                                                                | LibreOffice的                                                                                                                                                      |
| 数学                                                                                                      | JupyterLab                                                                                                                                                        |
| Max/MSP                                                                                                 | PureData                                                                                                                                                          |
| Test out your new [Pull Request -PR-](https://help.github.com/articles/about-pull-requests/) Skills ... | ... by adding your own example [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**Cool! But if I make the switch will I be stuck: taking ages to learn a new tool/ without support /with buggy software.**

Good question! The answer is it depends. The best thing to do is find someone who's made the switch before and learn from their experience. Or just do a Google search! Some OSS is much better than their closed counterparts, some aren't, so it's worth choosing carefully.

## 制作好的软件以便重复使用 <a name="Reuse"></a>

The most likely person who might want to re-use your software in the future is...you! So while sharing is always better than not sharing, you can make your own life, and that of others, much easier through appropriate documentation. Documentation can include several things, such as including helpful comments and annotations in the code that help to explain why a particular action was performed, rather than what it is intended to achieve.

One of the most critical aspects of this is including an informative `README` file, that accompanies almost every OSS project, and some times even more than one. It can be a good practice to include one such file in every directory, that includes a list of files, a table of contents, and what the purpose of the directory is. The `README` file is typically just plain text or markdown (again, such as all of the ones for the MOOC!), and can include critical information for how to install and run software, previous dependencies and requirements, as well as tutorials or examples.

> **你知道吗** 术语 `README` 是一些次调皮地归因于刘易斯·卡罗尔的爱丽丝梦游著名的场景在仙境中的爱丽丝面对标有神奇的零食“吃我””和‘喝我’。 有效。

The purpose here is to provide sufficient information to maximise the re-use and reproducibility of the computational environment, such that someone with no experience with the project can easily access and re-use the software ([Sandve et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)). By lowering the barriers to entry, you increase the chances of others being able to re-use your work, which is one of the ultimate goals of OSS ([Ince et al., 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)).

An extension of this that can help to make things even easier for future re-use is 'container' technology. Containers are like an ecosystem frozen in time, where the code, the data, any other dependencies, are all perfectly preserved, packaged and saved in the present functioning versions. This means that anyone in the future any one can come in and run the analyses again. As such, they are generally good for re-use, but this can come at the sacrifice of modification or understanding by others, as often a lot of details can be hidden within the source code and its dependencies. Common examples of container implementation in research include [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) (a Docker container for the R language), [Binder](https://mybinder.readthedocs.io/en/latest/), and [Code Ocean](https://codeocean.com/).

**Sustainable software is good software.**

  


## 可重复计算研究的10条简单规则

The 10 simple rules for making computational research more reproducible, based on [Sandve et al., (2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF), are:

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

<p align="center"><i>Infographic adapted from Sandve et al., (2013). Feel free to download this and print it out to keep handy during your research!</i></p>

  


If you follow these steps, along with the processes in [**Task 1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [**Task 2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), you should be fine!

  


## 开源许可 <a name="Licensing"></a>

An Open Source license is a type of license designed specifically for software and code that make it explicit what the legal conditions for sharing and re-use are. As mentioned [above](#What_OSS), the addition of a suitable license is what differentiates publicly shared software from OSS. For example, the widely used [MATLAB](https://www.mathworks.com/products/matlab.html) is proprietary software, and [Octave](https://www.gnu.org/software/octave/) is an openly licensed alternative programming language.

There are currently more than 1,400 unique Open Source licenses, a complexity born from the difficulty in understanding the differences between the legal implications across different license.

Some of the more common licenses include:

- [Berkeley Software Distribution（“BSD”）](https://en.wikipedia.org/wiki/BSD_licenses)，
- [Apache](https://www.apache.org/licenses/LICENSE-2.0)，
- [麻省理工学院（麻省理工学院）](https://opensource.org/licenses/MIT)，或
- [GNU通用公共许可证（“GPL”）](https://www.gnu.org/licenses/gpl-3.0.en.html)。

You don't need to know all the legal itty gritty behind all of these, but it is good to at least know what options are avaiilable to you.

There are two ways in which contributions to a project become licensed:

1. *明确*，个人捐款具有明确指示的许可证，独立于主项目;要么
2. *隐含*，其中贡献属于主项目的原始许可代码。

Thankfully, the process of selecting an Open Source license is relatively trivial, thanks to user-friendly tools such as [Choose A License](https://choosealicense.com/) or [Public License Selector](https://ufal.github.io/public-license-selector/). Each of these licenses allows other users to use, copy, distribute, and build upon your work, often while ensuring that the creators are appropriately recognised for their work. Here, the key is selecting an appropriate license for your work, depending on what you want, or do not want, others to do with it.

  


## 软件引用 <a name="Citation"></a>

Citations provide one of the most important interactions in scholarly research, forming the basis of our referencing and metrics systems. Typically, this is performed thanks to the assistance of a permanent unique identifier such as a [Digital Object Identifiers](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI). A DOI is a persistent identifier, implemented in the [Handle System](https://en.wikipedia.org/wiki/Handle_System), that meets a common standard, depending on the purpose, such as for identifying academic information. Such identification is critical for tracking the genealogy and provenance of research, for reproducibility, as well as for giving appropriate credit to those who have created the software. Importantly, software should be considered a legitimate output from scholarly research, and citation is becoming an increasingly common way to indicate that.

In 2016, [Smith et al., 2016](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) wrote a research paper about the principles of software citation as part of the FORCE11 Software Citation Working Group. In the same way that you would want to cite software that you have used as part of good research practices, it is important to make your research easily citable too. When citing any software used for your own research, you should include at minimum:

- 作者姓名，
- 软件名称，
- 版本号，和
- 唯一标识符/定位符（DOI或URL）。

The six principles of software citation by [Smith et al., (2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) are provided here:

- **重要性**：软件应被视为合法且可引用的研究产品。 软件引用在学术记录中应与其他研究产品（如出版物和数据）的引用一样重要;它们应该包含在引用工作的元数据中，例如在期刊文章的参考列表中，不应该被省略或分开。 软件的引用应与任何其他研究产品（如纸张或书籍）相同，即作者应引用适当的软件产品集，就像它们引用适当的论文集一样。

- **信用和归属**：软件引用应有助于向软件的所有贡献者提供学术信用和规范的法律归属，并认识到单一的归属方式或机制可能不适用于所有软件。

- **唯一标识**：软件引用应包括一种机器可操作的识别方法，全球唯一，可互操作，并且至少由相应领域专家的社区识别，并且最好由一般公众研究人员识别。

- **持久性**：描述软件及其处置的唯一标识符和元数据应该保持不变 - 甚至超出他们描述的软件的生命周期。

- **可访问性**：软件引用应有助于访问软件本身及其相关的元数据，文档，数据以及人员和机器所需的其他材料，以便明智地使用所引用的软件。

- **特异性**：软件引用应有助于识别和访问所使用的特定软件版本。 软件标识应尽可能具体，例如使用版本号，修订号或平台等变体。

Note: For instructions on 'how to make your software citable' see the section [**Using GitHub and Zenodo**](#GitHub_Zenodo) below and [**Task 2: Linking GitHub and Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md).

  


## 使用GitHub和Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) is a popular tool for project management, content storage, and version control. Note that GitHub itself is not OSS. However, Git, the tool which it is based on, is. Git is designed to help manage the source code files, and the updates to them, for a software-related project. However, it can also be extended to other non-software projects; for example, this [MOOC](https://github.com/OpenScienceMOOC/)!

However, getting research onto GitHub is just the first step. It is equally important to make it persistent and re-usable, which is why having a Digital Object Identifier (DOI) associated with it can be useful. The simplest way to do this is through a service called [Zenodo](https://zenodo.org/), which is a free and open source multi-disciplinary repository created by OpenAIRE and CERN, and can be used to assign a DOI to individual GitHub repositories. There is a [GitHub Guide](https://guides.github.com/activities/citable-code/) that explains the details, which involve linking GitHub repositories directly through to Zenodo so that when developers create formal releases for their software, Zenodo creates and archives a that version of the software.

There's nothing special about using Zenodo for creating DOIs, other than its **free of cost**; other general repositories can also be used, such as [DataCite DOI Fabrica](https://doi.datacite.org/), or your own institutional repositories such as [Caltech's](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata).

A lot of researchers might typically be afraid of sharing code which is incomplete, buggy, or imperfect. However, in the OSS community, such a practice of sharing 'raw' code is fairly commonplace. Sharing code openly enables others to re-use and improve it, as well as to engage in a deeper way with any research associated with it. This is one of the fundamental aspects of peer-collaboration, perhaps best exemplified by the traditional process of research manuscript peer review.

Task 2 will guide you through the process of linking a GitHub repository to Zenodo for archiving.

> **您知道吗......** 为此MOOC制作的所有内容均作为 [Zenodo](https://zenodo.org/communities/open-science-mooc/)社区的一部分提供？

**[GO TO TASK 2: Linking GitHub and Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## 通过开源合作和贡献 <a name="Collaborating"></a>

Often, OSS is developed in a public, decentralised, collaborative manner between multiple contributors. The purpose of this is to enhance the diversity and scope of a project and its design, in order to become more beneficial and sustainable. Such an approach was famously likened to a 'bazaar' model by Eric Raymond, an early OSS proponent. One of the major guiding principles of this is that of **peer production**, which relies on self-organised communities to regulate the development of content, co-ordinated towards a shared goal or outcome.

OSS projects rely heavily on volunteer collaboration, which often entails a constant flux of newcomers in order to become productive and sustainable ([Steinmacher et al., 2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)). Creating the right social atmosphere for a project, and a welcoming engagement environment, are often critical to successful collaboraitons in OSS.

  


## 从这往哪儿走 <a name="Future_OSS"></a>

Hopefully now you have come to see the importance of software as a cornerstone of modern science, and the importance that OSS plays in this.

The **learning outcomes** from this should be:

1. 您现在可以定义OSS的特征，以及支持和反对它的一些道德，法律，经济和研究影响论点。

2. 根据社区标准，您现在可以描述共享和重用开放代码的质量要求。

3. 您现在可以使用一系列利用OSS的研究工具。

4. 您现在可以将为个人使用而设计的代码转换为其他人可访问和可重用的代码。

5. 软件开发人员将能够使他们的软件变得可信，软件用户将知道如何引用他们使用的软件。

  


**BONUS TASK**

If you have completed [Task 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [Task 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), we also have a **BONUS TASK** for you, if you want to take your skills a step further. [Task 3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) will take you a step deeper into integrating Git into a typical research workflow by showing you how to integrate it with R Studio. It is recommended that you have completed the first 2 tasks before proceeding with this one.

However, your Open Source journey does not stop here! This was just the beginning, and there are some incredible resources out there if you would like to do or learn more:

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

*These references here are just the beginning. They include some of the most useful general overviews of the Open Source landscape in research. However, if you want to be find something more specific to your own research field, then that path is there for you to explore!*

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

**Know a way this content can be improved?**

Time to take your new GitHub skills for a test-run! All content development primarily happens [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md). If you have a suggested improvement to the content, layout, or anything else, you can make it and then it will automatically become part of the MOOC content after verification from a moderator!

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)