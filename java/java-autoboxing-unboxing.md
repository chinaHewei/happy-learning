# Java Autoboxing And Unboxing

> [Autoboxing and Unboxing In Java™ Tutorials](https://docs.oracle.com/javase/tutorial/java/data/autoboxing.html)

## Java Primitive Types And Corresponding Wrapper Classes

| Primitive type | Wrapper class |
| :------------: | :-----------: |
| `int`          | `Integer`     |
| `short`        | `Short`       |
| `long`         | `Long`        |
| `double`       | `Double`      |
| `float`        | `Float`       |
| `boolean`      | `Boolean`     |
| `byte`         | `Byte`        |
| `char`         | `Character`   |

## Autoboxing

Converting a primitive value (an `int`, for example) into an object of the corresponding wrapper class (`Integer`) is called **autoboxing**. The Java compiler applies autoboxing in following situations:

* When a primitive value is passed as parameter to a method that expects an object of the corresponding wrapper class.
* When a primitive value is assigned to a variable of the corresponding wrapper class.

Java code demo:

```Java
List<Integer> li = new ArrayList<>();
for (int i = 1; i < 50; i += 2)
    li.add(i); // autoboxing, int -> Integer
```

Why can we add primitive type `int` into `List<Integer>`. Because the Java compiler creates an Integer object from `i` and adds the object to `li`.

Corresponding class:

```Class
List<Integer> li = new ArrayList<>();
for (int i = 1; i < 50; i += 2)
    li.add(Integer.valueOf(i));
```

## Unboxing

Converting an object of a wrapper type (`Integer`) to its corresponding primitive (`int`) value is called **unboxing**. The Java compiler applies unboxing in following situations:

* When a object of wrapper class passed as a parameter to a method that expects a value of the corresponding primitive type.
* When a object of wrapper class assigned to a variable of the corresponding primitive type.

Java code demo:

```Java
List<Integer> ls = new ArrayList<>();
ls.add(3); // autoboxing, int -> Integer
int val = ls.get(0); // unboxing
System.out.println(val);
```

Why can we add primitive type `int` into `List<Integer>`. Because the Java compiler creates an Integer object from `i` and adds the object to `li`.

Corresponding class:

```Class
List<Integer> ls = new ArrayList();
ls.add(3);
int val = (Integer)ls.get(0);
System.out.println(val);
```
