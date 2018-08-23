# 提交內容更新和勘誤
所有人都可以通過 https://github.com/shuowenjiezi/shuowen 爲 [說文解字](http://www.shuowen.org "說文解字") http://www.shuowen.org 提交內容更新和勘誤。

## 關於此文檔
這個文檔是寫給不會使用 github 的朋友的，如果你已經熟悉 clone 和 pull request，可以跳過此文檔。

## 提交更新的步驟
### （1）克隆代碼庫
前往：https://github.com/shuowenjiezi/shuowen 並點擊頁面上的 “Clone or download” 按鈕
![克隆代碼庫](https://raw.githubusercontent.com/shuowenjiezi/shuowen/master/doc/img/git-clone.png) 

### （2）查找您要更新的文件
[說文解字](http://www.shuowen.org "說文解字") 網站上所有的字頭都有對應的編號，可以通過鏈接地址找到字頭的編號。比如“帝”字的鏈接地址是 http://www.shuowen.org/view/7 ，那麼“帝”字的編號就是 “7”，對應的代碼庫文件就是 7.json。

先找到您要修改的字頭編號，然後到克隆的版本庫的 data 目錄下面去找以「編號」+「.json」命名的文件，比如「嚏」字的編號是 831，那麼對應的文件名就是 “**831.json**”。需要注意的是，因爲 data 目錄下面的文件太多，github 默認不展示全部文件，所以最簡單的方式就是點擊 “Find file” 搜索文件：

![查找文件](https://raw.githubusercontent.com/shuowenjiezi/shuowen/master/doc/img/git-find-file.png) 

進入搜索界面後，輸入您要找的文件名即可：

![搜索文件](https://raw.githubusercontent.com/shuowenjiezi/shuowen/master/doc/img/git-search-file.png) 

### （3）修改文件內容

找到要修改的文件後，可以直接在線編輯：

![编辑内容](https://raw.githubusercontent.com/shuowenjiezi/shuowen/master/doc/img/git-edit.png) 

文件內容的格式是 JSON，關於內容格式的定義，請參考 “[格式說明](https://github.com/shuowenjiezi/shuowen/blob/master/doc/FORMAT.md  "格式說明")”。

內容修改完成後，點擊 “Preview changes” 查看版本對比。

![預覽修改](https://raw.githubusercontent.com/shuowenjiezi/shuowen/master/doc/img/git-preview.png) 

在預覽頁面上面，紅色背景表示被修改的內容，綠色背景表示更新後的版本。

### （4）提交編輯內容

確認修改內容後，可以提交編輯內容。請務必備註修改的內容，格式爲：

[修改原因，包括“完善”和“勘誤”] #字頭編號 - 字頭 - 被修改的內容

例如：[勘誤] #172 - 𤧩 - 反切由 “鳥貫切” 更新爲 “烏貫切”

![提交更新](https://raw.githubusercontent.com/shuowenjiezi/shuowen/master/doc/img/git-commit.png) 

填寫好備註信息後，點擊 “Commit changes” 提交。

### （5）推送更新

到目前爲止，所有的更新都基於克隆後的代碼庫，現在需要將更新推送到原始代碼庫，要發送合併請求，只需要點擊 “New pull request” 按鈕，

![發送合併請求](https://raw.githubusercontent.com/shuowenjiezi/shuowen/master/doc/img/git-pr.png)  

在合併請求頁面，首先確認合併的目標分支是 dev，而不是 master，然後點擊 “Create pull request” 按鈕，

![確認合併分支](https://raw.githubusercontent.com/shuowenjiezi/shuowen/master/doc/img/git-pr-branch.png)  

填入更新描述，可直接使用第四步輸入的備註信息，如果需要，也可以在下面的文本框裏面輸入更多描述內容，然後點擊 “Create pull request” 按鈕，

![更新描述](https://raw.githubusercontent.com/shuowenjiezi/shuowen/master/doc/img/git-pr-comment.png)  

到這裏，一個完整的更新流程就結束了。

我會在收到合併請求後，確認更新內容，然後合併到 [說文解字](http://www.shuowen.org "說文解字") 的代碼庫，在一段時間之後，會從代碼庫加載數據到 [說文解字](http://www.shuowen.org "說文解字") 的數據庫，至此，更新的數據便會顯示到 [說文解字](http://www.shuowen.org "說文解字") 的網站上面。
