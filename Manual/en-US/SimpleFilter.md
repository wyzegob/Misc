##Caution

- Use at your own risk

##How To Build

- Read <a href="https://goo.gl/NZlNRH">Build an Add-on</a>

##How to use

- 0) Simple Filter uses the new WebRequest.jsm API and MatchPattern.jsm API
- 1) Simple Filter Rule contains Prefix, Sub-prefix, Match Pattern, Suffix, Redirect Target, Request Header, Resource Types
<p><img src="http://i66.tinypic.com/ztgdcn.png"></p>
    - 1.1.1) Prefix $ to determine Filter rule, Prefix ^ to determine Redirect Rule, Prefix % to determine HTTP Request Rule
    - 1.1.2) Sub-prefix ! to determine if the rule is whitelisted
    - 1.1.3) Read about how to write <a href="https://goo.gl/sZzTgN">Match Pattern</a>
    - 1.1.4) Suffix > is only available for Redirect rule, which means "redirect to", Suffix < is only available for HTTP Request rule, that are spltted by |
    - 1.1.5) Insert @ determines Rule will be filtered by Resource Types, which are splitted by | , Read more about <a href="https://goo.gl/wVla5U">Resource Types</a>
  - 1.2) See some rule samples <a href="https://goo.gl/veiWJZ">Simple Filter Sample List</a>
- 2) Use remote address http:// or https:// to subscribe proxy list, compatible with base64 encoding
  - 2.1) For example, <a href="https://goo.gl/Nf0B0a">Simple Filter Rulelist</a> by @523860169 converted from cjxlist
  - 2.2) Subscription(s) will be updated in 4 days
- 3) You can address absolute path using "Browse..." button in about:addons
- 4) You can address relative path using file.txt@profile to access the rulelist in Profile\SimpleFilter\file.txt
  - 4.1) profile stands for Profile\SimpleFilter\
  - 4.2) firefox stands for Mozilla Firefox\browser\SimpleFilter\
  - 4.3) winuser stands for %UserProfile%\SimpleFilter\
- 5) You can modify your rules by click "Edit: Rulelist **"
  - 5.1) You need to click "save" before you close the "editor" if any modification has been done
  - 5.2) Subscription(s) can not be modified
