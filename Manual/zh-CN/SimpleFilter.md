##注意

- 用户自行承担风险

##创建扩展

- 请阅读 <a href="https://github.com/jc3213/Misc/blob/master/Manual/zh-CN/HowToBuild.md">创建扩展的步骤</a>

## 使用说明

- 0) Simple Filter 使用全新 WebRequest.jsm API 与 MatchPattern.jsm API 编写
- 1) Simple Filter 规则包含 前缀, 次前缀, 匹配对象, 后缀, 目标对象, 资源类型
<p><img src="http://i66.tinypic.com/fvxl05.png"></p>
    - 1.1.1) 前缀 $ 代表 拦截 规则, 前缀 ^ 代表 重定向 规则
    - 1.1.2) 次前缀 ! 决定规则是否为白名单
    - 1.1.3) 阅读资料, 如何编写 <a href="https://developer.mozilla.org/en-US/Add-ons/WebExtensions/Match_patterns">匹配对象</a>
    - 1.1.4) 后缀 > 仅适用于 重定向 规则, 其意味着 重定向至
    - 1.1.5) 添加 @ 确定规则将按照 资源类型 进行 筛选 , 资源类型使用 | 进行分割, 阅读更多关于 <a href="https://developer.mozilla.org/en-US/docs/Mozilla/JavaScript_code_modules/WebRequest.jsm#Resource_types">资源类型</a>
  - 1.2) 你也可以查看 <a href="https://raw.githubusercontent.com/jc3213/Misc/master/Sample/SimpleProxy.txt">Simple Filter 规则样例</a>
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
