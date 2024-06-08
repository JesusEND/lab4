# Hey! I'm Filing Here

In this lab, I successfully created a 1MiB ext2 file system, which I then mounted. The filesystem includes two directories, the root directory, and the lost+found directory. Additionally, it contains a regular file, which is named hello-world and a symbolic link named hello, which points to hello-world. 

## Building
In order to build, you need to run the command 'make', this will create an executable file, which you can then run by doing ./ext2-create

## Running
These are the following commands which we can use in order to run 

-dumps the filesystem information to help debug
dumpe2fs cs111 -base.img 

-this will check that your filesystem is correct
fsck.ext2 cs111 -base.img

-create a directory to mnt your filesystem to
mkdir mnt 

-mount your filesystem , loop lets you use a file
sudo mount -o loop cs111 -base.img mnt

## Cleaning up

When cleaning up, you can run the commands
'sudo unmount mnt'

Then remove the mount with 
 'rmdir mnt'

Lastly run 
'make clean'
