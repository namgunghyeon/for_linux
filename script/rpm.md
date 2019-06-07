# RPM
- Redhat Package Manager

## Install package
```
rpm -ivh
```
- -i `install`
- v `자세한 정보 출력`
- h `설치 진행 상황을 # 문자를 이용하여 출력한다.`

## Remove package
```
rpm -e pakcage name
```

## Find installed package
```
rpm -qa | grep -e 'pckage'
```