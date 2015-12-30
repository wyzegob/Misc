#Add-ons SDK Styled Add-ons

##Step:
- 1) Install jpm via npm
- 2) Enter X: and cd X:\yyyyy\zzzzz to defined the folder where you put the source code
- 3) Run jpm xpi to generate my-addon.xpi and my-addon.update.rdf
  - 3.1) Upload my-addon.xpi to AMO to get signed
  - 3.2) If updateKey is defined, please skip step 3
- 4) Run jpm sign to build and sign your add-on, you'll get signed my-addon.xpi

##Attention:
- 1) You must change the UUID of the add-on in package.json
- 2) You must edit or delete the updateURL, updateLink, and updateKey keys in package.json
  - 2.1) If updateKey is defined, you have to edit the version and updateLink keys in <a href="https://raw.githubusercontent.com/jc3213/Misc/master/Update/soWatch_mk2.rdf">update.rdf</a> and sign it with McCoy

<img src="http://i66.tinypic.com/ml5abm.png"></br>

#Old Styled Add-ons

##Step:
- 1) Zip all the files into my-addon.zip (don't zip the folder)
- 2) Rename my-addon.zip to my-addon-xpi
- 3) Upload my-addon.xpi to AMO to get signed

##Attention:
- 1) You must change the UUID of the add-on in install.rdf
- 2) You must edit or delete the updateURL key in install.rdf
- 3) You must edit or delete the updateLink key in Update.rdf
- 4) updateKey key in install.rdf and signature key in update.rdf are signed by McCoy
  - 4.1) If you upload the .xpi files to a host over SSL, there's no need to define these keys.

<img src="http://i68.tinypic.com/29zzcpv.png"></br>
<img src="http://i67.tinypic.com/6944dl.png"></br>
