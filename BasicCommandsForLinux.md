# BasicLinux
## 文件和目录列表
查看当前路径
```shell
pwd
```
进入文件
```shell
cd filename
```
查找csv结尾的文件
```shell
ls -l *.csv
ls -l my_sr[ai]pt
ls -l my_sr[a-i]pt
```
创建空文件（修改时间、不修改内容）
```shell
touch test
```
复制文件（-R复制文件夹内容）
```shell
cp src dst
cp -i src dst #(overwrite)
cp -R test_one/ test_three
```
文件重命名
```shell
mv test_one test
```
文件删除
```shell
rm -i test
```
创建目录
```shell
mkdir test
```
删除空目录
```shell
rmdir test
```
删除目录下所有内容
```shell
rm -rf test
```
查看文件类型
```shell
file my_file
```
查看文件内容
```shell
cat my_file
cat -n my_file # 带行数
```
查看尾部内容
```shell
tail my_file
```
查看头部内容
```shell
head -5 my_file
```

## 监测程序
探查进程

a:显示所有程序 

u:以用户为主的格式来显示 

x:显示所有程序，不以终端机来区分
```shell
ps
ps -a
ps -aux|grep python
```
关闭进程
```shell
kill pid
```
查看磁盘空间
```shell
df
```
查看大文件
```shell
du -h # 显示文件大小
du -c # 显示文件总大小
```
搜索数据
```shell
grep pattern file
grep -c pattern file # 计数
```
压缩文件
```shell
gzip my* # 批量压缩
zip -r dir.zip dir
```
查看历史命令
```shell
history
```
数组变量
```shell
$ myset=(one two three)
$ echo $myset
one
$ echo $myset[1]
one[1]
$ echo ${myset[1]}
two
$ echo ${myset[*]}
one two three
unset myset[1] # 删除元素
```
查看变量内容
```shell
echo $variable
```
vim编辑器
```shell
:s/old/new/ # 替换一个单词
:s/old/new/g # 替换所有old
:n,ms/old/new/g # 替换n行和m行之间的单词
:%s/old/new/g # 替换所有old
```
查看GPU使用情况
```shell
nvidia-smi
```
后台运行程序
```shell
nohup xxx &
```
关闭程序
```shell
kill -9 PID # PID通过ps -a查看
```
防火墙
```shell
firewall-cmd --zone=public --add-port=8888/tcp --permanent  # 打开端口
firewall-cmd --reload  # 重新加载生效
firewall-cmd --zone=public --list-ports  # 查看打开端口
systemctl start firewalld
systemctl stop firewalld
```
