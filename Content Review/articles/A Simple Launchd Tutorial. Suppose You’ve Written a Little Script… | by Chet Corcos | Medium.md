Notes for A Simple Launchd Tutorial. Suppose You’ve Written a Little Script… | by Chet Corcos | Medium

## Source:
Author: Chet Corcos
Category: articles
Updated: 02/11/2021 10:21 AM
Highlights URL: https://readwise.io/bookreview/7675963
SourceUrl: https://medium.com/@chetcorcos/a-simple-launchd-tutorial-9fecfcf2dbb3

%%7675963topstart%%
#### Extras:
**launchd****launchctl****launchagent****Chet Corcos**
%%7675963topend%%
 
-----
 ## Highlights:

### A plist file is just Apple’s custom XML format for configura...
>A plist file is just Apple’s custom XML format for configurations. Paste this code in there ^rw144339259hl

Comment: Includes a good example of a simple plist file ^rw144339259comment

Highlighted: 02/11/2021 10:21 AM
Updated: 02/11/2021 10:21 AM

%%144339259start%%
#### Extras:
Writing to a log file means console.log and then setting the standard output and error paths

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
  <dict>
    <key>Label</key>
    <string>com.demo.daemon.plist</string>
    <key>RunAtLoad</key>
    <true/>
    <key>StartInterval</key>
    <integer>20</integer>
    <key>StandardErrorPath</key>
    <string>/Users/chet/demo/stderr.log</string>
    <key>StandardOutPath</key>
    <string>/Users/chet/demo/stdout.log</string>
    <key>EnvironmentVariables</key>
    <dict>
      <key>PATH</key>
      <string><!\[CDATA\[/usr/local/bin:/usr/local/sbin:/usr/bin:/bin:/usr/sbin:/sbin\]\]></string>
    </dict>
    <key>WorkingDirectory</key>
    <string>/Users/chet/demo</string>
    <key>ProgramArguments</key>
    <array>
      <string>/usr/local/bin/node</string>
      <string>main.js</string>
    </array>
  </dict>
</plist>

```

%%144339259end%%

------

