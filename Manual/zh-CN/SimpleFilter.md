##注意

- 用户自行承担风险

##创建扩展

- 请阅读 <a href="https://github.com/jc3213/Misc/blob/master/Manual/zh-CN/HowToBuild.md">创建扩展的步骤</a>

## 使用说明

- 0) Simple Filter 使用全新 WebRequest.jsm API 与 MatchPattern.jsm API 编写
- 1) Simple Filter Rule contains Preifx, Sub-prefix, Match Pattern, Suffix, Target String, Resource Types
<p><img src="http://i66.tinypic.com/2ce12lg.png"></p>
    - 1.1.1) Prefix $ to determine Filter rule, Prefix ^ to determine Redirect Rule
    - 1.1.2) Sub-prefix ! to determine if the rule is whitelisted
    - 1.1.3) Raad about how to write <a href="https://developer.mozilla.org/en-US/Add-ons/WebExtensions/Match_patterns">Match Pattern</a>
    - 1.1.4) Suffix > is only available for Redirect rule, which means "redirect to"
    - 1.1.5) Resource Types is determined by @ , and splitted by | , Read more about <a href="https://developer.mozilla.org/en-US/docs/Mozilla/JavaScript_code_modules/WebRequest.jsm#Resource_types">Resource Types</a>
  - 1.2) See some rule samples <a href="https://raw.githubusercontent.com/jc3213/Misc/master/Sample/SimpleProxy.txt">Simple Filter Sample Rule</a>
- 2） 可以通过添加 http:// 或 https:// 远程连接来订阅远程规则，支持base64编码的文件
  - 2.1） 例如 https://github.com/jc3213/Misc/raw/master/Sample/SimpleProxy.txt
  - 2.2） 订阅规则每4天自动更新一次
- 3） 可以通过 about:addons 设置界面的 “浏览...” 按钮来指定绝对路径中的文件
- 4） 可以通过 file.txt@profile 这样的格式来访问相对路径 Profile\SimpleFilter\file.txt 中的规则
  - 4.1) profile 代表 Profile\SimpleFilter\
  - 4.2) firefox 代表 Mozilla Firefox\browser\SimpleFilter\
  - 4.3) winuser 代表 %UserProfile%\SimpleFilter\
- 5) 可以通过点击 编辑：规则** 来修改你的规则
  - 5.1) 如果你有修改规则，你需要先点击 保存 按钮，然后再关闭 编辑器 窗口
  - 5.2) 订阅规则无法被修改
