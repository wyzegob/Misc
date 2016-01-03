##Caution

- Use at your own risk
- It will take some time to download the players after installation, please be patient if you would switch to Player Override

##How To Build

- Read <a href="https://github.com/jc3213/Misc/blob/master/Manual/en-US/HowToBuild.md">Build Step</a>

##About soWatch!

- soWatch! equivalent to the lesser function version of soWatch! mk2
- soWatch! do not have either Player Auto Update function or Toolbar UI
- If you want to use local players, you have to download or update them manually

##How To Use

###about:addons
- Toolbar UI, Add/remove the soWatch! mk2 button to/from the Toolbar
- Auto Update Period, the time gap between each auto update sessions
- Local Directory Option, where to save and syncs players
  - Firefox Profile, the Profiles\soWatch directory (default)
  - Firefox Program, the Mozilla Firefox\browser\soWatch directory
  - Windows Home, the %UserProfile%\soWatch directory
  - User Defined, if you have not defined local directory using Browse... , it will return to default
- Defined Local Directory, Browse... to define local directory
- Access Remote Host, access and load players directly from remote server
- Remote Server Option, where players were hosted
  - 15536900@bitbucket.org, players provided and hosted by 15536900 from bbs.kafan.cn (default)
  - 523860169@coding.io, players hosted by 523860169 from bbs.kafan.cn (not recommended)
  - User Defined, if you have not defined remote server, it will return to default
- Defined Remote Server, you can upload players to your private host and share with your friends
- Options per Site, options for each of the video sites, some of the preferences are binded together
  - Player Override, use moded player(s) instead of tje original player(s)
  - Filter XML Request, block certain XML request(s) (Default rule, switch to Player Override if any error occurs)
  - Original Behavior, stop the functions above and restore the original behavior
- Simulate per Site, modifiy the referer to avoid incoming cross domain problem

###Toolbar Button

- Restore All Settings, restore all settings to default (some are not affected)
  - Local Directory Option, Defined Local Directory, Remote Server Option, Defined Remote Server
- Access Remote Host, the same to about:addons
- Run Manual Update, download players immediately by ignore Auto Update Period , and Players Update Check
- Options per Site, the same to about:addons, but only displayed in certain conditions
