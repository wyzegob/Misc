##注意

- 用户自行承担风险

##创建扩展

- 请阅读 <a href="https://github.com/jc3213/Misc/blob/master/Manual/zh-CN/HowToBuild.md">创建扩展的步骤</a>

## 使用说明

- 0) Simple Filter 使用全新 WebRequest.jsm API 与 MatchPattern.jsm API 编写
  - 0.1) 有时更新规则后需要重启浏览器
- 1) 规则分为 过滤规则$ 与 重定向^ 规则
  - 1.1.1) 过滤规则例 $*://www.baidu.com/
  - 1.1.2) 重定向规则例 ^*://www.baidu.com>https://www.google.com
  - 1.1.3) 匹配对象 必须遵循 <a href="https://developer.mozilla.org/en-US/Add-ons/WebExtensions/Match_patterns">MatchPattern</a> 的规则
  - 1.3) 可以通过 @Type1|Type2|Type3 来针对 资源类型 进行筛选
    - 1.3.1) 如果没有输入 Types ，将默认拦截所有资源类型
    - 1.3.2) 详情请阅读 <a href="https://developer.mozilla.org/en-US/docs/Mozilla/JavaScript_code_modules/WebRequest.jsm#Resource_types">请求类型</a>
  - 1.4) 规则详解请看下图

<img src="http://i68.tinypic.com/mbk0v7.png">

- 2） 可以通过添加 http:// 或 https:// 远程连接来订阅远程规则，支持base64编码的文件
  - 2.1） 例如 https://test.com/testrule.txt (不可用)
  - 2.2） 订阅规则每4天自动更新一次
- 3） 可以通过 about:addons 设置界面的 “浏览...” 按钮来指定绝对路径中的文件
- 4） 可以通过 file.txt@profile 这样的格式来访问相对路径 Profile\SimpleProxy\file.txt 中的规则
  - 4.1) profile 代表 Profile\SimpleProxy\
  - 4.2) firefox 代表 Mozilla Firefox\browser\SimpleProxy\
  - 4.3) winuser 代表 %UserProfile%\SimpleProxy\
- 5) 可以通过点击 编辑：规则** 来修改你的规则
  - 5.1) 如果你有修改规则，你需要先点击 保存 按钮，然后再关闭 编辑器 窗口
  - 5.2) 订阅规则无法被修改
