# watch
주기적으로 커맨드 옵션을 실행할 수 있는 명령어

## Basic
```
$ watch -n <interval> <command>
$ watch -n <interval> -d <command>
```

## Options
```
-d differences
-n interval
```

## Examples
```
$ watch -n 0.5 -d df -h
Every 0.5s: df -h

Filesystem                                             Size   Used  Avail Capacity   iused               ifree %iused  Mounted on
/dev/disk1s1                                          477Gi  365Gi  109Gi    77%   5345593 9223372036849430214    0%   /
devfs                                                 193Ki  193Ki    0Bi   100%       666                   0  100%   /dev
/dev/disk1s4                                          477Gi  2.0Gi  109Gi     2%         1 9223372036854775806    0%   /private/var/vm
map -hosts                                              0Bi    0Bi    0Bi   100%         0                   0  100%   /net
map auto_home                                           0Bi    0Bi    0Bi   100%         0                   0  100%   /home
//namkunghyeon@namkunghyeon.local/home                3.5Ti  2.9Ti  573Gi    84% 786431951           150092561   84%   /Volumes/home
/dev/disk2s2                                          3.5Ti  2.9Ti  573Gi    84%  48813222          4246154057    1%   /Volumes/Time Machine
com.apple.TimeMachine.2018-08-28-215015@/dev/disk1s1  477Gi  364Gi  109Gi    77%   5345131 9223372036849430676    0%   /Volumes/com.apple.TimeMachine.localsnapshots/Backups.backupdb/mac88    iMac/2018-08-28-215015/Mac88
com.apple.TimeMachine.2018-07-20-234256@/dev/disk1s1  477Gi  342Gi  109Gi    76%   5154417 9223372036849621390    0%   /Volumes/com.apple.TimeMachine.localsnapshots/Backups.backupdb/mac88    iMac/2018-07-20-234256/Mac88
/Users/nkh/Downloads/Visual Studio Code 4.app         477Gi  365Gi  109Gi    77%   5345523 9223372036849430284    0%   /private/var/folders/my/nd3n5sn966jfg2ty2m7yv24h0000gn/T/AppTranslocation/0DFF336E-AF17-4B96-8975-7B7220297542
```