MUUMI-DL
========

Automatically download stuff from [YLE Areena][areena].

Downloads the latest episode of given shows. Run daily (or more often) to get all episodes.

## Instructions

1. Install [yle-dl]. On OS X you can install via [homebrew].
2. Put Areena search/program URLs into `muumi-dl.list`.
3. Run `muumi-dl`. Note that yle-dl output goes into log file.

## Running muumi-dl daily

Use cron or launchd.

### Linux / cron

1. `export EDITOR=nano`.
2. `crontab -e`.
3. Add line: `@daily ~/scripts/muumi-dl`.
4. Now muumi-dl runs daily at midnight.

### OS X / launchd

1. Copy `fi.sampumon.muumi-dl.plist` into `~/Library/LaunchAgents/`.
2. Modify `ProgramArguments` path in plist to where you installed muumi-dl. Note that you can't use `~`.
3. Add to launchd: `launchctl load ~/Library/LaunchAgents/fi.sampumon.muumi-dl.plist` (or reboot).
4. Now muumi-dl runs daily at noon. Start manually anytime: `launchctl start fi.sampumon.muumi-dl`.

[areena]:http://areena.yle.fi/
[yle-dl]:http://users.tkk.fi/~aajanki/rtmpdump-yle/
[homebrew]:http://github.com/sampumon/homebrew
