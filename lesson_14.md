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

### Lỗi sai đối số truyền vào phương thức

```java
package org.example;

/**
 * Cuốn sách.
 */
public class Book {

    /**
     * Tiêu đề của quyển sách.
     */
    String title;

    /**
     * Số trang.
     */
    int pages;

    public String getTitle() {
        return title;
    }

    public void setTitle(String title) {
        this.title = title;
    }

    public int getPages() {
        return pages;
    }

    public void setPages(int numberOfPages) {
        if (pages <= 0) {
            throw new IllegalArgumentException("Số trang sách không thể âm hoặc bằng 0.");
        } else {
            this.pages = numberOfPages;
        }
    }

}
```
and

```java
package org.example;

public class App {

    public static void main(String[] args) {
        Book effectiveJavaBook = new Book();
        effectiveJavaBook.setPages(-3);
        System.out.println("Số trang sách của quyển Effective Java là: " + effectiveJavaBook.getPages());
    }

}
```

Lỗi
```
Exception in thread "main" java.lang.IllegalArgumentException: Số trang sách không thể âm hoặc bằng 0.
	at org.example.Book.setPages...
```






