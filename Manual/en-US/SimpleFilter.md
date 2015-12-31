##Caution

- Use at your own risk

##How To Build

- Read <a href="https://github.com/jc3213/Misc/blob/master/Manual/en-US/HowToBuild.md">Build Step</a>

##How to use

- 0) Simple Filter uses the new WebRequest.jsm API and MatchPattern.jsm API
- 1) Rules must match the format of PATTERN or PATTERN@Type1|Type2|Type3
  - 1.1) Rule sample as below
    - 1.1.1) http://example.com/*@image|script
    - 1.1.2) <a href="https://github.com/jc3213/Misc/edit/master/Manual/en-US/SimpleFilter.md">*://example.com/*</a>
  - 1.2) PATTERN must follow the rule of <a href="https://developer.mozilla.org/en-US/Add-ons/WebExtensions/Match_patterns">MatchPattern</a>
  - 1.3) If no Types were defined, all resources types would be blocked
    - 1.3.1) Types must match main_frame, sub_frame, stylesheet, script, image, object, xmlhttprequest
- 2) Use remote address http:// or https:// to subscribe proxy list, compatible with base64 encoding
  - 2.1) For example, https://test.com/testrule.txt (not available)
  - 2.2) Subscription(s) will be updated in 4 days
- 4) You can address absolute path using "Browse..." button in about:addons
- 5) You can address relative path using file.txt@profile to access the rulelist in Profile\SimpleProxy\file.txt
  - 5.1) profile stands for Profile\SimpleProxy\
  - 5.2) firefox stands for Mozilla Firefox\browser\SimpleProxy\
  - 5.3) winuser stands for %UserProfile%\SimpleProxy\
- 6) You can modify your rules by click "Edit: Rulelist **"
  - 6.1) You need to click "save" before you close the "editor" if any modification has been done
  - 6.2) Subscription(s) can not be modified
