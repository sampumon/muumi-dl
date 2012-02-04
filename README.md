MUUMI-DL
========

Automatically download stuff from YLE Areena¹.

Downloads the latest episode from given shows. Run daily (or more often) to get all episodes.

¹ http://areena.yle.fi/

## Instructions

1. Install [yle-dl](http://users.tkk.fi/~aajanki/rtmpdump-yle/).
2. Put stuff into `muumi-dl.list`.
3. Run `muumi-dl`!

## Running muumi-dl daily

Use cron or launchd.

### Linux / cron

1. `export EDITOR=nano`
2. `crontab -e`
3. add line: `@daily ~/scripts/muumi-dl`

### OS X / launchd

1. Copy `fi.sampumon.muumi-dl.plist` into `~/Library/LaunchAgents/`.
2. Modify `ProgramArguments` path in plist to where you installed muumi-dl. Note that you can't use `~`.
3. Add to launchd: `launchctl load ~/Library/LaunchAgents/fi.sampumon.muumi-dl.plist` (or reboot).
