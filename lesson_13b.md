### Static inner class

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

        }

        public String toString() {
            return "Keyboard - Keys: " + this.keys;
        }
    }

}
```

