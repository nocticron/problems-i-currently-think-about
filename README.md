## Spark
1. Philosophically: why JVM. Why Scala (Java). Project Tungsten. Spark to Rust.
1. Philosophically: why bad Ops. Apache Ambari. Custom configuration and `start.sh` files. Lack of official Ansible/Puppet/Chef presets (templates) for different usecases (HDD/SSD/SDCard, CPU cache size, GPUs).
1. Tables' schema evolution: no batteries included, no best practices provided. Why no support of things like `alembic`/`liquibase` for migrations. Linkedin Dali.
1. Spark data lineage: easy (enough?) for Spark, because there's always a plan to dump (even for checkpoints). Why no native export to e.g. openmetadata.
1. No table-wide metadata for DF API? Only for columns but not shown in introduction doc.
1. Lack of methods like `DropTable`: people tend to use `spark.sql("DROP TABLE {}")` which leads to SQLi. `DropTableCommand(TableIdentidier(ParseSomething))` is a way, why buried deeply in javadoc. 
1. Same about Python management tasks go through `._jsession` proxy
1. Opaque memory model: fraction of a fraction of a fraction, no [kiddin](https://0x0fff.com/spark-memory-management/). 
1. Opaque computing model: partition count could be like HDFS blocks count, but sometimes not. No doc gradation: e.g. resource management for Junior/Middle/Senior specialists. 
1. Magic recipes like "keep partitions 128Mb" instead of good doc. Idea: browser tool: dial down your hardware config plus data shape, and we will tell you the estimate. Run the job couple of times, put the numbers from Spark UI and we will refine the numbers (cause we dont know your actual transformation code). Provide an execution plan for further refinement. Is this possible?
1. Terminology hell: Spark SQL, Hive SQL, Spark on Hive or Hive on Spark, Thrift-Hive-server?

### Further reading (TODO):
https://blog.octo.com/en/how-to-hack-spark-to-do-some-data-lineage/

https://docs.cloudera.com/runtime/7.2.10/atlas-reference/topics/atlas-spark-lineage.html

https://atlas.apache.org/

https://link.springer.com/article/10.1007/s13222-021-00387-7

https://engineeringblog.yelp.com/2022/08/spark-data-lineage.html

https://openlineage.io/blog/openlineage-spark/


### Goal

To develop a better understanding of Spark design decisions. To check if I am wrong or right about where bullets.

## Chinese CPUs
> "replace all foreign hardware and software from its public infrastructure with homegrown solutions" by 2023 (the so-called 3–5–2 policy)

1. make a chinese CPUs map, also TPUs, GPUs, RAM etc
1. overclocking!

### Futher reading: TODO
1. Hygon
1. Phytium
1. Zhaoxin
1. https://en.wikipedia.org/wiki/Semiconductor_industry_in_China