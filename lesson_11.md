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
