# Boostsrap5 客製化起手專案
## 前言
如果你看過 [Boostsrap3 Gulp 快速建立靜態切版目錄](https://github.com/suhan1220/bs3work)  
其實已經是很久以前的方式了。  
這次我們是要用[Bootstrap5](https://getbootstrap.com/docs/5.0/getting-started/introduction/)，如果你沒用過SCSS客製化，沒有真的了解Bootstrap5。又怎麼好意思說他肥大呢😏 (逃~)

老話一樣，如果剛好你也需要，那麼應該會很適合你。

1. 慣用 SCSS 來撰寫 CSS
2. 使用 Boostsrap5
3. 使用搭配Visual Studio Code  
HTML\CSS 更新預覽、靜態檔案的壓縮，改用 VSCode 搭配套件完成。
4. 基本靜態資料夾建立，方便切版起始作業。  
因可能搭配其他前端作業或是階段合作，因此盡量減少重複的gulp或webpack流程，一條龍作業不適用此參考。
---------------------------
## 基本環境處理

原則上應該只有第一次會需要處理，後續作業就會很快速。
### 基本環境軟體安裝
- [node (建議選擇穩定版)](https://nodejs.org/en)：運作必需工具
- [Git](https://git-scm.com/)：版控工具
- [Visual Studio Code](https://code.visualstudio.com/)：編輯器
- [Yarn](https://classic.yarnpkg.cn/docs/install/#windows-stable)：加快你安裝NPM套件的工具

詳細就自行去了解囉!
### Visual Studio Code套件
- Live Sass Comppiler：SCSS to CSS 工具 [介紹網址](https://marketplace.visualstudio.com/items?itemName=glenn2223.live-sass)
- Live Server：HTML 編輯即時預覽工具 [介紹網址](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
- MiniifyALL：CSS\JavaSctipt to Minfile工具 [介紹網址](https://marketplace.visualstudio.com/items?itemName=josee9988.minifyall)

以上請先完成安裝,並留意是否為最新版本。  

---------------------------
## 開始吧!
Step1.下載本專案  

Step2.在VSCode開啟專案，打開終端機
輸入 yarn init 設定你的基本package資訊  
輸入 yarn add bootstrap@5.2.3

Step3.打開 styles/_custom-bootstrap.scss  
我已設定好對應NPM位置的SCSS位置，  
註解掉你不需要的{components}.scss檔，需要的再取消註解即可。

Step4.打開 styles/main.scss 修改SCSS預設值  
( 不要再 !important 了 )

在 @import "custom-bootstrap"; 前，
將想修改的預設值修改，例：主色、文字、邊框顏色等等。  
專案範例中 _我有修改主色並移除"info","light","dark"顏色增加第三個主色 third。_

> 如果不知道預設的宣告名稱為什麼，可以進到node_modules/bootstrap/scss/_variables.scss 裡面尋找，下關鍵字找很快的。也可看[官方英文版](https://getbootstrap.com/docs/5.1/customize/sass/#variable-defaults)其實也有說明如何修改。

Step5.點擊 [Watch Sass]，存檔更新 css 檔案。  
Step6.點擊 Cheatsheet-Bootstrap5.html 檔案可見修改過後的客製化 bootstrap 樣式。
> 被關掉或移除的樣式就只會看到沒有樣式的狀態囉!


----------

後續可搭配 [Go Live] 檢視及時修改的靜態頁面。  

需要產出 min 的檔案只需右鍵點擊  
 [ Minify the select document and preserve the original] 產出。


