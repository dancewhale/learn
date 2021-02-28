字符转义
代码如下:
num=$(cat file.txt | head -n 1 |wc -w)

for ((i=1; i<=num; i++))
do
    awk -v num=$i  '{print $num}'  file.txt | xargs
done

bash的Compound Commands


awk 'pattern {action}'
