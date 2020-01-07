# Distributed-Filesystem
PDS-Term-project

1.Abstract 

The aim of the project in this period is to develop a primitive distributed file system that encompasses the new technologies that fit today, and how basic concepts actually work, what challenges design, and finally how to overcome these challenges through implementation and process. 
 
2.Introduction 

In this project, students are assigned to make a distributed file system which contains three nodes in itself and be able to perform mkdir, rmdir, ls, touch, cat, rm etc. operations like a local file system using fusepy. Fusepy is a python library which allows to create a virtual file system in user space. Details of implementation and project development process will be detailed under sections below. 
 
3.Architecture 
 
In this project we started to project with the decision making of the architecture then after some search we found a project of one of our graduated student’s, which we used as a template, and then we decided to our architecture. Like the project we found on Github, we also used the same architecture in our file system. 
In this architecture, we have 3 server nodes and a client node. We tried to use FUSE to create virtual file systems and xinetd services to the communication between nodes. Because of the experience we gained from previous assignments we also choosed to use xinetd services to deal with the communication. 
 
4.Implementation

After the architecture decision, we started to work on implementation part. And we started to work on source codes which we find. But there was a problem which is FUSE python library has deprecated since 1 January 2020 for python 2.7. Then we changed the code to be able to execute using python 3.6 and use another library (python-fuse) which allows us to perform the same operations as the fusepy library at python3. Then we tried to combine all the xinetd python and configuration files, fuse python files which are specially developed for server side and client side but because of the problems of importing related libraries to our Ubuntu servers we couldn’t raise the system which performs as wanted in given project. We tried to use different libraries and 
also pip versions which allows us to import those libraries to our environment but couldn’t get any longer after those solutions. Because of our failure to raise the system, we can not insert the screenshots of the process of system working. But as we mentioned, xinetd services were ready for the system working mechanism. Xinetd service status and related configurations shown below: 
 
Our services were: 1- exists 2- get 3- getlist 4- getsize 5- mkdir 6- put 7- putf 8- rmall 
 
5.Conclusion 

In this project we build a simple network with distributed node systems and connect the client to the server on the same network using python's rpyc library. After connecting to rpyc, we design the file and folder system commands to execute on the server by the client. 
 
