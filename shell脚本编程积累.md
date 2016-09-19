##日常编程问题记录

1. 对于 if 条件判断语句的编写必须要注意后面方括号里面，左括号后面和右括号前面都必须要有空格；
2. 判断字符串是否相等直接使用 = ，而判断数值是否相等利用 -eq, -lt, -gt, -le, -ge；
3. 字符串替换可以使用 sed 命令，它的用法为： `sed "s/str1/str2/g"` 这句话的意思是将 str1 用 str2 替换掉；同时要注意如果在 str2 中包含字符 '/' 就有可能会替换不正确，需要进行预处理
4. 取子串的方式为：
  
|表达式 | 含义  | 
|---|---|
| ${#str} | 得到字符串长度 |
| ${str:position} | 在字符串 $str 中，从 position 位置开始的子串|
| ${str:position:length | 字符串 $str 中，从 position 位置开始，长度为 length 的子串|
| ${str#substring} | 在 str 中，删除最短匹配 $substring 的子串，当写两个 # 号时就表示最长字串|
| ${str%substring} | 从变量 $str 的结尾，删除最短匹配 $substring 的子串 |
| ${str/substring/replacement}| 使用 $replacement 来代替第一个匹配的 $substring|
| ${str//substring/replacement}| 使用 $replacement 来代替所有匹配的 $substring|
  
5. 圆括号 () 表示的含义有：1）命令组。括号中的命令将会新开一个子 shell 顺序执行，所以括号中的变量不能被就脚本余下的部分使用。括号中多个命令之间用分号隔开，最后一个命令可以没有分号，各命令与括号之间不必有空格。2）命令替换。等同于cmd，shell扫描一遍命令行。
6. 方括号 []，bash 内部命令，等同于 test。通常用来判断括号里面的条件正确与否。
