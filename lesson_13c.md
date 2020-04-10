### Multiple inner class - Class lồng nhau nhiều lần

- Class ngoài nhất không thể là static.
- Class ở giữa dở dang, nếu cha của nó không là static, thì nó không thể là static.
- Nếu các class dở dang ở giữa là static, class ở trong nhất có thể là static hay không static điều được.

```java
package org.example;

public class B {
    public static class M {
        public static class G {
            public class X {
                public void printSomething() {
                    System.out.println();
                }
            }
        }
    }

}

```
