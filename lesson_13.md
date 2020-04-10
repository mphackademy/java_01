#### Lesson 13

```java
package org.example;

/**
 * Ô tô.
 */
public class Car {

    /**
     * Năm sản xuất.
     */
    private int year;

    /**
     * Lốp xe.
     */
    public class Tire {
        /**
         * Đường kính của lốp xe.
         */
        private double radius;

        /**
         * Constructor khởi tạo một đối tượng Lốp xe với Bán kính cho trước.
         *
         * @param radius
         */
        public Tire(double radius) {
            this.radius = radius;
        }

        /**
         * Lấy ra đường kính của lốp xe.
         *
         * @return
         */
        public double getRadius() {
            return radius;
        }
    }

    /**
     * Contructor khởi tạo một đối tượng ô tô với năm sản xuất cho trước.
     *
     * @param year
     */
    public Car(int year) {
        this.year = year;
    }

    /**
     * Trả về năm sản xuất của chiếc ô tô.
     *
     * @return
     */
    public int getYear() {
        return year;
    }

}
```

```java
package org.example;

public class LocalInnerTest {

    public static void main(String[] args) {
        RandomInteger rTop = new RandomInteger();
        System.out.println("Số nguyên ngẫu nhiên sử dụng Top class");
        System.out.println(rTop.getValue());
        System.out.println(rTop.getValue());
        System.out.println(rTop.getValue());

        RandomLocal local = new RandomLocal();
        RandomInteger rLocal = local.getRandomInteger();
        System.out.println("Số nguyên ngẫu nhiên sử dụng Inner class: ");
        System.out.println(rLocal.getValue());
        System.out.println(rLocal.getValue());
        System.out.println(rLocal.getValue());
    }

}
```

```java
package org.example;

public class Outer {

    public class Inner {
        // Members of the Inner class.
    }

    // Members of the Outer class.
}
```

```java
package org.example;

public class RandomLocal {

    public RandomInteger getRandomInteger() {
        class RandomIntegerLocal extends RandomInteger {
            @Override
            public int getValue() {
                System.out.println("<<<<<");
                long n1 = rand.nextInt(100);
                long n2 = rand.nextInt(100);
                int value = (int) ((n1 + n2) / 2);
                return value;
            }
        }
        return new RandomIntegerLocal();
    }

}
```

```java
package org.example;

public class SomeTopLevelClass {

    int value = 42;

    public void someMethod() {
        class SomeInnerClass {
            int foo = 5;
        }
        SomeInnerClass someInnerClass;
    }

}
```

```java
package org.example;

import java.util.ArrayList;
import java.util.Iterator;

/**
 * Danh sách các tiêu đề.
 */
public class TitleList {

    /**
     * Danh sách tiêu đề.
     */
    private ArrayList<String> titleList = new ArrayList<>();

    /**
     * Thêm một tiêu đề vào danh sách.
     *
     * @param title
     */
    public void addTitle(String title) {
        titleList.add(title);
    }

    /**
     * Loại bỏ một tiêu đề ra khỏi danh sách.
     *
     * @param title
     */
    public void removeTitle(String title) {
        titleList.remove(title);
    }

    public Iterator<String> titleIterator() {
        class TitleIterator implements Iterator<String> {
            int count = 0;
            @Override
            public boolean hasNext() {
                return (count < titleList.size());
            }
            @Override
            public String next() {
                return titleList.get(count++);
            }
        }
        TitleIterator titleIterator = new TitleIterator();
        return titleIterator;
    }

}
```

```java
package org.example;

import java.util.Iterator;

public class TitleListTest {

    public static void main(String[] args) {
        TitleList tl = new TitleList();
        tl.addTitle("Lập trình Java 8");
        tl.addTitle("Ôn tập C# cho kỳ thi Ref 70-483");
        Iterator iterator = tl.titleIterator();
        while (iterator.hasNext()) {
            System.out.println(iterator.next());
        }
    }

}
```

```java
package org.example;

public class TopLevel {

    private int value = 101;

    public int getValue() {
        return value;
    }

    public void setValue(int value) {
        this.value = value;
    }

}
```
