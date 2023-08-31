##### const用法
---
###### 修饰普通变量
```
const int a = 7; 
```
###### 修饰指针
```
// 修饰指针指向的内容
const int *p = 8;
// 修饰指针
int a = 8;
int* const p = &a;
```
###### 修饰类成员函数

```
// 防止成员函数修改被调用对象的值
#include<iostream>
using namespace std;
 
class Test
{
public:
    Test(){}
    Test(int _m):_cm(_m){}
    int get_cm() const
    {
       return _cm;
    }
 
private:
    int _cm;
};

void Cmf(const Test& _tt)
{
    cout<<_tt.get_cm();
}
 
int main(void)
{
    Test t(8);
    Cmf(t);
    system("pause");
    return 0;
}
```
