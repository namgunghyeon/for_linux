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