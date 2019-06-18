---
output:
  html_document: 默認
  pdf_document: 默認
---

# 任務2：如何使用GitHub和Zenodo使您的代碼可以使用

此任務專為希望在學術文獻中創建和重複使用基於GitHub的項目/存儲庫的學生和研究人員而設計。

不要忘記你可以參加我們的開放 [**Slack頻道**](https://osmooc.herokuapp.com/)。 請在＃module5opensource上自我介紹一下，並告訴我們你是誰，你的背景，以及你如何在這裡結束！

預計完成時間：45-60分鐘。

## 目錄

- [前言](#Foreword)
- [設置GitHub存儲庫](#Setup)
- [選擇您的GitHub存儲庫](#Choose)
- [登錄Zenodo](#Login)
- [授權GitHub與Zenodo聯繫](#Authorise)
- [選擇要存檔的存儲庫](#Archive)
- [檢查存儲庫設置](#Check)
- [創建一個新版本](#Release)
- [獲得DOI](#DOI)
- [引用項目的清單](#Checklist)
- [其他資源](#Resources)

<p align="center">
  <img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/Task2.png?raw=true" alt="任務2工作流程" width="600" height="861" style="margin-right: 30px; margin-left: 10px;" onmouseover="this.width='1200'; this.height='1722'" onmouseout="this.width='600'; this.height='861'">
</p>

<p align="center"><i>任務2的工作流程。 在完成任務時保持這個方便！</i></p>

  


## 前言 <a name="Foreword"></a>

雖然GitHub和Zenodo的集成使得現在使用這些工具變得更加容易（2019年1月），但重要的是要強調GitHub（Gitlab，Bitbucket，...）的替代品和Zenodo的替代品（其他存儲庫可能更適合您的社區，您可能會問您的同事）。 例如，可以使用Gitlab並手動將每個新版本上傳到您的大學存儲庫，獲取DOI。 原則（在線使用版本控制系統，並在存儲庫中存檔提供持久唯一標識符的主要版本 ）可以應用於不同的工作流程。

## 設置GitHub存儲庫 <a name="Setup"></a>

> **專業提示**：確保在存儲庫中包含LICENSE和README文件。 這將向人們表明項目的目的，以及他們將來如何與之合作。

了解如何在其他指南中設置GitHub存儲庫 [任務1：構建GitHub存儲庫](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.md) ，它也是“模塊5：開放研究軟件和開放源代碼”的一部分。

## 選擇您的GitHub存儲庫 <a name="Choose"></a>

進入GitHub項目列表頁面 [github.com](https://github.com) ，前往“存儲庫”選項卡。 選擇要存檔的存儲庫，然後將其打開。

  


## 登錄Zenodo <a name="Login"></a>

現在轉到 [zenodo.org](https://zenodo.org)。 Zenodo是一個可以永久存檔代碼和其他項目元素的平台。 Zenodo通過為項目分配 **數字對象標識符** （DOI）來實現這一點，這也有助於使工作更加可信。 這與GitHub不同，GitHub充當項目實際工作的地方，而不是長期存檔。 在GitHub中，可以修改，刪除，重寫和不可逆轉地更改內容，這使得用於更長時間的參考目的有點令人擔憂。 Zenodo為研究成果提供更多安全性和持久性。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/zenodo.png?raw=true" width="800" /></p>

<p align="center"><i>註冊Zenodo</i></p>

  


如果您已經擁有Zenodo帳戶，這很容易。 如果沒有，請按照步驟創建一個 - 您甚至可以使用GitHub帳戶或ORCID配置文件登錄以簡化操作，因為Zenodo具有內置的集成功能。 這可能比創建另一個研究帳戶和個人資料更容易。

  


## 授權GitHub與Zenodo聯繫 <a name="Authorise"></a>

在Zenodo網站上，授權它在'[Using GitHub](https://zenodo.org/account/settings/github/)'部分中連接到您的GitHub帳戶。 在這裡，Zenodo會將您重定向到GitHub，要求獲取在您的存儲庫中使用“[webhooks](https://developer.github.com/webhooks/)”的權限。 您想在此處使用構成這些鏈接所需的權限來授權Zenodo。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/zenodo_github.png?raw=true" width="800" /></p>

<p align="center"><i>授權Zenodo與GitHub連接</i></p>

  


如果您嘗試授予Zenodo訪問組織存儲庫的權限，您（或管理員）將需要確保Zenodo被授予第三方訪問權限。 GitHub將發送需要確認的授權電子郵件。 此時，回到GitHub上的存儲庫設置中，您還需要確保將存儲庫設置為“public”，而不是私有。

  


## 選擇要存檔的存儲庫 <a name="Archive"></a>

如果你已經做到這一點，這意味著Zenodo現在被授權配置存儲庫webhooks，它需要存檔存儲庫並向它發出一個DOI。 要執行此操作，請在Zenodo網站上導航到 [GitHub存儲庫列表第](https://zenodo.org/account/settings/github/) 頁，然後只需單擊存儲庫旁邊的“打開”按鈕。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/enabled_repos.png?raw=true" width="800" /></p>

<p align="center"><i>允許在Zenodo中保留單個GitHub存儲庫</i></p>

  


## 檢查存儲庫設置 <a name="Check"></a>

現在，您已在Zenodo和您的存儲庫之間設置了一個新的webhook。 在GitHub中，單擊存儲庫的設置，然後單擊左側菜單中的Webhooks選項卡。 這應該顯示配置為Zenodo的新Zenodo webhook。 請注意，webhook列表可能需要一些時間才能顯示出來。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/webhooks.png?raw=true" width="800" /></p>

<p align="center"><i>檢查是否為GitHub存儲庫啟用了webhooks。 這裡使用開放獎學金策略的示例</i></p>

  


## 創建一個新版本 <a name="Release"></a>

您第一次存檔存儲庫稱為“第一個版本”。 每次創建該存儲庫的新版本並將其存檔時，都會創建一個新版本。 這可以在GitHub（頂部中心）的存儲庫的“版本”選項卡中進行跟踪。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/first_release.png?raw=true" width="800" /></p>

<p align="center"><i>檢查存儲庫第一次發布是否成功。 這裡使用開放獎學金策略的示例</i></p>

  


對於存儲庫的第一個存檔版本，請單擊Zenodo中的“創建新版本”。 填寫表格並提供有關發佈內容的詳細信息。 對於第一個版本，請確保將其稱為v1.0.0，這是標準做法。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/create_release.png?raw=true" width="800" /></p>

<p align="center"><i>創建一個新版本。 這裡使用開放獎學金策略的示例，已經存在第一個版本</i></p>

  


最後，單擊“發布版本”，您的存檔將在GitHub上發布和版本化。

要在Zenodo上查看您的版本，您需要訪問 [上傳](https://zenodo.org/deposit) 選項卡。 要完成歸檔，Zenodo需要更多細節。

<p align="center"><img src="https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/images/upload_release.png?raw=true" width="800" /></p>

<p align="center"><i>檢查新版本是否已上傳。 此處使用開放獎學金策略顯示示例</i></p>

  


## 獲得DOI <a name="DOI"></a>

這有時被稱為DOI'minting'，並且需要關於Zenodo上的存儲庫的一些額外信息。 在Zenodo上，單擊主菜單中的 [Upload](https://zenodo.org/deposit) 選項卡，您新上載的存儲庫應該在那裡。 向下滾動頁面並根據需要填寫額外信息，必填字段標有紅色星號，然後單擊“發布”。

**注**：只有在添加了這些額外信息後，您的DOI才會生效。 DOI可能還需要很短的時間才能生效。 示例DOI如下所示（再次針對開放獎學金策略）。

> **專業提示**：將DOI的URL複製到GitHub倉庫的README文件中，以便更輕鬆地進行交叉鏈接，並提供清晰的突出顯示的DOI徽章，供用戶查看和使用您的DOI。 您只需要在第一次發布DOI時執行此操作，因為它充當“概念DOI”並且鏈接到所有後續版本DOI。

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1323437.svg)](https://doi.org/10.5281/zenodo.1323437)

GitHub / Zenodo集成現在將為項目存儲庫的每個版本/版本分配DOI。 這使用戶能夠引用和引用特定版本的項目。 此外，引用的作者列表由存儲庫使用的GitHub用戶帳戶名自動確定 - 這意味著沒有人被遺漏。 以後可以在Zenodo上編輯作者詳細信息。 Zenodo中使用的DOI通過 [DataCite](https://www.datacite.org/) 服務註冊。

> **專業提示**：在項目的自述文件中創建此引文的“人類可讀”版本。 這對於可能不熟悉使用DOI創建引文的研究人員很有幫助，並且可以讓其他人更容易引用您的軟件並確認您的工作。 這方面的一個例子可能是： Jon Tennant。 （2018年7月30日）。 開放獎學金戰略發展的基礎：第一次正式發布（1.2版）。 Zenodo。 <http://doi.org/10.5281/zenodo.1323437>

**恭喜！**

您的GitHub存儲庫現在存檔在Zenodo中，並且可以對DOI進行版本控制，以反映存儲庫版本隨時間的更新。 您應該可以在GitHub Zenodo頁面上查看存儲庫的詳細信息。 這也意味著您的歸檔項目也可以被其他使用DOI的索引服務和搜索引擎所接受。

為其他人提供長期存檔和DOI以便能夠正確引用它，因為這提供了基本的引文元數據。 對於開放科學，重要的是能夠引用您在研究中使用的軟件，並且這種集成的工作流程可以實現這一點，符合研究引用的最佳實踐。 此外，這種做法對於將軟件（和相關項目）的標準提升到其他研究成果的標準非常重要。

> **專業提示**：您的研究是否由歐盟資助資助？ 現在，您可以通過更新項目Zenodo記錄中元數據的授權部分，將已歸檔項目直接連接到您的授權。 這大大有助於提高其可發現性！

  


## 引用項目的清單 <a name="Checklist"></a>

所以現在你在Zenodo有一個可持續存檔的GitHub存儲庫，可以重複使用和引用！ 在繼續之前，請確保您擁有：

- []將您的GitHub項目鏈接到Zenodo。 如果您在Zenodo中看到GitHub存儲庫的完整副本，那麼一切正常。
- [] Zenodo和GitHub集成設置工作得很好。 例如，擁有所有作者姓名，並且正確的項目標題會傳到Zenodo。 如果沒有，或者如果作者只有暱稱，您可以在Zenodo中編輯這些詳細信息。
- []項目有第一個版本，帶有DOI。 您應該在項目Zenodo頁面上顯示DOI。 第一個DOI稱為“概念DOI”，是連接所有後續版本DOI的主DOI。 複製此DOI鏈接並將其嵌入GitHub項目README頁面。 你完成了！

### 其他資源 <a name="Resources"></a>

[使您的代碼可信](https://guides.github.com/activities/citable-code/) - GitHub指南。

**知道這種內容可以改進的方式嗎？**

是時候將新的GitHub技能用於測試運行了！ 所有內容的開發主要發生 [這裡](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.md)。 如果您對內容，佈局或其他任何內容有建議的改進，您可以製作它，然後在主持人驗證後它將自動成為MOOC內容的一部分！

[![CC0 Public Domain Dedication](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)