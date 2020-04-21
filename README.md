# SOLID-principle
1. **Single Responsibility Principle  – Nguyên lý Đơn Trách Nhiệm**. Nội dung nguyên lý:
```
Một class chỉ nên giữ một trách nhiệm duy nhất 
(Chỉ có thể thay đổi class vì một lý do duy nhất)
 _ Một module chỉ có 1 chức năng duy nhất(Nói vậy chứ việc xác định, gom nhóm chức năng không hề dễ đâu nhé)
```
2. **Open/Closed Principle – Nguyên lý Đóng Mở**. Nội dung nguyên lý:
```
Có thể thoải mái mở rộng 1 module, nhưng hạn chế sửa đổi bên trong module đó (open for extension but closed for modification).
khẩu súng. Để bắn được xa hơn, ta có thể gắn thêm ống ngắm; để không gây tiếng động, ta có thể gắn nòng giảm thanh; để tăng số lượng đạn, ta có thể gắn thêm băng đạn phụ;
// Ta có 3 class: vuông, tròn, tam giác, kế thừa class Shape (){ public double Area(); }
// Chuyển logic tính diện tích vào mỗi class
```
3. **Liskov Substitution Principle – Nguyên lý Thay Thế Lít Kốp**. Nội dung nguyên lý:
```
Để giữ tính đúng đắn của chương trình, class con phải thay thế được class cha.
Trong đời sống, A là B (chim cánh cụt là chim) không có nghĩa là class A nên kế thừa class B. Chỉ cho class A kế thừa class B khi class A thay thế được cho class B.
public class Bird {
  public virtual void Fly() { Console.Write("Fly"); }
}
public class Eagle : Bird {
  public override void Fly() { Console.Write("Eagle Fly"); }
}
public class Duck : Bird {
  public override void Fly() { Console.Write("Duck Fly"); }
}
public class Penguin : Bird {
  public override void Fly() { throw new NoFlyException(); }
}
```
4. **Interface Segregation Principle – Nguyên lý phân tách interface**. Nội dung nguyên lý:
```
Interface là một lớp rỗng chỉ chứa khai báo về tên phương thức không có khai báo về thuộc tính hay thứ gì khác và các phương thức này cũng là rỗng. Bởi vậy bất kỳ lớp nào sử dụng lớp interface đều phải định nghĩa các phương thức đã khai báo ở lớp interface.
```
```
Điều này tương đương với việc nếu ta tạo ra 1 interface bự (hơn 100 method chẳng hạn), mỗi class sẽ phải implement toàn bộ 100 method đó, kể những method không bao giờ sử dụng đến. Nếu áp dụng ISP, ta sẽ chia interface này ra thành nhiều interface nhỏ, các class chỉ cần implement những interface có chức năng mà chúng cần, không cần phải implement những chức năng thừa nữa.
```
