### Exception (tiếp)

### `java.lang.NullPointerException`

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
        if(title == null){
            throw new NullPointerException("Tiêu đề sách không thể bỏ trống.");
        }
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
        System.out.println("Tiêu đề của quyển Effective Java là: " + effectiveJavaBook.getTitle());
    }

}
```

Lỗi

```
Exception in thread "main" java.lang.NullPointerException: Tiêu đề sách không thể bỏ trống.
	at org.example.Book.getTitle(Book.java:...)
```



