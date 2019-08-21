## 1. Khai báo chuỗi ký tự

Trong Java, để khai báo 1 chuỗi ký tự thì chúng ta có 2 cách như sau:

**Cách 1:**
Cú pháp
```
String tenChuoi = "giá_trị_khởi_tạo";
```
trong đó, **giá_trị_khởi_tạo** của chuỗi có thể có hoặc không và nếu có thì phải đặt trong cặp dấu " ". Nếu một chuỗi có **giá_trị_khởi_tạo = " "** thì chuỗi đó được gọi là chuỗi rỗng.

**Ví dụ**
```
public static void main(String[] args) {
    // khai báo chuỗi rỗng
    String chuoi1 = "";
         
    // khai báo chuỗi có nội dung là "Welcome"
    String chuoi2 = "Welcome";
         
    // hiển thị giá trị của 2 chuỗi trên ra màn hình
    System.out.println("Chuỗi rỗng có giá trị = " + chuoi1);
    System.out.println("Chuỗi 2 có giá trị = " + chuoi2);
}
```
Kết quả sau khi biên dịch chương trình:
*Chuỗi rồng có giá trị =
Chuỗi 2 có giá trị = Welcom*

**Cách 2**
Sử dụng từ khóa new
Cú pháp
```
String tenChuoi = new String("giá_trị");
```
trong đó giá_trị là một chuỗi bất kỳ và phải đặt trong cặp dấu " ".

```
public static void main(String[] args) {
    // khai báo một chuỗi có nội dung là "Welcome to Java!"
    String chuoi = new String("Welcome to Java!");
    System.out.println(chuoi);
}
```
Kết quả sau khi biên dịch chương trình:
*Welcome to Java!

## Các hàm xử lý chuỗi ký tự

### Hàm xác định độ dài chuỗi ký tự
Cú pháp
```
int length = tên_chuỗi.length();
```

**Chức năng: Hàm trả về độ dài chuỗi ký tự bằng cách đếm các ký tự trong chuỗi.**

```
public static void main(String[] args) {
    String chuoi;
    int doDai;
    Scanner scanner = new Scanner(System.in);
         
    System.out.println("Nhập vào chuỗi bất kỳ từ bàn phím: ");
    chuoi = scanner.nextLine();
         
    // tính độ dài chuỗi
    doDai = chuoi.length();
         
    System.out.println("Chuỗi " + chuoi + " có độ dài = " + doDai);
}
```
Kết quar sau khi biên dịch chương trình
*Nhập vào chuỗi bất kỳ từ bàn phím:
hello
Chuỗi hello có độ dài = 5*
