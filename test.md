# MKCP C++ CP Course 
## 1. Cú pháp cơ bản
### Nhập, xuất dữ liệu
Một chương trình C++ sẽ có cấu trúc như sau:
```cpp
#include <bits/stdc++.h>

using namespace std;

int main() {
    //code
}
```
- ```#include <bits/stdc++.h>```: Sử dụng thư viện ```bits/stdc++.h``` của GNU Compiler.
- ```using namespace std;```: Sử dụng namespace ```std```.
- ```int main(){}```: Code sẽ được biên dịch trong hàm ```main```.

Ta sử dụng ```cin``` và ```cout``` để nhập xuất dữ liệu. Ngoài ra còn sử dụng ```printf``` và ```scanf``` để giảm thời gian chạy.
```cpp
int a,b;
cin>>a>>b;
cout<<"A = "<<a<<" B = "<<b<<"\n";
```
Một vài kiểu dữ liệu thường dùng:

| Số nguyên | Số thực | Xâu | Logic |
| -------- | -------- | -------- |-------
| ```short```    | ```float```     | ```char```|```bool```     |
| ```int```      | ```double```|```string```
| ```long```     | ```long double```
| ```long long```|

### Cấu trúc rẽ nhánh
Trong C++ thường dùng câu lệnh ```if ... else``` để biểu diễn cấu trúc rẽ nhánh, ngoài ra cũng sử dụng cả ```switch ... case```
```cpp
if (a>b){
    cout<<"Greater\n";
}
else if (a==b){
    cout<<"Equal\n";
}
else{
    cout<<"Smaller\n";
}
```
Một số toán tử thường dùng:

| Số học | Quan hệ & So sánh | Tăng & Giảm | Kết hợp | Logic |
| -------- | -------- | -------- | ----- | ----|
| +     | ==   | ++     | +=      | !
| -    | !=   | -- | -= | &&
| *    | <| | \*= | ==
| /    | >| | /=  |
| %    | <=| | %=  |
| | >= | | |

### Cấu trúc lặp
#### Vòng lặp for
Vòng lặp ```for``` thường được dùng để lặp với số lần biết trước.
```cpp
for (int i=0;i<=10;i++){
    cout<<i<<"\n";
}
```
#### Vòng lặp while
Vòng lặp ```while``` thường được dùng để lặp với số lần không biết trước.
```cpp
int i=0;
while (i<=10){
    cout<<i<<"\n";
    i+=2;
}
```
### Hàm
Hàm cho phép chia nhỏ chương trình thành các phần với các chức năng riêng. Hàm trong C++ được chia thành hàm có giá trị trả lại và hàm không có giá trị trả lại.
```cpp
#include <bits/stdc++.h>

using namespace std;

int add (int a, int b){
  int r;
  r=a+b;
  return r;
}

void solve (){
    int z;
    z=add(5,3);
    cout<<"Z = 5 + 3 = "<<z<<"\n";
}

int main (){
    solve();
}
```
### Mảng
Mảng gồm các phần tử được liên tiếp trong bộ nhớ và có thể truy cập bằng index.
```cpp
int a[10];
int sum=0;
for (int i=0;i<10;i++){
    cin>>a[i];
    sum+=a[i];
}
for (int i=0;i<10;i++){
    cout<<a[i]<<"\n";
}
cout<<"Sum = "<<sum<<"\n";
```
## 2. STL (Standard Template Library)
### Cấu trúc dữ liệu - Data Structure
#### Vector - Mảng động
```cpp
vector<int> a(10);
for (auto &it : a){
    cin>>it;
}
for (auto it : a){
    cout<<it<<"\n";
}
a.push_back(11);
cout<<a[10]<<"\n";
a.pop_back();
```
#### Linked List / Stack / Queue - Danh sách liên kết / Ngăn xếp / Hàng đợi
```cpp
list<int> a;
stack<int> b;
queue<int> c;

a.push_back(100);
a.push_front(99);
a.pop_back();
a.pop_front();

b.push(100);
b.top();
b.pop();

c.push(1);
c.push(2);
c.front();
c.pop();
```
#### Set / Map - Tập hợp / Ánh xạ
```cpp
set<int> a;
map<string,int> b;

a.insert(10);
a.insert(9);

b["abcd"]=1;
b["xyzafa"]=2;
cout<<b["abcd"]<<"\n";
```
### Thuật toán - Algorithm
#### Min / Max - Giá trị lớn nhất / nhỏ nhất
```cpp
int x=1,y=2;
cout<<max(x,y)<<" "<<min(x,y);
```
#### Permutation - Hoán vị
```cpp
string x="abc";
do{
    cout<<x<<"\n";
}
while (next_permutation(x.begin(),x.end()));
```
#### Sorting - Sắp xếp
```cpp
int a[] = {32,71,12,45,26,80,53,33};
sort(a,a+8);
for (int i=0;i<8;i++){
    cout<<a[i]<<"\n";
}
```
#### Binary Search - Tìm kiếm nhị phân
```cpp
int a[] = {32,71,12,45,26,80,53,33};
vector<int> b(a,a+8);
sort(b.begin(),b.end());
auto it=lower_bound(b.begin(),b.end(),26);
cout<<*it<<"\n";
it=upper_bound(b.begin(),b.end(),32);
cout<<*it<<"\n";
```
## 3. Competitive Programming
