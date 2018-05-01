## Linux find命令学习

find命令强大，但是选项较多，学习比较繁琐，占用内存消耗较大


### 命令展示

纷繁的选项

```markdown
按照名字搜索
find / -name install.log

find /root -name "install*"

find /root -name "*"


find /root -name "ab[cd]"


find /root -name "*[cd]"

find /root -iname install.log

find /root -user root

find /root -nouser

ll

按照属性时间筛选
find /root -nouser
没有所有者:内核产生的文件:/sys   /proc,外来文件(u盘)

find  /var/log -mtime +10   修改文件内容
find  /var/log -atime +10   访问文件时间
find  /var/log -ctime +10   改变文件属性

find  /var/log -ctime -10  十天内

find  /var/log -ctime 10  第十天

按照文件大小查找
ll -h 查看文件大小

find /etc -size 25k
find /etc -size +25k
find /etc -size 25k


find /etc -size +2M

find /root -size 25

find . -inum 262422


ls -i

find /root -inum 26241

find /etc -size +20k -a -size -50k

ls -lh /etc/mine.types

find /etc -size +20k -a -size -50k -exec ls -lh {} \;


find /root -inum 262421 -exec rm -rf {} \;




```
