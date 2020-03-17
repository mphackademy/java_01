``````java
package org.example;

/**
 * Con người.
 */
public abstract class People {

    /**
     * Tên gọi.
     */
    String firstName;

    /**
     * Họ và tên đệm.
     */
    String lastName;

    public People() {

    }

    /**
     * Lấy họ tên đầy đủ.
     *
     * @return Họ tên đầy đủ.
     */
    public String getFullName(){
        return lastName + " " + firstName;
    }

    public String getFirstName() {
        return firstName;
    }

    public void setFirstName(String firstName) {
        this.firstName = firstName;
    }

    public String getLastName() {
        return lastName;
    }

    public void setLastName(String lastName) {
        this.lastName = lastName;
    }
}
``````

``````java
package organization;

import org.example.People;

/**
 * Nhân viên.
 */
public abstract class Employee extends People {

}
``````

``````java
package organization;

/**
 * Nhân viên bảo vệ
 */
public class SecurityEmployee extends Employee {

}
``````

``````java
package organization;

import org.example.People;

public class Application {

    public static void main(String[] args) {
        People oldSecurityEmployeeAtGarage = new People() {
        };
        oldSecurityEmployeeAtGarage.setFirstName("Hùng");
        oldSecurityEmployeeAtGarage.setLastName("Nguyễn Văn");
        System.out.println(oldSecurityEmployeeAtGarage.getFullName());
    }

}
``````

