**insert into select**:

	Insert into Table2(field1,field2,...) select value1,value2,... from Table1
	# The Table2 must be exists.


**select into**:

	SELECT vale1, value2 into Table2 from Table1
	# 要求目标表Table2不存在，因为在插入时会自动创建表Table2，并将Table1中指定字段数据复制到Table2中


ref: http://www.cnblogs.com/freshman0216/archive/2008/08/15/1268316.html

