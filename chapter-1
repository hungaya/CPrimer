**Chapter 1: Getting Started**

Exercise 1.2
```cpp
int main() {
    return -1;
}
```

Exercise 1.3
```cpp
#include <iostream>

int main() {
    std::cout << "Hello, World" << std::endl;
    return 0;
}
```

Exercise 1.4
```cpp
#include <iostream>

int main() {
    std::cout << "Enter two numbers: " << std::endl;
    int v1 = 0, v2 = 0;
    std::cin >> v1 >> v2;
    std::cout << "The multiplication of " << v1 << " and " << v2
              << " is " << v1 * v2 << std::endl;
    return 0;
}
```

Exercise 1.5
```cpp
#include <iostream>

int main() {
    std::cout << "Enter two numbers: ";
    std::cout << std::endl;

    int v1 = 0;
    int v2 = 0;

    std::cin >> v1;
    std::cin >> v2;

    std::cout << "The sum of ";
    std::cout << v1;
    std::cout << " and ";
    std::cout << v2;
    std::cout << " is ";
    std::cout << v1 + v2;
    std::cout << std::endl;

    return 0;
}
```

Exercise 1.6
```cpp
std::cout << "The sum of " << v1;            // 1
          << " and " << v2;                  // 2
          << " is " << v1 + v2 << std::endl; // 3
```
Tại dòng thứ 2
* Toán tử `<<` bên trái không hợp lệ. Vì `<<` là toán tử hai ngôi, và đoạn code thiếu số hạng bên trái (left operand).
* Toán tử `<<` bên phải không hợp lệ. Số hạng bên trái của `<<` là biến kiểu `ostream`, nhưng đoạn code lại là một chuỗi `" and "` kiểu `string`.

Tại dòng thứ 3
* Toán tử `<<` thứ nhất không hợp lệ. Vì `<<` là toán tử hai ngôi, và đoạn code thiếu số hạng bên trái .
* Toán tử `<<` thứ hai không hợp lệ. Số hạng bên trái của `<<` là biến kiểu `ostream`, nhưng đoạn code lại là một chuỗi `" is "` kiểu `string`.
* Toán tử `<<` thứ ba không hợp lệ. Vì số hạng bên trái của `<<` là `v1 + v2`, mang kiểu `int`.

Exercise 1.8
Đúng
```cpp
std::cout << "/*";
```
Đúng
```cpp
std::cout << "*/";
```
Sai, comment trong đoạn code là `/* "*/`, dẫn đến các ký tự còn lại sau `<<` là ``" */`. Tuy nhiên, `" */` không là chuỗi do thiếu dấu nháy kép bên phải " (`" */"`)
```cpp
std::cout << /* "*/" */;
```
Đúng, comment thứ nhất là `/* "*/` bên phải toán tử `<<`, comment thứ hai là `/*" */` bên trái kí tự kết thúc `;`. Dẫn đến số hạng bên phải của toán tử `<<` là `" /* "`.
```cpp
std::cout << /* "*/" /* "/*" */;
```

Exercise 1.9
```cpp
#include <iostream>
int main() {
    int sum = 0, val = 50;
    while (val <= 100) {
        sum += val;
        ++val;
    }
    std::cout << "Sum of 50 to 100 inclusive is "
              << sum << std::endl;
    return 0;
}
```

Exercise 1.10
```cpp
#include <iostream>
int main() {
    int val = 10;
    while (val >= 0) {
        std::cout << val << std::endl;
        --val;
    }
    return 0;
}
```

Exercise 1.11
```cpp
#include <iostream>
int main() {
    int firstVal, secondVal;

    std::cout << "Enter the first number: ";
    std:: cin >> firstVal;

    std::cout << "Enter the second number (not less than the first one): ";
    std::cin >> secondVal;

    while (firstVal <= secondVal) {
        std::cout << firstVal << std::endl;
        ++firstVal;
    }
    return 0;
}
```

Exercise 1.12
Sau khi thực hiện câu  lệnh, giá trị của `sum` là `0`.
```cpp
int sum = 0;
for (int i = -100; i <= 100; ++i)
    sum += i;
