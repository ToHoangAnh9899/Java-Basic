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

*Chuỗi rồng có giá trị =*

*Chuỗi 2 có giá trị = Welcom*

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

*Welcome to Java!*

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

*Nhập vào chuỗi bất kỳ từ bàn phím:*

*hello*

*Chuỗi hello có độ dài = 5*

### Hàm nối 2 chuỗi ký tự
Trong Java, để nối 2 chuỗi ký tự lại với nhau thì chúng ta có 2 cách. Cách thứ nhất là chúng ta dùng dấu + để nối chuỗi (cách này tôi đã đề cập trong các bài trước) và cách thứ hai là dùng phương thức concat(). 

**Cú pháp**
```
String string3 = string1.concat(String string2);
```
**Chức năng: Hàm có tác dụng nối chuỗi string2 vào string1 và trả về chuỗi string3.**

**Ví dụ**

```
public static void main(String[] args) {
    String chuoi1 = "Happy ", chuoi2 = "new year!";
 
    /* 
     * nối chuỗi
     */
    String chuoi3 = chuoi1.concat(chuoi2);
    System.out.println(chuoi3); 
}
```
Kết quả sau khi biên dịch chương trình:

*Happy new year*

### Hàm trả về một ký tự trong chuỗi.

**Lưu ý:** Một chuỗi là tập hợp các ký tự và ký tự đầu tiên trong chuỗi sẽ có chỉ số (index) là 0. Ví dụ: một chuỗi có chiều dài là 10 thì chỉ số của các ký tự trong chuỗi đó sẽ được đánh số từ 0 đến 9.

Cú pháp:
```
char character = chuoi.charAt(int index);
```

**Chức năng: Hàm trả về ký tự character trong chuỗi có chỉ số là index.**
Ví dụ

```
public static void main(String[] args) {
    String chuoi = "Happy new year!";
         
    /* 
     * trả về ký tự có chỉ số là 4 trong chuỗi
     * ký tự 'H' có chỉ số là 0 
     * nên ký tự có chỉ số 4 là ký tự 'y'
     */
    char character = chuoi.charAt(4);
    System.out.println(character);
}
```
Kết quả sau khi biên dịch chương trình:

*y*

### Hàm so sánh 2 chuỗi ký tự
**Cú pháp**
```
int result = string1.compareTo(String string2);
```
**Chức năng: Hàm có tác dụng so sánh hai chuỗi string1, string2 và trả về kết quả:**

Nếu result = 0 thì hai chuỗi đó bằng nhau.

Nếu result < 0 thì chuỗi string1 < string2.

Nếu result > 0 thì chuỗi string1 > string2.

```
public static void main(String[] args) {
    int result;
    String string1 = "Happy new year!";
    String string2 = "Happy new year!";
         
    result = string1.compareTo(string2);
    if (result == 0) {
        System.out.println("Chuỗi " + string1 + " = " + string2);
    } else if (result < 0) {
        System.out.println("Chuỗi " + string1 + " < " + string2);
    } else {
        System.out.println("Chuỗi " + string1 + " > " + string2);
    }
}
```
Kết quả sau khi biên dịch chương trình:

*Chuỗi Happy new year! = Happy new yaer!*

### Hàm trả về vị trí xuất hiện đầu tiên của một chuỗi trong chuỗi khác.

**Cú pháp**


```
int result = string1.indexOf(String string2);
```

**Chức năng**: Hàm trả về vị trí xuất hiện đầu tiên của chuỗi string2 trong string1. Nếu chuỗi string2 không có trong chuỗi string1 thì kết quả trả về result = -1.

Ví dụ

```
public static void main(String[] args) {
    int result;
    String string1 = "Happy new year!";
    String string2 = "new year!";
         
    result = string1.indexOf(string2);
    System.out.println("Vị trí đầu tiên xuất hiện chuỗi " + string2 + 
        " trong chuỗi " + string1 + " = " + result);
}
```
Kết quả sau khi biên dịch chương trình:

*Vị trí đầu tiên xuất hiện chuỗi dsđs trong chuỗi Happy new year! = -1*

