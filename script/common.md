# Date
```shell
echo $(date);
```

## format
```shell
echo $(date +"%Y-%m-%d %H:%M:%S");
```

### UTC
```shell
echo $(date -u +"%Y-%m-%d %H:%M:%S");
```

### 날짜앞에 0제거
```shell
echo $(date +"%m") | sed "s/^0*//g; s/\.0*/./g";
```

# If
```shell
if [ ! -d "test" ]
then
mkdir -p "test"
fi
```

# find
```shell
grep -rnw <path> -e pattern
```

# for
```shell
for i in {1..10000}; do
  sleep 1
done
```

# symbolic link
```
ln -s 원본 링크파일
```

# loop
## date range
```shell
start=2015-01-01
end=2015-02-20

while [ ${start} != ${end} ]; do
  echo $start
  start=$(date --date="${start} + 1 day" +"%Y-%m-%d")
done
```
