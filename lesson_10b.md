#### Mẹo khi lập trình.

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

        //TODO: Lấy thêm ví dụ về ký tự Unicode trong Tiếng Việt.

        System.out.println(charValue);
        //FIXME: Khi mà gửi cho khách hàng, thì xóa dòng này đi trước đã.

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
    //TODO: Lấy id của công ty trước khi xử lý đơn hàng.

}

``````

1. Viết linh tinh vài ký tự sai syntax, để đánh dấu vị trí đang làm việc dở dang khi cần đi ra ngoài gấp.
2. Comment lại biến, hàm, class, IDE sẽ báo đỏ, khi đó chúng ta sẽ biết biến/hàm/class được tham chiếu, được dùng ở đâu.
3. Sử dụng ``// TODO: `` để tạo ghi chú công việc cần phải làm, khi có quá nhiều việc, dễ bị lãng quên.
4. Sử dụng ``// FIXME`` để tạo nhắc nhở phải sửa mã nguồn, vì hiện tại đang bị sai.

Có thể viết: ``//TODO`` hoặc ``//FIXME`` (không có dấu cách sau ``//``), áp dụng được cho cả IntelliJ IDEA và Eclipse, và có lẽ cả NetBeans IDE (các bạn học viên lúc nào có thời gian tự thử nghiệm nhé).

