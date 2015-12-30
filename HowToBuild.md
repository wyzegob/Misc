#Add-ons SDK Styled Add-ons

##Step:
- 1) Install jpm via npm
- 2) Enter X: and cd X:\yyyyy\zzzzz to defined the folder where you put the source code
- 3.1) Run jpm xpi to build xpi then upload to AMO to get signed
- 3.2) Run jpm sign to build and sign your add-on, you'll get signed xpi

##Attention:
- 1) You must change the UUID of the add-on in package.json
- 2) You must edit or delete the updateURL, updateLink, and updateKey keys in package.json
<img src="http://i66.tinypic.com/ml5abm.png">

#Old Styled Add-ons

##Step:
- 1) Zip all the files into my-addon.zip (don't zip the folder)
- 2) Rename my-addon.zip to my-addon-xpi
- 3) Upload my-addon.xpi to AMO and get signed

##Attention:
- 1) You must change the UUID of the add-on in install.rdf
- 2) You must edit or delete the updateURL, and updateKey keys in install.rdf
- 3) You must edit the updateLink keys in Update.rdf
<img src="http://i68.tinypic.com/29zzcpv.png">
<img src="http://i67.tinypic.com/im6p6w.png">
