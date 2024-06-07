# Hey! I'm Filing Here

This project involves the implementation of an ext2 filesystem image with specific inodes and directory structures. The ext2 filesystem image is built with a root directory, a lost+found directory, a regular file named hello-world, and a symbolic link named hello pointing to hello-world.

## Building

To build the project, use the following commands:

```shell
make
```

This command compiles the source code and generates the cs111-base.img filesystem image.

## Running
After building the project, you can inspect the filesystem image using: 

To run the executable to create cs111-base.img:

```shell
./ext2-create
```

To dump the filesystem information to help debug:

```shell
dumpe2fs cs111-base.img
```

To check that the filesystem is correct:

```shell
fsck.ext2 cs111-base.img
```

To create a directory to mount your filesystem to:

```shell
mkdir mnt
```

To mount the filesystem (loop lets you use a file):

```shell
sudo mount -o loop cs111-base.img mnt
```

To unmount the filesystem once done: 

```shell
sudo umount mnt
```

To delete the directory used for mounting when done:

```shell
rmdir mnt
```

## Cleaning up

To clean up the project, use the following command:

```shell
make clean
```

This command removes the compiled files and the generated filesystem image.

