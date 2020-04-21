# Sự khác biệt giữa 3 khái niệm trên:
```
1. Dependency Inversion: Đây là một nguyên lý để thiết kế và viết code.

2. Inversion of Control: Đây là một design pattern được tạo ra để code có thể tuân thủ nguyên lý Dependency Inversion. 
Có nhiều cách hiện thực pattern này: ServiceLocator, Event, Delegate, … Dependency Injection là một trong các cách đó.

3. Dependency Injection: Đây là một cách để hiện thực Inversion of Control Pattern (Có thể coi nó là một design pattern riêng cũng được). 
Các module phụ thuộc (dependency) sẽ được inject vào module cấp cao.
```
***Dependency Inversion***
```
1. High-level modules should not depend on low-level modules. Both should depend on abstractions. 
**High-lever module <-> abstract/interface <-> low-level module**
Các module cấp cao không nên phụ thuộc vào các module cấp thấp. Cả 2 nên phụ thuộc vào abstraction (hay interface).
2. Abstractions should not depend upon details. Details should depend upon abstractions. 
Interface (abstraction) không nên phụ thuộc vào mô đun cụ thể, 
mà ngược lại mô đun cụ thể phải phụ thuộc vào khung trìu tượng hoặc interface. 
(Các class giao tiếp với nhau thông qua interface, không phải thông qua implementation.)
```
