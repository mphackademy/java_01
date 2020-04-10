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


```java
package org.example;

public class B {
    public static class M {
        public static class G {
            public static class X {
                public void printSomething() {
                    System.out.println(">>>> hehe <<");
                }
            }
        }
    }

}
```

```java
package org.example;

public class BTest {

    public static void main(String[] args) {
        B.M.G.X x = new B.M.G.X();
        x.printSomething();
    }

}
```

```java
package org.example;

public class B {
    public static class M {
        public static class G {
            public static class X {
                public void printSomething() {
                    System.out.println(">>>> hehe <<");
                }
            }
        }

        public static class G2 {
            public static class X {
                public void printSomething() {
                    System.out.println(">>>> hehe keke @@@");
                }
            }
        }
    }

}
```


