##Caution

- Use at your own risk

##How To Build

- Read <a href="https://github.com/jc3213/Misc/blob/master/Manual/en-US/HowToBuild.md">Build Step</a>

##How to use

- 0) Simple Filter uses the new WebRequest.jsm API and MatchPattern.jsm API
  - 0.1) Sometimes a browser restart is needed after rules are updated
- 1) Rules must match the format of PATTERN or PATTERN@Type1|Type2|Type3
  - 1.1) Rule sample as below
    - 1.1.1) http://example.com/*@image|script
  - 1.2) PATTERN must follow the rule of <a href="https://developer.mozilla.org/en-US/Add-ons/WebExtensions/Match_patterns">MatchPattern</a>
  - 1.3) If no Types were defined, all resources types would be blocked
    - 1.3.1) Read <a href="https://developer.mozilla.org/en-US/docs/Mozilla/JavaScript_code_modules/WebRequest.jsm#Resource_types">Resources Types</a> for more detail
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
