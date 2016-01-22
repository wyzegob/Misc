##注意

- 用户自行承担风险

##创建扩展

- 请阅读 <a href="https://goo.gl/9aM7i7">创建扩展</a>

## 使用说明

- 0) Simple Proxy 不会覆盖 Firefox 本身的代理设置
- 1) Simple Proxy 规则包含 前缀, 次前缀, 匹配对象
  - 1.1) 完全兼容 Auto-proxy 规则列表 (分支1.x 限定)
  - 1.2) 使用 匹配对象 以获取更好的性能 (分支2.x 以后)
    - 1.2.0) 可以使用 <a href="https://goo.gl/vt6Jj4">Simple Converter</a> 对 Auto-proxy 规则列表进行转换
    - 1.2.1) 前缀 # 代表规则是否适用于自动化代理服务
    - 1.2.2) 次前缀 ! 决定规则是否为白名单
    - 1.2.3) 阅读资料, 如何编写 <a href="https://goo.gl/sZzTgN">匹配对象</a>
- 2) 服务器必须满足 类型::地址::端口 的格式
  - 2.1) 例如 socks::127.0.0.1::1080
  - 2.2) 支持的协议类型 http, socks, socks4
    - 2.2.1) http 支持 HTTP 及 HTTPS 协议
    - 2.2.2) socks 支持 SOCKS V5 协议
    - 2.2.3) socks4 支持 SOCKS V4 协议
- 3) 可以通过添加 http:// 或 https:// 远程连接来订阅远程规则，支持base64编码的文件
  - 3.1) 例如 <a href="https://goo.gl/ryMotb">GFWList</a> (分支1.x 限定)
  - 3.2) 订阅规则每4天自动更新一次
- 4) 可以通过 about:addons 设置界面的 “浏览...” 按钮来指定绝对路径中的文件
- 5) 可以通过 file.txt 来访问相对路径 Profile\SimpleProxy\file.txt 中的规则
- 6) 可以通过点击 编辑：规则** 来修改你的规则
  - 6.1) 如果你有修改规则，你需要先点击 保存 按钮，然后再关闭 编辑器 窗口
  - 6.2) 订阅规则无法被修改
- 7) 你可以通过点击 清除：档案** 来清理掉不再使用的档案
