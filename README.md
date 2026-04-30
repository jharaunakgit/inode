# The Concept of Inodes

People generally think that in Linux file system is similar to what we have in Windows. However, it is different and it consists of a combination of metadata and data. 

## Definition

It is a data structure that has all the data a regarding a file except its name. In Linux, individual file has an inode number and a metadata. 

## Contents of an Inode Number

An inode consists of the following factors:
* Size of a file
* Type of File
* Permissions
* Owner of the file
* Timestamps
* Pointers to actual data blocks 

## Where is the Filename?

These are stored in directories. A directory acts as a table. It stores the corresponding inode number for each file name.

Example:
 `` index.txt - inode 12345 ``
 
## How are we able to access file?

* You enter in terminal: `` cat index.txt ``
* Then, the system starts looking for the file in the directory. It gets to index.text - inode 12345
* Then, reads inode 12345 and locates actual data blocks. 
* In the end, it displays the file. 

## How to check inode in Linux?

You need to type in the terminal: `` ls -i ``
Output: `` 12345 index.txt ``
