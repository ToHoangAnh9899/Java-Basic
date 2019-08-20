## Sự khác nhau giữa overloading và overriding trong java

Nạp chồng phương thức (overloading) | Ghi đè phương thức (overriding)
------------ | -------------
Nạp chồng phương thức được sử dụng để giúp code của chương trình dễ đọc hơn.| Ghi đè phương thức được sử dụng để cung cấp cài đặt cụ thể cho phương thức được khai báo ở lớp cha.
Nạp chồng được thực hiện bên trong một class. | Ghi đè phương thức xảy ra trong 2 class có quan hệ kế thừa.
Nạp chồng phương thức thì tham số phải khác nhau.| Ghi đè phương thức thì tham số phải giống nhau.
Trong java, nạp chồng phương thức không thể được thực hiện khi chỉ thay đổi kiểu giá trị trả về của phương thức. Kiểu giá trị trả về có thể giống hoặc khác. Giá trị trả về có thể giống hoặc khác, nhưng tham số phải khác nhau.| Giá trị trả về phải giống nhau.

### Ví dụ nạp chồng phương thức

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
### Ví dụ ghi đè phương thức

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

## So sánh Array và ArrayList trong Java

Array | ArrayList
------------ | -------------
Array có kích thước cố định. Không thể thay đổi kích thước nếu nó đã được tạo. | đổi kích thước nếu nó đã được tạo.
Kích thước của ArrayList có thể thay đổi được. Kích thước của nó tự tăng (50% kích thước hiện có) nếu thêm một phần tử vượt quá sức chứa (compacity) hiện có của nó.
Có thể lưu trữ dữ liệu kiểu nguyên thủy và đối tượng. | Chỉ có thể lưu trữ dữ liệu kiểu đối tượng (Object). Kể từ Java 5, kiểu nguyên thủy được tự động chuyển đổi trong các đối tượng được gọi là auto-boxing. Ví dụ: không thể khai báo ArrayList<int>
Kích thước của Array có thể được kiểm tra bằng thuộc tính length.
Sử dụng for hoặc for-each để duyệt qua các phần tử của mảng. | Tương tự như Array, có thể duyệt qua các phần tử bằng lệnh for hoặc for-each. Tuy nhiên, nó có thể duyệt qua Iterator hoặc ListIterator. (https://gpcoder.com/2576-list-interface-trong-java/#ListIterator_Interface)
Kích thước của Array có thể được kiểm tra bằng thuộc tính length. | Kích thước của ArrayList được kiểm tra bằng phương thức size().
Không hỗ trợ kiểu Generic | Hỗ trợ kiểu Generic (https://viettuts.vn/java-new-features/generics-trong-java)
Các phần tử được thêm vào danh sách bằng lệnh gán. | Các phần tử được thêm vào danh sách bằng phương thức add().
