### Sử dụng lambda expression như là đối số của phương thức khác.

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

public class LambdaUtil {

    public void testAdder(Adder adder) {
        double x = 190.90;
        double y = 8.50;
        double sum = adder.add(x, y);
        System.out.println(x + " + " + y + " = " + sum);
    }

    public void testJoiner(Joiner joiner) {
        String s1 = "Hello";
        String s2 = "World";
        String s3 = joiner.join(s1, s2);
        System.out.println("\"" + s1 + "\" + \"" + s2 + "\" = \"" + s3 + "\"");
    }

}
```

```java
package org.example;

public class LambdaUtilTest {

    public static void main(String[] args) {
        LambdaUtil util = new LambdaUtil();

        // Call the testAdder() method.
        util.testAdder((x, y) -> x + y);

        // Call the testJoiner() method.
        util.testJoiner((x, y) -> x + y);

        // Call the testJoiner() method. The Joiner will add a space between the two strings.
        util.testJoiner((x, y) -> x + " " + y);

        // Call theh testJoiner() method. The Joiner will reverse the strings and join resulting strings
        // in reverse order adding a comma in between.
        util.testJoiner((x, y) -> {
            StringBuilder sbx = new StringBuilder(x);
            StringBuilder sby = new StringBuilder(y);
            sby.reverse().append(",").append(sbx.reverse());
            return sby.toString();
        });
    }

}
```



