in:

	select * from group_info gi 
	where gi.contact_count <> gi.member_count 
	and gi.group_id not in (select group_id from unreg_info group by group_id);

join:

	select * from group_info gi 
	left join unreg_info ui on ui.group_id=gi.group_id
	where gi.contact_count <> gi.member_count and ui.group_id is null;


`join` is faster than `in`, `join` Vs 'in', winner is `join`.

**`join`相对于`in`的使用，mysql不用在内存中创建临时表来处理,特别是当`group_id`是外键的时候会更快些。**

