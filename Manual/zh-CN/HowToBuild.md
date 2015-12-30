#基于 Add-ons SDK 的 Add-ons

##步骤:
- 1) 通过 npm 安装 jpm
- 2) 输入 X: 以及 cd X:\yyyyy\zzzzz 以选定存放源代码的文件夹
- 3) 运行 jpm xpi 生成 my-addon.xpi 文件 与 my-addon.update.rdf 文件
  - 3.1) 将 my-addon.xpi 上传至 AMO 获取签名
  - 3.2) 如果有使用 updateKey 的话必须请跳过第三步
- 4) 运行 jpm sign 可以直接生成已签名的 my-addon.xpi


##注意事项:
- 1) 你必须修改 package.json 中的 UUID
- 2) 你必须修改或删除 package.json 中的 updateURL, updateLink, updateKey 键值
  - 2.1) 如果使用 updateKey, 你必须参考<a href="https://raw.githubusercontent.com/jc3213/Misc/master/Update/soWatch_mk2.rdf">这里</a> 修改 version 和 updateLink 后再用 McCoy 签名

<img src="http://i66.tinypic.com/ml5abm.png"></br>

#旧式 Add-ons

##步骤:
- 1) 将所有文件压缩成 .zip文件 (不要直接压缩文件夹)
- 2) 将 my-addon.zip 文件更改为 my-addon.xpi 文件
- 3) 将 my-addon.xpi 文件上传至 AMO 签名

##注意事项:
- 1) 你必须修改 install.rdf 中的 UUID
- 2) 你必须修改或删除 install.rdf 中的 updateURL 键值
- 3) 你必须修改或删除 Update.rdf 中的 updateLink 键值
- 4) install.rdf 中的 updateKey 键值 与 Update.rdf 中的 signature 键值由 McCoy 签署颁发
  - 4.1) 如果你将文件上传至 支持 SSL加密 的服务器上则不需要使用 McCoy

<img src="http://i68.tinypic.com/29zzcpv.png"></br>
<img src="http://i67.tinypic.com/6944dl.png"></br>
