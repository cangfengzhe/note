
* 文件名作为文件内容的最后一列

```sh
for f in file1 file2 file3; do sed -i "s/$/\t$f/" $f; done
# 写入新文件
for f in file1 file2 file3; do sed "s/$/\t$f/" $f >> output.xls; done
```

* 并行

```sh
file_name=$1
count=0
while read a ;do
    count=$(($count+1))
    name=`basename $a`
    python hp_findv3.py --hpfile hotspot_seq.xls --fq $a --output_file output/${name}.output.xls &
    if [ $(($count%15)) -eq 0 ];then
        wait
    fi
done < $file_name
```

# 去除windows下的元字符 ^M

```sh
cat -A filename #就可以看到Windows下的断元字符 ^M
sed -i 's/^M//g' filename
#注意：^M的输入方式是 Ctrl + v ，然后Ctrl + M
```
