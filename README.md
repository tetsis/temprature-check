# temprature-check
サーバの温度を計るLinuxツール
crontab等を用いることで定期的な温度監視が可能

## 使い方
### 手動で実行
```
# ./temprature-check (ディスクのパス)
(例)
# ./temprature-check /dev/sda
```

### crontabで実行
```
# echo "(実行したい時間) root (temprature-checkがあるディレクトリパス)/temprature-check (ディスクのパス) > /dev/null 2>&1" >> /etc/crontab
(例)
# echo "  0  *  *  *  * root /root/temprature-check/temprature-check /dev/sda > /dev/null 2>&1" >> /etc/crontab
```
