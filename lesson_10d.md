#### Truyền đối số, chạy từ dòng lệnh

``````java
package org;

public class PassingArguments {

    public static void main(String[] args) {
        if (args.length > 0) {
            System.out.println("Các đối số truyền vào là: ");
            for (String argument : args) {
                System.out.println(argument);
            }
        } else {
            System.out.println("Hic, bạn không truyền vào đối số nào cả :(");
        }
    }

}
``````

Câu lệnh

``````
C:\Users\Admin\IdeaProjects\untitled2\practice\target\classes>java -Dfile.encoding=UTF-8 -cp . org.PassingArguments Chao ban Hung
``````

hoặc

``````
C:\Users\Admin\IdeaProjects\untitled2\practice\target\classes>java -cp . org.PassingArguments Chao ban Hung
``````

Đổi encoding của CMD https://stackoverflow.com/a/18439832/3728901

#### Đọc giá trị của các biến môi trường

``````java
package org.example;

import java.util.Map;

public class ReadEnvironmentVariables {

    public static void main(String[] args) {
        Map<String, String> enviromentVariables = System.getenv();
        for (String key : enviromentVariables.keySet()) {
            System.out.println("Biến " + key + " = " + enviromentVariables.get(key));
        }
    }

}
``````

