##注意

- 用户自行承担风险

##创建扩展

- 请阅读 <a href="https://github.com/jc3213/Misc/blob/master/Manual/zh-CN/HowToBuild.md">创建扩展的步骤</a>

## 使用说明

- 0) Simple Filter 使用全新 WebRequest.jsm API 与 MatchPattern.jsm API 编写
- 1) 规则必须满足 PATTERN 或 PATTERN@Type1|Type2|Type3 的格式
  - 1.1) 下面是规则样例
    - 1.1.1) http://example.com/*@image|script
  - 1.2) PATTERN 必须遵循 <a href="https://developer.mozilla.org/en-US/Add-ons/WebExtensions/Match_patterns">MatchPattern</a> 的规则
  - 1.3) 如果没有输入 Types ，将默认拦截所有请求类型
    - 1.3.1) 详情请阅读 <a href="https://developer.mozilla.org/en-US/docs/Mozilla/JavaScript_code_modules/WebRequest.jsm#Resource_types">请求类型</a>
- 2） 可以通过添加 http:// 或 https:// 远程连接来订阅远程规则，支持base64编码的文件
  - 2.1） 例如 https://github.com/gfwlist/gfwlist/raw/master/gfwlist.txt
  - 2.2） 订阅规则每4天自动更新一次
- 3） 可以通过 about:addons 设置界面的 “浏览...” 按钮来指定绝对路径中的文件
- 4） 可以通过 file.txt@profile 这样的格式来访问相对路径 Profile\SimpleProxy\file.txt 中的规则
  - 4.1) profile 代表 Profile\SimpleProxy\
  - 4.2) firefox 代表 Mozilla Firefox\browser\SimpleProxy\
  - 4.3) winuser 代表 %UserProfile%\SimpleProxy\
- 5) 可以通过点击 编辑：规则** 来修改你的规则
  - 5.1) 如果你有修改规则，你需要先点击 保存 按钮，然后再关闭 编辑器 窗口
  - 5.2) 订阅规则无法被修改
