# BatchEditTracker
批量修改qbittorrent、transmission tracker工具

# winForm版
群友shabby提供，**hdtime**种子authkey转passkey专用, 窗口程序，只需填写相关参数即可

QbTrackerUtil —— qbitorrent 

TrTrackerUtil —— transmission

注意：不要输入中文！WIN版为**hdtime**专用

# LM-BatchEditTracker-go
LM-BatchEditTracker-go  命令行工具

支持qbitorrent4+ transmission3+ transmission4+ 其他版本未做测试，可自行尝试

支持所有tracker服务器修改，包括但不限于hdtime等

## 运行：
### TR:
./LM-BatchEditTracker-go-linux-amd64 -client=tr -addr=127.0.0.1 -username=admin -password=admin -category=hdtime -old=https://tracker.hdtime.org/ -new=https://tracker.hdtime.org/announce.php?passkey=********
### QB:
./LM-BatchEditTracker-go-linux-amd64 -client=qb -addr=http://127.0.0.1:8080 -username=admin -password=admin -category=hdtime -old=https://tracker.hdtime.org/announce.php -new=https://tracker.hdtime.org/announce.php?passkey=********

## 参数说明：
-client 客户端类型，仅支持tr、qb

-addr 地址 tr仅支持默认9091端口,填写ip即可  qb填写全路径如：http://127.0.0.1:8080 不支持https,同时请关闭webui设置中所有安全中选项

-username web端登录帐号

-password web端登录密码

-category 客户端分类名,仅qb有效

-old 旧tracker服务器,填写网站地址即可,如:https://tracker.hdtime.org/

-new 新tracker地址,如：https://tracker.hdtime.org/announce.php?passkey=********
