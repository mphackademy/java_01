### Phần 2

``````java
package oop;

public class TuesdayApplication {

    public static void main(String[] args){
        System.out.println("test");
    }

}
``````

``````java
package oop;

import java.util.Date;

/**
 * Con người.
 */
public abstract class People implements Moveable {

    /**
     * Ngày tháng năm sinh.
     */
    Date dateOfBith;

    /**
     * Nơi sinh.
     */
    String homeTown;

}
``````

``````java
package oop;

/**
 * Có khả năng di chuyển
 */
public interface Moveable {

    /**
     * Di chuyển.
     */
    void move();
}
``````

``````java
package oop;

import java.util.Date;

/**
 * Nhân viên.
 */
public abstract class Employee extends People {

    /**
     * Ngày vào công ty.
     */
    public Date entryDate;

    /**
     * Kỹ năng chuyên môn chính.
     */
    public String mainSkill;

}
``````

``````java
package oop;

/**
 * Bác sỹ.
 */
public class Doctor extends Employee {

    @Override
    public void move() {

    }
}
``````

``````java
package oop;

/**
 * Lập trình viên.
 */
public class Programmer extends Employee {


    @Override
    public void move() {

    }
}
``````





