#### Interface

``````java
package org.example;

/**
 * Các sinh vật, vật thể có thể chạy được.
 */
public interface Runable {

}
``````

``````java
package org.example;

/**
 * Sinh vật, vật thể có thể học được.
 */
public interface Learnable {

}
``````

``````java
package org.example;

import java.time.LocalDate;
import java.time.Period;

/**
 * Học viên.
 */
public class Student implements Learnable, Runable {

    /**
     * Tên gọi.
     */
    String firstName;

    /**
     * Họ và tên đệm.
     */
    String lastName;

    /**
     * Giới tính.
     */
    String gender;

    /**
     * Địa chỉ thường trú.
     */
    String residenceAddress;

    /**
     * Ngày sinh của học viên.
     */
    LocalDate dateOfBirth;

    /**
     * In ra họ và tên đầy đủ của học viên.
     */
    public void printFullName() {
        System.out.println(lastName + " " + firstName);
    }

    /**
     * Tính tuổi của học viên.
     *
     * @return
     */
    public int getStudentAge() {
        // Thời điểm hiện tại.
        LocalDate now = LocalDate.now();
        return Period.between(dateOfBirth, now).getYears();
    }

    /**
     * In ra địa chỉ nơi cư trú của học viên.
     */
    public void printStudentResidenceAddress() {
        System.out.println("Địa chỉ nơi cư trú của học viên: " + residenceAddress);
    }

}
``````
and

````java
package org.example;

/**
 * Con mèo.
 */
public class Cat implements Runable {

    /**
     * Màu lông của con mèo.
     */
    String furColor;

    /**
     * Giới tính của con mèo.
     */
    String gender;

    /**
     * Tuổi của con mèo.
     */
    int age;

    /**
     * Số chân của con mèo.
     */
    int numberOfLengths = 4;

    /**
     * Săn mồi.
     *
     * @return Số con chuột mà mèo bắt được.
     */
    public int hunt(){
        // Số con chuột mà mèo bắt được.
        int catchedMouses = 2;
        System.out.println("Con mèo đã bắt được " + catchedMouses + " con chuột.");
        return catchedMouses;
    }

    /**
     * Kêu meo meo.
     */
    public void meow(){
        System.out.println("Meo meo gumm gumm");
    }

    /**
     * Mèo nhảy lên cao.
     *
     * @return Độ cao mà mèo nhảy được, tính bằng mét.
     */
    public int jump(){
        // Độ cao mà mèo nhảy được
        int height = 2;
        return height;
    }

    /**
     * Mèo leo trèo ở đâu đó.
     */
    public void clim(){
        System.out.println("Leo lên cây cau.");
    }

}
``````




