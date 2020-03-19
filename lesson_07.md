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
