### Bài tập thực hành, nhân 2 số, sử dụng Functional Interface của Java 8 lambda.

```java
package org.example;

/**
 * Cộng hai số.
 */
@FunctionalInterface
public interface Adder {

    /**
     * Cộng 2 số.
     * 
     * @param s1 Số hạng thứ nhất.
     * @param s2 Số hạng thứ hai.
     * @return
     */
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

    /**
     * Nối 2 xâu ký tự với nhau.
     * 
     * @param s1 Chuỗi thứ nhất.
     * @param s2 Chuỗi thứ hai.
     * @return
     */
    String join(String s1, String s2);

}
```

```java
package org.example;

/**
 * Bộ nhân.
 */
@FunctionalInterface
public interface Multiplier {

    /**
     * Nhân 2 số với nhau.
     *
     * @param o1 operator 1 - Thừa số thứ nhất
     * @param o2 operator 2 - Thừa số thứ hai.
     * @return
     */
    double multiply(double o1, double o2);

}
```

```java
package org.example;

public class TargetTypeTest {

    public static void main(String[] args) {
        // Create an Adder using a lambda expression.
        Adder adder = (x, y) -> x + y;

        // Create an Joiner using a lambda expression.
        Joiner joiner = (x, y) -> x + " " + y;

        // Cộng 2 số.
        double sum1 = adder.add(10.34, 89.11);
        System.out.println("Tổng của 2 số là " + sum1);

        // Ghép 2 xâu.
        String hungFullname = joiner.join("Phan Thế", "Hưng");
        System.out.println("Tên đầy đủ của Hưng là " + hungFullname);

        Multiplier multiplier = (o1, o2) -> o1 * o2;
        System.out.println("Tích của 2 số 3 và 4 là " + multiplier.multiply(3.0, 4.0));
    }

}
```


