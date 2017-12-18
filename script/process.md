# Process kill
```shell
ps aux | grep -i "process name" | awk {'print $2'} | xargs kill -9
```
