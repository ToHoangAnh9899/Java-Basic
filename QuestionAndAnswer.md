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

### Ví dụ
Khởi tạo một mảng có 5 phần tử: bạn không thể thêm phần tử thứ 6 vào mảng hoặc thay đổi kích thước của nó.

```
int []arr = new int[5];
 
arr[5] = 6;
```
Khi thực thi chương trình trên, bạn sẽ gặp lỗi **java.lang.ArrayIndexOutOfBoundsException.**

Tuy nhiên, đối với ArrayList không bị giới hạn về số lượng phần tử. Khi vượt quá kích thước khởi tạo, nó tự động tăng lên 50% để lưu thêm phần tử mới.

```
import java.lang.reflect.Field;
import java.util.ArrayList;
 
public class ArrayExample {
    public static void main(String[] args) throws Exception {
        ArrayList<String> list = new ArrayList<>(5);
        list.add("Item01");
        list.add("Item02");
        list.add("Item03");
        list.add("Item04");
        list.add("Item05");
        list.add("Item06");
        System.out.format("Size: %d", list.size());
    }
}
```
Kết quả thực thi chương trình trên:

**Size : 6**

## Sự khác nhau giữa String và StringBuffer trong java

String | StringBuffer
------------ | -------------
Lớp String là bất biến (immutable). | Lớp StringBuffer là có thể sửa đổi (mutable).
Khi bạn thực hiện nối nhiều chuỗi thì lớp String xử lý chậm và tốn nhiều bộ nhớ hơn, bởi vì mỗi lần nối thêm chuỗi nó tạo ra instance mới. | Khi bạn thực hiện nối nhiều chuỗi thì lớp StringBuffer xử lý nhanh và tốn ít bộ nhớ hơn.
Lớp String ghi đề phương thức equals() của lớp Object. Vì thế bạn có thể so sánh nội dung của 2 chuỗi bằng phương thức equals(). | Lớp StringBuffer không ghi đề phương thức equals() của lớp Object.

### Test hiệu suất của String và StringBuffer
```
public class ConcatTest {
    public static String concatWithString() {
        String t = "Java";
        for (int i = 0; i < 10000; i++) {
            t = t + "Hello";
        }
        return t;
    }
 
    public static String concatWithStringBuffer() {
        StringBuffer sb = new StringBuffer("Java");
        for (int i = 0; i < 10000; i++) {
            sb.append("Hello");
        }
        return sb.toString();
    }
 
    public static void main(String[] args) {
        long startTime = System.currentTimeMillis();
        concatWithString();
        System.out.println("Thời gian nối chuỗi của lớp String: "
                + (System.currentTimeMillis() - startTime) + "ms");
        startTime = System.currentTimeMillis();
        concatWithStringBuffer();
        System.out.println("Thời gian nối chuỗi của lớp StringBuffer: "
                + (System.currentTimeMillis() - startTime) + "ms");
    }
}

```

Output

**Thời gian nối chuỗi của lớp String: 350ms
Thời gian nối chuỗi của lớp StringBuffer: 1ms**