### Hàm trả về vị trí xuất hiện cuối cùng của một chuỗi trong chuỗi khác.

**Cú pháp**

```
int result = string1.lastIndexOf(String string2);
```

**Chức năng:** Hàm trả về vị trí xuất hiện cuối cùng của chuỗi string2 trong string1. Nếu chuỗi string2 không có trong chuỗi string1 thì kết quả trả về result = -1.

Ví dụ
```
public static void main(String[] args) {
    int result;
    String string1 = "Happy new year and new year!";
    String string2 = "new year!";
         
    result = string1.lastIndexOf(string2);
    System.out.println("Vị trí cuối cùng xuất hiện chuỗi " + string2 + 
        " trong chuỗi " + string1 + " = " + result);
}
```
Kết quả sau khi biên dịch chương trình:
*Vị trí cuối cùng xuất hiện chuỗi new year! trong chuỗi Happy new year and new year! = 19

### Hàm thay thế một chuỗi con trong chuỗi ký tự bằng chuỗi khác
**Cú pháp**

```
string1.replace(char oldChar, char newChar);
```
**Chức năng:** Hàm sẽ thay thế ký tự oldChar bằng ký tự newChar trong chuỗi string1. Nếu ký tự cần thay thế không có trong chuỗi string1 thì chương trình sẽ trả về chuỗi string1.

Ví dụ

```
public static void main(String[] args) {
    String string1 = new String("Happy new year!");
         
    // ký tự thay thế 'l' không có trong chuỗi string1
    System.out.println(string1.replace('l', 'r'));
         
    // thay thế ký tự 'y' trong string1 thành 'r'
    System.out.println("Chuỗi sau khi thay thế là " + 
        string1.replace('y', 'r'));
}
```
Kết quả sau khi biên dịch chương trình:

*Happy new year!
Chuỗi sau khi thay thế là Happr new rear!

### Hàm loại bỏ các khoảng trắng thừa ở đầu và cuối chuỗi

**Cú pháp**

```
String string1 = string1.trim();
```

**Chức năng:** Hàm sẽ loại bỏ các khoảng trắng thừa ở đầu và cuối chuỗi string1. Nếu chuỗi đó không có khoảng trắng thừa thì chương trình sẽ trả về chuỗi gốc.

Ví dụ

```
public static void main(String[] args) {
    String string1 = new String("   Welcome to Class Java Lab!   ");
         
    // loại bỏ các khoảng trắng thừa trong chuỗi string1
    string1 = string1.trim();
         
    System.out.println("Chuỗi sau khi loại bỏ khoảng trắng thừa là " + string1);
}
```
Kết quả sau khi biên dịch chương trình:

*Chuỗi sau khi loại bỏ khoảng trắng thừa là Welcome to Class Java Lab!*

### Hàm tạo một chuỗi con từ vị trí index trong chuỗi cha

**Cú pháp**

```
String chuoiCon = chuoiCha.substring(int beginIndex);
String chuoiCon = chuoiCha.substring(int beginIndex, int endIndex);
```
**Chức năng:** Hàm sẽ tạo một chuỗi con từ vị trí có chỉ số là beginIndex trong chuỗi cha. Trong cú pháp thứ 2, thì hàm sẽ tạo một chuỗi con bắt đầu từ vị trí có chỉ số là beginIndex và kết thúc tại vị trí có chỉ số endIndex - 1 trong chuỗi cha.

Ví dụ
```
public static void main(String[] args) {
    String chuoiCha = new String("Welcome to Freetuts.net!");
         
    // tạo một chuỗi con từ vị trí 11 trong chuỗi string1
    String chuoiCon1 = chuoiCha.substring(11);  // Freetuts.net!
    System.out.println(chuoiCon1);
         
    /*
     * tách một chuỗi con bắt đầu từ vị trí 11
     * và kết thúc tại vị trí 19 trong chuỗi cha
     */
    String chuoiCon2 = chuoiCha.substring(11, 19);  // Freetuts
    System.out.println(chuoiCon2);
}
```
Kết quả sau khi biên dịch chương trình:

*Freetuts.net!*

*Freetuts*
