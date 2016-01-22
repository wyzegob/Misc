##Caution

- Use at Userr own risk

##How To Build

- Read <a href="https://goo.gl/NZlNRH">Build an Add-on</a>

##How to use

- 0) Simple Proxy will not override proxy settings of Firefox 
- 1) Simple Proxy Rule contains Prefix, Sub-prefix, Match Pattern
  - 1.1) Full compatibility with Auto Proxy Rulelist (branch 1.x)
  - 1.2) Switch to MatchPattern.jsm API for better performance (branch 2.x)
    - 1.2.0) User can use <a href="https://goo.gl/vt6Jj4">Simple Converter</a> to convert Auto Proxy Rulelist
    - 1.2.1) Prefix $ to determine if the rule is used for auto proxy serivce
    - 1.2.2) Sub-prefix ! to determin if the rule is whitelisted
    - 1.2.3) Read about how to write <a href="https://goo.gl/sZzTgN">Match Pattern</a>
- 2) Server must match the form of protocol::address::port
  - 2.1) For example, socks::127.0.0.1::1080
  - 2.2) Supported protocol: http, socks, socks4
    - 2.2.1) http support both HTTP and HTTPS protocol
    - 2.2.2) socks support SOCKS V5 protocol
    - 2.2.3) socks4 support SOCKS V4 protocol
- 3) Use remote address http:// or https:// to subscribe proxy list, compatible with base64 encoding
  - 3.1) For example, <a href="https://goo.gl/ryMotb">GFWList</a> (branch 1.x)
  - 3.2) Subscription(s) will be updated in 4 days
- 4) User can address absolute path using "Browse..." button in about:addons
- 5) User can address relative path using file.txt to access the rulelist in Profile\SimpleProxy\file.txt
- 6) User can modify the rules by click "Edit: Rulelist **"
  - 6.1) User need to click "save" before "close" the "editor" if any modification has been done
  - 6.2) Subscription(s) can not be modified
- 7) User can clear the profile which is no longer in use by press "Clear: Profile **"
