# systemctl
- init(System V Init)를 대체하는 역할
- 부팅, 자원 관리, 데몬 로깅 등 centos7부터 탑재
- 서비스가 죽어도 자동으로 재시작
## systemctl list
```
$ systemctl
  UNIT                                                          LOAD   ACTIVE SUB       DESCRIPTION
  proc-sys-fs-binfmt_misc.automount                             loaded active waiting   Arbitrary Executable File Formats File System Automount Point
  sys-devices-platform-serial8250-tty-ttyS1.device              loaded active plugged   /sys/devices/platform/serial8250/tty/ttyS1
  sys-devices-platform-serial8250-tty-ttyS2.device              loaded active plugged   /sys/devices/platform/serial8250/tty/ttyS2
  sys-devices-platform-serial8250-tty-ttyS3.device              loaded active plugged   /sys/devices/platform/serial8250/tty/ttyS3
```

## systemctl register
```
vi /etc/systemd/system/<service name>.service

[Service]
Type=simple
ExecStart=<start file>
Restart=always
StandardOutput=syslog
StandardError=syslog
SyslogIdentifier=<service name>
User=<user>

[Install]
WantedBy=multi-user.target

systemctl deamon-reload
systemctl enabled <service name>
```

## systemctl command
```
systemctl enabled <service name>: 부팅시 활성화
systemctl start <service name>: 시작
systemctl restart <service name>: 재시작
systemctl status <service name>: 상태
systemctl stop <service name>: 정지
systemctl disable <service name>: 사용하지 않음
systemctl systemd-analyze <service name>: 분석
```

## systemctl config
[service](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/sect-managing_services_with_systemd-unit_files)
[systemctl](https://www.loggly.com/ultimate-guide/linux-logging-with-systemd/)


## systemctl log
```
$ journalctl --since yesterday: 어제부터 전체 로그 확인
$ journalctl -f -u  <service name>: 실시간 마지막 로그 확인
```

## systemctl log size
```
$ journalctl --disk-usage
Archived and active journals take up 6.1M on disk.
```