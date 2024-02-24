{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ไฟล์ PC - ไฟล์ซอร์สโค้ด Pro*C - ไฟล์ .pc คืออะไร และวิธีการเปิด",
  "description" : "เรียนรู้เกี่ยวกับไฟล์ซอร์สโค้ด PC Pro*C และวิธีการเปิด",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-th",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## ไฟล์พีซีคืออะไร

ไฟล์ PC หรือไฟล์ .pc เป็นไฟล์ซอร์สโค้ด ProC ProC เป็นพรีคอมไพเลอร์ที่ใช้กับฐานข้อมูล Oracle เพื่อฝังคำสั่ง SQL ภายในโค้ด C หรือ C++ เมื่อคุณคอมไพล์ไฟล์ Pro*C ไฟล์จะสร้างโค้ด C หรือ C++ ปกติพร้อมคำสั่ง SQL ที่ฝังอยู่ สิ่งนี้ทำให้คุณสามารถรวมการทำงานของฐานข้อมูล SQL เข้ากับโปรแกรม C หรือ C++ ของคุณได้อย่างราบรื่น

ต่อไปนี้คือตัวอย่างพื้นฐานของไฟล์ Pro*C ที่อาจมีลักษณะดังนี้:

```
#include <stdio.h>
#include <sqlca.h>

EXEC SQL INCLUDE sqlca;

int main() {
    EXEC SQL BEGIN DECLARE SECTION;
    int emp_id;
    char emp_name[50];
    EXEC SQL END DECLARE SECTION;

    /* Connect to database */
    EXEC SQL CONNECT :user IDENTIFIED BY :password;

    /* Fetch employee details */
    EXEC SQL SELECT employee_id, employee_name INTO :emp_id, :emp_name FROM employees WHERE employee_id = :input_id;

    /* Print fetched details */
    printf("Employee ID: %d\n", emp_id);
    printf("Employee Name: %s\n", emp_name);

    /* Disconnect from database */
    EXEC SQL COMMIT WORK RELEASE;
    return 0;
}
```

ในตัวอย่างนี้ คำสั่ง SQL จะขึ้นต้นด้วย EXEC SQL เพื่อระบุว่าเป็นคำสั่ง SQL ที่ฝังอยู่ คำสั่งเหล่านี้จะถูกประมวลผลโดยพรีคอมไพเลอร์ Pro*C เมื่อมีการคอมไพล์ไฟล์ และโค้ด C ที่เหมาะสมจะถูกสร้างขึ้นเพื่อโต้ตอบกับฐานข้อมูล Oracle

## เปิดไฟล์พีซีได้อย่างไร

หากต้องการเปิดไฟล์ PC โดยทั่วไปคุณจะต้องมีโปรแกรมแก้ไขข้อความหรือ Integrated Development Environment (IDE) ที่รองรับการแก้ไขซอร์สโค้ด C หรือ C++ นี่คือตัวเลือกทั่วไปบางส่วน:

1.  **เครื่องมือแก้ไขข้อความ:**
    
- **สมุดบันทึก** (วินโดวส์)
- **แก้ไขข้อความ** (Mac)
- **gedit** (ลินุกซ์)
- **ข้อความประเสริฐ**
- **อะตอม**
- **โค้ด Visual Studio**
2.  **สภาพแวดล้อมการพัฒนาแบบรวม (IDE):**
    
- **Eclipse** พร้อม CDT (เครื่องมือการพัฒนา C/C++)
- **Visual Studio** พร้อม Visual C++ หรือ Visual Studio Code พร้อมส่วนขยาย C++
- **รหัส::บล็อก**
- **NetBeans** พร้อมแพ็ก C/C++
  
## อ้างอิง
* [โปร*ซี](https://en.wikipedia.org/wiki/Pro*C)


