#基于 Add-ons SDK 的 Add-ons

##步骤:
- 1) 通过 npm 安装 jpm
- 2) 输入 X: 以及 cd X:\yyyyy\zzzzz 以选定存放源代码的文件夹
- 3) 运行 jpm xpi 生成 my-addon.xpi 文件 与 my-addon.update.rdf 文件
  - 3.1) 将 my-addon.xpi 上传至 AMO 获取签名
- 4) 运行 jpm sign 可以直接生成已签名的扩展 （如果有使用 updateKey 的话必须请跳过第三步）

##注意事项:
- 1) 你必须修改 package.json 中的 UUID
- 2) 你必须修改或删除 package.json 中的 updateURL, updateLink, updateKey 键值
  - 2.1) 如果你需要使用 updateKey 的话，jpm xpi生成的 update.rdf 文件无法通过 McCoy 应用签名
  - 2.2) 你必须参考<a href="https://raw.githubusercontent.com/jc3213/Misc/master/Update/soWatch_mk2.rdf">这里</a> 修改版本号后再用 McCoy 应用签名

<p><img src="http://i66.tinypic.com/ml5abm.png"></p>

#老扩展

##步骤:
- 1) 将所有文件压缩成 .zip文件 (不要直接压缩文件夹)
- 2) 将 my-addon.zip 文件更改为 my-addon.xpi 文件
- 3) 将 my-addon.xpi 文件上传至 AMO 签名

##注意事项:
- 1) 你必须修改 install.rdf 中的 UUID
- 2) 你必须修改或删除 install.rdf 中的 updateURL, updateKey 键值
- 3) 你必须修改或删除 Update.rdf 中的 updateLink, signature 键值

<p><img src="http://i68.tinypic.com/29zzcpv.png"></p>
<p><img src="http://i67.tinypic.com/6944dl.png"></p>
