# java

Java application launcher.

# javac

Java complier.

# javap

Java class file disassembler. The `javap` command disassembles a Java class file (`.class` file).

```shell
$ javap --help
$ javap -public Demo.class
$ javap -protected Demo.class
$ javap -package Demo.class
$ javap -private Demo.class
$ javap -v Demo.class
$ javap -c Demo.class
```

# jar

Java archive tool.

List contents of jar file.

```shell
$ jar t[v]f Demo.jar
```

Extract jar file.

```shell
$ jar x[v]f Demo.jar
```
