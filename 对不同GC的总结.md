## 对不同GC的总结


###Serial GC
####语法：
`
-Xmx512m -Xms512m -PrintGCDetails -XX:+UseSerialGC
`

串行GC共计回收16次，其中年轻代回收9次，FullGC回收7次，平均回收时长38.1ms,FullGC
最长用时70ms，最短用时30ms
----

###Parallel GC
####语法：
`
-Xmx512m -Xms512m -PrintGCDetails -XX:+UseParallelGC
`
并行GC共计回收32次，其中年轻代回收23次，FullGC回收9次，平均回收时长18.7ms,FullGC
最长用时60ms，最短用时30ms
----
###CMS GC
####语法：
`
-Xmx512m -Xms512m -PrintGCDetails -XX:+UseConcMarkSweepGC
`
并行GC共计回收18次，其中年轻代回收15次，FullGC回收5次。年轻代平均回收时长27.33ms,
年轻代GC最短用时0ms,最长用时90ms。FullGC平均用时50ms, 最长用时70ms，最短用时40ms
----
###G1 GC
####语法：
`
-Xmx512m -Xms512m -PrintGCDetails -XX:+UseG1GC
`
并行GC共计回收18次，其中年轻代回收15次，FullGC回收5次。年轻代平均回收时长27.33ms,
年轻代GC最短用时0ms,最长用时90ms。FullGC平均用时50ms, 最长用时70ms，最短用时40ms
----




