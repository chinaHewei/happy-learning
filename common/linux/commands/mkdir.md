# mkdir

> Make directories.

```shell
mkdir [-pv] [-m mode] directory_name ...
```

* `-p`: Parents. Create intermediate directories as required.
* `-v`: Verbose. List dir as they are created.
* `-m mode`: Set the permissions of the directory while creating the directory.

## command demo

Create 50 directories from sa1 through sa50

```shell
mkdir sa{1..50}
```

Create directories 1, 2, and 3

```shell
mkdir {1,2,3}
```

Using expressiong in mkdir command.

```shell
mkdir -p `date '+%y%m%d'`/{1,2,3} 
mkdir -p $USER/{1,2,3}
```

Create directories for maven project.

```shell
mkdir -p -v src/{main/{java,resources},test/{java,resources}}
```
