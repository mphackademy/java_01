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


