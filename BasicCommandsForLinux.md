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




