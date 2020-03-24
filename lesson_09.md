### Buổi 09

``````java
package oop;

import java.util.Date;

/**
 * Con người.
 */
public abstract class People {

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

}
``````

