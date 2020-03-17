#### Lập trình hướng đối tượng

Bài tập về nhà

**Bài 01.** Khai báo đối tượng con mèo với 
Thuộc tính:
- Màu lông.
- Giới tính.
- Tuổi.
- Số chân.

Phương thức:
- Đi săn mồi.
- Kêu "Meo meo.".
- Nhảy lên cao.
- Leo.

**Bài 02.** Khai báo đối tượng học viên (Student) với

Thuộc tính:

- Tên gọi (firstName)
- Tên họ và tên đệm (lastName)
- Giới tính
- Địa chỉ thường trú (residenceAddress) gồm thông tin đầy đủ về số nhà, phường/xã, quận/huyện, tỉnh/thành phố.
- Ngày sinh (sử dụng kiểu dữ liệu `java.util.Date`)


Phương thức:
- In ra tên đầy đủ (fullName)
- Trả về tuổi của học viên.
- In ra tỉnh/thành phố của Địa chỉ thường trú của học viên.

Gợi ý:

```java
package vn.mphackademy.course;

import java.util.Date;

public class Student {

    /**
     * Ngày sinh của học viên.
     */
    Date dateOfBirth;
    
    //....
    
}
```

Nộp bài trước buổi học học tối thứ năm, gửi vào email vydn@mpsoftware.com.vn

Đáp án

````java
package org.example;

/**
 * Con mèo.
 */
public class Cat {

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
     * @return
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

    
    
}
```


