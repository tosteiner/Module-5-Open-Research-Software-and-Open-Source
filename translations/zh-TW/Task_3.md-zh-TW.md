---
output:
  html_document: 默認
  pdf_document: 默認
---

# 任務3：如何將Git與R Studio集成

此任務專為希望在標準的基於R的工作流程中實施版本控制系統的學生和研究人員而設計。 這可以應用於一系列軟件開發，數據分析和項目管理任務。 您未來的研究自我將感謝您的方便。

不要忘記你可以參加我們的開放 [**Slack頻道**](https://osmooc.herokuapp.com/)。 請在＃module5opensource上自我介紹一下，並告訴我們你是誰，你的背景，以及你如何在這裡結束！

預計完成時間：30分鐘

估計完成後的時間節省：幾乎無限

**注** 此任務的視頻指南版現已在 [YouTube](https://www.youtube.com/watch?v=Q-6jfjSAspA)。

## 目錄

* [入門](#Getting_started) 
  * [混帳](#Git)
  * [R Studio](#Rstudio)
* [第一步：下載所有內容](#one)
* [第二步：在RStudio中配置Git](#two)
* [第三步：為什麼我這樣做？](#three)
* [第四步：Git和R之間的完美結合](#four)
* [第五步：獲取內容內容](#five)
* [第六步：勇敢的承諾](#six)
* [第七步：推！](#seven)

## 入門 <a name="Getting_started"></a>

恭喜你到目前為止！ 如果你正在閱讀這篇文章，你就可以倖免於拉請求，網絡鉤子，甚至可以告訴我們FOSS中的F代表什麼（*不是* 挫折...）希望你已經克服了任何懷疑或不情願為了GitHub和開源軟件的好處，並準備採取下一步措施。

在開始此任務之前，請確保您已完成 [任務1](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) 和 [任務2](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)，以便您更熟悉GitHub和一些標準的開源實踐。

此任務將教您如何將版本控制軟件Git與流行的編碼環境RStudio集成。 是的，Git就像GIF或上帝一樣，而不是Jit就像發出錯誤的方式一樣。

如果您是那些認為代碼分佈在等待破解的多個硬盤驅動器，Dropbox，Google Drive或任何其他非專業軟件的研究人員之一，則此任務僅適合您。 如果您曾經歷過讓不同的共同作者之間有多個“最終”版本的紙張反复的令人頭疼的過程，這也適合您。

我們所有人偶爾會對這些事情感到內疚，但有一些方法可以做到這對你，未來的你和那些可能從你的工作中受益的人更好。

  


### 得到Git <a name="Git"></a>

那麼，什麼是Git，它與GitHub有何不同？ Git是一個版本控制系統，它使您能夠在整個開發過程中保存和跟踪工作時間戳的副本。 它也適用於非代碼項，例如MOOC，其中大部分是用RStudio中的markdown編寫的，並與Git / GitHub工作流集成。

這很重要，因為所有研究都經歷了變化，有時我們想知道這些是什麼。 您是否刪除了一些您認為重要的文字？ 版本控制將為您保存。 您的代碼在過去是否完美運行，但現在已經超出了信念範圍？ 版本控制。 這是避免混亂狀態的好方法，在這種情況下，您擁有相同文件的多個副本，但沒有愚蠢和煩人的文件命名約定。 `FINAL_Revised_2.2_supervisor_edits_ver1.7_scream.txt` 將成為過去。

GitHub是一個平台，允許您從工作區（例如，筆記本電腦）無縫共享代碼，以便在線空間中託管。 所以，有點像GitHub的公共接口。 Git / GitHub的優點是：

1. 你可以隨時隨地保留所有作品的副本;
2. 您可以通過時間比較不同副本的工作，這有助於發現錯誤或錯誤;
3. 其他人可以公開與您的工作合作;
4. 您的工作本地和在線副本都保持同步;
5. 關於誰做出貢獻，為什麼做出貢獻以及何時做出貢獻，這是完全透明的。和
6. 您可以讓多個人同時在同一個項目上工作。

雖然這主要是為源代碼而設計的，但它應該立即變得如此成為幾乎所有研究工作流程的強大工具。

  


### RStudio <a name="Rstudio"></a>

對於使用統計編程語言R的研究人員來說，RStudio是一個流行的編碼環境。它帶有一個文本編輯器，因此您不必安裝另一個並在它們之間切換。 它還包括Git和GitHub的圖形用戶界面（GUI），我們將在這裡使用它。

當輝煌的開源工具無縫集成時，這不是很好。 這應該有助於使您日常使用Git更簡單。

如果您在任何時候需要為R安裝新軟件包，只需使用以下命令：

`install.packages（“PACKAGE NAME”，依賴項= TRUE）`

用呃包名替換 `PACKAGE NAME`。 可能出現的一些例子，你可以與發揮有益包括 `knitr`， `devtools` 或 `GGPLOT2`。

  


## 第一步：下載所有內容 <a name="one"></a>

1. 如果您已經執行了之前的任務，那麼您現在應該已經擁有一個GitHub帳戶。 如果沒有， [標誌在這裡](https://github.com/)。 為所有人免費提供無限量的存儲庫！
2. 下載並安裝最新版本的 [R](https://www.r-project.org/)。 也適用於 [Mac](https://cloud.r-project.org/) 和 [Linux](https://cloud.r-project.org/bin/linux/)。
3. 下載並安裝最新版本的 [Rstudio](https://www.rstudio.com/products/rstudio/#Desktop)。 哦，嘿，看起來是開源！ 沙沙。
4. 下載並安裝最新版本的 [Git](https://gitforwindows.org/)。 **確保在安裝過程中選擇“從Windows命令提示符使用Git”。**

> **專業提示**：要將所有R軟件包更新為一個，只需執行以下代碼 `update.packages（ask = FALSE，checkBuilt = TRUE）`

現在，只需為每個安裝選擇所有常用的默認選項。 根據哪個操作系統（例如，Mac，Windows，Linux），每個人可能會有所不同。 就目前而言，對於此任務的其餘部分，我們將堅持使用簡單的Windows方式（但也提供使用命令行的一些說明）。

對於Linux或Debian用戶，只需使用以下命令安裝Git：

`sudo apt-get install git-core`

對於Mac用戶， [此鏈接](http://git-scm.com/download/mac)，或購買具有不同操作系統的新筆記本電腦。

如果需要，您還可以下載 [本地版本的GitHub](https://desktop.github.com/) 並通過簡單的GUI使用它。 它可以在Windows，Mac和Linux上使用，並且可以讓您的生活更輕鬆，特別是如果您想使用不同的平台來訪問RStudio。

> **專業提示：** 您在安裝Git時會看到'使用Git Bash作為Git項目的shell？'在這裡您可以使用命令行從RStudio外部訪問Git。 這是一個強大的野獸。 嘗試以下兩個命令開始：

`混帳配置--global user.name'您的用戶名'`   
`混帳配置--global user.email'您的email“`   


## 第二步：在RStudio中配置Git <a name="two"></a>

是的，這很容易做到。 接下來，進入RStudio，在頂部的選項卡中轉到 **工具>全局選項> Git / SVN**。 SVN只是像Git這樣的另一個版本控制系統，我們不需要在此擔心。

在其中顯示 *Git可執行文件*，將此路徑添加到您剛剛在上一步中下載的git.exe文件中。 確保此處的框顯示 **啟用RStudio項目** 版本控制界面。 現在，它已將版本控制與RStudio中的未來項目聯繫起來，為協作或獨奏工作提供了一個非常強大的附加維度。

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/git_svn.png?raw=true" width="400px"/>
</p>

<p align="center"><i>RStudio中的全局選項窗口</i></p>

  


接下來，點擊此窗口中的按鈕，該按鈕顯示 *創建RSA密鑰*，這是一個用於在不同系統之間進行身份驗證的私鑰，使您無需反复輸入密碼。 在這裡，它將彈出一個帶有公鑰的新窗口，您希望將其複製到剪貼板。

轉到GitHub，轉到您的配置文件設置，以及 *SSH和GPG鍵* 選項卡。 單擊 *新SSH密鑰*。 在這裡，粘貼來自RStudio的密鑰，稱之為'RStudio'之類的富有想像力的東西。

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/ssh_key.png?raw=true" width="800px"/>
</p>

<p align="center"><i>在GitHub裡面，您需要輸入剛才在RStudio中生成的密鑰</i></p>

  


好的，現在抓住你的屁股，我們進入命令行。 如果您以前從未使用過shell，請不要擔心，因為它與使用R或任何其他編碼系統非常相似。 這裡的主要區別在於，不是調用R中的函數，而是調用命令。

回到RStudio，轉到 **工具> Shell**，它將打開一個命令提示符窗口。 如果你已經玩過上面的Git Bash，你應該已經完成了這一步。 輸入以下兩個命令：

`混帳配置--global user.name'您的用戶名'`   
`混帳配置--global user.email'您的email“`   


希望不必說在您自己的GitHub用戶名和電子郵件中替換。 您可以通過在Windows中找到“Shell”來隨時訪問它。 或者，如果您右鍵單擊桌面上鍊接到GitHub存儲庫的任何文件夾，您可以立即打開Shell並將其打開。

這個階段所做的是將Git（在桌面上運行的軟件）配置到GitHub，這是一個存儲庫網站。

重啟R Studio。 哇，那太難了。 下一個。

  


## 第三步：為什麼我這樣做？ <a name="three"></a>

好吧，保持呼吸，我們將暫停這裡只是為了學習一些基本的Git命令。 您可以通過學習做的一些關鍵因素是：

* **添加**：這是您在提交之前將文件提交到臨時區域的位置。

* **提交** 這就像通過創建新版本或副本來“保存”您的工作。

* **推送**：這是您將文件從本地項目發送到在線存儲庫的方式。

* **拉**：這是您從在線存儲庫獲取文件到本地項目的方式。

回到RStudio，在 *終端*中輸入以下內容，或者打開一個新的Shell：

`git add。`

現在它實際上並不會做任何事情，但在未來將增加在當前工作目錄下的所有文件（這是什麼 `。` 那樣），以分期準備好提交。

  


## 第四步：Git和R之間的完美結合 <a name="four"></a>

現在，在任務1中，您應該已經學會瞭如何構建第一個GitHub存儲庫。 如果你還沒有這樣做，我們可以在你去的時候在這裡等待。 如果您已經擁有或擁有現有的GitHub存儲庫，我們可以繼續前進。

所以，你應該在GitHub上有一個存儲庫，包含一個 `README` 文件，一個 `LICENSE` 文件和一些其他位和bob。

我們現在要做的是將該存儲庫與Git集成。 現在穩定。

1. 首先，轉到 **Project> Create Project> Version Control> Git**。
2. 回到GitHub，您應該看到有一個https：// URL。 這是指向您的存儲庫的鏈接，它為您提供了在桌面上克隆它的選項。 現在，只需複制該鏈接，切換回RStudio，然後按照指示將其粘貼到“存儲庫URL”中。
3. 為項目提供目錄名稱，例如test，Jim或任何您想要的名稱。
4. 接下來，瀏覽桌面上您希望此項目生效的位置，即其子目錄。
5. 點擊“創建項目”，讓魔術完成！

你剛剛做的是告訴RStudio將R中的新項目與GitHub上的特定存儲庫相關聯。

## **第四步：替代方案**

如果你還沒有在GitHub上構建你的第一個存儲庫，我們可以在這裡做一些稍微不同的事情。 在RStudio中，單擊 *New project* ，然後單擊 *New Directory*。 調用它你想要的並根據需要更改目錄，確保勾選 *創建一個git存儲庫*，然後單擊 *創建項目*。 這產生了 `.Rproj` 文件，它可以在通常的方式通過RStudio管理，包括添加 `README.md`和 `LICENSE.md` 文件作為在任務1討論。

## 第五步：獲取內容內容 <a name="five"></a>

還記得我們創建的 `README` 文件嗎？ 好吧，是時候寫了。 回想一下任務1，我們說有一些特定的東西是一個很好的 `README` 文件。 你還記得他們中的任何一個嗎？ 為了更新你的記憶，這些是：

* 這個項目是關於什麼的，它做了什麼。
* 人們為什麼要關心，為什麼它有用。
* 如何有人開始為項目做貢獻。
* 如果有人需要幫助，可以聯繫誰。
* 許可證，貢獻指南和行為準則的鏈接。
* 項目結構的描述。
* 誰參與，他們的角色是什麼。
* 項目的當前狀態。

因此，在RStudio中，打開該文件嘗試為您的項目添加一些有關此信息的信息。 如果您正在為實際項目執行此操作，請嘗試使其有用。 如果你現在只是修修補補，你可以添加你想要的東西。

請記住，您的 `README` 文件採用markdown（.md）格式。 有關一些簡單的語法降價用法的複習，請查看這個 [方便的備忘單](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)。

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/markdown.png?raw=true" width="600px"/>
</p>

<p align="center"><i>在開發期間，此模塊在markdown中查看的內容的屏幕截圖。 元。</i></p>

  


## 第六步：勇敢的承諾 <a name="six"></a>

好的，現在你應該有一個編輯得很好的 `README` 文件。 現在我們將使用Git將其“提交”到項目中。 這基本上相當於保存了這個版本的項目，並記錄了所做的更改。 連續提交產生的歷史可以在以後檢查，讓您自信地工作。

有幾種方法可以做到這一點。

1. 轉到 **工具>版本控制>提交**
2. 在RStudio的環境窗格中，應該有一個新的“Git”選項卡。 便利。
3. 在您的控制台窗格中，現在應該有一個新的“終端”，您可以通過它運行Git命令行。

讓我們暫時堅持第二種選擇。 這個Git窗格顯示了哪些文件已被更改，並包含我們之前看到的最重要的Git命令的按鈕。

在Git窗口中選擇 `README` 文件，如果您對其進行了任何編輯，該文件應自動顯示。 這會將該文件添加到“臨時”區域，這有點像您工作的預先節省空間。 單擊“提交”，將彈出一個新窗口。

在這裡，您有機會查看您的更改，並編寫一個很好的提交消息。 輸入簡短的內容，但提供有關您在此版本或工作快照中所做更改的信息。 您希望這是足夠的信息，以便如果您或其他人回顧它，您就會知道為什麼要進行此提交以及與之相關的更改。 這些就像您的項目的安全網，以防您因某些原因需要退回。

> **專業提示**：在這裡，您將看到自上次提交以來所做的所有更改的列表。 較舊的刪除行為紅色，新添加的行為綠色。 仔細檢查這些以確保您所做的編輯是您打算進行的編輯。 這對於發現拼寫錯誤，雜散編輯以及您可能偶然引入的任何其他小錯誤非常有用。 安全第一。

**注意** 如果您是色盲並且無法看到添加或刪除了哪些行，則可以使用窗口左側兩列中的行號作為指導。 此處，第一列中的數字標識舊版本，第二列中的數字標識新版本。

現在，當您單擊“提交”時，將彈出另一個窗口，告訴您已更改的文件數以及該文件中已更改的行數。 關閉那個小窗口。

  


## 第七步：推！ <a name="seven"></a>

單擊新窗口右上角的 *Push* 按鈕。 現在會彈出一個新窗口。 這樣做是將本地存儲庫中更改的文件與 `README` 文件同步到GitHub上項目的在線版本。

要從命令行管理器執行此操作，請使用以下命令：

`git push -u origin master`

有時在這裡會提示您從GitHub添加您的用戶名和密碼，如果被問到，您應該這樣做。

關閉那個窗口，然後關閉下一個窗口。 轉到GitHub上的項目，刷新並檢查 `README` 文件是否仍然存在於其所有新編輯的榮耀中。 您應該看到您在文件旁邊創建的提交消息。

  


**可選的高級/令人敬畏的步驟**

好吧，所以你只是把一些內容推到你的第一個回購中，太棒了！ 現在讓我們為實際項目付諸實踐。 就像，你現在參與的那個。 我們來試試吧：

1. 在 [GitHub](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source)上轉到此項目的存儲庫

2. 將存儲庫分成您自己的GitHub帳戶。 這個URL應該是： `https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source.git`

3. 進入RStudio，轉到 **File> New Project**，選擇 *Version Control*，選擇 *Git*，然後粘貼在您的存儲庫副本中找到的分叉存儲庫URL。 您現在擁有自己的整個模塊的版本副本。 整齊。 將其保存在本地計算機上。

4. 現在，您需要告訴Git該項目的不同版本存在。 打開 *Shell*，然後輸入命令： `git remote add upstream https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source`

5. 你剛剛做了什麼就把原來的分支命名為 `上游`，只是為了讓事情變得簡單。 現在，創建一個新的 **分支** ，以獨立於主分支記錄您對此的更改。 輸入命令： `git checkout -b proposed-changes master`

6. 您剛剛創建了一個名為 `proposed-changes` 的新分支，您現在可以編輯所有內容和文件，讓您心滿意足。 希望這個項目的結構足夠簡單，您可以瀏覽。 可以在 `content_development` 文件夾中找到MOOC的所有原始文件，這是 `Task_3.md`。

7. 如果您滾動到 `Task_3.md`的底部，您應該會看到一個可以在您的姓名和所屬關係中進行編輯的地方。 添加這些，然後完成上面提到的提交過程。 如果您還看到其他需要編輯的內容，請隨意添加！

8. 現在，您希望將更改推送回原始分支。 在 *Shell*： `git push origin proposed-changes`使用以下命令

9. 回到GitHub，在這裡找到你的叉子。 單擊綠色小按鈕，然後創建拉取請求。 這本質上是一個綜述，將對MOOC項目的原始分支所做的更改進行整合。

10.     負責MOOC項目的業主現在將收到通知，審核並確認是否一切按計劃進行！ 我們將對其進行審核，如果一切順利，您的名字現在將永遠顯示為完成此高級任務的人。
      

11.     喝一杯茶，咖啡或葡萄酒來慶祝！
      

**恭喜**

您剛剛將Git與R Studio集成，並首次更改為版本控制項目。 您的生活現在將永遠不變，您的研究工作流程可能比以往更加快速，靈活和協作。 祝你好運回到Word。

最棒的是，這不必僅用於代碼。 您可以將它用於純文本，markdown，html以及R代碼。 可能性是無限的 - 您剛學到的是一種新形式的公開協作項目管理，適用於各種各樣的任務。

從現在開始，這完全取決於你！ 一些建議是：

* 經常提交。 像你的小狗一樣對待Git，因為它需要不斷和特別的關注。 只是輕輕拍打頭部就足以讓它滿意，但是持續服務會很開心。

* 執行此操作的最佳方法是在每次處理特定問題時進行提交。 例如，編寫段落，運行分析或修復錯誤。

* 經常推。 不要讓這些提交累積起來，否則會冒更大的風險進入合併衝突。 看到這些可能是噩夢的事情，只要確保經常推動。

* 經常拉。 如果其他人在同一個項目上遠程工作，您將需要及時了解他們的更改。 確保經常從GitHub中提取更改，以確保您完全同步。

* 實驗和探索！ 這項任務實際上只是觸及表面，並且有許多不同的功能，工具和方法可以使用。 實際上，您需要了解如何使用這些信息來改進您的研究工作流程，並最終在更好，更開放和可靠的研究上進行合作！

* 要了解有關問題，分支，合併衝突，拉取請求以及使用Git和RStudio的其他高級方面的更多信息，請查看Hadley Wickham撰寫的這篇 [真棒指南](http://r-pkgs.had.co.nz/git.html)。

  


**知道這種內容可以改進的方式嗎？**

是時候將新的GitHub技能用於測試運行了！ 所有內容的開發主要發生 [這裡](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.md)。 如果您對內容，佈局或其他任何內容有建議的改進，您可以製作它，然後在主持人驗證後它將自動成為MOOC內容的一部分！

## 完成此任務的ADVANCED版本的參與者列表

* 科恩大學CRF-C的Brendan Palmer
* Lisa Matthias，柏林自由大學
* 萊斯特大學的Hollie Marshall 
* Eric D. Wilkey，加拿大西部大學
* José-RaúlCanay-Pazos，西班牙聖地亞哥德孔波斯特拉大學
* EncarnaciónMartínezÁlvarez，西班牙
* Alberto Albz Marocchino，意大利
* Iratxe Rubio，巴斯克氣候變化中心BC3
* Gabriele Orlandi，法國巴黎社會科學高級研究學院（EHESS）
* HandeSodacı，土耳其
* Luke W. Johnston，丹麥奧胡斯大學
* Philippe Joly，WZB和HU-Berlin
* Paul Griffiths，NCAS和U. Cambridge
* Harin Lee，倫敦大學金史密斯學院
* 秘魯天主教大學路易斯卡馬喬
* 湯姆克里德福德，倫敦帝國理工學院
* 斯塔萬格大學Nithiya Streethran 

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)