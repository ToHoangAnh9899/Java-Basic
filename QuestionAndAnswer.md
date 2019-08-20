## Sự khác nhau giữa overloading và overriding trong java

Nạp chồng phương thức (overloading) | Ghi đè phương thức (overriding)
------------ | -------------
Nạp chồng phương thức được sử dụng để giúp code của chương trình dễ đọc hơn.| Ghi đè phương thức được sử dụng để cung cấp cài đặt cụ thể cho phương thức được khai báo ở lớp cha.
Nạp chồng được thực hiện bên trong một class. | Ghi đè phương thức xảy ra trong 2 class có quan hệ kế thừa.
Nạp chồng phương thức thì tham số phải khác nhau.| Ghi đè phương thức thì tham số phải giống nhau.
Trong java, nạp chồng phương thức không thể được thực hiện khi chỉ thay đổi kiểu giá trị trả về của phương thức. Kiểu giá trị trả về có thể giống hoặc khác. Giá trị trả về có thể giống hoặc khác, nhưng tham số phải khác nhau.| Giá trị trả về phải giống nhau.

## Ví dụ nạp chồng phương thức

```
public class OverloadingExample {
    static int add(int a, int b) {
        return a + b;
    }
 
    static int add(int a, int b, int c) {
        return a + b + c;
    }
}
```
## Ví dụ ghi đè phương thức

```
class Animal {
    void eat() {
        System.out.println("eating...");
    }
}
 
class Dog extends Animal {
    void eat() {
        System.out.println("eating bread...");
    }
}
```
