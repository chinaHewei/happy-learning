# Java Generic Type

> [Java™ Tutorials](https://docs.oracle.com/javase/tutorial/java/generics/index.html)

Generics were introduced to the Java language to provide tighter type checks at compile time and to support generic programming.

## Generic Types

> [Generic Types In Java™ Tutorials](https://docs.oracle.com/javase/tutorial/java/generics/types.html)

Generic type is a generic class or interface that is parameterized over types and we can call it **parameterized type**.

Generic class:

```Java
class ClassName<T1, T2, ...., Tn> { /* ... */ }
```

Generic interface:

```Java
interface InterfaceName<T1, T2, ...., Tn> { /* ... */ }
```

T1, T2 ...., Tn was called **type parameters** (also called type variables).

## Generic Methods

> [Generic Mehtods In Java™ Tutorials](https://docs.oracle.com/javase/tutorial/java/generics/methods.html)

Generic methods are methods that introduce their own type parameters. The type parameter's scope is **limited to the method** where it is declared. **Static** and **non-static** generic methods are allowed, as well as generic class constructors.

The synatxs for a generic mehtod includes a list of type parameters, **inside angle brackets**, which appears **before the method's return type**.

Generic methods:

```Java
// static method
public static <K, V> boolean compare(Pair<K, V> p1, Pair<K, V> p2) { /* ... */ }

// non-static method
public <K, V> void addToExt(Map<K, V> ext, K key, V value) { /* ... */ }
public <T> void addToList(List<T> list, T t) { /* ... */ }
```
