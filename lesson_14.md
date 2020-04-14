### Nói về những lỗi lầm. Exception

```java
package org.example;

public class App {

    public static void main(String[] args) {
        System.out.println(3 / 0);
    }

}
```

Lỗi
```
Java HotSpot(TM) 64-Bit Server VM warning: Sharing is only supported for boot loader classes because bootstrap classpath has been appended
Exception in thread "main" java.lang.ArithmeticException: / by zero
```


