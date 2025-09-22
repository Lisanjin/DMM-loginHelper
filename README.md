# DMM-loginHelper
dmm游戏多账号登录

### `在setting中添加删除游戏`  
具体的名称以“神绊的导师”为例：  
PC浏览器端“神绊的导师”的游戏地址为，http://pc-play.games.dmm.co.jp/play/cravesagax/  
那么填入setting的  
["神绊的导师", "cravesagax"],  
前一个值"神绊的导师"为你自定义的游戏名，后一个为游戏url中play后面的部分即"cravesagax"  
不同游戏用,号分隔，记得是英文逗号，最后一个游戏的最后不要带逗号  

### `账号添加`  
和上面的差不多，逗号分隔，保持格式

> **Warning**  
> 为了你的账号安全，如果不确信该软件（可执行文件exe）的来源是否可靠  
请到github下载源代码自行打包  
https://github.com/Lisanjin/DMM-loginhelper  


登录相关的代码来自沖田KENC  

`2024.10.12`  
尝试使用chromium代替默认浏览器启动游戏，以绕过chrome的后台休眠  
请在这里下载[chromium](https://download-chromium.appspot.com/)解压  
并将chrome.exe的路径填入到setting.json的"chromiun路径"中(注意使用/代替路径中的\\)  
如果你需要继续使用你的默认浏览器，请将"使用chromiun"设置为"否"  
为dmm部分游戏（目前有deepone和otogi，其他暂时不清楚）的st获取api变更添加了处理  

`2024.12.11` 
新游戏angelica aster也用了artemis这个api获取st，估计以后会越来越多，在设置里添加了对使用artemis api游戏的处理
目前我已知的就的deepone、童话、angelica这三款，如果还有其他的，请自行添加到setting的artemis_api列表

`2025.09.22`
dmm上的游戏应该已经全部改成了artemis这个api获取st，所以移除了老的登录方式。原来的代码依然保留，只是注释掉了。
添加了一个记忆账号上次启动游戏的功能。
