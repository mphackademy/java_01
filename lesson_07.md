### Không ai tắm hai lần trên một dòng sông.

``````java
package org.example;

import java.time.LocalDate;

/**
 * Application.
 */
public class App {

    public static void main(String[] args) {
        LocalDate todayLocalDate = LocalDate.of(2020, 3, 19);
        System.out.println("Hôm nay là: " + todayLocalDate);

        LocalDate tomorrow = todayLocalDate.plusDays(1L);
        System.out.println("Ngày mai là: " + tomorrow);

        LocalDate aDayAfterTomorrow = tomorrow.plusDays(1L);
        System.out.println("Ngày kia là: " + aDayAfterTomorrow);
        System.out.println("Ngày kia là thứ mấy? " + aDayAfterTomorrow.getDayOfWeek());


        // Ngày này năm trước.
        LocalDate thisDayLastYear = todayLocalDate.minusYears(1L);
        System.out.println("Ngày này năm trước là: " + thisDayLastYear);
        System.out.println("Ngày này năm trước là thứ mấy? " + thisDayLastYear.getDayOfWeek());
        
    }
}
``````

### Bài tập về nhà

``````java
package org.example;

import java.time.LocalDate;
import java.time.Period;

public class TimeApplication {

    public static void main(String[] args) {
        LocalDate today = LocalDate.now();

        // Ngày này của tháng trước.
        LocalDate thisDayLastMonth = today.minusMonths(1L);
        System.out.println("Ngày này của tháng trước là ngày thứ mấy trong tháng? " + thisDayLastMonth.getDayOfMonth());
        System.out.println("Ngày này của tháng trước là ngày thứ bao nhiêu trong năm? " + thisDayLastMonth.getDayOfYear());


        // Năm mới tiếp theo.
        LocalDate nextNewYear = LocalDate.of(2021, 1, 1);
        // Số ngày còn nữa cho đến Tết Dương lịch.
        Period daysToNewYear = Period.between(today, nextNewYear);
        System.out.println("Còn ... ngày nữa là đến Tết Dương lịch.");

    }

}
````````

Tính xem còn bao nhiêu ngày nữa thì đến Tết dương lịch?



