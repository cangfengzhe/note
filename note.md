** 工作笔记

*** CNV

1. 以下CNV可以验证

MET、EGFR、ERBB2、FGFR3、IDH1

2. 接头污染
查看 rawfq2sortbam log 文件，  Both Surviving 小于 90% 为接头污染严重

过滤软截断跑融合的命令：/biocluster/data/biobk/user_test/yangcan/date_test/fil.sh <nbam> <tbam> <outdir> <panel> <sample>

3. kill all
ps -ef|grep genedock|grep -v grep|cut -c 9-15|xargs kill -9

parent id
ps -ef|grep genedock|grep -v grep|cut -c 17-23|xargs kill -9
