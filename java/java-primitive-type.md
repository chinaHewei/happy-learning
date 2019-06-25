# Primitive Data Types

> [Primitive Data Types In Java™ Tutorilas](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)

| Data type | Data range                                               | Default value (for fields) | Description                                       |
| :-------: | :------------------------------------------------------: | :------------------------: | :-----------------------------------------------: |
| `byte`    | [-2<sup>7</sup>, 2<sup>7</sup>-1] or [-128, 127]         | 0                          | An **8-bit** signed two's complement integer      |
| `short`   | [-2<sup>15</sup>, 2<sup>15</sup>-1] or [-32,768, 32,767] | 0                          | A **16-bit** signed two's complement integer      |
| `int`     | [-2<sup>31</sup>, 2<sup>31</sup>-1]                      | 0                          | A **32-bit** signed two's complement integer      |
| `long`    | [-2<sup>63</sup>, 2<sup>63</sup>-1]                      | 0L                         | A **64-bit** two's complement integer             |
| `float`   |                                                          | 0.0f                       | A single-precision 32-bit IEEE 754 floating point |
| `double`  |                                                          | 0.0d                       | A double-precision 64-bit IEEE 754 floating point |
| `boolean` | `true` or `false`                                        | `false`                    |
| `char`    | `'\u0000'` to `'\uffff'` or [0, 65,535]                  | `'\u000'`                  | A single 16-bit Unicode character                 |

Recommended use of the primitive type

* `byte`: 
  * Useful for saving memory in large arrays.
  * Used in replace of int where their limits help to clarify code.
* `short`: same as `byte`.
* `float`:
  * Use a float (instead of double) if you need to save memory in large arrays
  * Never be used for precise values, such as currency, use the java.math.BigDecimal class instead.
* `double`: Never be used for precise values, such as currency, use the java.math.BigDecimal class instead.

For default value, fields that are declared but not initialized will be set to a reasonable default by the compiler. But local variables are slightly different, the compiler never assigns a default value to an uninitialized local variable.

```Java
public class Application {
    private static byte byteFiled;

    public static void main(String[] args) {
        // Ok, byteFiled will have default value 0;
        System.out.println(byteFiled);

        byte byteLocalVariable;
        // Not ok, compile error: Error:(15, 28) java: variable byteLocalVariable might not have been initialized
        System.out.println(byteLocalVariable);
    }
}
```