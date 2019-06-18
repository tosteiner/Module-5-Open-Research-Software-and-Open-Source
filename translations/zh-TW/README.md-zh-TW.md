# 第5單元內容開發

這些是此MOOC模塊的主要內容開發文件。

**狀態**： **現場直播！ 這個模塊現已上線，可以通過 [Eliademy](https://eliademy.com/catalog/oer/module-5-open-research-software-and-open-source.html)進入。**

該模塊的第三個版本現已準備就緒，已在Zenodo上發布：

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1434288.svg)](https://doi.org/10.5281/zenodo.1434288) 和介紹視頻也已經 [發表](https://www.youtube.com/watch?v=1fwGliIyAZs)。

要引用此工作，請使用以下參考：

喬恩坦南特;西蒙沃辛頓; Tania Allard; Philipp Zumstein; Daniel S. Katz;亞歷山大莫利; Stephan Druskat;朱利安·科倫;阿方史密斯;伊娜史密斯;托比亞斯施泰納; Rutger Vos; KonradFörstner; Heidi Seibold;亞歷山德羅·薩雷塔;阿比蓋爾Cabunoc梅斯。 （2018年12月4日）。 OpenScienceMOOC / Module-5-Open-Research-Software-and-Open-Source：第三版（3.0.0版）。 Zenodo。 <http://doi.org/10.5281/zenodo.1937708>。

在此處進行更改之前，請參閱 [貢獻指南](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/CONTRIBUTING.md)。

任何人都可以在GitHub</a> 上加入我們的 [開放Slack頻道](https://osmooc.herokuapp.com/) 和 開放團隊，參與整個MOOC項目。</p> 

## 核心內容

這些是草案內容文件。 內容完全可訪問，可單獨或作為一組用於學習目的，並可根據需要共享和重複使用。 但是，它們還沒有被整合到正式的MOOC平台中。 目前，它們以markdown格式編寫，然後使用 [註釋](https://github.com/aaren/notedown) 工具轉換為iPython筆記本格式。 PDF和HTML版本使用 [pandoc](https://pandoc.org/demos.html) 和 [Markdown打包到 [Atom](https://atom.io/)PDF](https://atom.io/packages/markdown-pdf) 包。

如上所述：

1. 確保你在Linux或Debian中工作
2. 更改工作目錄：例如 `cd / mnt / c / users / pc / desktop /`
3. 安裝說明： `pip install notesown`
4. 轉換文件： `表示input.md > output.ipynb`

**重要** 請編輯 **降價** 文件，而不是iPython / HTML文件。 這些將根據需要定期轉換和同步。

### 以降價格式

- [**主要內容**](MAIN.md) - 本模塊的主要內容。 （[YouTube視頻](https://www.youtube.com/watch?v=BHrOEmKk5zM)）
- [**TASK 1**](Task_1.md) - 如何在GitHub上設置第一個存儲庫。 （[YouTube視頻](https://www.youtube.com/watch?v=AnftV9HBPSc&t=4s)）
- [**TASK 2**](Task_2.md) - 如何使用GitHub和Zenodo使您的代碼可以使用。 （[YouTube視頻](https://www.youtube.com/watch?v=pjsbBQYOOaE&t=4s)）
- [**任務3**](Task_3.md) - 如何將Git與RStudio集成。 （[YouTube視頻](https://www.youtube.com/watch?v=Q-6jfjSAspA)）

### 在iPython筆記本格式中

注意：與GitHub查看器相比，這些最好在Juypter中查看完整功能。

- [**主要內容**](MAIN.ipynb) （點擊 [這裡](https://nbviewer.jupyter.org/github/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/MAIN.ipynb) 來查看）
- [**任務1**](Task_1.ipynb) （點擊 [這裡](https://nbviewer.jupyter.org/github/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_1.ipynb) 查看）
- [**任務2**](Task_2.ipynb) （點擊 [這裡](https://nbviewer.jupyter.org/github/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_2.ipynb) 查看）
- [**任務3**](Task_3.ipynb) （點擊 [這裡](https://nbviewer.jupyter.org/github/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/content_development/Task_3.ipynb) 查看）

## 以PDF格式

- [**主要內容**](MAIN.pdf)
- [**任務1**](Task_1.pdf)
- [**任務2**](Task_2.pdf)
- [**任務3**](Task_3.pdf)

## 以HTML格式

- [**主要內容**](MAIN.html)
- [**任務1**](Task_1.html)
- [**任務2**](Task_2.html)
- [**任務3**](Task_3.html)

## 生產文件

1. [計劃](01-plan.md) 
2. [設計](02-design.md)
3. [錄製和編輯](03-recording.md)
4. [內部審查](04-quizzes.md)

## [生產工具包](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/tree/master/production_toolkit)關鍵資源

- [模塊設計協議](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/production_toolkit/MODULE_DESIGN_PROTOCOL.md)
- [MOOC計劃模板](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/production_toolkit/MOOC_planning_template.md)
- [腳本模板](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/production_toolkit/Script_template.md)
- [視頻管理協議](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/production_toolkit/Video_management_protocol.md)
- [寫一個腳本](https://github.com/OpenScienceMOOC/Module-5-Open-Research-Software-and-Open-Source/blob/master/production_toolkit/Writing_a_script.md)