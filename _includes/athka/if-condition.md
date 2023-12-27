##  الجملة الشرطية IF 
**الفكرة:** ننسخ الكود ونضيف أمر طباعة للمتغير المطلوب
<details>
  <summary>الحل بلغة С++</summary>

```c++
#include <iostream>
using namespace std;
int main()
{
  int x = 11;
  int y = 29;
  int z;

  if (x % 2 != 0) {
    if (x > y) {
        z = 0;
    } else {
        z = 1;
    }
  } else {
    if (x > y) {
        z = 2;
    } else {
        z = 3;
    }
  }
  cout << z; // أضفنا أمر الطباعة
}
```

</details> 

<details>
  <summary>الحل بلغة بايثون</summary>
  
```py
x = 11
y = 29

if x % 2 != 0:
    if x > y:
        z = 0
    else:
        z = 1
else:
    if x > y:
        z = 2
    else:
        z = 3

print(z) # أضفنا أمر الطباعة
```

</details>