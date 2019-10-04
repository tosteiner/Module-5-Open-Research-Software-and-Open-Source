---
output:
  html_document: 默認
  pdf_document: 默認
---

# 第5單元：開放研究軟件和開源

## 目錄

- [介紹](#Introduction)
- [什麼是開源軟件](#What_OSS)
- [開源軟件原理](#Principles)
- [The Open Source community and its governance](#OS_Community)
- [開源軟件的現有平台和工具](#Platforms)
- [用於研究的開源軟件](#Research)
- [OSS入門 - 常見問題解答](#FAQ)
- [製作好的軟件以便重複使用](#Reuse)
- [開源許可](#Licensing)
- [軟件引用](#Citation)
- [使用GitHub和Zenodo](#GitHub_Zenodo)
- [通過開源協作](#Collaborating)
- [從這往哪兒走](#Future_OSS)

**請注意** 可以通過 [Soundcloud](https://soundcloud.com/open-science-mooc/module-5-open-source-and-open-research-software) 和 [YouTube](https://www.youtube.com/watch?v=BHrOEmKk5zM)下載音頻版本。

## 介紹 <a name="Introduction"></a>

歡迎來到開放科學MOOC的 **模塊5** ： **開放研究軟件和開源**。

該模塊已經開發 [在打開](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source) 通過協作通過的一個國際研究小組 [開源afficianados](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md#development-team-)。 您在此處看到的所有內容都是通過來自更廣泛社區的互動反饋和協作開放的。 它包含一系列視頻，信息圖表，基於文本的閱讀和實用任務，讓您沉浸其中。

不要忘記你可以參加我們的開放 [**Slack頻道**](https://osmooc.herokuapp.com/)。 請在＃module5opensource上自我介紹一下，並告訴我們你是誰，你的背景，以及你如何在這裡結束！

### 這個模塊是誰的？

該模塊主要面向研究生和本科生的計算研究人員，以及新興數據科學家和使用分析代碼或軟件的任何其他研究人員。 在現代研究環境中，這幾乎涵蓋了使用計算機進行工作的任何人。

> “關於計算結果的文章是廣告，而不是獎學金。 實際的獎學金是產生結果的完整軟件環境，代碼和數據。“ - J. Buckheit和DL Donoho，1995。

軟件和技術是現代研究的基礎，現在幾乎不可避免地以某種方式計算 - 搜索引擎，社交網絡平台，分析軟件和數字出版。 有了這個，對更複雜的開源軟件的需求不斷增加，相比之下，研究人員越來越願意公開合作開發新工具。

開源的力量在於它降低了協作和採用的障礙，因此允許思想和技術更快地傳播。 本單元將介紹將軟件轉換為可由其他人公開訪問和重用的內容所需的必要工具。

<img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/open_research_software_open_source.png?raw=true" width="800" />

<p align="center"><i>圖片來自Patrick Hochstenbach（CC0 1.0 Universal）</i></p>

  


### **本單元**具體學習目標：

1. 了解開放軟件的特點;了解 **倫理，法律，經濟和研究影響贊成和反對開源軟件**，進一步了解開放代碼的質量要求。

2. 能夠將個人使用的代碼轉換為其他人可以訪問的開放代碼。

3. 使用利用開放內容的軟件（工具）並鼓勵更廣泛的協作。

  


## 什麼是開源軟件 <a name="What_OSS"></a>

事實上，所有現代科學研究工作流程都依賴於一系列軟件工具，可以在不同的數據集上運行，使用不同的參數，以各種方式迭代應用（數據科學）或在不同的輸入上運行，並使用模型和方法預測某些輸出狀態（計算科學）。 開源軟件（OSS）是一種計算機軟件，其中完整的源代碼在特定許可下可用，使其他用戶可以出於任何目的訪問，查看，修改和重新分發該代碼。 由於OSS需要此類許可證，因此默認情況下通常保持免費。 這種明確的許可也是OSS與自由軟件的區別。 與專有軟件相比，重複使用OSS進行分析，模擬和可視化研究通常也更容易，更靈活。 通常，無論我們是否知道，我們已經將OSS作為我們自己的研究工作流程的一部分。

OSS適用於更廣泛的開放科學計劃，因為它有助於使完整的研究環境，包括產生研究結果的軟件，完全可訪問和可重用。 因此，它形成用於最佳實踐的必要組成部分（[門尼斯等人，2018](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf)）和可重複性和研究再現性（包括個人和其他），連同其它部件，諸如共享數據（[Stodden，2010](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf)）。

在某些情況下，共享源代碼甚至可以成為接受相關研究手稿的條件（[Shamir et al。，2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Shamir%20et%20al.%2C%202013.pdf)）。 人們普遍認為它會增加研究影響（[Vandwalle，2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Vandewalle%2C%202012.pdf)）。

開發人員的一些共同優勢包括：

- 提高開發人員的忠誠度和授權;

- 降低服務和營銷成本;

- 增加服務和產品的品牌;

- 以較低的費用生產高質量的軟件;

- 靈活性和快速創新;

- 定制和模塊化集成;

- 提高可靠性和獨立性;和

- 基於每個人都可以使用的開放標準。

這樣，研究人員的主要優點（用戶）包括 **降低成本**， **增加透明度**， **增加安全性和穩定性**， **沒有廠商'鎖定'具有增加的用戶控制**和 **的整體更高質量**。 此外，共享OSS允許研究人員為他們的努力獲得信譽，例如通過直接軟件引用 [（Smith等，2016）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf)。

常用的OSS包括 [Mozilla Firefox](https://www.mozilla.org/en-US/firefox/) 互聯網瀏覽器和 [LibreOffice](https://www.libreoffice.org/) 全辦公套件。 LibreOffice類似於流行的Microsoft Office，包括文字處理器，電子表格管理器和幻燈片演示軟件，但完全免費且開源。

一些人認為，開放源碼軟件運動代表了新自由主義和私有化的反向運動，通過蔑視信息的構建和再利用中的規則和規範，以及通過盡可能少地利用軟件大量提供軟件來實現現代資本主義的潛在轉變。 See [The free/open source software movement: Resistance or change?](https://doi.org/10.15448/1984-7289.2009.1.5569) by Panayiota Georgopoulou for more on this topic.

  


## 開源軟件原理 <a name="Principles"></a>

[開源倡議](https://opensource.org/)，OSS的先驅之一，提供以下 [定義](https://en.wikipedia.org/wiki/The_Open_Source_Definition#Definition)：

*別擔心，您不需要記住所有這些，但了解OSS的原理是很好的。*

- **免費再分發**：許可不得限制任何一方銷售或贈送軟件，作為包含來自多個不同來源的程序的軟件分發的組成部分。 許可證不需要特許權使用費或其他費用進行此類銷售。
    
    - **源代碼**：程序必須包含源代碼，並且必須允許在源代碼和編譯形式中進行分發。 如果某種形式的產品沒有與源代碼一起分發，則必須有一種廣為人知的獲取源代碼的方法，最好不要超過合理的複製成本，最好通過互聯網免費下載。 源代碼必須是程序員修改程序的首選形式。 不允許故意混淆源代碼。 不允許使用中間形式，例如預處理器或轉換器的輸出。
    
    - **衍生作品**：許可證必須允許修改和衍生作品，並且必須允許它們以與原始軟件許可證相同的條款進行分發。
    
    - **作者源代碼的完整性**：只有在許可證允許使用源代碼分發“補丁文件”以便在構建時修改程序時，許可證才可以限制源代碼以修改形式分發。 許可證必須明確允許分發由修改後的源代碼構建的軟件。 許可證可能要求派生作品攜帶與原始軟件不同的名稱或版本號。
    
    - **不歧視個人或團體**：許可證不得歧視任何人或團體。
    
    - **對奮鬥領域的歧視**：許可證不得限制任何人在特定領域努力使用該程序。 例如，它可能不會限製程序在企業中使用，也不會用於基因研究。
    
    - **許可證**分發：程序附帶的權利必須適用於程序重新分發的所有人，而無需由這些方執行額外的許可證。
    
    - **許可證不得特定於產品**：程序附帶的權利不得取決於程序是特定軟件分發的一部分。 如果程序是從該分發中提取並在程序許可條款中使用或分發的，則重新分發程序的所有各方應具有與原始軟件分發一起授予的權限相同的權限。
    
    - **許可證不得限制其他軟件**：許可證不得對與許可軟件一起分發的其他軟件加以限制。 例如，許可證不得堅持在同一介質上分發的所有其他程序必須是開源軟件。
    
    - **許可證必須是技術中立**：許可證的提供可以基於任何單獨的技術或界面風格。

現在，記住這一切可能有點複雜。 但是，它可以概括為 *使軟件盡可能可用於未來的工作，同時也可免費獲得*。

  


## 開源清單

有許多支持OSS和協作的現有平台和工具。 [開放科學培訓手冊](https://open-science-training-handbook.gitbook.io/book/) 提供了一個檢查表，用於評估現有研究軟件的“開放性”，基於上面的開源定義：

- []軟件是否可供下載和安裝？

- []軟件可以輕鬆安裝在不同的平台上嗎？

- []軟件是否有使用條件？

- []源代碼是否可供檢查？

- []源代碼的完整歷史記錄是否可通過公開版本歷史記錄進行檢查？

- []軟件（硬件和軟件）的依賴關係是否正確描述？ 這些依賴關係是否只需要相當少的努力來獲取和使用？

檢查，檢查，檢查，完成！ Simples。

  


## 開源社區及其治理 <a name="OS_Community"></a>

There are two main camps within the free/libre and open source software (FLOSS) community: The **free software movement**, and the **open source software movement** (OSS). 兩者都有不同的意識形態，這些意識形態基於用戶自由和軟件的實際應用。 The term 'FLOSS' is used as a overaching neutral term to refer to both; libre being French and Spanish for 'free' in the context of freedom.

In a similar way that people active in the open science movement are heterogeneous in their assumptions and aims, different opinions exist in the FLOSS community as well. Recalling module 1, two of the schools of thought in open science were the *Pragmatic school* and the *Democratic school*. While the former is driven by the assumption that research could be more efficient if scientists worked together, the latter wants to set straight an unequal distribution of knowledge. They probably both end up sharing their research, but each with different intentions.

This is roughly comparable to the OSS and the free software movement: The latter evolved around 1983 to protect what they call the four essential freedoms of a program's user. These include the freedom to run, copy, distribute, study, change and improve a program. Software that respects these freedoms with an appropriate license is considered 'free'. The four freedoms are seen as vital for a society as a whole in the sense that they only enable sharing, cooperation and ultimately freedom in general. In this sense the free software movement is a social movement that creates an ethical imperative.

The open source software movement, which splintered off in 1998, focuses on the practical advantages and does not campaign for principles. It is concerned with developing high-quality software, for which everyone's ability to obtain, modify and contribute back the source code is considered highly beneficial.

Among multiple conclusions they arrive at, access to a program's source code is a shared one. Software thus may be considered *free*, *open source*, or both, according to agreed-on definitions by the Free Software Foundation ([FSF](https://www.gnu.org/philosophy/free-sw.html)) and the Open Source Initiative ([OSI](https://opensource.org/osd)). The FSF argues that free software is a subset of OSS, with only a [fraction](https://www.gnu.org/philosophy/free-open-overlap.html) being open source but nonfree.

Thus, highlighting a particular license status of software in use—open source or free—is mostly about different philosophies, not about software not having the other status as well. Each movement has its share of problems explaining their term: *free* means more than being gratis and *open source* means more than having access to the source code. The [FSF](https://www.gnu.org/philosophy/open-source-misses-the-point.html) and the European counterpart [FSFE](https://fsfe.org/documents/whyfs.html) provide more information on this topic.

### 對於個別項目

A typical open source project has the following types of formal roles:

- **作者**：創建項目的人
- **所有者**：對組織或存儲庫具有管理所有權的人員 
- **維護者**：負責推動願景和管理項目組織方面的貢獻者。 （他們也可能是項目的作者或所有者。）
- **貢獻者**：已經為項目做出貢獻的用戶。
- **社區成員**：使用該項目的人員。 他們可能積極參與對話，創建新問題或表達他們對未來項目改進的意見。

Typically, roles are made public through either the `README` file, a Contributors file, or a separate team page for the project.

  


## 開源軟件的現有平台和工具 <a name="Platforms"></a>

Virtual environments and machines are becoming increasingly popular as high-powered research workflow enablers, and many of these are built upon OSS (e.g., operating systems, programming languages, and data processing frameworks). Popular services include [Google Cloud](https://cloud.google.com/compute/) and [Amazon Web Services](https://aws.amazon.com/), which also assist with database storage and content delivery, as well as computational power. [InsideDNA](https://insidedna.me/) is a computing platform for reproducible research in bioinformatics, genomics and the life sciences.

As mentioned [above](#What_OSS), LibreOffice provides an Open Source alternative to Microsoft Office. The two are almost completely compatible, just with different default file formats. For citation managers, [Zotero](https://www.zotero.org/) is the most popular Open Source alternative to proprietary platforms such as Mendeley or EndNote.

[Zotero](https://www.zotero.org/) uses the BibTeX (pronounced 'bib-tech') format, based on LaTeX (pronounced 'lay-tech'), and has browser plugins to make citation management simple. By integrating this with other software such as LibreOffice, it is now possible to have a fully Open Source research workflow in many cases.

### GitHub上 <a name="GitHub"></a>

> 您是否知道整個項目是作為 [GitHub](https://github.com/OpenScienceMOOC/)的開放和協作社區工作而構建的？

[GitHub](https://github.com/) is a popular hosting site for both software and non-software content (often called 'notebooks'), with added capabilities for version control, project management and tracking, and storage services. GitHub is built on top of the OSS [Git](https://git-scm.com/), which enables users to work remotely to maintain, share, and collaborate on research software and other non-software based projects.

Version control is essentially a process that takes snapshots of the files in a repository, and tracks modifications to them. It records when the changes were made, what they were, and who did them. If several people are working on one file at once, any overlapping changes are detected, and must be resolved prior to continuing. This provides a much more streamlined and automated process than manually saving and recording changes as projects develop. It also avoids the inevitable lists of confusing named file versions...

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>GitHub helps us to avoid, er, sub-optimal file naming conventions (source: XKCD)</i></p>

  


One of the more popular and useful functions of GitHub is the [issue tracker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues), which is used to organise OSS development. The above link takes you to the issue tracker for the development of this module! If you think there is something here that can improved, or you want to comment on, anyone can add or contribute to an issue there!

Other similar project hosting services include [BitBucket](https://bitbucket.org/), [GitLab](https://about.gitlab.com/), and [Launchpad](https://launchpad.net/). If the recent acquisition of GitHub by Microsoft is a bit off-putting to you, these are great alternatives.

However, we also know that GitHub can have quite a high learning curve. Which is why the first practical task for this MOOC will teach you how to set up your first GitHub project repository!

**[GO TO TASK 1: Building your first GitHub repository](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## 用於研究的開源軟件 <a name="Research"></a>

Especially in scientific research, Open Source Software usage and development has become practically the norm. There's a number of reasons for this beyond those that apply to the general acceptance of OSS by, for example, consumers, industry, or government. Among these reasons are:

- 在分析軟件中實施的算法越來越多地成為學術出版物中描述的方法的組成部分。 因此，如果這些算法實現對外人關閉，那麼它與嚴格的同行評審完全不一致。

- 科學合作往往跨越多個機構和分佈式研究網絡，其中保密和命令層次不是以封閉源開發“必要”的方式維護的。

- 許多計算分析在虛擬化環境（例如機構，國家或國際“雲”基礎架構）中運行，並託管在多用戶服務器上。 封閉源，商業軟件通常不允許這樣的使用。

- OSS的發展往往依賴於志願者。 在科學研究的預算限制時期，這是一個明顯的優勢。

For these and other reasons, Open Source tools are very commonly used in scientific research. This includes usage in fields where many researchers are amateur developers themselves and rely on tools such as [R](https://www.r-project.org/) for statistical analysis and scripting, which, in the last decade, has almost completely displaced commercial software for statistical analysis such as SPSS or JMP in a lot of fields. In fields such as bioinformatics, that involve a lot of file handling of the outputs of DNA sequencing platforms, general purpose scripting languages such as [Python](https://www.python.org/) and commonly used libraries built on top of it (such as [biopython](http://biopython.org)) have become a vital part of the toolkit of many researchers.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>Python</i></p>

  


Tools such as R and Python are essentially software for writing software. Although programming is an increasingly common activity among researchers, of course not *every* scientist does this. One step away from programming is the chaining together of the inputs and outputs of various analysis tools in longer workflows. As an example from genomics, a very common workflow is to start out with high-throughput sequencing reads and then i) do basic quality control checks; ii) map the reads against a reference genome; iii) identify the points where the new data are at variance with the reference. These steps are routinely executed as a workflow where a different Open Source executable is run in a Linux command-line environment for each of the three steps. Although this is arguably not quite open source software development, it does involve the usage and production of open source artifacts (such as Linux shell scripts) for which the principles that we discuss in this module are applicable.

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>R</i></p>

  


Lastly, OSS is also used in scientific research for reasons that more closely mirror those that drive the adoption of OSS in wider society, namely that it is cheap. For example, individuals or organizations might decide to switch from Microsoft Office to LibreOffice for manuscript writing or spreadsheet processing because the latter is free (both as in [**'free beer'**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) and 'free speech'). Likewise, the choice to switch from ArcGIS to [QGIS](https://www.qgis.org/en/site/) for the analysis of geographic information might be prompted simply by cost considerations.   


## OSS入門 - 常見問題解答 <a name="FAQ"></a>

**I'm using X[e.g. Matlab,STATA,Excel] and I want to transition to something more open. What are the next steps?**

Even if you are using proprietary software, you can usually still share your source code/documents etc. *The best first step is sharing whatever you can*.

**Great! I can put them in my new github repo.**

If that's enough for you for now great! If not for most pieces of proprietary software there are Open Source equivalents. Have a go with one and see what you think.

| 關閉                                                                                                      | 打開                                                                                                                                                                |
| ------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| MATLAB                                                                                                  | Python，朱莉婭                                                                                                                                                        |
| STATA / SPSS                                                                                            | [R                                                                                                                                                                |
| 微軟Office                                                                                                | LibreOffice的                                                                                                                                                      |
| 數學                                                                                                      | JupyterLab                                                                                                                                                        |
| Max/MSP                                                                                                 | PureData                                                                                                                                                          |
| Test out your new [Pull Request -PR-](https://help.github.com/articles/about-pull-requests/) Skills ... | ... by adding your own example [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**Cool! But if I make the switch will I be stuck: taking ages to learn a new tool/ without support /with buggy software.**

Good question! The answer is it depends. The best thing to do is find someone who's made the switch before and learn from their experience. Or just do a Google search! Some OSS is much better than their closed counterparts, some aren't, so it's worth choosing carefully.

## 製作好的軟件以便重複使用 <a name="Reuse"></a>

The most likely person who might want to re-use your software in the future is...you! So while sharing is always better than not sharing, you can make your own life, and that of others, much easier through appropriate documentation. Documentation can include several things, such as including helpful comments and annotations in the code that help to explain why a particular action was performed, rather than what it is intended to achieve.

One of the most critical aspects of this is including an informative `README` file, that accompanies almost every OSS project, and some times even more than one. It can be a good practice to include one such file in every directory, that includes a list of files, a table of contents, and what the purpose of the directory is. The `README` file is typically just plain text or markdown (again, such as all of the ones for the MOOC!), and can include critical information for how to install and run software, previous dependencies and requirements, as well as tutorials or examples.

> **你知道嗎** 術語 `README` 是一些次調皮地歸因於劉易斯·卡羅爾的愛麗絲夢遊著名的場景在仙境中的愛麗絲面對標有神奇的零食“吃我”“和”喝我“。 有效。

The purpose here is to provide sufficient information to maximise the re-use and reproducibility of the computational environment, such that someone with no experience with the project can easily access and re-use the software ([Sandve et al., 2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)). By lowering the barriers to entry, you increase the chances of others being able to re-use your work, which is one of the ultimate goals of OSS ([Ince et al., 2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)).

An extension of this that can help to make things even easier for future re-use is 'container' technology. Containers are like an ecosystem frozen in time, where the code, the data, any other dependencies, are all perfectly preserved, packaged and saved in the present functioning versions. This means that anyone in the future any one can come in and run the analyses again. As such, they are generally good for re-use, but this can come at the sacrifice of modification or understanding by others, as often a lot of details can be hidden within the source code and its dependencies. Common examples of container implementation in research include [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) (a Docker container for the R language), [Binder](https://mybinder.readthedocs.io/en/latest/), and [Code Ocean](https://codeocean.com/).

**Sustainable software is good software.**

  


## 可重複計算研究的10條簡單規則

The 10 simple rules for making computational research more reproducible, based on [Sandve et al., (2013)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF), are:

1. 對於每個結果，跟踪它的生成方式。
2. 避免手動數據操作步驟。
3. 存檔所有使用的外部程序的確切版本。
4. 版本控制所有自定義腳本。
5. 盡可能以標準格式記錄所有中間結果。
6. 對於包含隨機性的分析，請注意基礎隨機種子。
7. 始終將原始數據存儲在圖表後面。
8. 生成分層分析輸出，允許檢查增加細節的層。
9. 將文本語句連接到基礎結果。
10. 提供對腳本，運行和結果的公共訪問。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/simple_rules.png?raw=true" width="800" /></p>

<p align="center"><i>Infographic adapted from Sandve et al., (2013). Feel free to download this and print it out to keep handy during your research!</i></p>

  


If you follow these steps, along with the processes in [**Task 1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [**Task 2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), you should be fine!

  


## 開源許可 <a name="Licensing"></a>

An Open Source license is a type of license designed specifically for software and code that make it explicit what the legal conditions for sharing and re-use are. As mentioned [above](#What_OSS), the addition of a suitable license is what differentiates publicly shared software from OSS. For example, the widely used [MATLAB](https://www.mathworks.com/products/matlab.html) is proprietary software, and [Octave](https://www.gnu.org/software/octave/) is an openly licensed alternative programming language.

There are currently more than 1,400 unique Open Source licenses, a complexity born from the difficulty in understanding the differences between the legal implications across different license.

Some of the more common licenses include:

- [Berkeley Software Distribution（“BSD”）](https://en.wikipedia.org/wiki/BSD_licenses)，
- [Apache](https://www.apache.org/licenses/LICENSE-2.0)，
- [麻省理工學院（麻省理工學院）](https://opensource.org/licenses/MIT)，或
- [GNU通用公共許可證（“GPL”）](https://www.gnu.org/licenses/gpl-3.0.en.html)。

You don't need to know all the legal itty gritty behind all of these, but it is good to at least know what options are avaiilable to you.

There are two ways in which contributions to a project become licensed:

1. *明確*，個人捐款具有明確指示的許可證，獨立於主項目;要么
2. *隱含*，其中貢獻屬於主項目的原始許可代碼。

Thankfully, the process of selecting an Open Source license is relatively trivial, thanks to user-friendly tools such as [Choose A License](https://choosealicense.com/) or [Public License Selector](https://ufal.github.io/public-license-selector/). Each of these licenses allows other users to use, copy, distribute, and build upon your work, often while ensuring that the creators are appropriately recognised for their work. Here, the key is selecting an appropriate license for your work, depending on what you want, or do not want, others to do with it.

  


## 軟件引用 <a name="Citation"></a>

Citations provide one of the most important interactions in scholarly research, forming the basis of our referencing and metrics systems. Typically, this is performed thanks to the assistance of a permanent unique identifier such as a [Digital Object Identifiers](https://en.wikipedia.org/wiki/Digital_object_identifier) (DOI). A DOI is a persistent identifier, implemented in the [Handle System](https://en.wikipedia.org/wiki/Handle_System), that meets a common standard, depending on the purpose, such as for identifying academic information. Such identification is critical for tracking the genealogy and provenance of research, for reproducibility, as well as for giving appropriate credit to those who have created the software. Importantly, software should be considered a legitimate output from scholarly research, and citation is becoming an increasingly common way to indicate that.

In 2016, [Smith et al., 2016](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) wrote a research paper about the principles of software citation as part of the FORCE11 Software Citation Working Group. In the same way that you would want to cite software that you have used as part of good research practices, it is important to make your research easily citable too. When citing any software used for your own research, you should include at minimum:

- 作者姓名，
- 軟件名稱，
- 版本號，和
- 唯一標識符/定位符（DOI或URL）。

The six principles of software citation by [Smith et al., (2016)](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) are provided here:

- **重要性**：軟件應被視為合法且可引用的研究產品。 軟件引用在學術記錄中應與其他研究產品（如出版物和數據）的引用一樣重要;它們應該包含在引用工作的元數據中，例如在期刊文章的參考列表中，不應該被省略或分開。 軟件的引用應與任何其他研究產品（如紙張或書籍）相同，即作者應引用適當的軟件產品集，就像它們引用適當的論文集一樣。

- **信用和歸屬**：軟件引用應有助於向軟件的所有貢獻者提供學術信用和規範的法律歸屬，並認識到單一的歸屬方式或機制可能不適用於所有軟件。

- **唯一標識**：軟件引用應包括一種機器可操作的識別方法，全球唯一，可互操作，並且至少由相應領域專家的社區識別，並且最好由一般公眾研究人員識別。

- **持久性**：描述軟件及其處置的唯一標識符和元數據應該保持不變 - 甚至超出他們描述的軟件的生命週期。

- **可訪問性**：軟件引用應有助於訪問軟件本身及其相關的元數據，文檔，數據以及人員和機器所需的其他材料，以便明智地使用所引用的軟件。

- **特異性**：軟件引用應有助於識別和訪問所使用的特定軟件版本。 軟件標識應盡可能具體，例如使用版本號，修訂號或平台等變體。

Note: For instructions on 'how to make your software citable' see the section [**Using GitHub and Zenodo**](#GitHub_Zenodo) below and [**Task 2: Linking GitHub and Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md).

  


## 使用GitHub和Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) is a popular tool for project management, content storage, and version control. Note that GitHub itself is not OSS. However, Git, the tool which it is based on, is. Git is designed to help manage the source code files, and the updates to them, for a software-related project. However, it can also be extended to other non-software projects; for example, this [MOOC](https://github.com/OpenScienceMOOC/)!

However, getting research onto GitHub is just the first step. It is equally important to make it persistent and re-usable, which is why having a Digital Object Identifier (DOI) associated with it can be useful. The simplest way to do this is through a service called [Zenodo](https://zenodo.org/), which is a free and open source multi-disciplinary repository created by OpenAIRE and CERN, and can be used to assign a DOI to individual GitHub repositories. There is a [GitHub Guide](https://guides.github.com/activities/citable-code/) that explains the details, which involve linking GitHub repositories directly through to Zenodo so that when developers create formal releases for their software, Zenodo creates and archives a that version of the software.

There's nothing special about using Zenodo for creating DOIs, other than its **free of cost**; other general repositories can also be used, such as [DataCite DOI Fabrica](https://doi.datacite.org/), or your own institutional repositories such as [Caltech's](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata).

A lot of researchers might typically be afraid of sharing code which is incomplete, buggy, or imperfect. However, in the OSS community, such a practice of sharing 'raw' code is fairly commonplace. Sharing code openly enables others to re-use and improve it, as well as to engage in a deeper way with any research associated with it. This is one of the fundamental aspects of peer-collaboration, perhaps best exemplified by the traditional process of research manuscript peer review.

Task 2 will guide you through the process of linking a GitHub repository to Zenodo for archiving.

> **您知道嗎......** 為此MOOC製作的所有內容均作為 [Zenodo](https://zenodo.org/communities/open-science-mooc/)社區的一部分提供？

**[GO TO TASK 2: Linking GitHub and Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## 通過開源合作和貢獻 <a name="Collaborating"></a>

Often, OSS is developed in a public, decentralised, collaborative manner between multiple contributors. The purpose of this is to enhance the diversity and scope of a project and its design, in order to become more beneficial and sustainable. Such an approach was famously likened to a 'bazaar' model by Eric Raymond, an early OSS proponent. One of the major guiding principles of this is that of **peer production**, which relies on self-organised communities to regulate the development of content, co-ordinated towards a shared goal or outcome.

OSS projects rely heavily on volunteer collaboration, which often entails a constant flux of newcomers in order to become productive and sustainable ([Steinmacher et al., 2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)). Creating the right social atmosphere for a project, and a welcoming engagement environment, are often critical to successful collaboraitons in OSS.

  


## 從這往哪兒走 <a name="Future_OSS"></a>

Hopefully now you have come to see the importance of software as a cornerstone of modern science, and the importance that OSS plays in this.

The **learning outcomes** from this should be:

1. 您現在可以定義OSS的特徵，以及支持和反對它的一些道德，法律，經濟和研究影響論點。

2. 根據社區標準，您現在可以描述共享和重用開放代碼的質量要求。

3. 您現在可以使用一系列利用OSS的研究工具。

4. 您現在可以將為個人使用而設計的代碼轉換為其他人可訪問和可重用的代碼。

5. 軟件開發人員將能夠使他們的軟件變得可信，軟件用戶將知道如何引用他們使用的軟件。

  


**BONUS TASK**

If you have completed [Task 1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) and [Task 2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md), we also have a **BONUS TASK** for you, if you want to take your skills a step further. [Task 3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) will take you a step deeper into integrating Git into a typical research workflow by showing you how to integrate it with R Studio. It is recommended that you have completed the first 2 tasks before proceeding with this one.

However, your Open Source journey does not stop here! This was just the beginning, and there are some incredible resources out there if you would like to do or learn more:

- 如果您對此感到特別鼓舞，您可以認可 [科學代碼宣言](http://sciencecodemanifesto.org/)，它基於代碼，版權，引用，信用和策展的五項原則。

- 為了啟動和開發您自己的項目， [開源指南](https://opensource.guide/) 計劃提供了一系列實用指南和技能，以幫助啟動和推進您的OSS項目。

- 有關基於OSS的研究工作流程的詳細介紹，Pedro L. Fernandes和Rutger A. Vos的 [開放科學，開放數據，開源](https://pfern.github.io/OSODOS/gitbook/) 手工指南是在線的頂級資源之一。

- 基於軟件的文章也存在更為正式的期刊場所，包括 [The Journal of Open Research Software](https://openresearchsoftware.metajnl.com/) 和 [The Journal of Open Source Software](https://joss.theoj.org/)。 這些場地的清單也是 [可用](https://www.software.ac.uk/which-journals-should-i-publish-my-software)。

- [PLOS開源工具包](https://channels.plos.org/open-source-toolkit) 為開源硬件和軟件研究和應用提供了一個全球論壇。

- [NumFOCUS](http://www.numfocus.org) 是一個非營利組織，支持和推廣世界一流的創新開源科學軟件。 他們贊助的一些項目包括：
    
    - [IPython](http://ipython.org) 和 [Jupyter Notebook](https://jupyter.org) 計劃。
    
    - [rOpenSci](http://ropensci.org)，它促進開源R統計環境，以實現透明和可重複的研究。
    
    - 為了獲得更多的OSS經驗， [Software Carpentry](https://software-carpentry.org/) 社區定期舉辦研討會，以提高基於實驗室的計算技能（[Wilson et al。，2017](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf)）。

  


### 進一步閱讀 <a name="Reading"></a>

*These references here are just the beginning. They include some of the most useful general overviews of the Open Source landscape in research. However, if you want to be find something more specific to your own research field, then that path is there for you to explore!*

- 自由/開源軟件開發研究的未來 [（Scacchi，2010）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Scacchi%2C%202010.pdf)。

- 實踐中的科學方法：計算科學中的再現性 [（Stodden，2010）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Stodden%2C%202010.pdf)。

- 開放計算機程序的案例 [（Ince et al。，2012）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)。

- 關於開源軟件社區的當前問題和研究趨勢 [（Martinez-Torres和Diaz-Fernandez，2013）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Martinez-Torres%20and%20Diaz-Fernandez%2C%202013.pdf)。

- 可重複計算研究的十個簡單規則 [（Sandve et al。，2013）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)。

- 關於開源軟件項目新人面臨的障礙的系統性文獻綜述 [（Steinmacher et al。，2014）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)。

- 開源軟件社區中的知識共享：動機和管理 [（Iskoujina和Roberts，2015）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Iskoujina%20and%20Roberts%2C%202015.pdf)。

- 軟件引用原則 [（Smith等，2016）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf)。

- Rocker介紹：R [Docker容器（Boettiger和Eddelbuettel，2017）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf)。

- 足夠好的科學計算實踐 [（Wilson et al。，2017）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Wilson%20et%20al.%2C%202017.pdf)。

- 鼓勵研究軟件 [最佳實踐的四個簡單建議（Jiménez等，2017）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Jim%C3%A9nez%20et%20al.%2C%202018.pdf)。

  


### 開發團隊 <a name="Development_team"></a>

- [Alex Morley](https://twitter.com/alex__morley)，Open Sourceror，英國牛津大學。
- [Kevin Moerman](https://twitter.com/KMMoerman)，Open Sourceror，麻省理工學院，美國。
- [Tania Allard](https://twitter.com/ixek)，開源，英國利茲大學數據美女。
- [Simon Worthington](https://twitter.com/mrchristian99)，Book Liberationist，TIB，Germany。
- [Paola Masuzzo](https://twitter.com/pcmasuzzo)，開源蝙蝠俠，意大利。
- [Ivo Grigorov](https://twitter.com/OAforClimate)，開源羅賓，丹麥。
- [Rutger Vos](https://twitter.com/rvosa)，Open Sourceror，荷蘭Naturalis生物多樣性中心。
- [Julien Colomb](https://twitter.com/j_colomb)，Open Ninja，Berlin。
- [Jon Tennant](https://twitter.com/protohedgehog)，Dinosaur Whisperer。

**Know a way this content can be improved?**

Time to take your new GitHub skills for a test-run! All content development primarily happens [here](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md). If you have a suggested improvement to the content, layout, or anything else, you can make it and then it will automatically become part of the MOOC content after verification from a moderator!

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)