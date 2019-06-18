---
output:
  html_document: 默認
  pdf_document: 默認
---

# 任務1：如何在GitHub上設置存儲庫

此任務專為希望在GitHub上創建其第一個開源項目（軟件或非軟件）的學生和研究人員而設計。 GitHub是一個讓您來玩和嘗試新的研究工作流程的地方，而且實際上只是幫助您為自己的途徑和想法創造舞台的開始。

不要忘記你可以參加我們的開放 [**Slack頻道**](https://osmooc.herokuapp.com/)。 請在＃module5opensource上自我介紹一下，並告訴我們你是誰，你的背景，以及你如何在這裡結束！

**請注意** 此功能的屏幕錄製也可通過 [YouTube](https://www.youtube.com/watch?v=AnftV9HBPSc&)。

預計完成時間：30-45分鐘。

估計一旦完成時間節省：難以想像..

## 目錄

* [入門](#Getting_started) 
  * [設置GitHub配置文件](#Profile)
  * [GitHub語言](#Language)
  * [創建一個新的存儲庫](#Create_new)
* [基本步驟](#Foundation) 
  * [選擇許可證](#License)
  * [創建README文件](#Readme)
  * [創建貢獻指南](#Contributing)
  * [制定行為準則](#Conduct)
  * [使你的代碼可以理解](#Citation)
* [讓您的問題保持最新](#Issues)
* [啟動項目的檢查清單](#Check-list)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task1.png?raw=true" alt="任務1工作流程" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
</p>

<p align="center"><i>任務1的工作流程。 在完成任務時保持這個方便！</i></p>

  


## 入門 <a name="Getting_started"></a>

“存儲庫”實際上只是GitHub上項目的一個奇特名稱。 GitHub是一個在線地方，您可以在其中管理項目，存儲文件以及與他人公開協作。 這一切都是通過使用版本控制來跟踪項目進展情況來實現的。 因此，GitHub是軟件和非軟件項目的強大工具。

在這個早期階段要考慮的最重要的事情之一是考慮您希望更廣泛的社區如何與您的項目進行互動。 當您在公開場合工作時，您希望確保其他人在訪問，查看和參與您的工作時感到舒適。 以降低進入壁壘的方式建立存儲庫，並且擔心成為“局外人”是維持成功項目的第一步。

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/octocat.png?raw=true" width="150px" height="125px"/>
</p>

<p align="center"><i>Octocat，GitHub的小吉祥物</i></p>

  


### 設置GitHub配置文件 <a name="Profile"></a>

要設置GitHub配置文件，只需轉到主頁面，然後單擊 [註冊GitHub](https://github.com/join)。 在這裡，您可以使用用戶名，電子郵件和密碼作為標準創建個人帳戶。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/github_signup.png?raw=true" width="800" /></p>

<p align="center"><i>註冊GitHub</i></p>

  


下一步是製定個人計劃。 目前，只需選擇“無限制公共存儲庫免費”計劃，除非您擔心隱私，在這種情況下選擇私人計劃。 如果您打算為組織設置項目，也可以選擇該選項。

  


### GitHub語言 <a name="Language"></a>

這可能是GitHub最令人困惑和反感的方面。 以下是一些最常用的術語及其定義：

* **初始化**：創建一個空存儲庫。
* **Checkout**：創建本地存儲庫的工作副本。
* **克隆**：將存儲庫複製到計算機上的本地目錄中。
* **分叉**：創建存儲庫的個人分支以並行處理它。
* **分支**：存儲庫的獨立並行版本。 更改不會影響主分支。
* **Master**：存儲庫的主分支和默認分支。
* **清潔**：分支上沒有待處理的提交。
* **階段**：添加準備好提交給分支的更新。
* **提交**：對存儲庫的修訂，如版本化的“保存”功能。
* **提交消息**：提交隨附的更改的描述。
* **檢查**：狀態檢查。
* **取**：與狗沒什麼關係。 指的是從在線存儲庫獲取最新更改而不合併它們。
* **索引**：充當臨時區域的“樹”。
* **工作目錄**：保存文件的“樹”。
* **頭**：表示最後提交的“樹”。
* **推送**：將已提交的更改添加到遠程存儲庫的頭部。
* **合併**：完成後將一個分支中所做的更改與主分支相結合。
* **拉**：通過獲取和合併最新提交來更新存儲庫。
* **拉請求**：將更新的分支合併到主分支的請求。
* **問題**：與存儲庫相關的建議改進，任務或問題。

呼！ 不要擔心記不住 *所有* 的這些現在。 像任何新技能一樣，熟悉程度來自經驗。

您可以看到其中一些與保存，複製，粘貼等標準工作流操作非常相似，但適用於軟件管理過程。 有一個 [幾個](https://mirrors.edge.kernel.org/pub/software/scm/git/docs/gitglossary.html) 太大，但這應該為入門做。

如果您有興趣，這些術語大多來自底層的 [Git系統](https://git-scm.com)。 Git的構建允許開發人員以分佈式方式管理不同版本的源代碼，這很好。 它有很多的功能，並做大量的複雜的東西的能力，通過書面 [非常聰明的傢伙](https://www.linuxfoundation.org/blog/2015/04/10-years-of-git-an-interview-with-git-creator-linus-torvalds/)。 但是， [用戶界面的設計並未考慮到新用戶](https://xkcd.com/1597/)，因此很難學習。

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git.png?raw=true" width="150px"/>
</p>

<p align="center"><i>無與倫比的使用Git指南。 （資料來源：XKCD）</i></p>

  


### 創建一個新的存儲庫 <a name="Create_new"></a>

在GitHub配置文件中，單擊“創建新存儲庫”。 第一步是創建一個名稱作為項目的品牌。 理想情況下，它應該是令人難忘的，並給出項目的功能。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/new_repo.png?raw=true" width="800" /></p>

<p align="center"><i>創建一個新的存儲庫</i></p>

  


確保不要復制名稱，侵犯其他商標，或將其命名為可能被認為具有攻擊性的任何商標。

  


## 基本步驟 <a name="Foundation"></a>

任何GitHub存儲庫都需要4個關鍵元素才能開始並開始開發一個熱情的社區：

1. 開源許可證;
2. 一個 `README` 文件;
3. 貢獻指南;和
4. 行為準則。

這些是用戶了解其合法權利，期望，項目目的以及改善整體用戶體驗的任何項目的關鍵方面和最佳實踐。

所有這四個文件都應保存在項目存儲庫的根目錄中。 這是約定使用降價的文件格式（`.MD`）大多數這些文件的（儘管許可證文件是最常見的純文本（`.TXT`）），並利用所有文件名。 而不是文件名中的空格，請確保使用下劃線 `_`。

所以你最終應該選擇這樣的基礎文件：

1. `LICENSE.md`
2. `README.md`
3. `CONTRIBUTING.md`
4. `CODE_OF_CONDUCT.md`

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/foundation.png?raw=true" width="800" /></p>

<p align="center"><i>基本的存儲庫結構</i></p>

  


### 選擇許可證 <a name="License"></a>

選擇適當的許可證將使您的開源存儲庫與公開可用的軟件區別開來。 雖然您沒有義務選擇許可證，但這樣做可以保證其他人能夠在法律框架內修改，共享，重複使用和構建您的項目。

首先，您要檢查 [選擇許可證](https://choosealicense.com/) 以查找最適合您的存儲庫意圖的許可證。

三個主要可供選擇的是：

* **麻省理工學院許可證**：許可許可證，允許人們對您的代碼做任何他們想做的事情，只要他們向您提供適當的歸屬，並且不會讓您承擔責任。
* **Apache許可證2.0**：對MIT許可證的類似權限，但也向用戶的貢獻者提供明確的專利權授予。
* **GNU通用公共許可證（GPL）第三版**：一個 [copyleft的](https://en.wikipedia.org/wiki/Copyleft) 許可證需要任何人誰重新分配你的代碼，或衍生作品，使源可按照同樣的條件與原許可證;還向用戶的貢獻者提供明確的專利權授予。

值得慶幸的是，當您在GitHub上啟動新存儲庫時，您可以從下拉菜單中選擇現有許可證。 您應始終（極少數例外）使用現有許可證，因為這是潛在用戶和貢獻者在選擇使用或貢獻您的軟件之前會看到的。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/license.png?raw=true" width="800" /></p>

<p align="center"><i>選擇示例許可證</i></p>

  


如果他們沒有您想要的，您可以手動添加一個。 要執行此操作，只需單擊存儲庫中的“創建新文件”，然後復制並粘貼現有許可證文本。 將文件命名為 `LICENSE.txt` 或 `LICENSE.md` 以使其清除，並將其保存在主存儲庫文件夾（即根目錄）中。 確保添加一個乾淨的提交消息，你就完成了！

> **助手**：此MOOC對代碼內容和非代碼內容使用不同的許可證組合。 在這裡，您可以找到我們申請的所有代碼和軟件的 [MIT許可證](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/LICENSE.md) 的示例，該代碼和軟件是作為MOOC生產的一部分生成的。

  


### 創建README文件 <a name="Readme"></a>

初始化新存儲庫時，應該有一個使用 `README` 文件的選項。 就像愛麗絲夢遊仙境一樣，這些正是他們所說的 - 提供關於項目的關鍵信息。 這些通常是外部貢獻者在訪問您的存儲庫時會看到的第一件事，因此讓他們提供信息和歡迎是關鍵。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/readme.png?raw=true" width="800" /></p>

<p align="center"><i>此模塊的README文件的一部分</i></p>

  


該文件最初將採用markdown（`.md`）格式。 這是一種純文本格式的輕量級標記語言。 要學習一些基本的降價，請參見 [此備忘單](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)。 但就目前而言，我們可以使用純文本。

您需要在 `README` 文件中包含以下幾項內容：

* 這個項目是關於什麼的，它做了什麼。
* 人們為什麼要關心，為什麼它有用。
* 如何有人開始為項目做貢獻。
* 如果有人需要幫助，可以聯繫誰。
* 許可證，貢獻指南和行為準則的鏈接。
* 項目結構的描述。
* 誰參與，他們的角色是什麼。
* 項目的當前狀態。

> **專業提示**：隨著項目的發展，您可能希望根據社區反饋添加常見問題解答，或者幫助用戶了解項目工作原理的教程。

請記住，並非所有參與您項目的人都是專家，或了解您正在做什麼以及為什麼。 擁有詳細記錄的 `README` 文件將增強具有一系列先驗知識的人的用戶體驗。

當 `README` 文件包含在根目錄中時，GitHub將自動在存儲庫的主頁上顯示該文件。 這意味著這是人們經常看到的第一件事，所以算一算！

> **助手**：在這裡，您可以找到用於此 [MOOC模塊](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/README.md)的 `README` 文件。 這包括有關狀態，基本原理，學習成果，開發團隊，關鍵文檔和幫助許可的信息。 您可以根據需要為自己的項目複製和調整此結構。

  


### 創建貢獻指南 <a name="Contributing"></a>

貢獻指南旨在向潛在的貢獻者傳達如何與您的項目和社區互動的簡短指南。 您希望確保歡迎，並表明您渴望參與者參與您的項目。 每當參與者打開新的拉取請求或創建新問題時，他們都會看到指向您的貢獻文件的鏈接。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/contributing.png?raw=true" width="800" /></p>

<p align="center"><i>該模塊的“貢獻”指南的一部分</i></p>

  


堅持使用全部大寫文件名，下一步是創建一個 `貢獻` 文件。 單擊“創建新文件”，並確保像以前一樣以標記格式保存。 該文件將告訴其他用戶他們如何參與和參與您的項目。 這是圍繞您的項目建立社區的第一步，因此請使其具有吸引力，簡潔和信息。

`CONTRIBUTING` 文件應包含以下信息：

* 您正在尋找什麼樣的貢獻。
* 如何建議更新或新功能。
* 如何使用GitHub的功能（例如拉取請求協議）與項目交互。
* 如何提交錯誤報告或創建問題。
* 項目的最終目標，願景或路線圖。
* 如何联系項目負責人。
* 指向任何外部文檔或網站的鏈接。

> **專業提示**：考慮讓人們花時間考慮貢獻，請考慮簡短的感謝信 - 他們點擊了文件了解更多信息！ 如果您還有其他識別方法，請務必將它們包含在此處。

在這裡，您基本上是在鼓勵人們自願花時間推進您的項目。 確保熱情友好，並確保人們如何參與。 在撰寫本文時，請務必從用戶的角度考慮這一點 - 在提交拉取請求和打開問題以使整個項目更順暢地運行時，如何讓他們的生活更輕鬆。

> **幫助手**：此MOOC模塊的 [貢獻指南](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CONTRIBUTING.md) 包括一些非常具體的內容：使用Git和GitHub的介紹，入門提示，聯繫信息，如何更改內容和報告問題，鏈接到 `README` 文件，以及有關首選內容和代碼樣式的信息。 您可以根據需要隨意複製和修改此項目。

  


### 制定行為準則 <a name="Conduct"></a>

行為準則對於為項目貢獻者設定預期行為和參與的基本規則非常重要，並且是一個易於參考的文檔，用於顯示您的項目團隊認真對待建設性對話。 因此，它是創造和維持一個健康社區的關鍵因素，在積極的社會氛圍中以建設性和富有成效的方式參與其中。

行為準則不僅提供了對行為的期望，而且還描述了這些期望適用於誰，何時適用，如果違反代碼會發生什麼，以及針對此的行動項目。 因此，需要在行為準則中明確聯繫點。 通常，這應該是私人方式，例如電子郵件地址。

> **專業提示**：如果需要報告有關收到這些報告的人的違規行為，請確保包含聯繫輔助方的選項。

要添加行為準則，您可以通過添加新的降價文件從頭開始創建自己的行為，或者使用現有模板，例如 [Contributor Covenant](https://contributor-covenant.org/)。 將文件命名為 `CODE_OF_CONDUCT.md`，並確保它在 `README` 文件中可見。

> **助手**：本MOOC還有基於貢獻者公約的 [行為準則](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CODE_OF_CONDUCT.md)。 如您所見，它包括有關行為的預期標準，社區中的責任以及CoC執行的信息，包括聯繫方式。 您可以隨意重新使用並根據需要將其調整到您的項目中。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/code_of_conduct.png?raw=true" width="800" /></p>

<p align="center"><i>此模塊的CODE OF CONDUCT文件的一部分，基於Contributor Covenant</i></p>

  


確保執行行為準則非常重要，因為它表明您不僅重視代碼，還尊重它對您社區的影響。 重要的是要尊重社區中的每個成員，尊重他們應得的尊重，禮貌和重要性。 如果發生違規行為，或重複違規者一致違規，最好參考 [開源指南](https://opensource.guide/code-of-conduct/#enforcing-your-code-of-conduct) ，了解如何執行行為準則。

  


### 使你的代碼可以理解 <a name="Citation"></a>

如果你想從一開始就讓代碼變得可行，你應該通過創建一個 `[codemeta.json]（https://codemeta.github.io)` 文件或 `[CITATION.cff]（https： //citation-file-format.github.io)5` 文件。 兩者都將允許當前正在開發的工具自動創建引文信息，而不是要求您稍後在表單中鍵入它。

如果您有興趣， [cite.research-software.org](https://cite.research-software.org) 提供了有關學術界軟件引用的更多背景信息。

  


## 讓您的問題保持最新 <a name="Issues"></a>

問題不一定是項目的問題，而是改進建議，未來發展的事情，以及有關項目的評論和反饋。 他們可以根據需要與貢獻者公開分享和討論，有點像論壇。

如果您是項目負責人，那麼維護一系列問題非常重要，這些問題可以使貢獻者清楚地了解項目的哪些方面需要注意。 同樣重要的是以積極的方式與其他人討論盡可能多的問題，以表明你認真對待他們的貢獻。

問題的關鍵要素包括：

* 信息標題和描述;
* 用於分類和過濾的Coloud編碼標籤/標籤;
* 將問題與特定功能或項目階段相關聯的里程碑;
* 受讓人表明誰負責處理某個問題;
* 提供反饋的評論。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/issues.png?raw=true" width="800" /></p>

<p align="center"><i>開放獎學金戰略項目的問題跟踪器</i></p>

  


在問題中，可以使用@ mentions通知其他contirbutors有關該問題，並讓合適的人員以有效的方式參與。 GitHub有一個內部通知系統，就像Facebook或Twitter一樣，也可以向問題跟踪器中提到的人發送電子郵件。 這些都可以在用戶設置中為個人定制。

  


## 啟動項目的清單 <a name="Checklist"></a>

所以現在你已準備好啟動你的項目，開始做廣告，並獲得貢獻！ 在繼續之前，請確保您擁有：

* []項目有一個令人難忘和信息豐富的名稱
* [] Project有一個 `LICENSE` 文件，它是開源許可證的精確副本
* []完整的文檔包括一個 `自述`， `貢獻`，和 `CODE_OF_CONDUCT` 檔
* []項目至少有一個明確標註的問題
* []此階段包含的任何代碼都有明確的結構和註釋

**恭喜！**

您現在已經啟動了一個開源研究項目！ 希望從現在開始，您的工作將有利於更廣泛的社區，建立新的合作，並為您創造新的和夢幻般的機會。 嘗試並考慮將這些技能應用於未來項目的方式，以及它們在過去如何幫助過一些項目。

從現在開始，這完全取決於你！ 一些建議是：

* 寫清潔代碼;
* 有一個結構良好的項目;
* 經常提交乾淨的信息;
* 保持項目記錄良好;
* 有明確的貢獻準則;
* 利用描述和標籤功能;
* 除非你打算對它們進行處理，否則不要分叉別人的存儲庫;
* 確保也為其他人的項目做出貢獻。

**知道這種內容可以改進的方式嗎？**

是時候將新的GitHub技能用於測試運行了！ 所有內容的開發主要發生 [這裡](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md)。 如果您對內容，佈局或其他任何內容有建議的改進，您可以製作它，然後在主持人驗證後它將自動成為MOOC內容的一部分！

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)