目标：
基于Hibernate，构建一套声明式的API，类似于Ebean。

如：
Member member =
	Repository.find(Member.class)
	.select("id,name, age, createTime")
	.where()
	.eq("name", "kaiba")
	.one();

List<Member> members =
	Repository.find(Member.class)
	.select("id,name, age, createTime")
	.where()
	.eq("age", 18)
	.like("name", "Rob%")
	.orderBy("createTime desc");
	.list();