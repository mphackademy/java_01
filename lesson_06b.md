#### Abstract class

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

    /**
     * Lấy họ tên đầy đủ.
     * 
     * @return Họ tên đầy đủ.
     */
    public String getFullName(){
        return lastName + firstName;
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

public class SecurityEmployee extends Employee {
    
}

``````
