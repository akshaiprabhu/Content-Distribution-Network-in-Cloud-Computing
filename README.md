# Content-Distribution-Network-in-Cloud-Computing
An application to exchange files between peers located across the world, implemented using Amazon Web Services (AWS) with features for proximity based file search, version control and caching, load balancing across servers and fail safe mechanisms

Files:

 There are three major java files namely MainServer, EdgeServer and Client.

 We did setup up our whole server system in AWS using S3 and EC2 instances whereas it

can also be run on normal systems.

 If it has to be run on normal systems the ip’s in all the three files should be changed.

 Moreover, there are three East and three West servers and their location must be far

away to demonstrate the proximity better.

 The SplitFile and JoinFile java files are for splitting and joining a large file respectively.

MainServer should have the SplitFile and Client should have the JoinFile.

 GetLocation java file is used by the client to find its location (latitude and longitude)

using Google API.

Steps to run:

o Compile all the java files.

o Run the EdgeServers first.

o Run the MainServer. Once MainServer is started it checks for any files in its “local\” drive and send it to the edge servers. If the file size is greater than the threshold value (30 MB), then it is split by 3 and sent to EdgeServers part wise.

o Run the Client from any location and request for any file.

o Any kind of files can be sent from server to client.
