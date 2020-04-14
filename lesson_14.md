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

```java
package org.example;

public class App {

    public static void main(String[] args) {
        int[] numberArray = {3, 4, 3, 5, 4, 5};
        System.out.println(numberArray[9]);
    }

}
```

Lỗi

```
Java HotSpot(TM) 64-Bit Server VM warning: Sharing is only supported for boot loader classes because bootstrap classpath has been appended
Exception in thread "main" java.lang.ArrayIndexOutOfBoundsException: Index 9 out of bounds for length 6
```

### Lỗi ép kiểu

```java
package org.example;

public class App {

    public static void main(String[] args) {
        String bar = "covid-19";
        Object something = bar;
        Integer fooNumber = (Integer) something;
        System.out.println(something);
    }

}
```
Lỗi

```
Exception in thread "main" java.lang.ClassCastException: class java.lang.String cannot be cast to class java.lang.Integer (java.lang.String and java.lang.Integer are in module java.base of loader 'bootstrap')
	at org.example.App.main
````




