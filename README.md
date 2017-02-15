1)Cluster:
	In a computer system, a cluster is a group of servers and other resources that act like a single system and enable high availability and, in some cases, load balancing and parallel processing
Hadoop Cluster:
A Hadoop cluster is a special type of computational cluster designed specifically for storing and analyzing huge amounts of unstructured data in a distributed computing environment. 
Such clusters run Hadoop's open source distributed processing software on low-cost commodity computers. Typically one machine in the cluster is designated as the NameNode and another machine the as JobTracker; these are the masters. The rest of the machines in the cluster act as both DataNode and TaskTracker; these are the slaves. Hadoop clusters are often referred to as "shared nothing" systems because the only thing that is shared between nodes is the network that connects them. 

2)Rack:
		A rack is a collection of 30 or 40 nodes that are physically stored close together and are all connected to the same network switch. Network bandwidth between any two nodes in rack is greater than bandwidth between two nodes on different racks
Rack arrangement in Hadoop cluster:
	Usualy Hadoop clusters of more than 30-40 nodes are configured in multiple racks.Communication between two data nodes on the same rack is efficient than the same between two nodes on different racks.
In large clusters of Hadoop,in order to improve network traffic while reading/writing HDFS files,Namenode chooses data nodes which are on the same rack or a near by rack to read/write request.
Namenode achieves this rack information by maintaining rack ids of each data node. This concept of choosing closer data nodes based on racks information is called Rack awareness In hadoop

