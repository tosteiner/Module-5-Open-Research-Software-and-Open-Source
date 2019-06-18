---
output:
  html_document: 默认
  pdf_document: 默认
---

# 任务2：如何使用GitHub和Zenodo使您的代码可以使用

此任务专为希望在学术文献中创建和重复使用基于GitHub的项目/存储库的学生和研究人员而设计。

不要忘记你可以参加我们的开放 [**Slack频道**](https://osmooc.herokuapp.com/)。 请在＃module5opensource上自我介绍一下，并告诉我们你是谁，你的背景，以及你如何在这里结束！

预计完成时间：45-60分钟。

## 目录

- [前言](#Foreword)
- [设置GitHub存储库](#Setup)
- [选择您的GitHub存储库](#Choose)
- [登录Zenodo](#Login)
- [授权GitHub与Zenodo联系](#Authorise)
- [选择要存档的存储库](#Archive)
- [检查存储库设置](#Check)
- [创建一个新版本](#Release)
- [获得DOI](#DOI)
- [引用项目的清单](#Checklist)
- [其他资源](#Resources)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task2.png?raw=true" alt="任务2工作流程" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
</p>

<p align="center"><i>任务2的工作流程。 在完成任务时保持这个方便！</i></p>

  


## 前言 <a name="Foreword"></a>

虽然GitHub和Zenodo的集成使得现在使用这些工具变得更加容易（2019年1月），但重要的是要强调GitHub（Gitlab，Bitbucket，...）的替代品和Zenodo的替代品（其他存储库可能更适合您的社区，您可能会问您的同事）。 例如，可以使用Gitlab并手动将每个新版本上传到您的大学存储库，获取DOI。 原则（在线使用版本控制系统，并在存储库中存档提供持久唯一标识符的主要版本 ）可以应用于不同的工作流程。

## 设置GitHub存储库 <a name="Setup"></a>

> **专业提示**：确保在存储库中包含LICENSE和README文件。 这将向人们表明项目的目的，以及他们将来如何与之合作。

了解如何在其他指南中设置GitHub存储库 [任务1：构建GitHub存储库](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) ，它也是“模块5：开放研究软件和开放源代码”的一部分。

## 选择您的GitHub存储库 <a name="Choose"></a>

进入GitHub项目列表页面 [github.com](https://github.com) ，前往“存储库”选项卡。 选择要存档的存储库，然后将其打开。

  


## 登录Zenodo <a name="Login"></a>

现在转到 [zenodo.org](https://zenodo.org)。 Zenodo是一个可以永久存档代码和其他项目元素的平台。 Zenodo通过为项目分配 **数字对象标识符** （DOI）来实现这一点，这也有助于使工作更加可信。 这与GitHub不同，GitHub充当项目实际工作的地方，而不是长期存档。 在GitHub中，可以修改，删除，重写和不可逆转地更改内容，这使得用于更长时间的参考目的有点令人担忧。 Zenodo为研究成果提供更多安全性和持久性。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/zenodo.png?raw=true" width="800" /></p>

<p align="center"><i>注册Zenodo</i></p>

  


如果您已经拥有Zenodo帐户，这很容易。 如果没有，请按照步骤创建一个 - 您甚至可以使用GitHub帐户或ORCID配置文件登录以简化操作，因为Zenodo具有内置的集成功能。 这可能比创建另一个研究帐户和个人资料更容易。

  


## 授权GitHub与Zenodo联系 <a name="Authorise"></a>

在Zenodo网站上，授权它在'[Using GitHub](https://zenodo.org/account/settings/github/)'部分中连接到您的GitHub帐户。 在这里，Zenodo会将您重定向到GitHub，要求获取在您的存储库中使用“[webhooks](https://developer.github.com/webhooks/)”的权限。 您想在此处使用构成这些链接所需的权限来授权Zenodo。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/zenodo_github.png?raw=true" width="800" /></p>

<p align="center"><i>授权Zenodo与GitHub连接</i></p>

  


如果您尝试授予Zenodo访问组织存储库的权限，您（或管理员）将需要确保Zenodo被授予第三方访问权限。 GitHub将发送需要确认的授权电子邮件。 此时，回到GitHub上的存储库设置中，您还需要确保将存储库设置为“public”，而不是私有。

  


## 选择要存档的存储库 <a name="Archive"></a>

如果你已经做到这一点，这意味着Zenodo现在被授权配置存储库webhooks，它需要存档存储库并向它发出一个DOI。 要执行此操作，请在Zenodo网站上导航到 [GitHub存储库列表第](https://zenodo.org/account/settings/github/) 页，然后只需单击存储库旁边的“打开”按钮。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/enabled_repos.png?raw=true" width="800" /></p>

<p align="center"><i>允许在Zenodo中保留单个GitHub存储库</i></p>

  


## 检查存储库设置 <a name="Check"></a>

现在，您已在Zenodo和您的存储库之间设置了一个新的webhook。 在GitHub中，单击存储库的设置，然后单击左侧菜单中的Webhooks选项卡。 这应该显示配置为Zenodo的新Zenodo webhook。 请注意，webhook列表可能需要一些时间才能显示出来。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/webhooks.png?raw=true" width="800" /></p>

<p align="center"><i>检查是否为GitHub存储库启用了webhooks。 这里使用开放奖学金策略的示例</i></p>

  


## 创建一个新版本 <a name="Release"></a>

您第一次存档存储库称为“第一个版本”。 每次创建该存储库的新版本并将其存档时，都会创建一个新版本。 这可以在GitHub（顶部中心）的存储库的“版本”选项卡中进行跟踪。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/first_release.png?raw=true" width="800" /></p>

<p align="center"><i>检查存储库第一次发布是否成功。 这里使用开放奖学金策略的示例</i></p>

  


对于存储库的第一个存档版本，请单击Zenodo中的“创建新版本”。 填写表格并提供有关发布内容的详细信息。 对于第一个版本，请确保将其称为v1.0.0，这是标准做法。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/create_release.png?raw=true" width="800" /></p>

<p align="center"><i>创建一个新版本。 这里使用开放奖学金策略的示例，已经存在第一个版本</i></p>

  


最后，单击“发布版本”，您的存档将在GitHub上发布和版本化。

要在Zenodo上查看您的版本，您需要访问 [上传](https://zenodo.org/deposit) 选项卡。 要完成归档，Zenodo需要更多细节。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/upload_release.png?raw=true" width="800" /></p>

<p align="center"><i>检查新版本是否已上传。 此处使用开放奖学金策略显示示例</i></p>

  


## 获得DOI <a name="DOI"></a>

这有时被称为DOI'minting'，并且需要关于Zenodo上的存储库的一些额外信息。 在Zenodo上，单击主菜单中的 [Upload](https://zenodo.org/deposit) 选项卡，您新上载的存储库应该在那里。 向下滚动页面并根据需要填写额外信息，必填字段标有红色星号，然后单击“发布”。

**注**：只有在添加了这些额外信息后，您的DOI才会生效。 DOI可能还需要很短的时间才能生效。 示例DOI如下所示（再次针对开放奖学金策略）。

> **专业提示**：将DOI的URL复制到GitHub仓库的自述文件中，以便更轻松地进行交叉链接，并提供清晰的突出显示的DOI徽章，供用户查看和使用您的DOI。 您只需要在第一次发布DOI时执行此操作，因为它充当“概念DOI”并且链接到所有后续版本DOI。

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1323437.svg)](https://doi.org/10.5281/zenodo.1323437)

GitHub / Zenodo集成现在将为项目存储库的每个版本/版本分配DOI。 这使用户能够引用和引用特定版本的项目。 此外，引用的作者列表由存储库使用的GitHub用户帐户名自动确定 - 这意味着没有人被遗漏。 以后可以在Zenodo上编辑作者详细信息。 Zenodo中使用的DOI通过 [DataCite](https://www.datacite.org/) 服务注册。

> **专业提示**：在项目的自述文件中创建此引文的“人类可读”版本。 这对于可能不熟悉使用DOI创建引文的研究人员很有帮助，并且可以让其他人更容易引用您的软件并确认您的工作。 这方面的一个例子可能是： Jon Tennant。 （2018年7月30日）。 开放奖学金战略发展的基础：第一次正式发布（1.2版）。 Zenodo。 <http://doi.org/10.5281/zenodo.1323437>

**恭喜！**

您的GitHub存储库现在存档在Zenodo中，并且可以对DOI进行版本控制，以反映存储库版本随时间的更新。 您应该可以在GitHub Zenodo页面上查看存储库的详细信息。 这也意味着您的归档项目也可以被其他使用DOI的索引服务和搜索引擎所接受。

为其他人提供长期存档和DOI以便能够正确引用它，因为这提供了基本的引文元数据。 对于开放科学，重要的是能够引用您在研究中使用的软件，并且这种集成的工作流程可以实现这一点，符合研究引用的最佳实践。 此外，这种做法对于将软件（和相关项目）的标准提升到其他研究成果的标准非常重要。

> **专业提示**：您的研究是否由欧盟资助资助？ 现在，您可以通过更新项目Zenodo记录中元数据的授权部分，将已归档项目直接连接到您的授权。 这大大有助于提高其可发现性！

  


## 引用项目的清单 <a name="Checklist"></a>

所以现在你在Zenodo有一个可持续存档的GitHub存储库，可以重复使用和引用！ 在继续之前，请确保您拥有：

- []将您的GitHub项目链接到Zenodo。 如果您在Zenodo中看到GitHub存储库的完整副本，那么一切正常。
- [] Zenodo和GitHub集成设置工作得很好。 例如，拥有所有作者姓名，并且正确的项目标题会传到Zenodo。 如果没有，或者如果作者只有昵称，您可以在Zenodo中编辑这些详细信息。
- []项目有第一个版本，带有DOI。 您应该在项目Zenodo页面上显示DOI。 第一个DOI称为“概念DOI”，是连接所有后续版本DOI的主DOI。 复制此DOI链接并将其嵌入GitHub项目README页面。 你完成了！

### 其他资源 <a name="Resources"></a>

[使您的代码可信](https://guides.github.com/activities/citable-code/) - GitHub指南。

**知道这种内容可以改进的方式吗？**

是时候将新的GitHub技能用于测试运行了！ 所有内容主要发展发生 [这里](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)。 如果您对内容，布局或其他任何内容有建议的改进，您可以制作它，然后在主持人验证后它将自动成为MOOC内容的一部分！

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)