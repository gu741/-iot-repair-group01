# 实际测试记录

语言与版本：Java

测试人员GitHub用户名：gu741

运行命令：
```text
cd src/java
javac StatusRule.java StatusRuleTest.java
java StatusRuleTest
编号	当前状态	目标状态	预期	实际	结论
T01	PENDING	  PROCESSING	true	true	PASS
T02	PROCESSING	COMPLETED	true	true	PASS
T03	PENDING	COMPLETED	false	false	PASS
T04	COMPLETED	  PROCESSING	false	false	PASS

原始输出
text
T01 PASS: PENDING -> PROCESSING, expected=true, actual=true
T02 PASS: PROCESSING -> COMPLETED, expected=true, actual=true
T03 PASS: PENDING -> COMPLETED, expected=false, actual=false
T04 PASS: COMPLETED -> PROCESSING, expected=false, actual=false
Summary: 4/4 passed
测试范围
本次规定4项测试，其他状态组合是否额外执行：未额外执行。
从个人分支下载ZIP复测情况：结果符合预期。
