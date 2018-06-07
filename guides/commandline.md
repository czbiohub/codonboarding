# commandline

Use this to: get started using commandline in Terminal on MAC OS

## `cd`
* `cd` is a command that will change your directory.
* `cd ..` will bring you to the parent directory
	- HISTORY
		- The builtin manual page first appeared in FreeBSD 3.4.


## `pwd`
- `pwd` is a command that will print your current or working directory

## `mkdir`
- `mkdir` is a command that will make a folder or directory in your current directory
- `mkdir -p`: not only generates the *parent* folder in the current working directory but will also generate a *child* folder within the new *parent* folder

	For example:

	```
	$ mkdir -p code/cupcakes
	$ pwd
	/Users/rene.sit/code/cupcakes
	```

## `rm`
- `rm`: stands for "remove"  
- `rm -R`: removes the directory indicated and all subsequent directories and files within folder

## `mv`
- `mv`: renames files or directories

	For example:
	```
	$ pwd
	/Users/rene.sit/code
	$ ls
	cupcake
	$ mv cupcakes cupcake-new
	$ ls
	cupcake-new
	```

## `ls`
* `ls -F` or  `ls -Fa` will print items in current directory that are hidden

## `ln`
* `ln` make a link
	- HISTORY
		- An `ln` command appeared in Version 1 AT&T UNIX.

		### `mkdir`
		- `mkdir`: generates a new folder/directory in the current working directory


# GIT help: Jenai notes

* `git checkout -b branchname` will make a new branch

* `git status` will show history of project. Shows untracked files.

* `git add filename` will update a file to the branch that is not yet committed

* `git commit -m "notes about what you did"`
