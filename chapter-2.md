Exercise 2.1
Điểm khác nhau giữa `short`, `int`, `long` và `long long`
* Kích thước (size) khác nhau. Tuy nhiên, các tính chất sau được đảm bảo
  * `size(short)` <= `size(int)`
  * `size(int)` <= `size(long)`
  * `size(long)` <= `size(long long)`

Điểm khác nhau giữa `unsigned` và `signed`
* `unsigned` cho kiểu dữ liệu số không âm
* `signed` cho dữ liệu số có chứa số âm

Điểm khác nhau giữa `float` và `double`
* Số chữ số có nghĩa (significant digits) khác nhau, của `float` là 7, của `double` là 16

Exercise 2.2
Dòng tiền (principal) và kỳ hạn (payment) là các số nguyên dương, lãi suất (rate) tính theo phần trăm
```cpp
double rate;
int principal;
int payment;
```

Exercise 2.3
```cpp
unsigned u = 10, u2 = 42;
std::cout << u2 - u << std::endl; // 32
std::cout << u - u2 << std::endl; // 4294967264

int i = 10, i2 = 42;
std::cout << i2 - i << std::endl; // 32
std::cout << i - i2 << std::endl; // -32

std::cout << i - u << std::endl;  // 0
std::cout << u - i << std::endl;  // 0
```

Exercise 2.5
(a) 
```
'a'  => char
L'a' => wchar_t
"a"  => string of chars
L"a" => string of wchar_ts
```
(b)
```
10   => int
10u  => unsigned int
10L  => long
10uL => unsigned long
012  => int
0xC  => int
```
(c)
```
3.14  => double
3.14f => float
3.14L => long double
```
(d)
```
10     => int
10u    => unsigned int
10.    => double
10e^-2 => double
```

Exercise 2.6
Câu lệnh sau bị lỗi, vì số 9 không nằm trong hệ cơ số 8.
Số `07` trong hệ cơ số 8 chuyển thành số `7` trong hệ cơ số 10.
```cpp
int month = 09, day = 07;
```

Exercise 2.7
(a) `"Who goes with Fergus\n"` => `int`
(b) `3.14e1L = 31.4L` => `long double`
(c) `1024f` => syntax error
(d) `3.14L` => `long double`

Exercise 2.8
```cpp
#include <iostream>
int main() {
    std::cout << "2M\n" << std::endl;
    std::cout << "2\tM\n" << std::endl;
    return 0;
}
```

Exercise 2.9
(a) Nhận giá trị cho biến kiểu `int` tên `input_value`. Câu lệnh lỗi.
```cpp
int input_value;
std::cin >> input_value;
```
(b) Định nghĩa và khởi tạo biến `i` có giá trị `3`. Ta thấy giá trị khởi tạo là `3.14` đã bị cắt đi và chỉ giữ phần nguyên là `3`. Câu lệnh lỗi.
```cpp
int i = 3.14;
```
(c) Định nghĩa 2 biến `salary` và `wage`, và khởi tạo 2 biến có cùng giá trị `9999.99`. Câu lệnh lỗi
```cpp
double salary = 9999.99, wage = salary;
```
(d) Tương tự như (b), nhưng câu lệnh không bị lỗi.
```cpp
int i = 3.14;
```

Exercise 2.10
```
global_str : empty string
global_int : 0
local_int  : undefined
local_str  : empty string
```

Exercise 2.11
(a) Definition, vì có khởi tạo (initialization)
```cpp
extern int ix = 1024;
```
(b) Definition
```cpp
int iy;
```
(c) Declaration
```cpp
extern int iz;
```

Exercise 2.12
(a) Invalid, vì `double` là từ khoá (keyword)
```cpp
int double = 3.14;
```
(b) Valid
```cpp
int _;
```
(c) Invalid, vì chứa ký tự `-`
```cpp
int catch-22;
```
(d) Invalid, vì ký tự đầu tiên là số
```cpp
int 1_or_2 = 1;
```
(e) Valid
```cpp
double Double = 3.14;
```

Exercise 2.13
```cpp
j = 100;
```

Exercise 2.14
```
100 45
```

Exercise 2.15
(a) Valid. Giá trị `ival` là `1`
```cpp
int ival = 1.01;
```
(b) Invalid. Kiểu reference không khởi tạo bằng một hằng số.
```cpp
int &rval1 = 1.01;
```
(c) Valid
```cpp
int &rval2 = ival;
```
(d) Invalid. Chưa khởi tạo biến reference.
```cpp
int &rval3;
```

Exercise 2.16
```cpp
int i = 0, &r1 = i; double d = 0, &r2 = d;
```
(a) Valid
```cpp
r2 = 3.14159;
```
(b) Valid. Biến `i` kiểu `int` được chuyển thành kiểu `double` và gán vào biến `d`
```cpp
r2 = r1;
```
(c) Valid. Biến `d` kiểu `double` được chuyển thành kiểu `int` và gán vào biến `i`
```cpp
i = r2;
```
(d) Valid. Biến `d` kiểu `double` được chuyển thành kiểu `int` và gán vào biến `i`
```cpp
r1 = d;
```

