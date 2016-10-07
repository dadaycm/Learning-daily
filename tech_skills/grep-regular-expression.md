# Known issues
## Greedy & lazy *?   +?


# Done:
 ^\s*#     comment; before #, there is 0 or many spaces


 ^\s+#     comment; before #, there is at least one space or more spaces

 e-?mail   email or e-mail.   ? means 0/1

 \.(jpg|gif|png)$       :   a picture file
 ^/([^/]+)              :   a directory folder

?
*
+
\d  
\D
\s

.


## Head/Tail of line/whole string:
 * for each single line  ^ $    
 * for the whole string (multi-lines)  \A,  \z

[0-9] [a-z]
[^abc]       : single character which is not a, not b, not c.

# 反向引用/命名分组
()  Capture a group which can be backreferenced as  $1,  $2,... $9


## 模式字符串内部引用前面出现过的内容
```
s="13917000661"
patten=/(\d)\1/
patten =~ s

s="18606069707"
pattern = /(\d)\d\1/
pattern =~ s
p $1

```
## 模式字符串外表举例 Atom replace: swap two words
(\b\w+\b)\s+(\b\w+\b)
$2 $1

##  模式字符串外表举例  sample to parse mobile number:
 - input

+86 13917000661

+61 0490001677
 - solution

(.\d\d) (\d\d\d)(\d\d\d)(\d+)

($1) $2-$3-$4

 - result

(+86) 139-170-00661

(+61) 049-000-1677

```
patten = /(.\d\d)\s+(\d\d\d)(\d\d\d)(\d+)/
s="+61 0490001677"
patten =~ s
p $1
p $2
p $3
p $4
# NOT WORK!!!
p "($1) $2-$3-$4"
p '($1) $2-$3-$4'



```
