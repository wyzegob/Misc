##Caution

- Use at your own risk

##How To Build

- Read <a href="https://github.com/jc3213/Misc/blob/master/Manual/en-US/HowToBuild.md">Build Step</a>

##How to use

- 0) Simple Filter uses the new WebRequest.jsm API and MatchPattern.jsm API
- 1) Simple Filter Rule contains Preifx, Sub-prefix, Match Pattern, Suffix, Target String, Resource Types
<p><img src="http://i65.tinypic.com/34ozdb5.png"></p>
    - 1.1.1) Prefix $ to determine Filter rule, Prefix ^ to determine Redirect Rule
    - 1.1.2) Sub-prefix ! to determine if the rule is whitelisted
    - 1.1.3) Raad about how to write <a href="https://developer.mozilla.org/en-US/Add-ons/WebExtensions/Match_patterns">Match Pattern</a>
    - 1.1.4) Suffix > is only available for Redirect rule, which means "redirect to"
    - 1.1.5) Resource Types is determined by @ , and splitted by | , Read more about <a href="https://developer.mozilla.org/en-US/docs/Mozilla/JavaScript_code_modules/WebRequest.jsm#Resource_types">Resource Types</a>
  - 1.2) See some rule samples <a href="https://raw.githubusercontent.com/jc3213/Misc/master/Sample/SimpleProxy.txt">Simple Filter Sample Rule</a>
- 2) Use remote address http:// or https:// to subscribe proxy list, compatible with base64 encoding
  - 2.1) For example, https://github.com/jc3213/Misc/raw/master/Sample/SimpleProxy.txt
  - 2.2) Subscription(s) will be updated in 4 days
- 3) You can address absolute path using "Browse..." button in about:addons
- 4) You can address relative path using file.txt@profile to access the rulelist in Profile\SimpleFilter\file.txt
  - 4.1) profile stands for Profile\SimpleFilter\
  - 4.2) firefox stands for Mozilla Firefox\browser\SimpleFilter\
  - 4.3) winuser stands for %UserProfile%\SimpleFilter\
- 5) You can modify your rules by click "Edit: Rulelist **"
  - 5.1) You need to click "save" before you close the "editor" if any modification has been done
  - 5.2) Subscription(s) can not be modified