Exercise 2.17
```
10 10
```

Exercise 2.18
Change the value of a pointer
```cpp
int i = 0, j = 1, *p = &i;
p = &j;
```
Change the value to which the pointer points
```cpp
int i = 0, j = 1; *p = &i;
*p = j;
```

Exercise 2.19
Sự khác nhau giữa pointer và reference
* Pointer là object, reference không là object
* Phép gán (assignment) thực hiện được với pointer, nhưng không thực hiện được với reference
* Pointer có thể không cần khởi tạo, reference bắt buộc khởi tạo (initialize)
* Pointer có thể thay đổi giá trị, reference chỉ khởi tạo một lần và không được thay đổi giá trị

Exercise 2.20
Lệnh 1 định nghĩa biến `i` kiểu `int` và có giá trị ban đầu là `42`
Lệnh 2 định nghĩa biến con trỏ `p1` có base type là `int`, và chứa địa chỉ của biến `i`
Lệnh 3 gồm các bước:
* `*p1` lấy giá trị mà `p1` trỏ tới, tức là giá trị của biến `i`, hay `42`
* Phép gán có thể được viết lại là `*p1 = 42 * 42`, hay `*p1 = 1764`
* Giá trị biến `i` được thay bằng `1764`, thông qua con trỏ `p1`
```cpp
int i = 42;      // 1
int *p1 = &i;    // 2
*p1 = *p1 * *p1; // 3
```

Exercise 2.21
```cpp
int i = 0;
```
(a) Invalid. Base type của con trỏ `dp` là `double`, không trùng với kiểu của biến `i` là `int`
```cpp
double* dp = &i;
```
(b) Invalid. Hai biến `ip` và `i` không cùng kiểu dữ liệu. Biến `ip` kiểu con trỏ `int`, trong khi biến `i` kiểu `int`
```cpp
int *ip = i;
```
(c) Valid
```cpp
int *p = &i;
```

Exercise 2.22
Lệnh 1 thực hiện chuyển kiểu con trỏ của biến `p` thành kiểu `bool`.
* Nếu `p` trỏ với một địa chỉ bất kì thì kiểu `bool` tương ứng là `true`, và đoạn lệnh trong `if` được thực hiện.
* Nếu `p` nhận giá trị `nullptr`, hoặc `NULL`, hoặc `0`, kiểu `bool` tương ứng là `false`, và câu lệnh trong `if` không được thực hiện.

Lệnh 2 thực hiện `*p`, lấy giá trị mà con trỏ `p` trỏ tới, tạm gọi là `i = *p`. Sau đó:
* Nếu base type của biến `i` là `bool`, lệnh `if` thực hiện hay không tuỳ vào giá trị của biến `i`. 
* Nếu base type của biến `i` không là `bool`, biến `i` được chuyển sang kiểu `bool`, và giá trị `bool` tương ứng sẽ quyết định câu lệnh trong `if` thực hiện hay không.
```cpp
if (p)  // ... // 1
if (*p) // ... // 2
```

Exercise 2.23
Không xác được object mà con trỏ `p` trỏ tới là "valid object" hay không.
Nếu `p` nhận giá trị `nullptr` (hoặc giá trị tương đương), thì `p` trỏ tới "invalid object"
Nếu `p` nhận giá trị khác `nullptr`. Giá trị của `p` là một số nhị phân thể hiện địa chỉ của ô nhớ. Lúc này ta chỉ có duy nhất một thông tin là địa chỉ ô nhớ, ta không thể biến tại địa chỉ đó object có phải là "valid object" hay không.

Exercise 2.24
Lệnh 1: biến `p` có base type là `void`, nên `p` có thể nhận địa chỉ của bất cứ base type khác, trong đoạn code là `int`.
Lệnh 2: Base type của `lp` là `long`, không trùng với kiểu dữ liệu của biến `i` là `int`.
```cpp
int i = 42;
void *p = &i;  // 1
long *lp = &i; // 2
```

Exercise 2.25
(a)
```cpp
int *ip, &r = ip;
// ip: pointer to int
// r:  reference to int
```
(b)
```cpp
int i, *ip = 0;
// i:  int
// ip: pointer to int
```
(c)
```cpp
int* ip, ip2;
// ip:  pointer to int
// ip2: int
```

