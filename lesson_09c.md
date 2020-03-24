Nguồn: https://docs.oracle.com/javase/tutorial/java/IandI/abstract.html

``````java
package oop;

public interface Bicycle {
    //  wheel revolutions per minute
    void changeCadence(int newValue);

    void changeGear(int newValue);

    void speedUp(int increment);

    void applyBrakes(int decrement);

}

``````

``````java
package oop;

public class ACMEBicycle implements Bicycle {

    int cadence = 0;
    int speed = 0;
    int gear = 1;

    // The compiler will now require that methods
    // changeCadence, changeGear, speedUp, and applyBrakes
    // all be implemented. Compilation will fail if those
    // methods are missing from this class.

    public void changeCadence(int newValue) {
        cadence = newValue;
    }

    public void changeGear(int newValue) {
        gear = newValue;
    }

    public void speedUp(int increment) {
        speed = speed + increment;
    }

    public void applyBrakes(int decrement) {
        speed = speed - decrement;
    }

    void printStates() {
        System.out.println("cadence:" +
                cadence + " speed:" +
                speed + " gear:" + gear);
    }
}
``````

### Sửa lại một chút cho vui.

``````java
package oop;

/**
 * Xe đạp
 */
public interface Bicycle {
    //  wheel revolutions per minute

    /**
     * Số vòng quay của bánh xe mỗi phút.
     *
     * @param newValue Giá trị mới của Số vòng quay/phút.
     */
    void changeCadence(int newValue);

    /**
     * Sang số.
     *
     * @param newValue
     */
    void changeGear(int newValue);

    /**
     * Tăng tốc lên nào.
     *
     * @param increment
     */
    void speedUp(int increment);

    /**
     * Phanh kít.
     *
     * @param decrement
     */
    void applyBrakes(int decrement);

}
``````

``````java
package oop;

/**
 * Xe đạp Thống Nhất - Made in Vietnam.
 */
public class ThongNhatBicycle implements Bicycle {
    
    @Override
    public void changeCadence(int newValue) {
        System.out.println("Thay đổi số vòng quay/phút.");
    }

    @Override
    public void changeGear(int newValue) {
        System.out.println("Đổi số");
    }

    @Override
    public void speedUp(int increment) {
        System.out.println("Tăng tốc rồi, đi nhanh quá bạn ơi.");
    }

    @Override
    public void applyBrakes(int decrement) {
        System.out.println("Đã phanh rồi nhé, vì phía đằng trước là cái ổ gà.");
    }
}
``````




