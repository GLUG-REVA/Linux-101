# Linux-101

## About Linux

Linux is a free, open-source operating system. It broadly denotes operating systems distributions built around the Linux kernel. Linux kernel is an operating system kernel first released on September 17, 1991 by [Linus Torvadls](https://en.wikipedia.org/wiki/Linus_Torvalds).

_This guide will introduce you to the Linux operating system and will equip you to learn more about Linux._

## Your new best friend: The Terminal

The Linux terminal is an extremely powerful tool that goes well beyond the GUI. To open a terminal, the shortcut Ctrl+Alt+T will work on most distributions and desktop environments.

This is the basic anatomy of most Linux commands:

```shell
[sudo] command [optional switch] [file or directory path]
```

The Linux commands are case-sensitive. When the command is `pwd` everything part for `pwd` would throw an error. For example, `Pwd`, `PWD`, `pWd`, etc

A space is also equally important.

Note: The infamous Ctrl+C and Ctrl+V won't work! Instead, you must use Ctrl+Shift+C and Ctrl+Shift+V; or you can right click and use the commands from the dropdown menu.

Before you dive into the basics it is probably helpful to remember these:

- `[command] --help` will show the usage of the command, and the available options and switches
- `man [command]` will show the command's manual, which is an extended version of the --help output

And just so you know, not all Linux commands have a manual page. But, most of them that you would be learning, do have a manual page.

## Basic Linux commands

_All the commands henceforth demonstrated are expected to be typed into your terminal unless otherwise specified._

### Navigation

In this section, we demonstrate commands that will help you navigate to particular directories (folders) and locate files.

#### ls

**ls -- list directory contents**

This command is used for listing all the directory contents. Make sure you read the ls --help to learn about the options...

```shell
ls
```

#### cd

**cd -- change directory**

This command is used for navigation within your file system.

To put in 'Windows' terms this command is used to switch between folders.

```shell
cd [directory]
```

#### pwd

**pwd -- print working directory**

This command is used to print the full path to the directory that you are presently situated in. pwd stands for print working directory.

```shell
pwd
```

#### find

**find -- search for a file**

This command is used to find a particular file in the present working directory.

```shell
find [file or directory]
```

#### locate

**locate -- locate a file or directory** This command is used to locate a file or a directory in the entire file system.

```shell
locate [file or directory]
```

### File handling

In this section you will learn how to create, delete, and basic file manipulation.

#### mkdir

**mkdir -- make directory**

This command is used to create a directory.

```shell
mkdir [path to new directory]
```

You can include the absolute path to the directory to create it anywhere on the disk.

#### touch

**touch -- create an empty file**

This command is used to create a new(empty) file.

```shell
touch [path to file]
```

If the file already exists, `touch` won't erase its contents, it will just change the last access time to the current time.

#### cp

**cp -- copy**

This command is used to, well, copy stuff.

```shell
cp [path to source] [path to destination]
```

The `cp` command copies the file at source to the file at destination. This is the equivalent copy-paste.

If the file at destination does not exist then, the file is created.

To copy directories and their contents, we need to use:

```shell
cp -r [path to source] [path to destination]
```

#### mv

**mv -- move**

This command is used to move files between locations

```shell
mv [path to source] [path to destination]
```

The `mv` command is the equivalent of cut-paste. The command also works with directories without the need of an option.

The `mv` command is the only way to rename files in Linux.

#### rm

**rm -- remove**

This command is used to delete files or directories.

```shell
rm [path]
```

To delete a directory and all its contents, we need to use:

```shell
rm -r [path to directory]
```

The rm command will immediately remove any files/directories, without using Trash. Exercise caution while usage of this command.

#### zip

**zip -- creates a zipped folder**

This command creates a zipped folder that contains a compressed file.

```shell
zip [archive.zip] [file]
```

#### unzip

**unzip -- unzips a compressed folder**

This command unzips a compressed folder.

```shell
unzip [archive.zip]
```

By default, unzip will extract all the files in the working directory.

### Accessing contents of a file

#### echo

**echo - write arguments to standard output**

This command writes the arguments to the specified location.

```shell
echo "text" > [path to file]
```

Caution! If the file already exists, the `echo "text" > file` will overwrite it, deleting all of its previous content.

Using `>>` instead of `>` will append the text at the end.

```shell
echo "text" >> [path to file]
```

#### cat

**cat -display the contents of the file**

This command display all the contents of a text file on the terminal.

```shell
cat [path to file]
```

We can also use `head [text file]` to only show the first ten lines, and `tail [text file]` to display the last ten lines.

#### wc

**wc -- word count**

Prints the word count, number of lines and the number of characters in a file.

```shell
wc [path to file]
```
