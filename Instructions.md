# Flume_Streaming  
  
## Executions  
```code
flume-ng agent --name a1 --conf-file ~/flume_demo/example.conf
flume-ng agent --name wh --conf-file /home/cloudera/wslogstohdfs/wshdfs.conf
```
  
## Passing Inputs via Telnet    
```code
sudo yum install telnet
telnet localhost 7777
```
  
### Generating logs via /opt/gen_logs in CDH  
```code
# gen_logs directory was given in this repository. This is used to generate the logs.
[cloudera@quickstart gen_logs]$ cd /opt/gen_logs/

[cloudera@quickstart gen_logs]$ ls -ltr
total 24
-rwxr-xr-x 1 cloudera cloudera   51 Aug  1  2014 tail_logs.sh
drwxr-xr-x 2 cloudera cloudera 4096 Sep 25  2014 logs
drwxr-xr-x 2 cloudera cloudera 4096 Sep 25  2014 data
-rwxr-xr-x 1 cloudera cloudera   76 Oct  8  2014 start_logs.sh
-rwxr-xr-x 1 cloudera cloudera  131 May 14  2015 stop_logs.sh
drwxr-xr-x 2 cloudera cloudera 4096 Oct 23  2017 lib

[cloudera@quickstart gen_logs]$ ls -ltr data/
total 64
-rw-r--r-- 1 cloudera cloudera 55172 Sep 25  2014 products.json
-rw-r--r-- 1 cloudera cloudera   280 Sep 25  2014 departments.json
-rw-r--r-- 1 cloudera cloudera  2433 Sep 25  2014 categories.json

[cloudera@quickstart gen_logs]$ ls -ltr logs/
total 36
-rw-r--r-- 1 cloudera cloudera 32029 Sep 14 16:14 access.log
[cloudera@quickstart gen_logs]$ ls -ltr lib/
total 8
-rwxrwxr-x 1 cloudera cloudera 6179 Oct 21  2014 genhttplogs.py

[cloudera@quickstart gen_logs]$./start_logs.sh
[cloudera@quickstart gen_logs]$./stop_logs.sh
```
