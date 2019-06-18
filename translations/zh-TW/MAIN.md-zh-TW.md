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
- [開源社區，治理和貢獻](#OS_Community)
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

一些人認為，開放源碼軟件運動代表了新自由主義和私有化的反向運動，通過蔑視信息的構建和再利用中的規則和規範，以及通過盡可能少地利用軟件大量提供軟件來實現現代資本主義的潛在轉變。 請參閱 [自由/開源軟件運動：阻力還是變化？](http://www.redalyc.org/html/742/74212712006/) 由Panayiota Georgopoulou提供有關此主題的更多信息。

  


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

自由軟件社區中有兩個主要陣營： **自由軟件運動**和 **OSS運動**。 兩者都有不同的意識形態，這些意識形態基於用戶自由和軟件的實際應用。 通常，“FLOSS”一詞用於調和這兩個政治陣營，意為“自由/自由和開源軟件”; Libre在自由的背景下是“免費”的法語和西班牙語。

重用的核心原則是將OSS與“自由軟件”區分開來。 免費和開源軟件（FOSS）是一個包容性術語，用於描述可分為免費和開源的軟件。 FOSS的一個很好的例子是 [Ubuntu Linux](https://www.ubuntu.com/) 操作系統。

自由軟件和OSS之間的最大區別在於，前者必須在與原始版本相同的許可下分發更新版本，而較新版本的OSS可以在不同許可下分發。 FOSS結合了兩全其美。

這些定義現在已被國際政府以及一些大型組織廣泛採用，如 [Mozilla Foundation](https://www.mozilla.org/en-US/foundation/) 和 [Wikimedia Foundation](https://wikimediafoundation.org/wiki/Home)。 FLOSS領域的主要組織包括英國 [軟件可持續發展研究所](https://www.software.ac.uk/)，他們提供寶貴的資源，例如最近的 [研究人員軟件存款指南](https://softwaresaved.github.io/software-deposit-guidance/)。

### 對於個別項目

典型的開源項目具有以下類型的正式角色：

- **作者**：創建項目的人
- **所有者**：對組織或存儲庫具有管理所有權的人員 
- **維護者**：負責推動願景和管理項目組織方面的貢獻者。 （他們也可能是項目的作者或所有者。）
- **貢獻者**：已經為項目做出貢獻的用戶。
- **社區成員**：使用該項目的人員。 他們可能積極參與對話，創建新問題或表達他們對未來項目改進的意見。

通常，角色通過 `README` 文件，Contributors文件或項目的單獨團隊頁面公開。

  


## 開源軟件的現有平台和工具 <a name="Platforms"></a>

虛擬環境和機器作為高性能研究工作流程推動者正變得越來越流行，其中許多基於OSS（例如，操作系統，編程語言和數據處理框架）。 流行的服務包括 [Google Cloud](https://cloud.google.com/compute/) 和 [Amazon Web Services](https://aws.amazon.com/)，它們還有助於數據庫存儲和內容交付以及計算能力。 [InsideDNA](https://insidedna.me/) 是一個可重複研究生物信息學，基因組學和生命科學的計算平台。

如所提及的 [以上](#What_OSS)，LibreOffice的提供了一種開源替代的Microsoft Office。 兩者幾乎完全兼容，只是使用不同的默認文件格式。 對於引文管理者來說， [Zotero](https://www.zotero.org/) 是最受歡迎的開源替代品，如Mendeley或EndNote等專有平台。

[Zotero](https://www.zotero.org/) 使用BibTeX（發音為'bib-tech'）格式，基於LaTeX（發音為'lay-tech'），並具有瀏覽器插件，使引文管理變得簡單。 通過將其與LibreOffice等其他軟件集成，現在可以在許多情況下擁有完全開源的研究工作流程。

### GitHub上 <a name="GitHub"></a>

> 您是否知道整個項目是作為 [GitHub](https://github.com/OpenScienceMOOC/)的開放和協作社區工作而構建的？

[GitHub](https://github.com/) 是軟件和非軟件內容（通常稱為“筆記本”）的流行託管站點，具有版本控制，項目管理和跟踪以及存儲服務的附加功能。 GitHub構建於OSS [Git](https://git-scm.com/)之上，使用戶能夠遠程工作以維護，共享和協作研究軟件和其他非基於軟件的項目。

版本控製本質上是一個過程，它捕獲存儲庫中文件的快照，並跟踪對它們的修改。 它記錄了更改的時間，更改的內容以及執行更改的人員。 如果有多個人同時處理一個文件，則會檢測到任何重疊的更改，並且必須在繼續之前解決。 與項目開發時手動保存和記錄更改相比，這提供了更加簡化和自動化的過程。 它還避免了不可避免的混淆命名文件版本列表......

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/xkcd.png?raw=true" width="200" /></p>

<p align="center"><i>GitHub幫助我們避免，呃，次優的文件命名約定（來源：XKCD）</i></p>

  


GitHub的一個比較流行和有用的功能是 [問題跟踪器](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/issues)，用於組織OSS開發。 以上鍊接將您帶到問題跟踪器以開發此模塊！ 如果你認為這裡有一些可以改進的東西，或者你想評論，任何人都可以在那裡添加或貢獻一個問題！

其它類似的項目託管服務，包括 [到位桶](https://bitbucket.org/)， [GitLab](https://about.gitlab.com/)和 [的Launchpad](https://launchpad.net/)。 如果微軟最近對GitHub的收購對你有點不利，那麼這些都是很好的選擇。

但是，我們也知道GitHub可以有很高的學習曲線。 這就是為什麼這個MOOC的第一個實際任務將教你如何設置你的第一個GitHub項目存儲庫！

**[轉到任務1：構建您的第一個GitHub存儲庫](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)**

  


## 用於研究的開源軟件 <a name="Research"></a>

特別是在科學研究方面，開源軟件的使用和開發已經成為一種常態。 除了適用於消費者，行業或政府等普遍接受OSS的原因之外，還有很多原因。 其中包括：

- 在分析軟件中實施的算法越來越多地成為學術出版物中描述的方法的組成部分。 因此，如果這些算法實現對外人關閉，那麼它與嚴格的同行評審完全不一致。

- 科學合作往往跨越多個機構和分佈式研究網絡，其中保密和命令層次不是以封閉源開發“必要”的方式維護的。

- 許多計算分析在虛擬化環境（例如機構，國家或國際“雲”基礎架構）中運行，並託管在多用戶服務器上。 封閉源，商業軟件通常不允許這樣的使用。

- OSS的發展往往依賴於志願者。 在科學研究的預算限制時期，這是一個明顯的優勢。

由於這些原因和其他原因，開源工具在科學研究中非常常用。 這包括在許多研究人員都是業餘開發人員自己的領域中使用，並依賴於 [R](https://www.r-project.org/) 等工具進行統計分析和編寫腳本，在過去的十年中，這些工具幾乎完全取代了用於統計分析的商業軟件，如SPSS或JMP。很多領域。 在生物信息學等領域，涉及DNA測序平台輸出的大量文件處理，通用腳本語言，如 [Python](https://www.python.org/) 和基於它的常用庫（如 [biopython](http://biopython.org)）已成為至關重要的許多研究人員的工具包的一部分。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/python.png?raw=true" width="400" /></p>

<p align="center"><i>蟒蛇</i></p>

  


R和Python等工具本質上是編寫軟件的軟件。 雖然規劃是研究人員一個越來越普遍的活動，當然不是 *每* 科學家做到這一點。 離編程只有一步的步驟是將較長工作流程中各種分析工具的輸入和輸出鏈接在一起。 作為基因組學的一個例子，一個非常常見的工作流程是從高通量測序讀數開始，然後i）進行基本的質量控制檢查; ii）將讀數映射到參考基因組; iii）確定新數據與參考不一致的點。 這些步驟通常作為工作流執行，其中在Linux命令行環境中為三個步驟中的每一步運行不同的開源可執行文件。 雖然這可能不是一個非常開源的軟件開發，但它確實涉及開源工件（例如Linux shell腳本）的使用和生產，我們在本模塊中討論的原則適用於這些工件。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/r.png?raw=true" width="200" /></p>

<p align="center"><i>[R</i></p>

  


最後，OSS也用於科學研究，其原因更接近於那些推動OSS在更廣泛社會中採用的原因，即它很便宜。 例如，個人或組織可能決定從Microsoft Office切換到LibreOffice進行稿件編寫或電子表格處理，因為後者是免費的（如 [**'免費啤酒'**](https://www.youtube.com/watch?v=dQw4w9WgXcQ) 和'言論自由'）。 同樣，可以簡單地通過成本考慮來選擇從ArcGIS切換到 [QGIS](https://www.qgis.org/en/site/) 以分析地理信息。   


## OSS入門 - 常見問題解答 <a name="FAQ"></a>

**我正在使用X [例如Matlab，STATA，Excel]，我希望轉換到更開放的東西。 什麼是下一個步驟？**

即使您使用的是專有軟件，您通常仍可以共享源代碼/文檔等。 *最好的第一步是盡可能分享*。

**大！ 我可以把它們放在我的新github回購中。**

如果這對你來說已經足夠了！ 如果不是大多數專有軟件，則有開源等價物。 和一個人一起去看看你的想法。

| 關閉                                                                              | 打開                                                                                                                                             |
| ------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| MATLAB                                                                          | Python，朱莉婭                                                                                                                                     |
| STATA / SPSS                                                                    | [R                                                                                                                                             |
| 微軟Office                                                                        | LibreOffice的                                                                                                                                   |
| 數學                                                                              | JupyterLab                                                                                                                                     |
| 測試你的新 [拉請求-PR-](https://help.github.com/articles/about-pull-requests/) 技能...... | ... 在這裡添加你自己的例子 [](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md) |

**涼！ 但是，如果我進行切換，我將陷入困境：需要多年才能學習新工具/沒有支持/使用有缺陷的軟件。**

好問題！ 答案取決於它。 最好的辦法是找一個以前做過轉換的人，並從他們的經驗中學習。 或者只是進行谷歌搜索！ 有些OSS比封閉式對應物要好得多，有些則不然，所以值得仔細選擇。

## 製作好的軟件以便重複使用 <a name="Reuse"></a>

最有可能在將來重新使用您的軟件的人是......你！ 因此，雖然共享總是優於不共享，但通過適當的文檔，您可以更輕鬆地創建自己和他人的生活。 文檔可以包含幾個內容，例如在代碼中包含有用的註釋和註釋，以幫助解釋執行特定操作的原因，而不是它要實現的目標。

其中一個最重要的方面是包含一個信息豐富的 `README` 文件，幾乎每個OSS項目都有，有時甚至不止一個。 在每個目錄中包含一個這樣的文件是一個好習慣，其中包括文件列表，目錄以及目錄的用途。 `README` 文件通常只是純文本或markdown（再次，例如MOOC的所有文件！），並且可以包含有關如何安裝和運行軟件的關鍵信息，以前的依賴關係和要求，以及教程或例子。

> **你知道嗎** 術語 `README` 是一些次調皮地歸因於劉易斯·卡羅爾的愛麗絲夢遊著名的場景在仙境中的愛麗絲面對標有神奇的零食“吃我”“和”喝我“。 有效。

這裡的目的是提供足夠的信息以最大化計算環境的重用和再現性，使得沒有項目經驗的人可以輕鬆訪問和重用軟件（[Sandve等，2013](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)）。 通過降低進入壁壘，您可以增加其他人重新使用您工作的機會，這是OSS的最終目標之一（[Ince et al。，2012](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Ince%20et%20al.%2C%202012.pdf)）。

這種擴展有助於使未來重複使用更加容易，是“容器”技術。 容器就像一個及時凍結的生態系統，代碼，數據和任何其他依賴關係都完美地保存，打包並保存在當前功能版本中。 這意味著將來任何人都可以進入並再次運行分析。 因此，它們通常適合重複使用，但這可能是由於其他人修改或理解而犧牲的，因為通常很多細節都可以隱藏在源代碼及其依賴項中。 研究中容器實現的常見示例包括 [Rocker](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Boettiger%20and%20Eddelbuettel%2C%202017.pdf) （R語言的Docker容器）， [Binder](https://mybinder.readthedocs.io/en/latest/)和 [Code Ocean](https://codeocean.com/)。

**可持續軟件是很好的軟件。**

  


## 可重複計算研究的10條簡單規則

根據 [Sandve et al。，（2013）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Sandve%20et%20al.%2C%202013.PDF)，使計算研究更具可重複性的10條簡單規則是：

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

<p align="center"><i>信息圖改編自Sandve等，（2013）。 隨意下載並打印出來，以便在研究期間保持方便！</i></p>

  


如果您按照這些步驟，以及 [**任務1**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) 和 [**任務2**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)，您應該沒問題！

  


## 開源許可 <a name="Licensing"></a>

開源許可證是一種專門為軟件和代碼設計的許可證，它明確了共享和重用的法律條件。 如所提及的 [以上](#What_OSS)，加入合適的許可的是什麼區別公開從OSS共享軟件。 例如，廣泛使用的 [MATLAB](https://www.mathworks.com/products/matlab.html) 是專有軟件， [Octave](https://www.gnu.org/software/octave/) 是一種公開許可的替代編程語言。

目前有超過1,400個獨特的開源許可證，由於難以理解不同許可證之間的法律影響之間的差異而產生的複雜性。

一些更常見的許可證包括：

- [Berkeley Software Distribution（“BSD”）](https://en.wikipedia.org/wiki/BSD_licenses)，
- [Apache](https://www.apache.org/licenses/LICENSE-2.0)，
- [麻省理工學院（麻省理工學院）](https://opensource.org/licenses/MIT)，或
- [GNU通用公共許可證（“GPL”）](https://www.gnu.org/licenses/gpl-3.0.en.html)。

你不需要知道所有這些背後的所有法律因素，但至少知道哪些選項可供你使用是好的。

有兩種方式可以對項目的貢獻獲得許可：

1. *明確*，個人捐款具有明確指示的許可證，獨立於主項目;要么
2. *隱含*，其中貢獻屬於主項目的原始許可代碼。

值得慶幸的是，由於用戶友好的工具，例如 [選擇許可證](https://choosealicense.com/)，選擇開源許可證的過程相對簡單。 這些許可證中的每一個都允許其他用戶使用，複製，分發和構建您的工作，通常同時確保創作者的工作得到適當的認可。 在這裡，關鍵是為您的工作選擇合適的許可證，具體取決於您想要或不想要的，其他人使用它。

  


## 軟件引用 <a name="Citation"></a>

引文提供了學術研究中最重要的互動之一，形成了我們的參考和指標系統的基礎。 通常，這是由於諸如 [數字對象標識符](https://en.wikipedia.org/wiki/Digital_object_identifier) （DOI）之類的永久唯一標識符的幫助而執行的。 DOI是在 [句柄系統](https://en.wikipedia.org/wiki/Handle_System)實現的持久標識符，其根據目的滿足共同標準，例如用於識別學術信息。 這種識別對於跟踪研究的系譜和來源，重現性以及為創建軟件的人提供適當的信譽至關重要。 重要的是，軟件應該被認為是學術研究的合法輸出，引用正在成為一種越來越常見的方式來表明這一點。

在2016年， [Smith等人，2016年](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) 撰寫了一篇關於軟件引用原則的研究論文，作為FORCE11軟件引用工作組的一部分。 與您想要引用您作為良好研究實踐的一部分使用的軟件的方式相同，重要的是使您的研究也很容易引用。 在引用用於您自己研究的任何軟件時，您應至少包括：

- 作者姓名，
- 軟件名稱，
- 版本號，和
- 唯一標識符/定位符（DOI或URL）。

由六個原則軟件引證的 [。Smith等人，（2016）](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Smith%20et%20al.%2C%202016.pdf) ，這裡提供：

- **重要性**：軟件應被視為合法且可引用的研究產品。 軟件引用在學術記錄中應與其他研究產品（如出版物和數據）的引用一樣重要;它們應該包含在引用工作的元數據中，例如在期刊文章的參考列表中，不應該被省略或分開。 軟件的引用應與任何其他研究產品（如紙張或書籍）相同，即作者應引用適當的軟件產品集，就像它們引用適當的論文集一樣。

- **信用和歸屬**：軟件引用應有助於向軟件的所有貢獻者提供學術信用和規範的法律歸屬，並認識到單一的歸屬方式或機制可能不適用於所有軟件。

- **唯一標識**：軟件引用應包括一種機器可操作的識別方法，全球唯一，可互操作，並且至少由相應領域專家的社區識別，並且最好由一般公眾研究人員識別。

- **持久性**：描述軟件及其處置的唯一標識符和元數據應該保持不變 - 甚至超出他們描述的軟件的生命週期。

- **可訪問性**：軟件引用應有助於訪問軟件本身及其相關的元數據，文檔，數據以及人員和機器所需的其他材料，以便明智地使用所引用的軟件。

- **特異性**：軟件引用應有助於識別和訪問所使用的特定軟件版本。 軟件標識應盡可能具體，例如使用版本號，修訂號或平台等變體。

注意：有關“如何使您的軟件可用”的說明，請參閱下面的 [**使用GitHub和Zenodo**](#GitHub_Zenodo) 以及 [**任務2：鏈接GitHub和Zenodo**](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)。

  


## 使用GitHub和Zenodo <a name="GitHub_Zenodo"></a>

[GitHub](#GitHub) 是一個用於項目管理，內容存儲和版本控制的流行工具。 請注意，GitHub本身不是OSS。 然而，Git，它所基於的工具，是。 Git旨在幫助管理與軟件相關的項目的源代碼文件及其更新。 但是，它也可以擴展到其他非軟件項目;例如，這 [MOOC](https://github.com/OpenScienceMOOC/)！

然而，對GitHub進行研究只是第一步。 使其持久且可重複使用同樣重要，這就是為什麼擁有與之相關的數字對象標識符（DOI）可能很有用的原因。 最簡單的方法是通過名為 [Zenodo](https://zenodo.org/)的服務，這是一個由OpenAIRE和CERN創建的免費開源多學科存儲庫，可用於為各個GitHub存儲庫分配DOI。 有一個 [GitHub指南](https://guides.github.com/activities/citable-code/) 解釋了細節，其中涉及將GitHub存儲庫直接鏈接到Zenodo，以便當開發人員為他們的軟件創建正式版本時，Zenodo創建並存檔該版本的軟件。

使用Zenodo創建DOI並沒有什麼特別之處，除了 **免費**;也可以使用其他通用存儲庫，例如 [DataCite DOI Fabrica](https://doi.datacite.org/)，或您自己的機構存儲庫，例如 [Caltech](https://www.library.caltech.edu/news/enhanced-software-preservation-now-available-caltechdata)。

許多研究人員可能通常害怕共享不完整，錯誤或不完美的代碼。 但是，在OSS社區中，這種共享“原始”代碼的做法相當普遍。 公開共享代碼使其他人能夠重複使用和改進代碼，並且可以更深入地參與與之相關的任何研究。 這是同行合作的基本方面之一，也許最好的例子是傳統的研究手稿同行評審過程。

任務2將指導您完成將GitHub存儲庫鏈接到Zenodo以進行存檔的過程。

> **您知道嗎......** 為此MOOC製作的所有內容均作為 [Zenodo](https://zenodo.org/communities/open-science-mooc/)社區的一部分提供？

**[轉到任務2：鏈接GitHub和Zenodo](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)**

  


## 通過開源合作和貢獻 <a name="Collaborating"></a>

通常，OSS是在多個貢獻者之間以公共，分散，協作的方式開發的。 其目的是增強項目及其設計的多樣性和範圍，以便變得更有益和可持續。 這種方法被著名的早期OSS支持者Eric Raymond稱為“市集”模型。 其中一個主要的指導原則是 **同伴製作**，它依靠自組織社區來規範內容的發展，協調共同的目標或結果。

OSS項目在很大程度上依賴於志願者合作，這通常需要不斷變化的新移民才能變得富有成效和可持續（[Steinmacher et al。，2014](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/Reading%20Material_Open%20Source%20and%20Open%20Research%20Software/Steinmacher%20et%20al.%2C%202014.pdf)）。 為項目創造合適的社交氛圍和熱情的參與環境通常對OSS中成功的合作關係至關重要。

  


## 從這往哪兒走 <a name="Future_OSS"></a>

希望現在你已經看到了軟件作為現代科學基石的重要性，以及OSS在這方面的重要性。

這個 **學習成果** 應該是：

1. 您現在可以定義OSS的特徵，以及支持和反對它的一些道德，法律，經濟和研究影響論點。

2. 根據社區標準，您現在可以描述共享和重用開放代碼的質量要求。

3. 您現在可以使用一系列利用OSS的研究工具。

4. 您現在可以將為個人使用而設計的代碼轉換為其他人可訪問和可重用的代碼。

5. 軟件開發人員將能夠使他們的軟件變得可信，軟件用戶將知道如何引用他們使用的軟件。

  


**獎金任務**

如果你已經完成了 [任務1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) 和 [任務2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)，我們還有 **獎金任務** ，如果你想進一步提高你的技能。 [任務3](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md) 將向您介紹如何將Git與R Studio集成，從而更深入地將Git集成到典型的研究工作流程中。 建議您在繼續執行此任務之前完成前2個任務。

但是，您的開源之旅並不止於此！ 這只是一個開始，如果你想做或了解更多，那裡有一些令人難以置信的資源：

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

*這裡的這些參考僅僅是開始。 它們包括一些對研究中開源領域最有用的概述。 但是，如果您想要找到更適合您自己研究領域的東西，那麼您可以在那裡探索！*

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

**知道這種內容可以改進的方式嗎？**

是時候將新的GitHub技能用於測試運行了！ 所有內容的開發主要發生 [這裡](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.md)。 如果您對內容，佈局或其他任何內容有建議的改進，您可以製作它，然後在主持人驗證後它將自動成為MOOC內容的一部分！

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)