##Caution

- Use at your own risk

##How To Build

- Read <a href="https://github.com/jc3213/Misc/blob/master/Manual/en-US/HowToBuild.md">Build Step</a>

##How to use

- 0) Simple Filter uses the new WebRequest.jsm API and MatchPattern.jsm API
  - 0.1) Sometimes a browser restart is needed after rules are updated
- 1) Supported Rules are Filter Rule with $ , and Redirect Rule with ^
  - 1.1.1) Filter Rule sample, $*://www.baidu.com/
  - 1.1.2) Redirect Rule sample, ^*://www.baidu.com/>https://www.google.com/
  - 1.1.3) Pattern must follow the rule of <a href="https://developer.mozilla.org/en-US/Add-ons/WebExtensions/Match_patterns">MatchPattern</a>
  - 1.3) You could define @Type1|Type2|Type3 to filter resource types
    - 1.3.1) None of Types will match all resource types
    - 1.3.2) Read more about <a href="https://developer.mozilla.org/en-US/docs/Mozilla/JavaScript_code_modules/WebRequest.jsm#Resource_types">Resource Types</a>
  - 1.4) See pic below for more details
<p><img src="http://i67.tinypic.com/2wn47yr.png"></p>
- 2) Use remote address http:// or https:// to subscribe proxy list, compatible with base64 encoding
  - 2.1) For example, https://test.com/testrule.txt (not available)
  - 2.2) Subscription(s) will be updated in 4 days
- 3) You can address absolute path using "Browse..." button in about:addons
- 4) You can address relative path using file.txt@profile to access the rulelist in Profile\SimpleProxy\file.txt
  - 4.1) profile stands for Profile\SimpleProxy\
  - 4.2) firefox stands for Mozilla Firefox\browser\SimpleProxy\
  - 4.3) winuser stands for %UserProfile%\SimpleProxy\
- 5) You can modify your rules by click "Edit: Rulelist **"
  - 5.1) You need to click "save" before you close the "editor" if any modification has been done
  - 5.2) Subscription(s) can not be modified
