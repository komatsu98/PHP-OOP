# PHP-OOP
| Public | Protected | Private |
|---|---|---|
| Có thể được access ở trong, ngoài class khai báo nó và các class kế thừa class đó | Chỉ có thể được access ở trong class khai báo nó và các class kế thừa class đó | Chỉ có thể được access ở trong class khai báo nó |


|   | Trait | Interface class | Abstract class |
|---|---|---|---|
| Khái niệm | Là một nhóm các method mà ta muốn include vào một class nào đó. Hoạt động như copy paste các method vào class đích để tránh việc lặp lại code. | Là một class "abstract hoàn toàn". Tất cả method của nó không thể implement và thay vì nói một class con nào đó của interface, ta nói class ấy implement interface đó. Như là khung xương được implement cho các nhu cầu khác nhau. Lưu ý: Không thể đặt tên interface giống với tên class. | Là class mà chỉ có thể được implement một phần bởi lập trình viên. Class này có thể chứa một hay nhiều abstract method, các method đó phải được định nghĩa bởi các class con extend class này để có thể sử dụng với các hình thức khác nhau. Lưu ý: Không thể định nghĩa một abstract method trong một class non-abstract|
| Khác nhau 1 vs 2| Cung cấp khả năng thực hiện việc nào đó cho object | Chỉ ra object có thể làm việc nào đó|  |
| Khác nhau 2 vs 3 | | Không có method nào được implement | Implement 1 phần | 
| Một số ứng dụng | Khi muốn thêm method nào đó cho nhiều object (nhưng không phải tất cả) cùng implement một interface | Xây dựng interface DB | Xây dựng các method cùng tên nhưng thực hiện khác nhau cho các object cùng implement một số method nào đó |

|Từ khóa final|
|---|
|Ngăn chặn các class con ghi đè method
Ví dụ đoạn code sau sẽ báo lỗi: ```Fatal error: Cannot override final method BaseClass::moreTesting()```
``` 
<?php

   class BaseClass {
     ...
      
      final public function moreTesting() {
         echo "BaseClass::moreTesting() called<br>";
      }
   }
   
   class ChildClass extends BaseClass {
      public function moreTesting() {
         echo "ChildClass::moreTesting() called<br>";
      }
   }
?> 
```
|
