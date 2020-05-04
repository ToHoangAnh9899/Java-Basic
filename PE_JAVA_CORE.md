# Practice Exam Java core

<br />

## Bài 1

> **Cho đoạn string sau đây : <br /> "java is a general-purpose programming language that is class-based,object-oriented,And designed to have as few implementation dependencies as possible.It is intended to let application developers write once,Run anywhere"**

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
//nguyen thuy (int , char , double, float..)
//doi tuong (String, StringBuilder, StringBuffer..)
public class StringPE {

    // to hoang anh
    public static String nomallyString(String str) {
        String results = "";
        //insert space after "." and ","
        String strL = str.toLowerCase();
        for (int i = 0; i < strL.length() - 1; i++) {
            if (strL.charAt(i) == '.' && strL.charAt(i + 1) != ' ') {
                results = strL.replaceAll("\\.", ". ");
            }
            if (strL.charAt(i) == ',' && strL.charAt(i + 1) != ' ') {
                results = results.replaceAll("\\,", ", ");
            }
        }
        StringBuilder builder = new StringBuilder(results);
        
        for(int i = 0 ; i < builder.length()-2 ; i++ ){
            if(builder.charAt(i) == '.'){
                builder.setCharAt(i+2, Character.toUpperCase(builder.charAt(i+2)));
            }
        }
        
        results = builder.toString();
        
        
        //uppercase first character
        results = results.replaceFirst(results.charAt(0) + "", Character.toUpperCase(results.charAt(0)) + "");
        //insert dot in last string
        results += ".";

        return results;
    }

    public static void main(String[] args) {
        System.out.println("OUTPUT:");
        String str = "java is a general-purpose programming language that is class-based,object-oriented,And designed to have as few.implementation dependencies as possible.it is intended to let application developers write once,Run anywhere";
        System.out.println(nomallyString(str));
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
