**Directory traversal exists in dedecms v5.7.87**


There is a vulnerability file:uploads/include/dialog/select_templets.php

The $activepath parameter is controllable, and there is a regular bypass.

![WPS图片(1)](https://user-images.githubusercontent.com/108608882/229717843-bb8d01a5-e32d-4705-adca-9d4052823d42.png)


The dir() function lists the directory, then the read() function loops through the contents of the directory.

![WPS图片(2)](https://user-images.githubusercontent.com/108608882/229718065-fae31d92-1ff0-4082-b686-34334b18812c.png)

By way of... \ Can bypass filtering to achieve directory traversal, resulting in directory traversal

![WPS图片(3)](https://user-images.githubusercontent.com/108608882/229718178-6cd43455-f57d-4342-99b2-20d97548f83e.png)