Exercise 2.26
(a) Invalid. Khai báo biến `buf` kiểu `const int`, nhưng chưa khởi tạo giá trị.
(b) Valid. Khai báo biến `cnt` kiểu `int`, khởi tạo giá trị `0`.
(c) Valid. Khai báo biến `sz` kiểu `const int`, khởi tạo giá trị `0`.
(d) Invalid.
* Biến `cnt` kiểu `int`, lệnh `++cnt` tăng giá trị `cnt` lên `1`.
* Biến `sz` kiểu `const int`.
  * tăng giá trị `sz` lên `1`, bước này hợp lệ.
  * gán giá trị `sz + 1` tính được vào biến `sz`. Bước gán bị lỗi, vì `sz` là biến `const int`.
```cpp
const int buf;
int cnt = 0;
const int sz = cnt;
++cnt; ++sz;
```

Exercise 2.27
(a) Invalid. Biến reference `r` chỉ khởi tạọ với biến `int`, không khởi tạo với hằng số `int`.
```cpp
int i = -1, &r = 0;
```
(b) Valid. Biến `p2` là con trỏ hằng (const pointer)
```cpp
int *const p2 = &i2;
```
(c) Valid. Biến `r` kiểu reference tới `const int`, nên có thể khởi tạo `r` bằng hằng số `0`.
```cpp
const int i = -1, &r = 0;
```
(d) Valid. Biến `p3` là con trỏ **hằng** (const pointer) tới `const int`. Biến `i2` kiểu `int`.
```cpp
const int *const p3 = &i2;
```
(e) Valid. Biến `p1` là con trỏ tới `const int`. Biến `i2` kiểu `int`.
```cpp
const int *p1 = &i2;
```
(f) Invalid
* Không có kiểu "const reference", nên C++ không có cú pháp dạng `&const`.
* Biến reference `r2` chưa có giá trị khởi tạo.
```cpp
const int &const r2;
```
(g) Valid.
* Gán giá trị "non-const" của biến `i` vào biến `i2` kiểu `const int`.
* Biến `r` kiểu reference to `const`, biến `i` là "non-const".
```cpp
const int i2 = i, &r = i;
```

Exercise 2.28
(a)
* Biến `i` kiểu `int`. 
* Biến `cp` là const pointer tới `int`.
```cpp
int i, *const cp;
```
(b)
* Biến `p1` là con trỏ tới `int`.
* Biến `p2` là const pointer tới `int`.
```cpp
int *p1, *const p2;
```
(c)
* Biến `ic` kiểu `const int`.
* Biến `r` là reference tới `int`, không là reference tới `const int`. Do đó phép gán `&r = ic` là lỗi.
```cpp
const int ic, &r = ic;
```
(d) Biến `p3` là const pointer tới `const int`.
```cpp
const int *const p3;
```
(e) Biến `p` là con trỏ tới `const int`.
```cpp
const int *p;
```

Exercise 2.29
(a) Valid.
(b) Invalid. Low-level const của `p1` là "non-const". Low-level const của `p3` là `const`.
(c) Invalid. Low-level const của `p1` là "non-const". Biến `ic` kiểu `const int`.
(d) Valid. Low-level const của `p3` là `const`. Biến `ic` kiểu `const int`.
(e) Invalid. Top-level const của `p2` là `const`, nên `p2` không ở phía bên trái phép gán.
(f) Invalid. Top-level const của `ic` là `const`, nên `ic` không ở phía bên trái phép gán.
```cpp
i = ic;   // (a)
p1 = p3;  // (b)
p1 = &ic; // (c)
p3 = &ic; // (d)
p2 = p1;  // (e)
ic = *p3; // (f)
```

Exercise 2.30
* Biến `v2`: top-level const là `const`, không có low-level const.
* Biến `v1`: top-level const là "non-const", không có low-level const.
* Biến `p1`: top-level const là "non-const", low-level const là "non-const".
* Biến `r1`: không có top-level const, low-level const là "non-const".
* Biến `p2`: top-level const là "non-const", low-level const là `const`.
* Biến `p3`: top-level const là `const`, low-level const là `const`.
* Biến `r2`: không có top-level conset, low-level const là `const`.
```cpp
const int v2 = 0;  int v1 = v2;
int *p1 = &v1, &r1 = v1;
const int *p2 = &v2, *const p3 = &i, &r2 = v2;
```

Exercise 2.31
(a) Invalid. Low-level const của `r1` là "non-const", low-level const của `v2` là `const`.
(b) (c), (d), (e) Valid. Bỏ qua top-level const.
```cpp
r1 = v2; // (a)
p1 = p2; // (b)
p2 = p1; // (c)
p1 = p3; // (d)
p2 = p3; // (e)
```

Exercise 2.32
```cpp
int null = 0, *p = null;
```
Cách đặt tên của biến `null` là hợp lệ (chú ý, `null` khác `NULL`). Biến `null` là một biến thông thường, có kiểu `int`.
Biến `p` là con trỏ tới `int`. Giá trị khởi tạo của biến `p` phải thuộc kiểu `int*`, nên ta cần sửa `*p = null` thành `*p = &null`. (thêm toán tử `&`)
```cpp
int null = 0, *p = &null;
```
