### Static inner class

```java
package org.example;

public class A {

    // static member class.
    public static class B {
        // Body for class B goes here.
    }

}
````


```java
package org.example;

/**
 * Linh kiện máy tính.
 */
public class ComputerAccessory {

    /**
     * Màn hình máy vi tính.
     */
    public static class Monitor {

        /**
         * Kích thước của màn hình máy vi tính.
         */
        private int size;

        public Monitor(int size) {
            this.size = size;
        }

        public String toString() {
            return "Monitor - Size: " + this.size + " inch.";
        }
    }

    /**
     * Bàn phím.
     */
    public static class KeyBoard {

        /**
         * Số phím của bàn phím.
         */
        private int keys;

        public KeyBoard(int keys) {
            this.keys = keys;
        }

        public String toString() {
            return "Keyboard - Keys: " + this.keys;
        }
    }

}
```

