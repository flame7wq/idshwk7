# Method One
## 隐藏过程
`copy /b lib.jpg+hiddeninfo.txt 1.jpg`

windows下在cmd中使用copy命令合并文件，将文本文件以二进制的形式合并到图像中

`copy /b lib.jpg+hiddeninfo.zip lib_info.jpg`

先压缩文本文档再合并

## 提取过程
* 使用 Winhex 或 Notepad++ 打开图片 可在文件末尾看到隐藏信息
* 也可以使用 binwalk 工具

*提取结果见图片 result.jpg*

# Method Two
（详见图片 steghide_method.jpg）
## 影藏过程
steghide embed -cf lib_sec.jpg -ef hiddeninfo.txt

*passphrase：57117217*

## 提取过程
steghide extract -sf lib_sec.jpg

# Method Three（DCT变换域图像隐藏，待时间充裕加以补充）

