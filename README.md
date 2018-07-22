# Hadoop

I. About
After the invention and later advancements made in web during 90's most of the companies adopted it by integrating
it into their business processes and infrastructure. 

It seemed that web could be used as:
i. A channel to reach out customers located in any part of the world and there by expanding their business. 
ii. Streamline and automate most of the existing manual processes and workflows 
in order to increase business value by
a. Reducing operational costs and increase benefits.
b. Reducing amount of paper work and management.
c. Reduce turn-around time to have happy customers.
d. Reachability to any part of the world through global business presence.

But over a decade:
a. Number of users and transactions on web have increased so much that they
are generating more and more data on a daily basis and will continue to do so
for the coming years. Increase in Volume is causing challenges to storage, processing
and visualization there by an increase in total costs.
b. Format has varied over a period of time ranging from images, videos, text files,
XML, Excel docs, word doc, PDF etc. Initially data was structured based on a set
of entities and databases played a huge role w.r.t storage and processing the data 
but today the format of data is mostly unstructured and it accounts for 90% of the data,
which the databases can neither capture into a schema nor scale it to store and process it.
Variation in format is causing challenges in storage and processing there by increase in total costs.

For example:
a. New York Stock Exchange generates about one terabyte of new trade data per day.
b. Facebook hosts approximately 10 billion photos, taking up one petabyte of storage.

So there’s a lot of data out there and you are probably wondering how it affects you. 
Success in the future will be dictated to a large extent by the ability to extract 
value from past data. Based on the past trends, managements can have a clear approach 
and idea as to how the business has been doing and how it could be improved based 
on which they can forecast and set goals for future, which will help in taking decisions, 
improve productivity, gain competitive advantage, 
Be more efficient and profitable => Increase financial value.

Ever increasing:
a.	Volume: Transactions, Social Media, Sensors, Web logs, Forum Comments, GPS output.
b.	Variety: Structured, Unstructured.
c.	Velocity:  How fast data is produced. How fast it must be processed to meet demand.
d.	Speed
e.	Scale
f.	Integration
g.	Analysis
h.	Visualization


                    ===========================================

II.
Data set size is beyond ability of commonly used software tools to capture,manage and process within a tolerable 
elapsed time.

Performance: It's all about doing one thing. Faster.
Scalability: It's all about doing the same one thing. In a bigger way.
Performance is about how fast. Scalability is about how much. 

Moore's Law: Number of transistors that can be inexpensively placed on an integrated 
circuit is increasing exponentially.

Though storage capacities have increased but still the access speeds i.e, rate at which data 
can be read from drives have not kept up.

And with the fast pace of computer hardware design, it seems inevitable that single-chip hardware will be 
able to "grow up" to handle the larger volumes of data. 
After all, Moore's Law (named after Gordon Moore, the founder of Intel) 
states that the number of transistors that can be placed in a processor will double approximately every 
two years, for half the cost. But trends in chip design are changing to face new realities. While we can 
still double the number of transistors per unit area at this pace, this does not necessarily result in 
faster single-threaded performance. New processors such as Intel Core 2 and Itanium 2 architectures now 
focus on embedding many smaller CPUs or "cores" onto the same physical device. This allows multiple threads 
to process twice as much data in parallel, but at the same speed at which they operated previously.
Even if hundreds or thousands of CPU cores are placed on a single machine, it would not be possible to 
deliver input data to these cores fast enough for processing. Individual hard drives can only sustain 
read speeds between 60-100 MB/second.

                    ===========================================

III.
Open-source, Java-based framework supporting parallel processing of large unstructured 
data sets in a distributed computing environment.

Two Components: Distributed storage and Distributed parallel processsing (MapReduce).

