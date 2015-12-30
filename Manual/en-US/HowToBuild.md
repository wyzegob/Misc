#Add-ons SDK Styled Add-ons

##Step:
- 1) Install jpm via npm
- 2) Enter X: and cd X:\yyyyy\zzzzz to defined the folder where you put the source code
- 3) Run jpm xpi to generate my-addon.xpi and my-addon.update.rdf
  - 3.1) Upload my-addon.xpi to AMO to get signed
- 4) Run jpm sign to build and sign your add-on, you'll get signed my-addon.xpi
  - 4.1) If updateKey is defined, please skip step 3

##Attention:
- 1) You must change the UUID of the add-on in package.json
- 2) You must edit or delete the updateURL, updateLink, and updateKey keys in package.json

<img src="http://i66.tinypic.com/ml5abm.png"></br>

#Old Styled Add-ons

##Step:
- 1) Zip all the files into my-addon.zip (don't zip the folder)
- 2) Rename my-addon.zip to my-addon-xpi
- 3) Upload my-addon.xpi to AMO to get signed

##Attention:
- 1) You must change the UUID of the add-on in install.rdf
- 2) You must edit or delete the updateURL, and updateKey keys in install.rdf
- 3) You must edit or delete the updateLink, and signature keys in Update.rdf

<img src="http://i68.tinypic.com/29zzcpv.png"></br>
<img src="http://i67.tinypic.com/6944dl.png"></br>
