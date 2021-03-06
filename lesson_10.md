#### Thực hành kiểu dữ liệu

``````java
public class DeclarationsExample {

    public static void main(String[] args) {
        // Giá trị mặc định là false nếu chỉ khai báo biến mà không gán giá trị.
        // boolean booleanValue = true;
        boolean booleanValue;

        // Ký tự Unicode UTF-16.
        char charValue = '\u0990';  // Ґ
        // u0490 Ґ
        // u0491 ґ
        // u0492 Ғ
        // u0992 ঒

        System.out.println(charValue);

        byte foo;  // Kích thước 1 byte, giá trị từ -127 đến 127.
        short bar; // Kích thước 2 bytes (= 16 bit). Giá trị từ -32_768 đến 32_767.

        short largeShortNumber = 32767; // Không bị lỗi, đây là giá trị lớn nhất của kiểu dữ liệu short.
        // short largeShortNumber = 32768; // Sẽ bị lỗi.
        System.out.println(largeShortNumber);

        int integerValue; // 4 bytes (32 bits), giá trị từ -2^16 đến +2^16 -1.
        long longValue; // 8 bytes (64 bit), giá trị từ 2^32 đến 2^32 - 1.

        float floatValue = 3.14159F;
        double doubleValue = 0.339;
        
        String descriptionSentence = "Hôm nay tôi đi học muộn.";
        String newDescriptionSentence = descriptionSentence.replace("nay", "qua");
        System.out.println(newDescriptionSentence);


    }

}
``````

#### Tầm vực của field

``````java
public class TestClass {

    private long visibleOnlyThisClass;
    double visibleFromEntirePackage;

    void setLong(long valueFoo) {
        visibleOnlyThisClass = valueFoo;
    }

    long getLong() {
        return visibleOnlyThisClass;
    }

}
``````

### Truy cập biến có tầm vực ``private`` bởi phương thức trung gian

``````java
public class VisibilityCheck {

    public static void main(String[] args){
        TestClass testClass = new TestClass();
        testClass.setLong(42);

        testClass.visibleFromEntirePackage = 3.14;
        System.out.println(testClass.getLong());

        System.out.println(testClass.visibleFromEntirePackage);
    }

}
``````


