#### Java 8 lambda

```java
package org.example;

import java.util.Arrays;
import java.util.List;

public class StreamExample {

    public static void main(String[] args) {
        //List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 6, 8, 13, 35);
        //int sum = 0;
        //for (int n : numbers) {
        //    if (n % 2 == 0){
        //        sum += n;
        //    }
        //}
        //System.out.println("Tổng của các số chẵn là " + sum);

        List<Integer> numbers = Arrays.asList(35, 2, 1, 3, 4, 6, 8, 13);
        int sum = numbers
                .stream()
                .filter(n -> n % 2 == 1)
                .reduce(0, Integer::sum);
        System.out.println("Tổng các số lẻ là: " + sum);
    }

}
```

```java
package org.example;

import java.nio.ByteBuffer;
import java.nio.InvalidMarkException;

public class Application {

    public static void main(String[] args) {
        ByteBuffer byteBuffer = ByteBuffer.allocate(8);
        System.out.println("Capacity: " + byteBuffer.capacity());
        System.out.println("Limit: " + byteBuffer.limit());
        System.out.println("1. Position: " + byteBuffer.position());

        byteBuffer.position(3);
        System.out.println("2. Position: " + byteBuffer.position());
        try{
            byteBuffer.reset();
            System.out.println("3. Position = " + byteBuffer.position());
        }catch (InvalidMarkException e){
            System.err.println("Mark is not set.");
        }
    }

}
```

```java
package org.example;

import java.util.Arrays;
import java.util.List;

public class App {

    public static void main(String[] args) {
        List<Integer> numbers = Arrays.asList(1, 2, 5, 8, 9, 10, 12, 15, 16, 18);
        int sum = numbers.parallelStream().filter(n -> n % 3 == 0)
                .reduce(0, Integer::sum);
        System.out.println("Tổng các số chia hết cho 3 là " + sum);
    }

}
```



