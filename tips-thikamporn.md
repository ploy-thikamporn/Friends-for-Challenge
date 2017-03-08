# C Programing Tips #

> เทคนิคบางอย่างที่อาจต้องรู้ เพื่อช่วยในการเขียนภาษา C

### math-code ###
*  HOW TO DEVIDE OF TWO NUMBERS // การหาร โดยใช้ "/" 
    * สำหรับการหาร ถ้าจำนวนทั้ง 2 จำนวนเป็น "integer" แล้วหารลงตัว 
    ~~~
        #include <stdio.h>
        int main()
        {
            int a = 4, b = 2, total;
            total = a/b;
            printf("%d", total);  /// total = 2 
        }
    
    ~~~
    
    * สำหรับการหาร ถ้าจำนวนทั้ง 2 จำนวนเป็น "float หรือ double" แล้วหารลงตัว 
    ~~~
        #include <stdio.h>
        int main()
        {
            float a = 4, b = 2, total;
            total = a/b;
            printf("%f", total);  /// total = 2.000000 
        }
    
    ~~~
    * สำหรับการหาร ถ้าจำนวนทั้ง 2 จำนวนเป็น "integer" แล้วหารลงไม่ตัว 
    ~~~
        #include <stdio.h>
        int main()
        {
            int a = 5, b = 2, total;
            total = a/b;
            printf("%d", total);  ///** จะพบว่า total = 2 ซึ่งค่าที่ได้จริงๆจะต้องเป็น total = 2.5
        }
    ~~~
        ---------------------------------------------------------------------------------------
        
            * กรณีนี้มีทางแก้ไขได้ 
            -- คือการ แก้ไข type ของตัวแปร ให้เป็น float ทั้ง 2 ตัวแปรร หรือตัวใดตัวนึงก็ได้
            
               #include <stdio.h>
               int main()
               {
                     float a = 5, b = 2, total;
                     total = a/b;
                     printf("%d", total);  ///** จะพบว่า total = 2 ซึ่งค่าที่ได้จริงๆจะต้องเป็น total = 2.5
               }
             
            
            **สำหรับโจทย์ที่ถูกกำหนด ข้อมูลเข้าเป็น integer ทั้ง 2 ตัว แต่ต้องการผลที่ได้จากการคำนวณเป็นเป็นจำนวนจริง คือ
                -กำหนด type ที่ต้องการ ให้เลขพวกนั้นใหม่ ในขั้นตอนกาคำนวณ-
                
                    #include <stdio.h>
                    int main()
                    {
                        int a = 5, b = 2;
                        printf("%f", (float)a/(float)b);  ///** total = 2.500000
                    }
          
                    หรือ
          
                    #include <stdio.h>
                    int main()
                    {
                        int a = 5, b = 2;
                        printf("%f", a./b);  ///** total = 2.500000
                    }
             
                    หรือ
              
                    #include <stdio.h>
                    int main()
                    {
                        int a = 5, b = 2;
                        printf("%f", a.0/b);  ///** total = 2.500000
                    }
              
                    

### standard-input-output ###
*   การรับค่าจาก standard input
*   การพิมพ์ค่าไปที่ standard output

### sorting ###
*   ตัวอย่างการใช้ Bubble Sort เรียงค่าน้อยไปมาก , มากไปน้อย