a. Popular option to process, store and analyze huge volumes of 
semi-structured, unstructured or raw data that often comes from disparate data sources.
b. Distributed parallel processing of huge amounts of data across inexpensive, industry-standard 
servers that both store and process the data, and can scale without limits.
c. Large data sets (100's of TB in a single job) and provides HDFS that provides reliable scalable 
store to 1000's of nodes and PB of data.
d. Master/slave architecture for both distributed storage and distributed computation. The 
distributed storage system is called the Hadoop File System, or HDFS.

Why not Grid Computing ?..
Map Reduce tries to collocate the data with the compute node, 
which is not offered by Grid computing model where nodes share data of a 
file system which could cause performance issues during network transfer.
Grids tend to be more loosely coupled, heterogeneous, and geographically dispersed.

Not an RDBMS Killer: Complement, not eliminate Relational databases.
Runs on cheaper commodity hardware and storage than RDBM’s.
Full file-store, without any referential integrity.
Data written once, read many times in large chunks instead of single records.
Analytical workloads not for Transaction processing.

Structured data is data organized into entities that have a defined format, such as XML documents 
or database tables that conform to a particular predefined schema is the realm of the RDBMS.

Unstructured data does not have any particular internal structure such as plain text or image data
for which RDBMS is not a good choice. MapReduce works well on unstructured or semistructured
data, since it is designed to interpret the data at processing time.

Not a Data warehouse: ELT not ETL.
DW’s host big structured, integrated data. Perform analysis using BI tools. 
Hadoop excels in handling raw, unstructured & complex data with vast prog. flexibility.

                              =========================================== 
IV.
Hadoop started out as a subproject of Nutch, which was a subproject of Apache Lucene. 
Lucene is a full-featured text indexing and searching library, targeted at indexing millions of documents.

Reason behind Nutch project was to build a web search engine from scratch which can 
handle indexing billions of web pages without becoming exorbitantly expensive to operate.
Nutch needs a layer to handle distributed processing, redundancy, automatic failover, and load balancing.

Around 2004, Google published two papers describing the Google File System (GFS) and the 
MapReduce framework . Google claimed to use these two technologies for scaling its own search system.

In 2004, they set about writing an open source implementation which immediately boosted 
Nutch’s scalability. It started to handle several hundred million web pages and could run on clusters 
of dozens of nodes.

Doug realized that a dedicated project to flesh out the two technologies was needed to get to web scale, and 
Hadoop was born. 

Yahoo! hired Doug in January 2006 and provided a dedicated team and the resources to turn Hadoop into 
a system that ran at web scale.

In January 2008, Hadoop was made its own top-level project at Apache, confirming its success 
and its diverse, active community.

                                  =========================================== 

V. 

Filesystem designed for large-scale distributed data processing to store tera bytes/ peta bytes of data.
Fault tolerance is handled by usage of replication.


Name Node:
----------
Name Node is the master of HDFS that is responsible to maintain file system namespace, metadata.
It directs the slave Data Node daemons to perform the 
low-level I/O tasks. The Name Node is the bookkeeper of HDFS; it keeps track of how your 
files are broken down into file blocks, which nodes store those blocks, and the overall health of the 
distributed file system. The function of the NameNode is memory and I/O intensive. 

Data Node:
-----------
Data Node daemon performs reading and writing HDFS blocks to actual files on the local file system. 
When data has to be read or written, file is broken into blocks and the Name Node will tell 
your client which Data Node each block resides in. Your client communicates directly with the Data 
Node daemons to process the local files corresponding to the blocks.  Data Nodes are constantly 
reporting to the Name Node. 
Upon initialization, each of the Data Node informs the Name Node of 
the blocks it’s currently storing. After this mapping is complete, the Data Nodes continually poll 
the Name Node to provide information regarding local changes as well as receive instructions to create, 
move, or delete blocks from the local disk.

Secondary Name Node:
--------------------
The Secondary Name Node (SNN) is an assistant daemon for monitoring the state of the cluster HDFS. 
Doesn’t receive or record any real-time changes to HDFS. Communicates with the Name Node to 
take snapshots of the HDFS metadata at intervals defined by the cluster configuration. 

                                         ===========================================

VI.
Distributed data processing model and execution environment running on large clusters 
of commodity machines in parallel.

Batch-based, distributed computing framework which allows to parallelize work over a large amount of raw 
data, which could take days or longer using conventional serial programming techniques, 
can be reduced down to minutes using MapReduce on a Hadoop cluster. 

Abstracting away the complexities involved in working with distributed systems, 
such as computational parallelization, work distribution, and dealing with unreliable hardware and software. 

MapReduce allows the programmer to focus on addressing business needs, rather than getting 
tangled up in distributed system complications.

Data locality: Map Reduce tries to collocate the data with the compute node, 
which is not offered by Grid computing model where nodes share data of a file system which could cause 
performance issues during network transfer. Shared-nothing architecture, meaning that tasks have no 
dependence on one other.

Map Reduce working:
--------------------
a. Client asks the jobtracker for a new job ID and submits the job.
b. Job tracker checks the output specification of the job. 
c. Computes the input splits for the job.
c. Copies the resources needed to run the job, including the job JAR file, the configuration
file, and the computed input splits, to the jobtracker’s filesystem in a directory named after the job ID.
d. Job tracker puts the job into an internal queue from where the job scheduler will pick it up and initialize it.
e.To create the list of tasks to run, the job scheduler first retrieves the input splits computed
by the client from the shared filesystem.
f. Tries to determine the Task trackers which are very nearer to data and they have fixed number of slots 
for map tasks and for reduce tasks.
g. Task tracker localizes the job JAR by copying it from the shared filesystem to the tasktracker’s
filesystem and any files needed from the distributed cache by the application to the local disk.
h. TaskRunner launches a new JVM to run each task, so that any bugs in the user-defined map and reduce 
functions don’t affect the tasktracker. It is, however, possible to reuse the JVM between tasks.
i. To choose a reduce task, the jobtracker simply takes the next in its list of yet-to-be-run
reduce tasks, since there are no data locality considerations.

Map Reduce execution:
--------------------
MapReduce program processes data by manipulating (key/value) pairs in the general form 
map: (K1,V1) ➞ list(K2,V2)
reduce: (K2,list(V2)) ➞ list(K3,V3)

1.The input to application must be structured as a list of (key/value) pairs , list(<k1, v1>). 
2.The list of (key/value) pairs is broken up and each individual (key/value) pair, <k1, v1>, is processed 
by calling the map function of the mapper. 
3 The output of all the mappers are (conceptually) aggregated into one giant list of <k2, v2> pairs. 
All pairs sharing  the same k2 are grouped together into a new (key/value) pair, <k2, list(v2)>. 
4. The framework asks the reducer to process each one of these aggregated (key/value) pairs individually. 



Combiner:
To activate a combiner, users should provide a mapper, a reducer, and a combiner as input to 
the MapReduce job. In that setting, Hadoop executes the combiner in the same node as the mapper 
function just after running the mapper. With this method, the combiner can pre-process the data 
generated by the mapper before.


Shuffle:
MapReduce makes the guarantee that the input to every reducer is sorted by key. The process by 
which the system performs the sort—and transfers the map outputs to the reducers as inputs—is known as the shuffle.


VII.
Usage of Hadoop in an enterprise:
-----------------------------------
a. Process data extracted from data warehouse/ database - Sqoop.

b. Pushing log files into Hadoop - Flume, Chukwa, Scribe
Log data has long been prevalent across all applications, but with Hadoop 
came the ability to process the large volumes of log data produced by production systems. Various
systems produce log data, from network devices and operating systems to web servers
and applications. These log files all offer the potential for valuable insights into how systems
and applications operate as well as how they’re used.

c. Pushing and pulling semistructured and binary files from Remote servers- File Slurper

d. Schedule regular ingress activities - Oozie
If your data is sitting on a filesystem, web server, or any other system accessible from
your Hadoop cluster, you’ll need a way to periodically pull that data into Hadoop.

e. Creation of automatic, redundant backups.




 







