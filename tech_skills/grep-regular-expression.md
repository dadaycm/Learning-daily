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
 ^ $
[0-9] [a-z]
[^abc]       : single character which is not a, not b, not c.
()  Capture a group which can be backreferenced as  $1,  $2,... $9

##  sample to parse mobile number:
 - input

+86 13917000661

+61 0490001677
 - solution

(.\d\d) (\d\d\d)(\d\d\d)(\d+)

($1) $2-$3-$4

 - result

(+86) 139-170-00661

(+61) 049-000-1677
