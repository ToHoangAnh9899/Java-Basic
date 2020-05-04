# Practice Exam Java core

<br />

## Bài 1

> **
Cho đoạn string sau đây :
"java is a general-purpose programming language that is class-based,object-oriented,And designed
to have as few implementation dependencies as possible.It is intended to let application developers write once,Run anywhere"
**

Hãy chuẩn hóa đoạn chuỗi trên theo các yêu cầu sau : 

- Chữ cái đầu tiên của đầu đoạn văn phải in hoa, ví dụ : "Java"
- Cuối của đoạn phải có dấu chấm câu "."
- Sau dấu phẩy dấu chấm câu phải được cách bởi kí tự space " ".
- Sau dấu chấm câu chữ đầu tiên phải được viết in hoa còn lại đều là chữ in thường.


<br />

Template:
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package pedemo;

/**
 *
 * @author To Hoang Anh
 */
public class StringPE {

    public static String nomallyString(String str) {
    // Add your code in here:

    }
    
    // Fixed Do not edit anything here.
    public static void main(String[] args) {
    	System.out.println("OUTPUT:");
        String str = "java is a general-purpose programming language that is class-based,object-oriented,And designed to have as few 		implementation dependencies as possible.It is intended to let application developers write once,Run anywhere";
        
    }
}

```

<br />

Màn hình kết quả chương trình:

Test case 1
```java
Java is a general-purpose programming language that is class-based, object-oriented, and designed to have as few implementation dependencies as possible. It is intended to let application developers write once, run anywhere.
```
<br />

## Bài 2

> **Nhập 1 chuỗi string sau đó đếm số lần xuất hiện của các kí tự, số lần xuất hiện của các từ có trong chuỗi nhập vào.**

<br />

Template:
```java
package counter;

public class Counter {

    public static void main(String[] args) {
    // Add your code in here:
    }
    
    // Fixed Do not edit anything here.
    public void display() {
    System.out.println("OUTPUT:");
    // Add your code in here:
    }

    public void analyze(String content) {
    // Add your code in here:
    }
}

```

<br />

Màn hình kết quả chương trình:

Test case 1
```java
Enter your content: 
to hoang anh
{anh=1, to=1, hoang=1}
{a=2, t=1, g=1, h=2, n=2, o=2}
BUILD SUCCESSFUL (total time: 3 seconds)
```

<br />
