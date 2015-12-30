#基于 Add-ons SDK 的 Add-ons

##步骤:
- 1) 通过 npm 安装 jpm
- 2) 输入 X: 以及 cd X:\yyyyy\zzzzz 以选定存放源代码的文件夹
- 3) 运行 jpm xpi 生成 my-addon.xpi 文件 与 update.rdf 文件
  - 3.1) 将 my-addon.xpi 上传至 AMO 获取签名 (可选)
- 4) 运行 jpm sign 可以直接生成已签名的扩展

##注意事项:
- 1) 你必须修改 package.json 中的 UUID
- 2) 你必须修改或删除 package.json 中的 updateURL, updateLink, updateKey 键值
<img src="http://i66.tinypic.com/ml5abm.png">

#老扩展

##步骤:
- 1) 将所有文件压缩成 .zip文件 (不要直接压缩文件夹)
- 2) 将 my-addon.zip 文件更改为 my-addon.xpi 文件
- 3) 将 my-addon.xpi 文件上传至 AMO 签名

##注意事项:
- 1) 你必须修改 install.rdf 中的 UUID
- 2) 你必须修改或删除 install.rdf 中的 updateURL, updateKey 键值
- 3) 你必须修改或删除 Update.rdf 中的 updateLink, signature 键值
<img src="http://i68.tinypic.com/29zzcpv.png">
<img src="http://i67.tinypic.com/6944dl.png">
