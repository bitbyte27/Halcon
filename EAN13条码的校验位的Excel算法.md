## EAN13条码的校验位的Excel算法

<pre name="code" class="Excel">
校验位原公式：
单元格=10-RIGHT(SUM(MID($B3,{1;2;3;4;5;6;7;8;9;10;11;12},1)*{1;3;1;3;1;3;1;3;1;3;1;3}))
</pre>

<pre name="code" class="Excel">
简化公式：
单元格=10-RIGHT(SUM(MID($B3,{0,1}+{1;3;5;7;9;11},1)*{1,3}))
</pre>

<pre name="code" class="Excel">
最简公式：
单元格=RIGHT(SUM(LEFT($B3,{0,1}+{1;3;5;7;9;11})*{9,7}))
</pre>

> [EAN13条码的校验位的Excel算法](https://blog.csdn.net/bitezijie/article/details/24318969)
