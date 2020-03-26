### Chuyển đổi số sang ký tự, và từ ký tự sang số.

``````java
public class StringConvert {

    public static void main(String[] args) {
        double piNumber;
        String stringValue;

        // Chuyển từ ký tự --> số.
        piNumber = Double.parseDouble("3.1415926535897932384626433");

        // Chuyển từ số --> ký tự, để in ra màn hình.
        System.out.println("Số PI là "+  Double.toString(piNumber));
    }

}

``````
