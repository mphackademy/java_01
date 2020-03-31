### Debug Java 8 lambda stream API

```java
package org.example;

import java.util.Arrays;
import java.util.stream.Stream;

public class App {

    public static void main(String[] args) {
        int sum = Stream.of(1, 2, 3, 4, 5)
                .peek(e -> System.out.println("Lấy ra số nguyên " + e))
                .filter(n -> n % 2 == 1)
                .peek(m3 -> System.out.println("Lấy ra số lẻ: " + m3))
                .map(z -> z * z + 1)
                .peek(y -> System.out.println("y bình phương cộng 1 là " + y + "\n------------"))

                .reduce(0, Integer::sum);

    }

}
```

Kết quả debug:

```
Lấy ra số nguyên 1
Lấy ra số lẻ: 1
y bình phương cộng 1 là 2
------------
Lấy ra số nguyên 2
Lấy ra số nguyên 3
Lấy ra số lẻ: 3
y bình phương cộng 1 là 10
------------
Lấy ra số nguyên 4
Lấy ra số nguyên 5
Lấy ra số lẻ: 5
y bình phương cộng 1 là 26
------------
```

In ra kết quả
```java
package org.example;

import java.util.Arrays;
import java.util.stream.Stream;

public class App {

    public static void main(String[] args) {
        int sum = Stream.of(1, 2, 3, 4, 5)
                .peek(e -> System.out.println("Lấy ra số nguyên " + e))
                
                .filter(n -> n % 2 == 1)
                .peek(m3 -> System.out.println("Lấy ra số lẻ: " + m3))

                .map(z -> z * z + 1)
                .peek(y -> System.out.println("y bình phương cộng 1 là " + y + "\n------------"))

                .reduce(0, Integer::sum);

        System.out.println("Tổng của các số hạng (n^2 + 1) là " + sum);

    }

}
```

Kết quả
```
Lấy ra số nguyên 1
Lấy ra số lẻ: 1
y bình phương cộng 1 là 2
------------
Lấy ra số nguyên 2
Lấy ra số nguyên 3
Lấy ra số lẻ: 3
y bình phương cộng 1 là 10
------------
Lấy ra số nguyên 4
Lấy ra số nguyên 5
Lấy ra số lẻ: 5
y bình phương cộng 1 là 26
------------
Tổng của các số hạng (n^2 + 1) là 38
```

