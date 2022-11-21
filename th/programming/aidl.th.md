{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ AIDL - ไฟล์ภาษานิยามอินเทอร์เฟซ Android",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ AIDL พร้อมตัวอย่างและ API ที่สามารถสร้างและเปิดไฟล์ AIDL",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## ไฟล์ AIDL คืออะไร??

ไฟล์ AIDL (Android Interface Definition Language) ช่วยให้นักพัฒนา Android สร้างการสื่อสารระหว่างแอพต่างๆ ตามอินเทอร์เฟซการเขียนโปรแกรม ทั้งไคลเอนต์และบริการตกลงที่จะสื่อสารโดยใช้การสื่อสารระหว่างกระบวนการ (IPC) ไฟล์ AIDL มีซอร์สโค้ด [Java](/th/programming/java/) สำหรับกำหนดอินเทอร์เฟซและสัญญาสำหรับการสื่อสารระหว่างแอป

คุณสามารถเปิดไฟล์ AIDL ด้วย Google Android Studio หรือโปรแกรมแก้ไขข้อความใดๆ เช่น Microsoft Notepad และ Notepad++

## รูปแบบไฟล์ AIDL - ข้อมูลเพิ่มเติม

AIDL เป็นไฟล์ข้อความที่มีอินเทอร์เฟซสำหรับการสื่อสารระหว่างแอพต่างๆ Android OS ไม่อนุญาตให้กระบวนการหนึ่งเข้าถึงหน่วยความจำของกระบวนการอื่น สิ่งนี้นำไปสู่กระบวนการแยกออบเจ็กต์ออกเป็นแบบพื้นฐานเพื่อความเข้าใจในระบบปฏิบัติการพื้นฐาน และสร้างกระบวนการโครงสร้างการสื่อสารสำหรับนักพัฒนา

### ประเภทข้อมูลใดบ้างที่ AIDL รองรับ

AIDL รองรับประเภทข้อมูลต่อไปนี้ตามค่าเริ่มต้น

* ประเภทดั้งเดิมทั้งหมดในภาษาโปรแกรม Java (เช่น int, long, char, boolean และอื่นๆ)
* สตริง
* ลำดับอักขระ
* รายการ
* แผนที่

## ตัวอย่างไฟล์ AIDL

ต่อไปนี้เป็นตัวอย่างไฟล์ AIDL

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## อ้างอิง

* [ภาษาคำจำกัดความของอินเทอร์เฟซ Android (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

