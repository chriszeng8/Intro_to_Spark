##LEC 3
Notes taken from edX: Introduction to Spark from BerkeleyX
Chris Zeng
Jun, 2015

####Memory vs Disk
Using memory instead of disks offers two huge benefits. 

1. The first benefit is that **memory is much faster than disks**. The time to read or write a value to memory is only a few nanoseconds, while the time to read or write is several milliseconds - that means memory is a million times faster than disks. 
2. The second benefit is that keeping intermediate results in memory means that they **do not have to be converted into a format that can be stored on disks**. The process of converting a memory object to a disk object is called **serialization** and the process of converting a disk object to a memory object is called **deserialization**. Serializing and deserializing objects is a very expensive and time consuming process. Keeping intermediate results in memory avoids this significant overhead. 

Taken together, the faster access times and avoidance of serialization/deserialization overhead make Spark much faster than Map Reduce - up to 100 times faster!

####Spark Computing Framework (RDD)
Users give Spark instructions, then they do not need to worry about
1. do not need to worry about **where it runs**
2. do not need to worry about **slow nodes or failed nodes**, Spark will automatically run multiple times to guarantee correct results.

Four Components
``SQL`` ``Spark Streaming`` ``MLib(Machine Learning)`` ``GraphX``
and 
``                    Apache Spark (Core)              ``

####Resilient Distributed Datasets (RDD)
What is RDD?



####References
* 1956-1979: Stanford, MIT, CMU, and other universities develop set/list operations in LISP, Prolog, and other languages for parallel processing (see [http://www-formal.stanford.edu/jmc/history/lisp/lisp.html](http://www-formal.stanford.edu/jmc/history/lisp/lisp.html))

* Circa 2004: [Google: MapReduce: Simplified Data Processing on Large Clusters](http://research.google.com/archive/mapreduce.html) by Jeffrey Dean and Sanjay Ghemawat.

* Circa 2006: Apache Hadoop, originating from the Yahoo!’s Nutch Project Doug Cutting

* Circa 2008: Yahoo! web scale search indexing - Hadoop Summit, Hadoop User Group

* Circa 2009: Cloud computing with Amazon Web Services Elastic MapReduce (AWS EMR), a Hadoop version modified for Amazon Elastic Cloud Computing (EC2) and Amazon Simple Storage System (S3), including support for Apache Hive and Pig.