```

Exercise 1.13
```cpp
// exercise 1.9
#include <iostream>
int main() {
    int sum = 0;
    for (int val = 50; val <= 100; ++val)
        sum += val;
    std::cout << "Sum of 50 to 100 inclusive is "
              << sum << std::endl;
    return 0;
}
```
```cpp
// exercise 1.10
#include <iostream>
int main() {
    for (int val = 10; val >= 0; --val)
        std::cout << val << std::endl;
    return 0;
}
```
```cpp
// exercise 1.11
#include <iostream>
int main() {
    int firstVal; secondVal;
    std::cout << "Enter two numbers: ";
    std::cin >> firstVal >> secondVal;
    for (; firstVal <= secondVal; ++firstVal)
        std:cout << firstVal << std::endl;
    return 0;
}
```

Exercise 1.14
Lợi ích của lệnh `for` so với `while`:
* Thích hợp khi số lần lặp được biết trước.
* Phù hợp cho các thao tác duyệt (traversal) các cấu trúc dữ liệu có dạng tuần tự (sequential data structures)
Bất lợi của lệnh `for` so với `while`:
* Khi số lần lặp không biết trước.
* Cấu trúc dữ liệu không có dạng tuần tự (trees, graphs), cấu trúc dữ liệu tuần tự nhưng số lượng không dự đoán được (infinite stream, online stream).

Exercise 1.15
**Bỏ qua**. Nội dung trả lời phụ thuộc vào Compiler và Operating System đang sử dụng.

Exercise 1.16
```cpp
#include <iostream>
int main() {
    int sum = 0, value = 0;
    while (std::cin >> value)
        sum += value;
    std::cout << "Sum is " << sum << std::endl;
    return 0;
}
```

Exercise 1.17
Không thực hiện các câu lệnh của phần `else`, thực hiện một lần lệnh `std::cout` của lệnh `if(std::cin >> currVal)`. Vì vậy kết quả chương trình là một dòng như sau
```
<<number>> occurs <<counter>> times
```

  Exercise 1.18
Trường hợp tất cả inputs đều giống nhau, kết quả là một dòng như Câu 1.16.
Trường hợp tất cả các số của inputs đều khác nhau, trong input có bao nhiêu số thì có đúng bấy nhiêu dòng dạng
```
<<number>> occcurs 1 times
```
Ví dụ, với input đầu vào là `21 8 3 19`. Ta thấy đầu vào chương trình là một dãy gồm 4 số nguyên khác nhau. Kết quả của chương trình tương ứng với 4 dòng
```
21 occurs 1 times
8 occurs 1 times
3 occurs 1 times
19 occurs 1 times
```

Exercise 1.19
Xem lại source code Câu 1.11


Exercise 1.20
```cpp
#include <iostream>
#include "Sales_item.h"
int main() {
    Sales_item book;
    std::cin >> book;
    std::cout << book << std::endl;
    return 0;
}
```

Exercise 1.21
```cpp
#include <iostream>
#include "Sales_item.h"
int main() {
    Sales_item item1, item2;
    std::cin >> item1 >> item2;
    std::cout << item1 + item2 << std::endl;
    return 0;
}
```
```cpp
#include <iostream>
#include "Sales_item.h"
int main() {
    Sales_ item item, total
    if (std::cin >> total) {
        while (std::cin >> item)
            total += item;
    }
    std::cout << total << std::endl;
    return 0;
}
```

Exercise 1.22
```cpp
// Bookstore program
#include <iostream>
#include "Sales_item.h"
int main() {
    Sales_item total;
    if (std::cin >> total) {
        Sales_item trans;
        while (std::cin >> trans) {
            if (total.isbn() == trans.isbn())
                total += trans;
            else {
                std::cout << total << std::endl;
                total = trans;
            }
        }
        std::cout << total << std::endl;
    } else {
        std::cerr << "No data?!" << std::endl;
        return -1; 
    }
    return 0;
}
```
