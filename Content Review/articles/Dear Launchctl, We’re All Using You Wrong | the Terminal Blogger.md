Notes for Dear Launchctl, We’re All Using You Wrong | the Terminal Blogger

## Source:
Author: joelsenders.wordpress.com
Category: articles
Updated: 02/11/2021 10:28 AM
Highlights URL: https://readwise.io/bookreview/7676065
SourceUrl: https://joelsenders.wordpress.com/2019/03/14/dear-launchctl-were-all-using-you-wrong/


#### Extras:
**launchd****launchctl****launchagent****bootstrap****Joel Senders**

 
-----
 ## Highlights:

### load | unload
>load | unload ^rw144342983hl

Comment: huh? launchctl load and unload are old commands and will some day become unimplemented. ^rw144342983comment

Highlighted: 02/11/2021 10:27 AM
Updated: 02/11/2021 10:28 AM


#### Extras:
the right new way to launch is 
```
launchctl bootstrap
Usage: launchctl bootstrap <domain-target> [service-path, service-path2, ...]
```

What is the right way to load a service with launchctl? #flashcard 
With the command launchctl bootstrap. load and unload are deprecated
<!--ID: 1614665312060-->





------

