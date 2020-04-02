#### Java 8 language features (tiếp)

```java
package org.example;

/**
 * Cộng hai số.
 */
@FunctionalInterface
public interface Adder {

    double add(double s1, double s2);

}

```

```java
package org.example;

/**
 * Nối 2 xâu vào với nhau.
 */
@FunctionalInterface
public interface Joiner {

    String join(String s1, String s2);

}
```

```java
package org.example;

public class TargetTypeTest {

    public static void main(String[] args) {
        // Create an Adder using a lambda expression.
        Adder add = (x, y) -> x + y;

        // Create an Joiner using a lambda expression.
        Joiner join = (x, y ) -> x + " " + y;

        // Cộng 2 số.
        double sum1 = add.add(10.34, 89.11);
        System.out.println("Tổng của 2 số là " + sum1);

        // Ghép 2 xâu.
        String hungFullname = join.join("Phan Thế", "Hưng");
        System.out.println("Tên đầy đủ của Hưng là " + hungFullname);
    }

}
```


